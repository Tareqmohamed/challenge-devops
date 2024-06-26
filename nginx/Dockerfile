FROM nginx

# Remove the default Nginx configuration file
RUN rm /etc/nginx/conf.d/default.conf

# Copy the custom Nginx configuration file into the container
COPY custom.conf /etc/nginx/conf.d/custom.conf

# Copy the self-signed SSL certificate and key into the container
COPY ./certs/nginx-selfsigned.crt /etc/ssl/certs/
COPY ./certs/nginx-selfsigned.key /etc/ssl/private/
