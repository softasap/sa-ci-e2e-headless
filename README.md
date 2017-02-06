sa-ci-e2e-headless
==================

[![Build Status](https://travis-ci.org/softasap/sa-ci-e2e-headless.svg?branch=master)](https://travis-ci.org/softasap/sa-ci-e2e-headless)

Installs selenium, chrome(optional), firefox(optional), chromium(optional), phantomjs(optional) with headless support (via xvfb). Optionally installs java & nodejs if needed.

Example of usage (all parameters are optional)

Simple

```YAML
  roles:
    - {
        role: "sa-ci-e2e-headless"
      }
```

Advanced:

```YAML

  roles:
    - {
        role: "sa-ci-e2e-headless",
        option_install_java: true,
        java_version: 7

        browser_phantomjs: true,
        browser_chromium: true,
        browser_firefox: true,
        browser_google_chrome: true,

        option_nodejs_install_with_nvm: true,
        nvm_version: 0.31.1,
        nodejs_version: "6.9.2",        

        option_nodejs_link_globally: false,
        option_integrate_w_bash: false,
        option_integrate_w_zsh: false

      }

```      


Copyright and license
---------------------

Code licensed under the [BSD 3 clause] (https://opensource.org/licenses/BSD-3-Clause) or the [MIT License] (http://opensource.org/licenses/MIT).

Subscribe for roles updates at [FB] (https://www.facebook.com/SoftAsap/)
