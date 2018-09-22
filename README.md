# IBM Watson Assistant Journey with IBM LinuxONE Systems

In this Code Pattern, you will learn how to build and deploy a cognitive microservice with IBM Cloud private running in the IBM LinuxONE Community Cloud. 

IBM Cloud Private is a private cloud platform for developing and running workloads locally. It is an integrated environment that enables you to design, develop, deploy and manage on-premises, containerized cloud applications behind a firewall. It includes the container orchestrator Kubernetes, a private image repository, a management console and monitoring frameworks.

When you will complete this Code Pattern, you will understand how to:

* Create an IBM Watson Assistant Service in IBM Cloud
* Build a Docker image from an existing application.
* Deploy a Docker image to IBM Cloud Private.
* Deploy an existing application using the IBM Cloud Private catalog.
* Talk & get it done with IBM LinuxONE systems !


# Architecture

This journey provides a chatbot interface to demonstrate how you can simply integrate with an IBM LinuxONE System or, potentially any other system. IBM Cloud private has been configured into the LinuxOne LinuxONE Community Cloud.


## Overview
1. The user creates a Cognitive service with an IBM Watson Assistant Service in IBM Cloud and load a pre-defined corpus,
2. The user code and create a Docker image (Node.js application based microservice) & publish it to the IBM Cloud Private Docker registry.
3. The user configures and runs a container based on the previous Docker image from IBM Cloud Private catalog.
4. A chatbot interface allows the user to "discuss" with the IBM LinuxONE System to deploy cloud services (execute actions).
5. The developer can extend this pattern to interact with its own on-premises servers using an IBM Secure Gateway service from IBM Cloud.

## Sequence Diagram Overview
Here is an overview of the interactions betwwen each layer of this code pattern. 
![alt text](https://github.com/SebLL/AWAP/blob/master/SequenceDiagram.png)

# Included components

* [IBM LinuxONE Systems](https://www.ibm.com/it-infrastructure/linuxone)
* [IBM Z (Mainframe)](https://www.ibm.com/it-infrastructure/z)
* [IBM Cloud Private](https://www.ibm.com/cloud/private)
* [OpenStack](https://www.openstack.org/)
* [Integration with VMWare vRealize Automation](https://www.ibm.com/blogs/systems/making-hybrid-cloud-easier-vmware-ibm-systems/)
* [Watson Assistant](https://www.ibm.com/watson/ai-assistant/)

# Featured technologies

* Open source technologies: Docker, Kubernetes, Node.js, OpenStack
* IBM Systems: IBM LinuxONE Systems, IBM Z
* IBM Private Cloud (ICP) solution
* Cognitive/AI technologies: Watson Assistant (aka. "Conversation Service")
* Partner solution (possible extensions): IBM VMWare vRealize Automation (vRA)
* Integration services: Rest APIs of OpenStack and vRA, IBM Secure Gateway services

# Steps

<!-- https://ecotrust-canada.github.io/markdown-toc/ -->

### Step 1 - Create an IBM Watson Assistant Service


### Step 2 - Build and deploy a Docker image to IBM Cloud private

- [Part 1 - Build the Docker image from the LinuxOne Community Cloud](#part-1---build-the-docker-image-from-the-linuxone-community-cloud)
- [Part 2 - Deploy the Docker image to IBM Cloud private](#part-2---deploy-the-docker-image-to-ibm-cloud-private)

### Step 3 - Instantiate the provisiong chatbot based microservice from the IBM Cloud private catalog

### Step 4 - Talk and get it done with IBM LinuxONE Systems

### Step 5 - Extend this solution to access your on-premises servers

---

# Step 1 - Discover and locally run the provisioning chatbot application

The objective is to discover the banking application located in the *banking-application* folder. This application is a Node.js application. It will be locally tested before packaging it into a Docker image for IBM Cloud private.

## Part 1 - Discover the provisioning chatbot application

1. Create a [GitHub account](https://github.com/).

	![alt text](images/github_signup.png "Sign up")
	* Pick a username. This will be referenced later as "YOUR_USERNAME".
	* Enter an email.
	* Create a password.
	* Click **Sign up for GitHub**.
	* Select the plan *Unlimited public repositories for free*.
	* A Confirmation email will be sent. Verify your email address to collaborate in Github.

2. Fork the provisioning chatbot application from this GitHub repository to your own GitHub repository.

	![alt text](images/fork.png "Fork the provisioning chatbot app")
	* Click **Fork**.
	* Github automatically forks this project from this repository *IBM/conversation-with-linuxone-using-watson-microservices* to your repository *YOUR_USERNAME/conversation-with-linuxone-using-watson-microservices*.
	* Discover your forked project (your fresh provisioning chatbot application) in your Github repository *YOUR_USERNAME/conversation-with-linuxone-using-watson-microservices*.

3. Install the [Git command line interface](https://git-scm.com/book/en/v2/Getting-Started-The-Command-Line) to manage your GitHub repository. Git has three main commands:
	* *git clone* is the command for creating a local copy of the source code from a GitHub repository.
	* *git pull* is the command for pulling fresh code from a GitHub repository.
	* *git push* is the command for pushing new code to a GitHub repository.

4. Launch a terminal and clone your GitHub repository *conversation-with-linuxone-using-watson-microservices* to create a local copy of your banking application:

   `git clone https://github.com/YOUR_USERNAME/conversation-with-linuxone-using-watson-microservices`
    
	![alt text](images/clone.png "Clone the provisioning chatbot app")
	
