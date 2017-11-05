# docker_payapp

**INSTALL**
* first copy your config  to `config`
* create an ssh key file to use in github  `repo-key`
* run `./create-image script`
* start by running `docker run -ti -p 8443:8443 erlang-mgsv /bin/bash`
* followed by `mgsv/bin/mgsv foreground`

***ALTERNATIVE RUN***
* start by running `docker run -d -p 8443:8443 erlang-mgsv`
