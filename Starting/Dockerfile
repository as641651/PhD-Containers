FROM centos:centos7.6.1810

RUN yum -y update
RUN yum -y install vim
RUN yum -y install redhat-lsb
RUN yum -y install epel-release
RUN yum -y install python36-pip
RUN yum clean all

RUN  pip3 install jupyter

RUN mkdir Docker
COPY . Docker/

RUN adduser user
USER user

WORKDIR /home/user

CMD ["bash"]
