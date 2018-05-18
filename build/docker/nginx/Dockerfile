FROM nginx:alpine

ARG PROJECT_HOST
ARG PROJECT_PUBLIC_PATH
ARG PROJECT_ROOT_PATH

RUN apk upgrade --update && apk --no-cache add \
    bash \
    mc \
    nano \
    vim

COPY site.conf /etc/nginx/conf.d/site.conf
RUN sed -i "s!<PROJECT_HOST>!${PROJECT_HOST}!g;s!<PROJECT_PUBLIC_PATH>!${PROJECT_PUBLIC_PATH}!g;s!<PROJECT_ROOT_PATH>!${PROJECT_ROOT_PATH}!g" /etc/nginx/conf.d/site.conf