# HTML on AWS EC2

This is just a small practice project I did to understand how to put a simple HTML page online using AWS EC2.  
I’m still learning, so this is very basic.

---

## What I did

- Created an Ubuntu EC2 (free tier)
- Opened ports for SSH (22) and HTTP (80)
- Logged in using my .pem key
- Installed Apache
- Put my HTML files inside `/var/www/html`

---

## Steps I followed (very simple)

1. Launched an EC2 Ubuntu server  
2. Connected to it:

   ```bash
   chmod 400 my-key.pem
   ssh -i my-key.pem ubuntu@PUBLIC_IP
Installed Apache:

bash
Copy code
sudo apt update
sudo apt install apache2 -y
Replaced default page with my own HTML:

bash
Copy code
cd /var/www/html
sudo rm index.html
sudo cp /home/ubuntu/*.html /var/www/html/
