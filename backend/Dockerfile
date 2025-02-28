FROM node:20
WORKDIR /opt/backend
COPY package.json .
COPY *.js .
# This will install all dependencies using package.json.
RUN npm install     
# As IP address will change everytime after container restart, we need to depend on dns names, so we have created NAMES for containers. "mysql" is the NAME of container.
ENV DB_HOST="mysql"  

# we use this for HOST NETWORK TYPE
# ENV DB_HOST="localhost"       
CMD ["node", "index.js"]