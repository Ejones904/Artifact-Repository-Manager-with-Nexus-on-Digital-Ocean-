# Artifact Repository Manager with Nexus on DigitalOcean

## Overview

## Technical Solution

## Technologies Used

## Key Skills Demonstrated

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

### Starting Nexus Manually Through CLI

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
