# mycard
in my card available all my social link

**deploye this site simply via EC2 **

2️⃣ Connect to Your EC2 Instance
ssh -i "myCard.pem" ubuntu@<EC2-Public-IP>

3️⃣ Install a Web Server
sudo apt update
sudo apt install apache2 -y

**Enable and start Apache:**
sudo systemctl enable apache2
sudo systemctl start apache2

3️⃣ Install Git on EC2
sudo apt update
sudo apt install git -y

4️⃣ Clone Your Repository
cd /var/www/html
sudo rm index.html   # remove default Apache page
sudo git clone https://github.com/<your-username>/card-website.git .

5️⃣ Verify Permissions
sudo chown -R www-data:www-data /var/www/html
sudo chmod -R 755 /var/www/html

6️⃣ Access Your Website
Open browser → http://<EC2-Public-IP>

Your card website should load 🎉
