FROM node:14.15
#Create directory of application
WORKDIR /usr/src/app

COPY package*.json ./
#Install packages
RUN npm ci

#GROUP application source
COPY . .
EXPOSE 8080
CMD ["npm", "run", "prod"]