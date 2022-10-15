FROM node:16-bullseye-slim as base
RUN echo "# Build of TodoList frontend started"

ENV CONTAINER_NAME="TodoList Frontend"

WORKDIR /code

COPY package.json /code/
COPY package-lock.json /code/

FROM base as pre-todo-list-frontend

# RUN yarn install

COPY ./ /code/

# RUN yarn build

FROM pre-todo-list-frontend as todo-list-frontend

CMD npm run dev
