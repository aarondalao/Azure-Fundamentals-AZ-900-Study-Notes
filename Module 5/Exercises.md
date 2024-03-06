## Exercise 1 
### Create-a-VM-using-Azure-Cloud-Shell

AzureCLI:
```
az vm create --resource-group "learn-9f5b46b7-e2d0-4ddd-843b-e62bad090805" --name my-vm --public-ip-sku Standard --image Ubuntu2204 --admin-username azureuser --generate-ssh-keys
```
#### Run the following `az vm extension set` command to configure Nginx on your VM:

```
az vm extension set --resource-group "learn-9f5b46b7-e2d0-4ddd-843b-e62bad090805" --vm-name my-vm --name customScript --publisher Microsoft.Azure.Extensions --version 2.1 --settings '{"fileUris":["https://raw.githubusercontent.com/MicrosoftDocs/mslearn-welcome-to-azure/master/configure-nginx.sh"]}' --protected-settings '{"commandToExecute": "./configure-nginx.sh"}'    
```

This command uses the Custom Script Extension to run a Bash script on your VM. The script is stored on GitHub. While the command runs, you can choose to [examine the Bash script](https://raw.githubusercontent.com/MicrosoftDocs/mslearn-welcome-to-azure/master/configure-nginx.sh) from a separate browser tab. To summarize, the script:

1. Runs `apt-get update` to download the latest package information from the internet. This step helps ensure that the next command can locate the latest version of the Nginx package.
2. Installs Nginx.
3. Sets the home page, _/var/www/html/index.html_, to print a welcome message that includes your VM's host name.

---
## Exercise 2 
### Configure-network-access
### Task 1: Access your web server

In this procedure, you get the IP address for your VM and attempt to access your web server's home page.

1. Run the following `az vm list-ip-addresses` command to get your VM's IP address and store the result as a Bash variable:
    
    Azure CLICopy
    
    ```
    IPADDRESS="$(az vm list-ip-addresses \
      --resource-group "learn-9f5b46b7-e2d0-4ddd-843b-e62bad090805" \
      --name my-vm \
      --query "[].virtualMachine.network.publicIpAddresses[*].ipAddress" \
      --output tsv)"    
    ```
    
2. Run the following `curl` command to download the home page:
    ```
    curl --connect-timeout 5 http://$IPADDRESS
    ```
    
    The `--connect-timeout` argument specifies to allow up to five seconds for the connection to occur. After five seconds, you see an error message that states that the connection timed out:
    
    Output: 
    ```
    curl: (28) Connection timed out after 5001 milliseconds
    ```
    
    This message means that the VM was not accessible within the timeout period.
    
3. As an optional step, try to access the web server from a browser:
    1. Run the following to print your VM's IP address to the console:
        ```
        echo $IPADDRESS       
        ```
        
        You see an IP address, for example, _23.102.42.235_.
        
    2. Copy the IP address that you see to the clipboard.
    
    3. Open a new browser tab and go to your web server. After a few moments, you see that the connection isn't happening. If you wait for the browser to time out, you'll see something like this:
        ![Screenshot of a web browser showing an error message that says the connection timed out.](https://learn.microsoft.com/en-us/training/wwl-azure/describe-azure-compute-networking-services/media/browser-request-timeout-d7cc0e02.png)
    4. Keep this browser tab open for later.
        
### Task 2: List the current network security group rules

Your web server wasn't accessible. To find out why, let's examine your current NSG rules.

1. Run the following `az network nsg list` command to list the network security groups that are associated with your VM:
    
    Azure CLI:
    ```
    az network nsg list \
      --resource-group "learn-9f5b46b7-e2d0-4ddd-843b-e62bad090805" \
      --query '[].name' \
      --output tsv    
    ```
    
    You see this:
    Output:
    
    ```
    my-vmNSG
    ```
    
    Every VM on Azure is associated with at least one network security group. In this case, Azure created an NSG for you called _my-vmNSG_.
    
2. Run the following `az network nsg rule list` command to list the rules associated with the NSG named _my-vmNSG_:
    
    Azure CLI:
    ```
    az network nsg rule list \
      --resource-group "learn-9f5b46b7-e2d0-4ddd-843b-e62bad090805" \
      --nsg-name my-vmNSG    
    ```
    
    You see a large block of text in JSON format in the output. In the next step, you'll run a similar command that makes this output easier to read.
    
3. Run the `az network nsg rule list` command a second time. This time, use the `--query` argument to retrieve only the name, priority, affected ports, and access (**Allow** or **Deny**) for each rule. The `--output` argument formats the output as a table so that it's easy to read.
    
    Azure CLI:
    ```
    az network nsg rule list \
      --resource-group "learn-9f5b46b7-e2d0-4ddd-843b-e62bad090805" \
      --nsg-name my-vmNSG \
      --query '[].{Name:name, Priority:priority, Port:destinationPortRange, Access:access}' \
      --output table    
    ```
    
    You see this:
    ```
    Name              Priority    Port    Access
    -----------------  ----------  ------  --------
    default-allow-ssh  1000        22      Allow
    
    ```
    
    You see the default rule, _default-allow-ssh_. This rule allows inbound connections over port 22 (SSH). SSH (Secure Shell) is a protocol that's used on Linux to allow administrators to access the system remotely. The priority of this rule is 1000. Rules are processed in priority order, with lower numbers processed before higher numbers.
    

By default, a Linux VM's NSG allows network access only on port 22. This enables administrators to access the system. You need to also allow inbound connections on port 80, which allows access over HTTP.

### Task 3: Create the network security rule

Here, you create a network security rule that allows inbound access on port 80 (HTTP).

1. Run the following `az network nsg rule create` command to create a rule called _allow-http_ that allows inbound access on port 80:
    
    Azure CLI:
    ```
    az network nsg rule create \
      --resource-group "learn-9f5b46b7-e2d0-4ddd-843b-e62bad090805" \
      --nsg-name my-vmNSG \
      --name allow-http \
      --protocol tcp \
      --priority 100 \
      --destination-port-range 80 \
      --access Allow    
    ```
    
    For learning purposes, here you set the priority to 100. In this case, the priority doesn't matter. You would need to consider the priority if you had overlapping port ranges.
    
2. To verify the configuration, run `az network nsg rule list` to see the updated list of rules:
    
    Azure CLI:
    ```
    az network nsg rule list \
      --resource-group "learn-9f5b46b7-e2d0-4ddd-843b-e62bad090805" \
      --nsg-name my-vmNSG \
      --query '[].{Name:name, Priority:priority, Port:destinationPortRange, Access:access}' \
      --output table    
    ```
    
    You see this both the _default-allow-ssh_ rule and your new rule, _allow-http_:
    
    Output:
    ```
    Name              Priority    Port    Access
    -----------------  ----------  ------  --------
    default-allow-ssh  1000        22      Allow
    allow-http          100        80      Allow    
    ```
### Task 4: Access your web server again

Now that you've configured network access to port 80, let's try to access the web server a second time.

 > **Note**
 > After you update the NSG, it may take a few moments before the updated rules propagate. Retry the next step, with pauses between attempts, until you get the desired results.

1. Run the same `curl` command that you ran earlier:
    ```
    curl --connect-timeout 5 http://$IPADDRESS
    ```
    
    You see this:
    ```
    <html><body><h2>Welcome to Azure! My name is my-vm.</h2></body></html>
    ```
2. 
3. As an optional step, refresh your browser tab that points to your web server. You see this:
![A screenshot of a web browser showing the home page from the web server. The home page displays a welcome message.](https://learn.microsoft.com/en-us/training/wwl-azure/describe-azure-compute-networking-services/media/browser-request-successful-df21c6f1.png)
    

Nice work. In practice, you can create a standalone network security group that includes the inbound and outbound network access rules you need. If you have multiple VMs that serve the same purpose, you can assign that NSG to each VM at the time you create it. This technique enables you to control network access to multiple VMs under a single, central set of rules.

## Clean up

The sandbox automatically cleans up your resources when you're finished with this module.

When you're working in your own subscription, it's a good idea at the end of a project to identify whether you still need the resources you created. Resources that you leave running can cost you money. You can delete resources individually or delete the resource group to delete the entire set of resources.