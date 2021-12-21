# pull the official base image
FROM node:alpine
# pull the official base image
WORKDIR /docker-app
# add `/app/node_modules/.bin` to $PATH
ENV PATH /docker-app/node_modules/.bin:$PATH
# install application dependencies
COPY package.json ./
COPY package-lock.json ./
RUN npm i
# add app
COPY . ./
# start app
CMD ["npm", "start"]
