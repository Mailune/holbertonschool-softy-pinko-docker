# Use the official Nginx image from the Docker Hub
FROM nginx:latest

# Copy the front-end files to the appropriate directory in the Nginx container
COPY ./softy-pinko-front-end /var/www/html/softy-pinko-front-end

# Copy the custom Nginx configuration file
COPY ./softy-pinko-front-end.conf /etc/nginx/conf.d/default.conf
