# Artifact Repository Manager with Nexus on DigitalOcean

## Overview

This project demonstrates the deployment and configuration of a self-hosted artifact repository using Sonatype Nexus Repository Manager on a DigitalOcean cloud server. The environment was built from the ground up by provisioning a Linux cloud instance, installing and configuring Nexus, creating user access controls, and integrating Java build tools to publish Maven and Gradle artifacts.

The goal of this project was to simulate an enterprise DevOps workflow where developers build applications and store versioned artifacts in a centralized repository for reliable deployment and distribution.

---

## Technical Solution

A DigitalOcean Ubuntu server was provisioned and secured using firewall rules and SSH access. Java 17 was installed as a dependency for Nexus Repository Manager, followed by the installation and configuration of Nexus as the artifact management platform.

Nexus security was configured by creating users, assigning roles, and managing repository permissions. Hosted repositories were configured to support Java artifacts, allowing both Gradle and Maven build systems to publish JAR files directly into Nexus.

The completed solution demonstrates the flow of application artifacts from local development environments into a centralized cloud-based repository.

---

## Architecture Overview

The project consists of a cloud-hosted artifact management environment running on DigitalOcean. Developers use Maven and Gradle build tools to package Java applications and publish versioned JAR artifacts to Nexus Repository Manager.

Architecture flow:

Developer Workstation  
↓  
Maven / Gradle Build Tool  
↓  
SSH Connection to Cloud Environment  
↓  
DigitalOcean Ubuntu Server  
↓  
Sonatype Nexus Repository Manager  
↓  
Hosted Maven / Gradle Artifact Repository

---
## Technologies Used

- DigitalOcean
- Ubuntu Linux
- Sonatype Nexus Repository Manager
- Java 17
- Gradle
- Apache Maven
- Git
- GitHub
- SSH
- Linux Command Line

---

## Key Skills Demonstrated

- Cloud Infrastructure Provisioning
- Linux Server Administration
- Secure Remote Access Using SSH
- Firewall Configuration
- Artifact Repository Management
- Maven Repository Configuration
- Gradle Build Automation
- Java Application Packaging
- User and Role-Based Access Control
- Troubleshooting Deployment Issues
- Version Control with Git

---

## Project Walkthrough


## 1. Provisioning DigitalOcean Infrastructure

### Creating the DigitalOcean Droplet

![Creating Droplet](images/01-droplet-creation.png)

### Applying Firewall Rules

![Firewall Rules](images/02-firewall-rule-applied.png)

### Connecting to the Droplet Using SSH

![SSH Connection](images/03-SSH-into-Droplet.png)

---

## 2. Installing and Configuring Nexus Repository Manager

### Installing Java 17

![Java Installation](images/04--install-java-17-on-droplet.png)

### Validating Java Installation

![Java Validation](images/06--java-install-validation.png)

### Installing Nexus

![Install Nexus](images/07-install-nexus.png)

### Extracting Nexus Files

![Extract Nexus](images/08-untar-nexus-tar-file.png)

### Creating Nexus User

![Nexus User Creation](images/09-nexus-user-creation.png)

### Changing Nexus File Ownership

![Change Ownership](images/10-chown-of-nexus-files.png)

### Configuring Nexus User

![Configure Nexus User](images/11-configure-nexus-user.png)

### Starting Nexus

![Run Nexus](images/12-run-nexus.png)

---

## 3. Configuring Nexus Security

### Updating Firewall Rules

![Firewall Update](images/13-firewall-update.png)

### Validating Browser Access

![Firewall Validation](images/14--browser-validation-of-firewall-rule.png)

### Creating Nexus User in Web UI

![Create Nexus User](images/15-create-nexus-user-in-ui.png)

### Restarting Nexus Manually Through CLI
- This was due to a break period
![Manual Nexus Start](images/16-manual-start-of-nexus-in-cli.png)

### Creating User Role

![Create Role](images/17--create-user-role.png)

### Updating User Permissions

![Updated Role](images/18--updated-user-with-new-role.png)

---

## 4. Publishing Gradle Artifacts to Nexus

### Adding Maven Plugin to Gradle Build

![Gradle Maven Plugin](images/19--add-maven-plugin-to-gradle-build.png)

### Running Gradle Build

![Gradle Build](images/21-gradle-build.png)

### Troubleshooting Gradle Publishing
- Through troubleshooting efforts this was determined to be a user permissions configuration issue.
![Gradle Troubleshooting](images/22-troubleshoot-gradle-publish.png)

### Successful Gradle Publish

![Gradle Publish Success](images/23-publish-success.png)

### Verifying Artifact in Nexus

![Gradle UI Validation](images/24-UI-validation.png)

---

## 5. Publishing Maven Artifacts to Nexus

### Creating Maven Directory and Settings Configuration

![Maven Settings](images/25--create-directory-and-settings-xml.png)

### Running Maven Package

![Maven Package](images/26--mvn-package-success.png)

### Validating JAR File

![JAR Validation](images/27--jar-file-validation.png)

### Deploying Maven Artifact

![Maven Deploy](images/28--mvn-deploy-success.png)

### Verifying Artifact in Nexus

![Maven UI Validation](images/29--ui-validation.png)

---

## Validation

The Nexus artifact repository deployment was validated through multiple testing steps:

- Confirmed successful Nexus web interface access
- Verified user authentication and role-based permissions
- Built Java applications using Gradle
- Published Gradle-generated JAR artifacts to Nexus
- Built Java applications using Maven
- Deployed Maven-generated JAR artifacts to Nexus
- Confirmed uploaded artifacts were available through the Nexus Repository UI

These validation steps demonstrate the complete artifact lifecycle from application build to centralized repository storage.

---

## Future Improvements

- Integrate Nexus authentication with LDAP or Active Directory for enterprise user management
- Automate Nexus deployment using Terraform or Ansible
- Integrate artifact publishing into CI/CD pipelines using GitHub Actions or Jenkins
- Configure Nexus as a systemd service for automated startup
- Implement repository backup and disaster recovery procedures
