FROM node:4.4.4-slim

EXPOSE 7070
WORKDIR /vstu-judge-back

COPY package.json /vstu-judge-back
RUN apt-get update                                           && \
    apt-get install --assume-yes git --no-install-recommends && \
    rm -rf /var/lib/apt/lists/*                              && \
    npm install                                              && \
    apt-get purge --assume-yes --auto-remove git

COPY . /vstu-judge-back

CMD ["npm", "start"]
