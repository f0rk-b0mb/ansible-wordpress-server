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
git clone https://github.com/f0rk-b0mb/ansible-wordpress-server


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

###################### GERMAN VERSION - DEUTSCHE VERSION ######################

# WordPress Server Setup

## Einführung

Dieses Repository enthält ein Ansible Playbook, das die Einrichtung eines WordPress-Servers automatisiert. Es installiert und konfiguriert die notwendigen Softwarepakete, richtet eine MySQL-Datenbank für WordPress ein, lädt WordPress herunter und richtet es ein, konfiguriert Nginx und erhält ein SSL-Zertifikat für Ihre Website und fügt eine `.bashrc`-Datei zum Home-Verzeichnis des angegebenen Benutzers hinzu.

## Voraussetzungen

1. [Ansible](https://www.ansible.com/) auf Ihrem lokalen Rechner installiert.
2. SSH-Zugriff auf den Server, den Sie einrichten möchten. Der Server sollte Ubuntu laufen haben.
3. Grundkenntnisse in SSH und Befehlszeilen-Interface.

## Nutzung

### Repository klonen

Um zu beginnen, klonen Sie dieses Repository auf Ihren lokalen Rechner:

BASH:
git clone https://github.com/f0rk-b0mb/ansible-wordpress-server


Ersetzen Sie `your-username` und `your-repo-name` durch Ihren tatsächlichen GitHub-Benutzernamen und den Namen des Repositorys.

### Das Playbook anpassen

Bevor Sie das Playbook ausführen, müssen Sie es so anpassen, dass es Ihren tatsächlichen Servernamen, Domain, E-Mail und MySQL root Passwort enthält. Diese Werte sind durch Platzhalter im Playbook dargestellt:

- `your_server`: Ersetzen Sie dies durch die IP-Adresse oder den Hostnamen Ihres Servers.
- `your_domain`: Ersetzen Sie dies durch den Domain-Namen, den Sie für Ihre WordPress-Site verwenden möchten.
- `your_email`: Ersetzen Sie dies durch Ihre E-Mail-Adresse. Diese wird von Let's Encrypt für den Versand von E-Mails in Bezug auf Ihr SSL-Zertifikat verwendet.
- `your_mysql_root_password`: Ersetzen Sie dies durch das gewünschte MySQL root Passwort.

Aus Sicherheitsgründen sollten Sie in Betracht ziehen, [Ansible Vault](https://docs.ansible.com/ansible/latest/user_guide/vault.html) zu verwenden, um sensible Daten wie Passwörter sicher zu speichern.

### Das Playbook ausführen

Navigieren Sie zu dem Verzeichnis, das das Playbook enthält, und führen Sie den folgenden Befehl aus:

BASH:
ansible-playbook main.yml


Möglicherweise werden Sie nach dem SSH-Passwort für Ihren Server gefragt. Nach Eingabe des Passworts beginnt Ansible mit der Ausführung der Aufgaben im Playbook.

Sobald das Playbook fertig ausgeführt ist, sollten Sie eine funktionierende WordPress-Site haben, die unter der von Ihnen angegebenen Domain zugänglich ist.

## Mitwirken

Beiträge sind willkommen! Wenn Sie einen Feature-Request, einen Fehlerbericht oder einen Vorschlag haben, können Sie gerne ein Issue auf GitHub öffnen. Wenn Sie Code beitragen möchten, können Sie das Repository forken und einen Pull-Request einreichen.

## Lizenz

Dieses Projekt ist unter der MIT-Lizenz lizenziert. Weitere Informationen finden Sie in der Datei `LICENSE` im Repository.
