scan des vulnerabilité avec try

docker run --rm \
  -v /var/run/docker.sock:/var/run/docker.sock \
  aquasec/trivy image sp-cnpi-app:latest



  conformité aux bonne pratique

git clone https://github.com/docker/docker-bench-security.git
cd docker-bench-security
sudo sh docker-bench-security.sh
