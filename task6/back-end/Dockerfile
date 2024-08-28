# Utilisez une image de base appropriée
FROM ubuntu:latest

# Installer les dépendances de base
RUN apt-get update && \
    apt-get upgrade -y && \
    apt-get install -y python3 python3-pip python3-venv

# Créer un environnement virtuel
RUN python3 -m venv /env

# Activer l'environnement virtuel
ENV PATH="/env/bin:$PATH"

# Installer Flask et Flask-CORS dans l'environnement virtuel
RUN pip install flask flask-cors

# Définir le répertoire de travail
WORKDIR /app

# Copier le code source dans l'image
COPY api.py /app/api.py

# Exposer le port sur lequel l'application Flask fonctionnera
EXPOSE 5252

# Définir la commande pour démarrer l'application Flask
CMD ["python", "api.py"]
