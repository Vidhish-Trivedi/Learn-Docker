# Image name on docker hub, or locally on our machine.
FROM node

# Set a working directory on the image. (`.` refers to WORKDIR)
WORKDIR /app

# Copy files from local machine to image, can be optimized.
# Docker looks for the first command (or Image Layer) which has been modified,
# and all subsequent instructions are run again.
# Here, we copied package.json seperately to avoid `npm install` from being executed unnecessarily (when only source code is changed).
# COPY . .
COPY package.json .

# Run a command after copying (By default, executed in the working directory on the image, i.e, root (`.`). Unless WORKDIR is set).
RUN npm install

# Copy remaining files.
COPY . .

# Now the image has been setup.

# Expose a certain port (from the container) to our local machine.
EXPOSE 80

# CMD runs when a new container is started using this image, not while creating an image. Usually it is the last instruction in a Dockerfile.
CMD [ "node", "server.js" ]
