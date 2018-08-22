# Run gtop (https://github.com/aksakalli/gtop) in a container.
# CPU graph and network statistics work fine using the host's PID and network namespaces
#
# docker run \
#	--pid host \ 
#	--net host \
#	--interactive \
#	--tty \
#	--rm \
#	--name gtop \
#	eikaas/gtop
FROM alpine:3.4
LABEL maintainer "Robin Eikaas <robin@eika.as>"

RUN apk add --update nodejs
RUN npm install gtop -g

ENV TERM=xterm-256color
ENV LANG=en_US.utf8

ENTRYPOINT ["gtop"]
