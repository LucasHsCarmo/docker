ARG TAG=20.04
FROM ubuntu:$TAG
LABEL dockerfile.mantainer="lucascarmo"
ENV PACKER_VERSION=1.7.8
ENV TF_VERSION=1.1.3
ENV PATH_LOCAL=/usr/local/bin
WORKDIR /tmp
CMD ["bash"]
RUN apt-get update && \
    apt-get install vim -y && \ 
    apt-get install tree -y && \ 
    apt-get install wget unzip curl software-properties-common -y && \ 
    add-apt-repository --yes --update ppa:ansible/ansible && \    
    apt-get install ansible -y && \    
    wget https://releases.hashicorp.com/packer/${PACKER_VERSION}/packer_${PACKER_VERSION}_linux_amd64.zip && \     
    unzip packer_${PACKER_VERSION}_linux_amd64.zip && \    
    mv packer ${PATH_LOCAL} && \    
    wget https://releases.hashicorp.com/terraform/${TF_VERSION}/terraform_${TF_VERSION}_linux_amd64.zip && \    
    unzip terraform_${TF_VERSION}_linux_amd64.zip && \
    mv terraform ${PATH_LOCAL} && \    
    rm -rf /var/lib/apt/lists/* && \    
    rm -rf /tmp/* && \    
    apt-get clean