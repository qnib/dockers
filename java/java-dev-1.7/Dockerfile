FROM iron/base

RUN echo '@edge http://nl.alpinelinux.org/alpine/edge/main' >> /etc/apk/repositories
RUN echo '@community http://nl.alpinelinux.org/alpine/edge/community' >> /etc/apk/repositories
RUN apk update && apk upgrade

RUN apk add openjdk7
# puts javac in the PATH
ENV PATH=/usr/lib/jvm/java-1.7-openjdk/bin:$PATH

# Clean APK cache
RUN rm -rf /var/cache/apk/*
