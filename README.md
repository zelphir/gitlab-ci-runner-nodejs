# gitlab-ci-runner-nodejs

This is docker image based on the Dockerfile provided by gitlabhq. See https://github.com/gitlabhq/gitlab-ci-runner/blob/master/Dockerfile by Sytse Sijbrandij <sytse@gitlab.com> for the original.

Differences from the original:

- no mysql
- no postgres
- no redis
- current stable node.js with npm, phantom.js, jshint, gulp and bower

# Installation

This image is available as a [Trusted Build](https://index.docker.io/u/ufirstgroup/gitlab-ci-runner-nodejs/). Import the build like this:

    docker pull zelphir/gitlab-ci-runner-nodejs

# Usage
Run like this:

    % docker run -d \
        -e CI_SERVER_URL=https://ci.example.com \
        -e REGISTRATION_TOKEN=replaceme \
        -e HOME=/root \
        -e GITLAB_SERVER_FQDN=gitlab.example.com \
        zelphir/gitlab-ci-runner-nodejs

