FROM evarga/jenkins-slave
MAINTAINER Matthias Vegh <matyas.vegh@gmail.com>

RUN apt-get update && \
	DEBIAN_FRONTEND="noninteractive" apt-get -y --no-install-recommends install\
	build-essential gcc wget libcap-dev

RUN wget "http://man7.org/tlpi/code/online/dist/namespaces/userns_child_exec.c"
RUN gcc -lcap -o /usr/local/bin/userns_child_exec userns_child_exec.c

COPY containedbash /usr/local/bin/
RUN echo "/usr/local/bin/containedbash" >> /etc/shells

RUN chsh --shell /usr/local/bin/containedbash jenkins
