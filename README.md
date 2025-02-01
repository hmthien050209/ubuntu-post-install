# ubuntu-post-install

These are the Ansible playbooks that I'm using to setup my Ubuntu system

## How to run?

1. Configure the `hosts` file (example file: `hosts.example`)
2. Install required dependencies:

```sh
# Install Ansible and OpenSSH Client, Server
# This should be run all the hosts that you plan to execute the playbooks
sudo apt install ansible openssh-client openssh-server -y

# Install required Ansible Galaxy dependencies
ansible-galaxy install -r requirements.yml

```

3. Test the connection to the targets:

```sh
ansible all -m ping
```

4. Set the variables inside the [group_vars/\*](/group_vars/) folders
5. Run the playbook

```sh
# Desktop
ansible-playbook run-desktop.yml -K

# Server
ansible-playbook run-server.yml -K
```

## Features

## License

Licensed under the MIT License.
Copyright (c) 2025 Minh Thiên Hoàng.

The file [assets/benjamin-voros-phIFdC6lA4E-unsplash.png](assets/benjamin-voros-phIFdC6lA4E-unsplash.png) is transcoded to PNG from the photo by [Benjamin Voros](https://unsplash.com/@vorosbenisop?utm_content=creditCopyText&utm_medium=referral&utm_source=unsplash) on [Unsplash](https://unsplash.com/photos/snow-mountain-under-stars-phIFdC6lA4E?utm_content=creditCopyText&utm_medium=referral&utm_source=unsplash).
