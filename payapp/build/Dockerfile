FROM erlang:latest

# Install Rebar3
RUN mkdir -p /buildroot/rebar3/bin
ADD https://s3.amazonaws.com/rebar3/rebar3 /buildroot/rebar3/bin/rebar3
RUN chmod a+x /buildroot/rebar3/bin/rebar3

# Setup Environment
ENV PATH=/buildroot/erlang/20.1/bin:/buildroot/rebar3/bin:$PATH

# Reset working directory
WORKDIR /buildroot

# Copy our Erlang application
COPY mgsv mgsv

WORKDIR mgsv

# copy the ssh key for github
COPY repo-key /root/.ssh/id_rsa
RUN echo -e "StrictHostKeyChecking no" >> /etc/ssh/ssh_config

# copy secret configurations
COPY config config

CMD rebar3 as prod release -o /artifacts