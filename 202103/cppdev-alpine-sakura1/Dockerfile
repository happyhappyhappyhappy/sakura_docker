FROM alpine:3.13.3
# ユーザーsakuraを作成した上で環境作成 20210307
RUN apk update && \
    apk add --no-cache bind-tools tzdata sudo && \
    apk add --no-cache coreutils alpine-sdk cmake clang && \
    apk add --no-cache libressl-dev vim bash shadow git 
RUN cp /usr/share/zoneinfo/Japan /etc/localtime
RUN addgroup -g 10001 -S nonroot
# https://qiita.com/cheekykorkind/items/ad499245bda4c85c6d75 参照
# RUN adduser --shell /bin/bash --uid 10000 -G nonroot --home /home/sakura
