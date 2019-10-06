FROM jenkins/jenkins:2.176.1

# Distributed Builds plugins
RUN /usr/local/bin/install-plugins.sh ssh-slaves

#Install GIT
RUN /usr/local/bin/install-plugins.sh git

# Artifacts
RUN /usr/local/bin/install-plugins.sh htmlpublisher

# UI
RUN /usr/local/bin/install-plugins.sh greenballs
RUN /usr/local/bin/install-plugins.sh simple-theme-plugin

# Scaling
RUN /usr/local/bin/install-plugins.sh kubernetes

VOLUME /var/jenkins_home
USER root
USER jenkins