FROM nginx:stable-alpine
RUN apk add --update nodejs
RUN apk add --update npm
WORKDIR /nginx
RUN chown nginx:nginx /nginx
USER nginx
COPY ./nginx.conf /etc/nginx/
CMD ["nginx"]
USER root
RUN mkdir -p /node/blog-app
RUN apk add git
WORKDIR /node/blog-app
RUN git clone -b ngnix-demo https://github.com/eslamkarim/node-blog.git
WORKDIR /node/blog-app/node-blog
RUN ls
RUN npm install
EXPOSE 3000
EXPOSE 80
EXPOSE 8080
CMD node index.js