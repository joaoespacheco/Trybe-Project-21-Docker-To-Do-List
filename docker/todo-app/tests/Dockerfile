FROM mjgargani/puppeteer:trybe1.0

WORKDIR /usr/app

ADD ./node_modules.tar.gz ./

COPY . .

ENTRYPOINT [ "npm", "test" ]