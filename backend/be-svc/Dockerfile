FROM node:10.15.1 as builder

# Create app directory
WORKDIR /app

# Install app dependencies
COPY package.json ./

COPY yarn.lock ./

COPY .sequelizerc ./

RUN yarn --silent --network-timeout 1000000

# Bundle app source
COPY app /app

ENV APP_NAME $APP_NAME

COPY run.sh /app/run.sh

EXPOSE 8080

CMD ["sh", "run.sh"]
