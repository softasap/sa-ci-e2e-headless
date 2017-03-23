sa-ci-e2e-headless
==================

[![Build Status](https://travis-ci.org/softasap/sa-ci-e2e-headless.svg?branch=master)](https://travis-ci.org/softasap/sa-ci-e2e-headless)

Swiss knife play to get some e2e up and running on your build server

Installs selenium(optional), webdriver(optional) , chrome(optional), firefox(optional), chromium(optional), phantomjs(optional) with headless support (via xvfb). Optionally installs java & nodejs if needed.

Example of usage (all parameters are optional)

Simple

Note: you need to select one, as selenium is installed by webdriver silently as its dependency.
Make sure to review browsers needed.

```YAML
  roles:
    - {
        role: "sa-ci-e2e-headless",
        options_install_selenium: false,
        options_install_webdriver: true,

        # optional browsers
        browser_phantomjs: true,
        browser_chromium: true,
        browser_firefox: true,
        browser_google_chrome: true
      }
```

Advanced:

```YAML

  roles:
    - {
        role: "sa-ci-e2e-headless",
        # optional java install
        option_install_java: true,
        java_version: 7

        # optional browsers
        browser_phantomjs: true,
        browser_chromium: true,
        browser_firefox: true,
        browser_google_chrome: true,

        # optional nodejs
        option_nodejs_install_with_nvm: true,
        nvm_version: 0.31.1,
        nodejs_version: "6.9.2",        

        option_nodejs_link_globally: false,
        option_integrate_w_bash: false,
        option_integrate_w_zsh: false,

        # optional selenium
        options_install_selenium: true,
        selenium_version: 2.49.1,

        # webdriver for angularjs testing with protractor
        options_install_webdriver: true,


      }

```      


Usage with ansible galaxy workflow
----------------------------------

If you installed the sa-ci-e2e-headless role using the command

`
   ansible-galaxy install softasap.sa-ci-e2e-headless
`

the role will be available in the folder library/softasap.sa-ci-e2e-headless
Please adjust the path accordingly.

```YAML

     - {
         role: "softasap.sa-ci-e2e-headless"
       }

```



Copyright and license
---------------------


Code licensed under the [BSD 3 clause] (https://opensource.org/licenses/BSD-3-Clause) or the [MIT License] (http://opensource.org/licenses/MIT).

Subscribe for roles updates at [FB] (https://www.facebook.com/SoftAsap/)

Join gitter discussion channel at [Gitter](https://gitter.im/softasap)
