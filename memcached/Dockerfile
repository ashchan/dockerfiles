FROM ubuntu:14.04
MAINTAINER James Chen <ashchan@gmail.com> (@ashchan)

RUN apt-get update
RUN apt-get install -y memcached

CMD ["-m", "128"]

USER daemon

EXPOSE 11211

ENTRYPOINT memcached

