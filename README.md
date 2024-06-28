# Static Website Deployment

## Overview

This repository contains a static website deployment project. The goal is to deploy a static website onto a cloud platform, specifically using Google Cloud Platform (GCP) and NGINX as the web server. This project is part of the HNG Internship, which is a helpful and self-development internship to become a world-standard DevOps engineer.

## Table of Contents

- [Task](#task)
- [Requirements](#requirements)
- [Acceptance Criteria](#acceptance-criteria)
- [Submission Mode](#submission-mode)
- [HNG Internship](#hng-internship)
- [How to Deploy on GCP](#how-to-deploy-on-gcp)
- [Contact Information](#contact-information)

## Task

In this stage, you'll step into the shoes of a DevOps engineer and deploy a static website onto a cloud platform.

### Steps:
1. **Cloud Platform:** Choose a cloud platform of your preference (AWS EC2, Azure, GCP, etc) to deploy your website.
2. **Web Server:** Select a web server software like NGINX or Apache to serve your static website content.
3. **Website Preparation:** Ensure your static website files (HTML, CSS, Javascript) are ready for deployment.
4. **Server Configuration:** Configure the chosen web server (NGINX or Apache) on your cloud instance to serve your website content.

## Requirements

- **Cloud Platform:** AWS EC2, Azure, or GCP (your choice)
- **Web Server:** NGINX or Apache
- **Static Website:** A ready-to-deploy static website project (HTML, CSS, Javascript) which includes your Name, username, and your email.

## Acceptance Criteria

- **Successful Deployment:** Your static website is accessible through a public IP address or a domain name after deployment. The IP address shouldn’t include ports asides port 80.
- **Web Server Configuration:** The chosen web server (NGINX or Apache) is configured correctly to serve your website content.

## Submission Mode

Submit your task through the designated submission form. Ensure you've:

- Double-checked all requirements and acceptance criteria.
- Provided a link to your deployed website in the submission form.
- Thoroughly reviewed your work to ensure accuracy, functionality, and adherence to the specified guidelines before you submit it.

## HNG Internship

The HNG Internship is a very helpful and self-development internship to become a world-standard DevOps engineer. For more information, visit [HNG Internship](https://hng.tech).

## How to Deploy on GCP

Follow these steps to deploy your static website on Google Cloud Platform (GCP) using NGINX:

1. **Create a GCP Account and Project**
    ![Create GCP Project](https://cloud.google.com/images/cloud-console.png)
2. **Enable Billing for Your Project**
    ![Enable Billing](https://cloud.google.com/billing/images/setting_up_billing.png)
3. **Create a VM Instance**
    ![Create VM Instance](https://cloud.google.com/images/creating-vm-instance.png)
4. **Connect to Your VM Instance**
    ![Connect to VM Instance](https://cloud.google.com/images/ssh-connection.png)
5. **Install NGINX on Your VM**
    ```bash
    sudo apt update
    sudo apt install nginx
    ```
    ![Install NGINX](https://www.nginx.com/wp-content/uploads/2018/08/NGINX-logo-rgb-large.png)
6. **Upload Your Website Files**
    ```bash
    scp -i /path/to/your-ssh-key -r /path/to/your-website-files username@your-vm-external-ip:/home/username
    ```
    ![Upload Files](https://cloud.google.com/images/upload-files.png)
7. **Move Your Website Files to the NGINX Directory**
    ```bash
    sudo mv /home/username/your-website-files/* /var/www/html/
    sudo chown -R www-data:www-data /var/www/html/
    ```
    ![Move Files](https://cloud.google.com/images/move-files.png)
8. **Restart NGINX**
    ```bash
    sudo systemctl restart nginx
    ```
    ![Restart NGINX](https://www.nginx.com/wp-content/uploads/2020/10/NGINX-Logo-2020-Graphics.jpg)
9. **Access Your Website**
    Open a web browser and navigate to your VM's external IP address. Your static website should be displayed.
    ![Access Website](https://cloud.google.com/images/access-website.png)

## Contact Information

- **Name:** Your Name
- **Username:** yourusername
- **Email:** youremail@example.com

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
