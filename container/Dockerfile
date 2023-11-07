# Test web app that returns the name of the host/pod/container servicing req
FROM node:current-alpine

RUN echo "Basic node downloaded."

LABEL org.opencontainers.image.title="Hello Docker Learners!" \
      org.opencontainers.image.description="Web server showing host that responded" \
      org.opencontainers.image.authors="@nigelpoulton"

RUN echo "Labels to the image added."

# Create directory in container image for app code
RUN mkdir -p /usr/src/app

# Copy app code (.) to /usr/src/app in container image
COPY . /usr/src/app

# Set working directory context
WORKDIR /usr/src/app

# Install dependencies from package.json
RUN echo "Installing dependencies..."
RUN npm install
RUN echo "Dependencies installed."

# Command for container to execute
ENTRYPOINT [ "node", "app.js" ]