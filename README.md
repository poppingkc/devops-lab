\# DevOps Lab: CI/CD Simulation with Vagrant, Docker, and Ansible



\## 🧭 Overview

This project simulates a real-world DevOps workflow using:

\- Vagrant + VirtualBox for multi-VM infrastructure

\- Docker Compose for container orchestration

\- Ansible for CI/CD-style automation and rollback logic



\## 🛠️ Tech Stack

\- Ubuntu 18.04 (via Vagrant)

\- Docker + Docker Compose

\- Ansible 2.9

\- Nginx container (base service)



\## 🚀 Features

\- Synced folder between host and VM

\- Automated container deployment via Ansible

\- Rollback logic triggered on deployment failure

\- Private IP access to containerized services



\## 📦 Folder Structure

devops-lab/ ├── Vagrantfile ├── app/ │   ├── docker-compose.yml │   ├── deploy.yml │   └── README.md



\## 🧪 How to Run

1\. Clone this repo

2\. Run `vagrant up` to launch the VM

3\. SSH into the VM: `vagrant ssh web`

4\. Run the playbook: `ansible-playbook /home/vagrant/app/deploy.yml`



\## 💡 What I Learned

\- Troubleshooting port forwarding and network isolation

\- Using Ansible blocks for error handling and rollback

\- Structuring a reproducible DevOps lab for portfolio use



