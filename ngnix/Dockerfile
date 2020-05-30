FROM nginx:stable-alpine
WORKDIR /nginx
RUN chown nginx:nginx /nginx
USER nginx
COPY ./conf /nginx/conf
CMD ["nginx", "-c", "/nginx/conf/nginx.conf"]
