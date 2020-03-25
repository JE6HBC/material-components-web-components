FROM node:13.10-stretch

# sample public root directory
RUN mkdir /hostMount
COPY ./ /hostMount/

## npm package should be installed with package.json

# install local dependencies
WORKDIR /hostMount/public
RUN npm install @material/mwc-button @webcomponents/webcomponentsjs

# install global dependencies for dev
RUN npm install -g es-dev-server

# deploy for dev
ENTRYPOINT ["es-dev-server", "--node-resolve", "--watch"]
