Here's a detailed `basic_installation.md` for your GitHub repository:

```markdown
# Basic Installation of Nginx on Ubuntu

This guide provides step-by-step instructions for installing Nginx on an Ubuntu system.

## Prerequisites

- A server running Ubuntu (18.04, 20.04, or 22.04).
- A user with `sudo` privileges.

## Step 1: Update the Package Index

Before installing any new software, it's good practice to update the package index to ensure you have the latest information about available packages.

```sh
sudo apt update
```

## Step 2: Install Nginx

Install the Nginx package from the default Ubuntu repositories using the following command:

```sh
sudo apt install nginx
```

The package manager will automatically download and install Nginx along with its dependencies.

## Step 3: Start and Enable Nginx

Once the installation is complete, start the Nginx service and enable it to start on boot.

### Start Nginx

```sh
sudo systemctl start nginx
```

### Enable Nginx to Start on Boot

```sh
sudo systemctl enable nginx
```

## Step 4: Verify Nginx Installation

To confirm that Nginx is running, you can check its status with the following command:

```sh
sudo systemctl status nginx
```

You should see output indicating that the service is active and running.

## Step 5: Configure Firewall (Optional)

If you are using `ufw` (Uncomplicated Firewall) to manage your firewall settings, you will need to allow traffic on HTTP (port 80) and HTTPS (port 443) ports.

### Allow HTTP and HTTPS Traffic

```sh
sudo ufw allow 'Nginx Full'
```

### Check the Status of the Firewall

```sh
sudo ufw status
```

## Step 6: Test Nginx

To ensure Nginx is working correctly, open your web browser and navigate to your server's IP address. You should see the default Nginx welcome page, which confirms that Nginx is installed and serving web pages.

### Access Nginx Default Page

1. Open a web browser.
2. Enter your server's IP address (e.g., `http://your_server_ip/`).

You should see the default Nginx welcome page with the message "Welcome to nginx!".

## Troubleshooting

- **Nginx is not running:** Check the status of the Nginx service with `sudo systemctl status nginx` and review the logs if necessary.

- **Firewall issues:** Ensure that the firewall is configured to allow HTTP and HTTPS traffic.

- **Permission issues:** Verify that you are using a user with `sudo` privileges for installation and configuration tasks.

## Conclusion

You have successfully installed Nginx on your Ubuntu server. You can now proceed with configuring Nginx for your specific needs or explore additional Nginx features.

For more detailed configuration options and advanced features, refer to the [Nginx Documentation](https://nginx.org/en/docs/).

```

This file should give users a clear and straightforward guide to getting Nginx up and running on Ubuntu.
