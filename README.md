sa-gluster-fs
=============

[![Build Status](https://travis-ci.org/softasap/sa-ci-e2e-headless.svg?branch=master)](https://travis-ci.org/softasap/sa-ci-e2e-headless)

Installs firefox, chromium, phantomjs with headless support (via xvfb). Optionally installs java if needed.

GlusterFS is a scalable network filesystem. Using common off-the-shelf hardware, you can create large, distributed storage solutions for media streaming, data analysis, and other data- and bandwidth-intensive tasks. GlusterFS is free and open source software.


Example of usage (all parameters are optional)

Simple

  roles:
    - {
        role: "sa-ci-e2e-headless"
      }


Advanced:


  roles:
    - {
        role: "sa-ci-e2e-headless",
        option_install_java: true,
        option_nodejs_install_with_nvm: true
      }
