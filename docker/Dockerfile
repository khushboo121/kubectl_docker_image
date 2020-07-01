FROM alpine:3.8

ARG KUBECTL_URL=https://amazon-eks.s3-us-west-2.amazonaws.com/1.11.5/2018-12-06/bin/linux/amd64/kubectl

ADD ${KUBECTL_URL} /usr/local/bin/kubectl
copy aws-iam-authenticator /usr/local/bin/


RUN apk add --update ca-certificates gettext && \
    chmod +x /usr/local/bin/kubectl && \
    chmod +x /usr/local/bin/aws-iam-authenticator 

RUN ls -l /
RUN kubectl 
RUN apk update
RUN apk -Uuv add groff less python py-pip
RUN pip install awscli
