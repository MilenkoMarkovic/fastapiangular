FROM node:18

# set up angular cli
RUN yarn global add @angular/cli@15.2.10

WORKDIR /app
COPY package.json /app
COPY yarn.lock /app
RUN yarn install --pure-lockfile
COPY . /app

# create watch files
CMD ng serve --host 0.0.0.0 --disable-host-check
EXPOSE 4200
