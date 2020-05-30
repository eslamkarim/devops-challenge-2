FROM node:alpine
RUN mkdir -p /node/blog-app & \
    apk add git
WORKDIR /node/blog-app
RUN git clone -b ngnix-demo https://github.com/eslamkarim/node-blog.git
WORKDIR /node/blog-app/node-blog
RUN ls & \
    npm install
EXPOSE 3000
CMD node index.js