FROM dev-iojs

#Install ruby, rubygems and sass
RUN gpg --keyserver hkp://keys.gnupg.net --recv-keys 409B6B1796C275462A1703113804BB82D39DC0E3 && \
    curl -L get.rvm.io | bash -s stable && \
    /bin/bash -l -c "rvm requirements" && \
    /bin/bash -l -c "rvm install 2.2.1" && \
    /bin/bash -l -c "rvm use 2.2.1 --default" && \
    /bin/bash -l -c "rvm rubygems current" && \
    /bin/bash -l -c "gem install bundler --no-ri --no-rdoc" && \
    /bin/bash -l -c "gem install sass --no-ri --no-rdoc"
    
ENTRYPOINT bash -l

#Define default command
CMD ["gem", "-v"]
