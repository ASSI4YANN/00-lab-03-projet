# Image de base Python légère (slim = version allégée)
FROM python:3.13-slim
 
# Information sur le mainteneur de l'image
LABEL maintainer="Yann Assi <yann84637@gmail.com>"

# Définit le dossier de travail dans le conteneur
# Toutes les commandes suivantes seront exécutées ici 
WORKDIR /app
 
# Copie les fichiers de l'API dans le répertoire racine du conteneur
COPY . .
  
# Installation des prérequis
RUN apt update -y && apt install -y build-essential python3-dev libsasl2-dev libldap2-dev libssl-dev &&  rm -rf /var/lib/apt/lists/*

#Installation des dépendances Python
RUN pip3 install -r /app/requirements.txt

# Créer le dossier /data dans le conteneur
RUN mkdir -p /data

# Déclarer /data comme volume
VOLUME ["/data"]

# Port d'exposition 
EXPOSE 5000

# Commande de démarrage du conteneur
CMD ["python", "./student_age.py"]
