# Use the official Redis base image
FROM redis:latest

# Expose the default Redis port (6379)
EXPOSE 6379

# Copy custom Redis configuration file
COPY redis.conf /etc/redis/redis.conf

# CMD is the default command to run when the container starts
CMD ["redis-server"]

