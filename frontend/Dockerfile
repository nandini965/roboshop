FROM          nginx
ENV CATALOGUE_HOST=catalogue \
    USER_HOST=user \
    CART_HOST=cart \
    SHIPPING_HOST=shipping \
    PAYMENT_HOST=payment \
    RATINGS_HOST=ratings
COPY          docker-nginx.conf /etc/nginx/nginx.conf
COPY          docker-roboshop.conf /etc/nginx/conf.d/default.conf
RUN           rm -rf /usr/share/nginx/html/*
COPY          ./ /usr/share/nginx/html/
#git pull
