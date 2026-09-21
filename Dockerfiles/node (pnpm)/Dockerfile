FROM mhart/alpine-node:14

RUN apk add curl

COPY [".", "/usr/src"]

WORKDIR "/usr/src"

RUN pnpm i

ARG NODE_ENV

CMD if [ "$NODE_ENV" = "develop" ] ; then pnpm run dev ; else pnpm run start ; fi