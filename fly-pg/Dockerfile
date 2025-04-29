ARG PG_MAJOR=17
FROM flyio/postgres-flex:${PG_MAJOR}
ARG PG_MAJOR

RUN apt-get update \
    && apt-get install -y --no-install-recommends postgresql-${PG_MAJOR}-pgvector \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/*

RUN echo "ja_JP.UTF-8 UTF-8" > /etc/locale.gen && locale-gen
# RUN localedef -i ja_JP -c -f UTF-8 -A /usr/share/locale/locale.alias ja_JP.UTF-8
ENV LANG ja_JP.UTF-8

ENV TZ Asia/Tokyo

# COPY init.sql /docker-entrypoint-initdb.d/
