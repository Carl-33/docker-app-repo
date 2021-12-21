# pull the official base image
FROM alpine:3.14

ENV NODE_VERSION 16.13.1
ENV NODE_ENV development
# Add a work directory
WORKDIR /docker-app
# Cache and Install dependencies
COPY package.json .
COPY yarn.lock .
RUN yarn install
# Copy app files
COPY . .
# Expose port
EXPOSE 3000
# Start the app
CMD [ "yarn", "start" ]
