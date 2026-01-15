Manuel ssh
 ssh-keygen -t ed25519 -C "your_email@example.com"

ancienne methode

ssh-keygen -t rsa -b 4096 -C "your_email@example.com"

generation de clé

Ajouter la clé publique à un serveur distant 

ssh-copy-id -i ~/.ssh/public_key.pub username@ip_address 

Verifier la connection 

ssh -i ~/.ssh/id_vps_contabo paul@IP_DU_SERVEUR
ou
ssh -T MON_HOST

Toujours de desactiver la connection ssh tu root

# Créer un utilisateur
adduser paul

# Donner les droits sudo
usermod -aG sudo paul

# Configurer la clé SSH (optionnel)
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

Host mon-compte(username github, ie:idpuniv)
    HostName github.com
    User git
    IdentityFile ~/.ssh/id_vps_contabo
    IdentitiesOnly yes
# Test la connectivité

ssh -T idpuniv

