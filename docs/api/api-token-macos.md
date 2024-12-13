# Step-by-Step Guide: Using an API Token on macOS

This tutorial explains how to securely use an API token on macOS.

 
<span style="display: inline-block; width: 60%;">
  <img src="docs/assets/Screenshot 2024-12-12 at 12.37.45 PM.png" >
</span>


## Steps to Use an API Token

## Step 1: Open Terminal
1. Launch the Terminal application on your Mac:
   - Use `Command + Space` to open Spotlight.
   - Type `Terminal` and press `Enter`.

---
<span style="display: inline-block; width: 60%;">
  <img src="docs/assets/Terminal Screenshot 1.png">
</span>

## Step 2: Store the API Token in an Environment Variable

1. Use a secure method to store the token:
   ```bash
   export  OPENAI_BASE_URL= "your_api_token_here"
2. To make it persistent across sessions, add the line to your shell profile file:
- For zsh (default in macOS):
     ```bash
        echo export OPENAI_BASE_URL="your_api_token_here" >> ~/.zshrc
- For bash:
    ```bash
        echo export OPENAI_BASE_URL="your_api_token_here" >> ~/.bash_profile

- Apply the changes:
    ```bash
    source ~/.zshrc   # For zsh
    source ~/.bash_profile  # For bash
<span style="display: inline-block; width: 60%;">
  <img src="docs/assets/Terminal Screenshot 2.png">
</span>
---

## Step 3: Verify the Variable 

### Step 3.1: Determine Your Shell

Check which shell you’re using by running:      
   ```echo $SHELL```

- If the output is /bin/zsh, your configuration file is ~/.zshrc.
- If the output is /bin/bash, your configuration file is ~/.bash_profile.

### Step 3.2: Open the Configuration File

Open the appropriate file in a text editor:

- For zsh: ```nano ~/.zshrc```

- For bash: ```nano ~/.bash_profile```

### Step 3.3: Add the Token

Add the following line to the file:

      export OPENAI_BASE_URL="sk-gYZ3JU2U_YQyHrx_vnJvNg"

### Step 3.4: Save and Exit

   In ```nano```, ```press Ctrl + O``` to save the file.
    Press ```Enter``` to confirm.
    Press ```Ctrl + X``` to exit.
- If the output is /bin/zsh, your configuration file is ~/.zshrc.
- If the output is /bin/bash, your configuration file is ~/.bash_profile.

- . Confirm the token is set correctly: 
   ```bash
   echo $OPENAI_BASE_URL 
- The terminal should display your token 

<span style="display: inline-block; width: 60%;">
  <img src="docs/assets/Terminal Screenshot 3.png">
</span>

---
## Step 4: Use the API Token in a cURL Request 


1. To test the token, use it in an API call:
    ```bash
        curl -H "Authorization: Bearer $OPENAI_BASE_URL" https://chat.cyverse.ai/endpoint

<span style="display: inline-block; width: 60%;">
  <img src="docs/assets/Terminal Screenshot 4.png">
</span>

---
## Step 5: Secure your Token 
1. Avoid hardcoding tokens in scripts.
2. Use .env files with tools like dotenv for larger projects.
3. Revoke unused or compromised tokens.

## Troubleshooting

- Token not found: Ensure you used source to reload your shell configuration.
- Permission denied: Check the file permissions of your shell profile.

## You're all set! 🎉 You can now use your API token securely on macOS.