FROM node:14  as builder
RUN mkdir /app
WORKDIR /app
RUN git clone https://github.com/Rhymond/product-compare-react
WORKDIR /app/product-compare-react
RUN npm install && npm run build

FROM nginx:latest
COPY --from=builder /app/product-compare-react/build /usr/share/nginx/html
