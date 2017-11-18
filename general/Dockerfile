FROM docker

ENV TARGET /MusicRoom

RUN apk add --no-cache \
        git \
        py-pip \
        && mkdir ${TARGET}

RUN pip install docker-compose

WORKDIR ${TARGET}

ADD docker-compose.yaml .

ADD git@github.com:MusicRoom42/mr-api.git \
ADD git@github.com:MusicRoom42/mr-mail.git

# RUN addgroup docker \
#         && adduser root docker

# # USER docker

ENTRYPOINT docker-compose up
