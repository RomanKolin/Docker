FROM alpine
RUN apk add openssh
RUN ssh-keygen -A
RUN echo "root:IT2017year" | chpasswd
RUN echo "AllowUsers root" >> /etc/ssh/sshd_config
RUN echo "PermitRootLogin yes" >> /etc/ssh/sshd_config
EXPOSE 22
CMD ["/usr/sbin/sshd", "-D"] 
