# Use the official Nginx base image
FROM nginx:latest

# rm your custom Nginx configuration file to the container
RUN rm -f /etc/nginx/conf.d/default.conf  

# (Optional) Add any additional configurations or files as needed
COPY nginx.conf /etc/nginx/conf.d/nginx.conf

# Expose the port on which Nginx will run
EXPOSE 80

# Command to start Nginx when the container starts
CMD ["nginx", "-g", "daemon off;"]

