FROM node:18-buster-slim as build

ENV EXPO_PUBLIC_API_URL = https://api.blackzone.mx
ENV EXPO_PUBLIC_ENV=production

WORKDIR /app
COPY . /app

# Install the dependencies
RUN npm install -g expo-cli
RUN yarn install
RUN yarn build:web

FROM ubuntu
RUN apt-get update
RUN apt-get install nginx -y
COPY --from=build /app/dist /var/www/html/
EXPOSE 80
CMD ["nginx","-g","daemon off;"]
#hello world