FROM ankane/pgvector

RUN echo "ja_JP.UTF-8 UTF-8" > /etc/locale.gen && locale-gen
# RUN localedef -i ja_JP -c -f UTF-8 -A /usr/share/locale/locale.alias ja_JP.UTF-8
ENV LANG ja_JP.UTF-8

COPY init.sql /docker-entrypoint-initdb.d/
