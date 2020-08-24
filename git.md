# Set up SSH Key for Mac & Windows

<!-- topics-start -->
* [Checking for existing SSH keys](#Checking-for-existing-SSH-keys)
* [Generating a new SSH key and adding it to the ssh-agent](Generating-a-new-SSH-key-and-adding-it-to-the-ssh-agent)
* [Adding your SSH key to the ssh-agent](Adding-your-SSH-key-to-the-ssh-agent)

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


