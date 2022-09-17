##Build
FROM beevelop/ionic:latest AS ionic
#Create directory of application
WORKDIR /usr/src/app

COPY package*.json ./

#install dependencies
RUN npm ci
#Group application sources
COPY . .
RUN ionic build 

## Launch
FROM nginx:alpine
#Copy www /usr/share/nginx/html
COPY --from=ionic /usr/src/app/www /usr/share/nginx/html