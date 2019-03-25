FROM jenkinsci/blueocean
COPY casc_configs/plugins.txt /usr/share/jenkins/ref/plugins.txt
COPY casc_configs/jenkins.yml /usr/share/jenkins/ref/jenkins.yml
RUN /usr/local/bin/install-plugins.sh < /usr/share/jenkins/ref/plugins.txt