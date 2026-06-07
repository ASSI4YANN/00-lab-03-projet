# Image de base Python légère (slim = version allégée)
FROM python:3.13-slim

# Information sur le mainteneur de l'image
LABEL maintainer="Yann Assi <yann84637@gmail.com>"

ADD student_age.py /
# Installation des prérequis
RUN apt update -y && apt install -y build-essential python3-dev libsasl2-dev libldap2-dev libssl-dev && rm -rf /var/lib/apt/lists/*

#Installation des dépendances Python
RUN pip3 install -r /app/requirements.txt

# Déclarer /data comme volume
VOLUME ["/data"]

# Port d'exposition 
EXPOSE 5000

# Commande de démarrage du conteneur
CMD ["python", "./student_age.py"]
