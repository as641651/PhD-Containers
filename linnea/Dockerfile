FROM centos:centos7.6.1810

RUN yum -y update
RUN yum -y install vim
RUN yum -y install redhat-lsb
RUN yum -y install epel-release
RUN yum -y install python36-pip
RUN yum -y install git
RUN yum clean all

RUN pip3 install jupyter
#RUN pip3 install git+git://github.com/HPAC/linnea.git

RUN mkdir Docker
COPY . Docker/

RUN git clone https://github.com/HPAC/linnea.git
WORKDIR linnea/
RUN git checkout dev-derivation
RUN python3 setup.py install

RUN adduser user
#USER user

WORKDIR /home/user

CMD ["bash"]
