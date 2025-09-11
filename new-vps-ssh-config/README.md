# Créer un utilisateur
adduser paul

# Donner les droits sudo
usermod -aG sudo paul

# Configurer la clé SSH
mkdir -p /home/paul/.ssh
cp /root/.ssh/id_vps_contabo /home/paul/.ssh/
cp /root/.ssh/id_vps_contabo.pub /home/paul/.ssh/
chown -R paul:paul /home/paul/.ssh
chmod 700 /home/paul/.ssh
chmod 600 /home/paul/.ssh/id_vps_contabo
chmod 644 /home/paul/.ssh/id_vps_contabo.pub

# Ajouter la clé publique dans authorized_keys
nano /home/paul/.ssh/authorized_keys

# Tester la connexion avec le nouvel utilisateur
ssh -i ~/.ssh/id_vps_contabo paul@IP_DU_SERVEUR

# Désactiver la connexion SSH root
sudo nano /etc/ssh/sshd_config
# Modifier la ligne :
PermitRootLogin no

# Redémarrer le service SSH
sudo systemctl restart ssh

# Configure SSH pour utiliser la bonne clé
nano ~/.ssh/config

Host github.com
    HostName github.com
    User git
    IdentityFile ~/.ssh/id_vps_contabo
    IdentitiesOnly yes

