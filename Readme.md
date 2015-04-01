This repository stores configuration files that can be launched using cloud-launcher.

To launch from the web UI, try:

http://www.cloud-launcher.io#config=cloud-launcher/clouds/master/sample.hjson

## Run Using Docker

To launch from the docker application, try:

    $ docker run \
              -i -t \
              -v $(pwd):/clouds \
              cloudlauncher/launch-cloud \
              cloud-launcher/clouds/master/sample.hjson

You will be prompted to select a provider(s) and location(s) to launch your cloud on. The launched cloud manifest will be stored in your current directory (or other directory if you selected a different one with the `-v` option).


The running cloud can be destroyed with:

    $ docker run \
              -i -t \
              -v $(pwd):clouds \
              cloudlauncher/launch-cloud \
              destroy sample.cloud


## Run Using npm

To launch from npm, try:

    $ npm install -g cloud-launcher
    $ launch-cloud cloud-launcher/clouds/master/sample.hjson

To destroy the running cloud, try:

    $ launch-cloud destroy sample.cloud


## Run Using Git Repo

To launch from the git repo, try:

    $ git clone https://github.com/cloud-launcher/launch-cloud
    $ cd launch-cloud
    $ ./launch-cloud cloud-launcher/clouds/master/sample.hjson

To destroy the running cloud, try:

    $ ./launch-cloud destroy sample.cloud