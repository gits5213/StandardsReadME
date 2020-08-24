# Set up SSH Key for Mac & Windows

<!-- topics-start -->
* [Checking for existing SSH keys](#Checking-for-existing-SSH-keys)
* [Generating a new SSH key and adding it to the ssh agent](#Generating-a-new-SSH-key-and-adding-it-to-the-sshAagent)
* [Adding your SSH key to the ssh agent](#Adding-your-SSH-key-to-the-sshAagent)
* [Adding a new SSH key to your GitHub account](#Adding-a-new-SSH-key-to-your-GitHub-account)

## Checking for existing SSH keys
### Before you generate an SSH key, you can check to see if you have any existing SSH keys.
- Open Terminal (Windows: CMD or Git Bash).
- Enter ls -al ~/.ssh to see if existing SSH keys are present:
    ```
    $ ls -al ~/.ssh
    # Lists the files in your .ssh directory, if they exist
    ```
- Check the directory listing to see if you already have a public SSH key. By default, the filenames of the public keys are one of the following:
    ```
    id_rsa.pub
    id_ecdsa.pub
    id_ed25519.pub
    ```
- If you don't have an existing public and private key pair, or don't wish to use any that are available to connect to GitHub, then generate a new SSH key.

# Generating a new SSH key and adding it to the ssh-agent
- Open Terminal or (Windows: CMD or Git Bash).
- Paste the text below, substituting in your GitHub email address.
    ```
    $ ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
    ```
    - This creates a new ssh key, using the provided email as a label.
    ```
    > Generating public/private rsa key pair.
    ```
- When you're prompted to "Enter a file in which to save the key," press Enter. This accepts the default file location.
    ```
    > Enter a file in which to save the key (/Users/you/.ssh/id_rsa): [Press enter]
    ```
- At the prompt, type a secure passphrase.
    ```
    > Enter passphrase (empty for no passphrase): [Type a passphrase]
    > Enter same passphrase again: [Type passphrase again]
    ```

# Adding your SSH key to the ssh-agent

### Before adding a new SSH key to the ssh-agent to manage your keys, you should have checked for existing SSH keys and generated a new SSH key. When adding your SSH key to the agent, use the default macOS ssh-add command, and not an application installed by macports, homebrew, or some other external source.

- Start the ssh-agent in the background.
    ```
    $ eval "$(ssh-agent -s)"
    > Agent pid 59566
    ```
- If you're using macOS Sierra 10.12.2 or later, you will need to modify your ~/.ssh/config file to automatically load keys into the ssh-agent and store passphrases in your keychain.
    - First, check to see if your ~/.ssh/config file exists in the default location.
    ```
    $ open ~/.ssh/config
    > The file /Users/you/.ssh/config does not exist.
    ```
    - If the file doesn't exist, create the file.
    ```
    $ touch ~/.ssh/config
    ```
    - Open your ~/.ssh/config file, then modify the file, replacing ~/.ssh/id_rsa if you are not using the default location and name for your id_rsa key.
    ```
    Host *
    AddKeysToAgent yes
    UseKeychain yes
    IdentityFile ~/.ssh/id_rsa
    ```
    - Add your SSH private key to the ssh-agent and store your passphrase in the keychain. If you created your key with a different name, or if you are adding an existing key that has a different name, replace id_rsa in the command with the name of your private key file.
    ```
    $ ssh-add -K ~/.ssh/id_rsa
    ```

    # Adding a new SSH key to your GitHub account
    ### To configure your GitHub account to use your new (or existing) SSH key, you'll also need to add it to your GitHub account.

    - Copy the SSH key to your clipboard.
    - If your SSH key file has a different name than the example code, modify the filename to match your current setup. When copying your key, don't add any newlines or whitespace.
    ```
    $ pbcopy < ~/.ssh/id_rsa.pub
    # Copies the contents of the id_rsa.pub file to your clipboard
    ```
    - LogInto GitHub and In the upper-right corner of any page, click your profile photo, then click Settings.
    - In the user settings sidebar, click SSH and GPG keys.
    - Click New SSH key or Add SSH key.
    - In the "Title" field, add a descriptive label for the new key. For example, if you're using a personal Mac, you might call this key "Personal MacBook Air".
    - Paste your key into the "Key" field.
    - Click Add SSH key.
    - If prompted, confirm your GitHub password.


    


