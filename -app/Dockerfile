# build environment
FROM node:current-alpine as build

ARG IMAGE_VERSION
ENV VERSION=$IMAGE_VERSION
ENV PORT 80

ARG API_URL
ENV REACT_APP_BASE_URL=$API_URL
ENV SKIP_PREFLIGHT_CHECK=true

WORKDIR /app
COPY . ./
RUN yarn install
RUN yarn build


FROM nginx:stable-alpine
COPY --from=build /app/build /usr/share/nginx/html
COPY --from=build /app/server.conf /etc/nginx/conf.d/default.conf
EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]
