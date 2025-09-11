adduser paul

usermod -aG sudo paul


mkdir -p /home/paul/.ssh
cp /root/.ssh/id_vps_contabo /home/paul/.ssh/
cp /root/.ssh/id_vps_contabo.pub /home/paul/.ssh/
chown -R paul:paul /home/paul/.ssh
chmod 700 /home/paul/.ssh
chmod 600 /home/paul/.ssh/id_vps_contabo
chmod 644 /home/paul/.ssh/id_vps_contabo.pub


nano /home/paul/.ssh/authorized_keys


ssh -i ~/.ssh/id_vps_contabo paul@IP_DU_SERVEUR

Désactiver SSH root login

sudo nano /etc/ssh/sshd_config

PermitRootLogin no

sudo systemctl restart ssh
