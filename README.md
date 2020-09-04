# Eventhub Documentation

# Get started
This guide will help you get up and running with your free EventHub account in minutes. It’s short and sweet.
1. Install the CLI
2. Sign up for your free EventHub-Account
3. Create your first event definition
4. Implement the client SDK in your application
5. Check event usage
6. Next Steps
## Step 1: Install the CLI
Before creating an account and writing your first event definition, install the eventhub CLI. It’s open source and available on GitHub.
```
pip install eventhub-cli
```
## Step 2: Sign up for your free EventHub-Account
Now that the eventhub CLI is installed on your operating system, let’s create an account. Run the signup command and claim yours:
```
eventhub-cli signup
```
You now have your very own EventHub account! Go ahead and create an organization and a workspace.
## Step 3: Create your first event definition
Create a new file and save it as `events.json`. Paste the following content:
```json
{
  "version": "0.0.0",
  "events": [
    {
      "name": "hello.world",
      "properties": {
        "hello": "string",
        "world": "string"
      }
    }
  ]
}
```
Use the eventhub CLI to upload the file into your workspace.
```
eventhub-cli push events.json -e [YOUR_EMAIL] -p [YOUR_PASSWORD] -o [YOUR_ORGANIZATION] -w [YOUR_WORKSPACE]
```
