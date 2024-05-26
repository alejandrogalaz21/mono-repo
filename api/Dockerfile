FROM node:latest

ARG NODE_ENV
ENV NODE_ENV=${NODE_ENV}

# Set the workdir to create the build
WORKDIR /usr/src/app

# Copy the required files to install the dependencies
COPY package.json yarn.lock ./

# Install the dependencies
RUN yarn install --pure-lockfile 

# Copy the source code to the workdir
COPY . ./
RUN yarn build

# Start the server using the production build
CMD [ "node", "dist/main.js" ]
