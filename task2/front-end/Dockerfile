# Use the latest version of nginx
FROM nginx:latest

# Copy the softy-pinko-front-end files to the Nginx HTML directory
COPY . /var/www/html/softy-pinko-front-end

# Copy the Nginx config file to the Nginx configuration directory
COPY softy-pinko-front-end.conf /etc/nginx/conf.d/default.conf

# Expose port 9000 for the web server
EXPOSE 9000

# Start Nginx when the container launches
CMD ["nginx", "-g", "daemon off;"]
