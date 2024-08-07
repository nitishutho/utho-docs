---
title: "How to install NGINX Web Server on Debian 12"
date: "2023-08-05"
title_meta: "GUIDE How to install  NGINX Web Server on Debian 12"
description: "A step-by-step guide on how to install NGINX, a high-performance web server and reverse proxy, on Debian 10."

keywords: ['Debian 10', 'NGINX', 'installation', 'web server', 'reverse proxy', 'Linux']

tags: ["NGINX"]
icon: "Debian"
lastmod: "2024-03-07T17:25:05+01:00"
draft: false
toc: true
aliases: ['/Web-Servers/Nginx/how-to-install-nginx-web-server-on-debian-12']
tab: true
---

![How to install NGINX Web Server on Debian 12](images/How-to-install-NGINX-Web-Server-on-Debian-12-1024x576.jpg)

## Introduction

In this article, you will learn how to install NGINX Web Server on Debian 12.

[NGINX](https://en.wikipedia.org/wiki/Nginx) is free software that can be used for serving web pages, reverse proxying, caching, balancing the load, streaming media, and more. It began out as a web server meant to be as fast and stable as possible. In addition to being an HTTP server, NGINX may also act as a proxy server for email (IMAP, POP3, and SMTP) and as a reverse proxy and load balancer for HTTP, TCP, and UDP servers.

## Step 1: Install NGINX

**1\. Install NGINX with the use of the package manager.**

```
# apt install nginx -y

```

**2\. The NGINX service immediately begins its normal operation. You can use the following command to check the current state of it:**

```
# systemctl status nginx

```

![nginx status](images/image-1234.png)

**3\. You can start using NGINX another time with the following command:**

```
# systemctl enable nginx

```

**4\. To check out how well your installation is working, go to the default NGINX website. You'll locate it by going to the server's IP address in your browser.**

```
# http://server\_ip

```

![Nginx](images/image-846.png)

#### Use NGINX

Through the use of NGINX, this section will guide you through the process of putting up your own website. This explains not only how to set up an NGINX proxy to deliver static content but also how to do so.

## Step 2: NGINX Configuration

**1\. Disable the NGINX configuration file that is provided by default.**

```
# unlink /etc/nginx/sites-enabled/default

```

**2\. Generate an NGINX configuration file for the website you're working on. In this example, replace both the filename and the contents of the file with your site's domain. Do the same thing from now on anytime you see example.com.**

```
# vi /etc/nginx/sites-available/example.com

```

Paste the following content in this file:

```
server {
    listen 80;
    listen [::]:80;
    server_name  example.com;

    root /var/www/example.com;
    index index.html;

    location / {
        try_files $uri $uri/ =404;
    }
}
```

**3\. Bring your NGINX site live.**

```
# ln -s /etc/nginx/sites-available/example.com /etc/nginx/sites-enabled/

```

**4\. Run the following command to check if the NGINX configuration file is correct or not:**

```
# nginx -t

```

![How to install NGINX Web Server on Debian 12](images/image-1235.png)

**5\. In order for changes to take effect, you will need to restart NGINX.**

```
# systemctl restart nginx

```

## Step 3: Set Up the Website

**1\. Make a directory to store the content of your NGINX website.**

```
# mkdir /var/www/example.com

```

**2\. In the new NGINX site directory, you must create an index.html page.**

```
# vi /var/www/example.com/index.html

```

**Paste the following content in this file:**

```
<!doctype html>
<html>
<body>
    <h1>Hello, Guys!</h1>
    <p>This is an example website running on NGINX.</p>
</body>
</html>
```

**3\. Just type your site's domain name into a browser to check it out. There should be a "Hello, Guys!" page shown on your domain.**

![install NGINX Web Server](images/image-849.png)

## Conclusion

Hopefully, you have learned how to install NGINX Web Server on Debian 12.

Also Read: [How to host a domain on centos 7](https://utho.com/docs/tutorial/how-to-host-a-domain-on-centos-7/)

Thank You 🙂
