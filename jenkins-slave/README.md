# jenkins-slave
A Jenkins slave based on
[evarga/jenkins-slave](https://hub.docker.com/r/evarga/jenkins-slave/), with the
addition of the login shell being changed from `sh` to bash, and using user and
mount namespaces to allow for mounting a tmpfs during jobs.
