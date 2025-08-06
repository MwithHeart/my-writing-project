# What is SSH?

SSH (Secure Shell) is a cryptographic network protocol that enables secure communication between your machine and remote servers. In the context of GitHub, SSH allows you to authenticate and interact with Git repositories securely without having to type your username and password every time.

## Why SSH is useful

1. Enables secure and password-less communication with GitHub. When you use https, you'll often need to enter your email and password from time to time.

2. Ideal for frequent contributors, teams, and automated worldflows

3. Security

## How SSH Works with GitHub

1. You generate an SSH key pair on your machine

    A public key shared with GitHub

    A private key stored securely on your device

2. You add the public key to your GitHub account.

3. GitHub verifies your identity using your private key whenever you perform Git actions.
