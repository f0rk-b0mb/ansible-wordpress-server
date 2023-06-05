# WordPress Server Setup

## Introduction

This repository contains an Ansible playbook that automates the setup of a WordPress server. It installs and configures the necessary software packages, sets up a MySQL database for WordPress, fetches and sets up WordPress, configures Nginx and obtains an SSL certificate for your site, and adds a `.bashrc` file to the home directory of the specified user.

## Prerequisites

1. [Ansible](https://www.ansible.com/) installed on your local machine.
2. SSH access to the server you want to set up. The server should be running Ubuntu.
3. Basic knowledge of SSH and command-line interface.

## Usage

### Clone the Repository

To get started, clone this repository to your local machine:

BASH:
git clone https://github.com/


Replace `your-username` and `your-repo-name` with your actual GitHub username and repository name.

### Modify the Playbook

Before running the playbook, you need to modify it to include your actual server name, domain, email, and MySQL root password. These values are represented by placeholders in the playbook:

- `your_server`: Replace this with the IP address or hostname of your server.
- `your_domain`: Replace this with the domain name you want to use for your WordPress site.
- `your_email`: Replace this with your email address. This is used by Let's Encrypt for sending emails related to your SSL certificate.
- `your_mysql_root_password`: Replace this with the desired MySQL root password.

For security reasons, you should consider using [Ansible Vault](https://docs.ansible.com/ansible/latest/user_guide/vault.html) to securely store sensitive data like passwords.

### Run the Playbook

Navigate to the directory containing the playbook and run the following command:

BASH:
ansible-playbook main.yml


You may be prompted for the SSH password for your server. After entering the password, Ansible will start running the tasks in the playbook.

Once the playbook has finished running, you should have a working WordPress site accessible at the domain you specified.

## Contributing

Contributions are welcome! If you have a feature request, bug report, or suggestion, feel free to open an issue on GitHub. If you want to contribute code, feel free to fork the repository and submit a pull request.

## License

This project is licensed under the MIT License. See the `LICENSE` file in the repository for more information.

