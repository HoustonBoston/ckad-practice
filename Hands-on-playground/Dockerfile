# Use the official Nginx image as a base image
FROM nginx:latest

# Copy custom configuration files into the container
COPY nginx.conf /etc/nginx/
COPY index.html /usr/share/nginx/html/index.html

# Expose port 800
EXPOSE 9080 

CMD ip=$(hostname -i) && echo "<p> hello from $ip !</p>" > /usr/share/nginx/html/index.html && nginx -g "daemon off;"

# Command to run when the container starts (if not default)
# CMD ["nginx", "-g", "daemon off;"] 

