FROM deeplymax/vstu-judge-back

WORKDIR /vstu-judge-queue

COPY package.json /vstu-judge-queue
RUN npm install

COPY . /vstu-judge-queue
ENV VSTU_JUDGE_QUEUE_BACK_SERVER http://localhost:7070

CMD ["npm", "start"]
