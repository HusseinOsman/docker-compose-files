# pull official base image
FROM node:16.10

WORKDIR /app
# To handle 'not get ui/get'
RUN npm config set unsafe-perm true

COPY ./react-app/ /app
# add `/app/node_modules/.bin` to $PATH
ENV PATH /app/node_modules/.bin:$PATH

# set working directory
RUN npm install 
RUN npm install react-scripts@3.4.4 -g


# start app
CMD npm start
