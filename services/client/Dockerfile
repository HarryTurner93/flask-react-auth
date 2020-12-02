# pull official base image
FROM node:15.2.0-alpine

# set working directory
WORKDIR /usr/src/app

# add to path
ENV PATH /usr/src/app/node_modules/.bin:$PATH

# install and cache app dependencies
COPY package.json .
COPY package-lock.json .
RUN npm ci
RUN npm install react-scripts@4.0.0 prettier@2.1.1 eslint@7.13.0 eslint-config-standard-jsx@10.0.0 -g --silent

# start app
CMD ["npm", "start"]