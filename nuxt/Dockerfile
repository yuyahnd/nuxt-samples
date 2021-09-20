FROM node:lts as builder

RUN yarn install \
  --prefer-offline \
  --frozen-lockfile \
  --non-interactive \
  --production=false

RUN rm -rf node_modules && \
  NODE_ENV=production yarn install \
  --prefer-offline \
  --pure-lockfile \
  --non-interactive \
  --production=true

ENV HOST 0.0.0.0
EXPOSE 80

# CMD [ "yarn", "start" ]
