FROM node:argon

# Install Sails globally
RUN npm install -g sails

# Create app directory
RUN mkdir -p /app
# Change Work directory to app
WORKDIR /app

# Install app dependencies
COPY package.json /app/
RUN npm install


# Bundle app source
COPY . /app

EXPOSE 1337

CMD ["sails", "lift"]