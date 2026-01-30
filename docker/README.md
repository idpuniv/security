## Scan des vulnérabilités avec Trivy

Trivy permet de scanner une image Docker afin de détecter les vulnérabilités connues.

### Commande

```bash
docker run --rm \
  -v /var/run/docker.sock:/var/run/docker.sock \
  aquasec/trivy image sp-cnpi-app:latest
