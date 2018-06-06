# Installing MIMO Using Docker

This guide covers a basic installation of MIMO on a single service using Docker.

## Requirements

- FQDN - a domain name - MIMO needs a fully qualified domain, like wisp.services
- Linux server - see requirements below
- Working DNS 

## Hardware Requirements
 
- Singal or dual core CPU (dual core recommended)
- 1 GB RAM minimum (with swap)
- 64 bit Linux compatible with Docker
- 10 GB disk space minimum

## Create a new server

Instructions for each provider to follow...

We recommend [Digital Ocean](https://m.do.co/c/8504487cbb3a) but you can use whoever you want. You can use [this link](https://m.do.co/c/8504487cbb3a) to get $10 off your first server - that's two months free ;)

## Domain Name

MIMO will NOT work without a domain name - you cannot use MIMO with an IP. 

If you don't have a domain name, there's a gazillion places online for you to get one from. We recommend [Namecheap](https://namecheap.pxf.io/c/1248558/386170/5618). They're cheap & reliable.

If you do have a domain name, all you need to do is add the records below to your DNS.

## DNS records

Find the public IP address for your newly created server. This needs to be the publicly available IP address.

Add the following A-records to your DNS records:

- api
- admin
- dashboard
- splash

For example, if your public IP address is 1.2.3.4 and your chosen domain is wisp.services you need the following records:

- api.wisp.services - 1.2.3.4
- admin.wisp.services - 1.2.3.4
- dashboard.wisp.services - 1.2.3.4
- splash.wisp.services - 1.2.3.4

Make sure these resolve *before* you start the installation.

We recommend using Cloudflare for your DNS however it's up to you who you chose. If you're using Cloudflare, you will need to disable their firewall before the installation. You can reactivate this afterwards.

## Firewall

Ports 80 and 443 must be allowed - update your firewall settings to ensure these are open and accessible.

## Email Server

MIMO requires a functioning SMTP / Email server. You can use whoever you want but we recommend one of the following:

- SendGrid
- Mailgun
- Elastic Email

Once you've created your account, save the credentials as you'll need them during the installation process.

We do not recommend using Gmail's SMTP server or your own one. The ones above are cheap and reliable.

## Login to your server

bla bla bla

Using your favourite shell, including putty or ssh, login to your newly created server:

```
ssh root@ip-address
```

If you're using [Digital Ocean](https://m.do.co/c/8504487cbb3a), you will need to update your password.

### Install Docker and Git

```
wget -qO- https://get.docker.com/ | sh
```

This installs Docker & Git on your machine. You may need to install Git manually.

Check they were installed correctly. Git:

```
git version
git version 2.7.4
```

Docker:

```
docker --version
Docker version 18.05.0-ce, build f150324
```

The exact versions may differ.

If either failed, please re-install. The git installation guide can be found here:

https://git-scm.com/book/en/v2/Getting-Started-Installing-Git

### Install MIMO

Create a new folder for your installation and clone the official MIMO images into it:

```
sudo -s
mkdir /var/mimo
git clone https://github.com/mimolabs/mimo-docker.git /var/mimo
cd /var/mimo
./docker-install.sh
```

You must enter valid SMTP credentials otherwise your MIMO installation won't work.

After the installation has completed, you should receive a welcome message.

### Finishing Up

The email that was sent includes a magic link that will allow you to complete the installation. If you did not get the email, please check your spam and ensure you set the correct SMTP credentials.

If you're sure the email is not in your spam - re-check your SMTP credentials. Run the installer again, adding the correct variables. 
