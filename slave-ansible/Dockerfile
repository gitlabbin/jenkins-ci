FROM openshift/jenkins-slave-base-centos7

LABEL org.centos.component="jenkins-slave-ansible" \
      name="jenkins-slave-ansible" \
      architecture="x86_64" \
      io.k8s.display-name="Jenkins Slave ansible" \
      io.k8s.description="Ansible tools on top of the jenkins slave base image" \
      io.openshift.tags="openshift,jenkins,slave,ansible"
USER root

RUN yum install epel-release -y
RUN yum install jq curl -y
RUN yum install -y git bzip2 ansible

RUN yum -y --setopt=tsflags=nodocs update && \
    yum -y --setopt=tsflags=nodocs install socat && \
    yum -y --setopt=tsflags=nodocs install wget && \
    yum -y --setopt=tsflags=nodocs install git && \
    yum -y --setopt=tsflags=nodocs install tmux

RUN yum clean all
RUN ansible --version

USER 1001
