# Development Environment Setup

*NB*: Assumes OS X

## Table of Contents

* [General Requirements](#general-requirements)
* [Per Language](#per-language)
  * [Javascript](#javascript)
  * [Python](#python)
  * [Ruby](#ruby)
* [Per Framework](#per-framework)
  * [React](#react)

## General Requirements

The following commands are not tied to a particular repository.

* [Homebrew](http://brew.sh) for managing software packages on OS X
    ```
    /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
    ```

* [Homebrew Bundle](https://github.com/Homebrew/homebrew-bundle) for bundling packages with Homebrew
    ```
    brew tap Homebrew/bundle
    ```

* [Docker for Mac](https://docs.docker.com/docker-for-mac/) for running project services in isolated environments
    * Create an account at [Docker Hub](https://hub.docker.com/)
    * Install and open [Docker for Mac](https://docs.docker.com/docker-for-mac/)
    * Finish setup

        ```
        docker login
        ```

* Configure your shell to enable automatic environment variable loading
    ```
    # in e.g. ~/.bash_profile

    if which direnv > /dev/null; then
      eval "$(direnv hook bash)"
    fi
    ```

    * Restart shell so that changes take effect

        ```
        source ~/.bash_profile
        ```

## Per Language

### Javascript

* Configure your shell to enable shims
    ```
    # in e.g. ~/.bash_profile

    if which nodenv > /dev/null; then
      eval "$(nodenv init -)"
    fi
    ```

* Install Node
    ```
    nodenv install -s $(cat ./.node-version)
    ```

* Install packages
    ```
    npm install -g yarn
    nodenv rehash
    yarn
    ```

### Python

* Configure your shell to enable shims
    ```
    # in e.g. ~/.bash_profile

    if which pyenv > /dev/null; then
      eval "$(pyenv init -)"
    fi
    ```

* Install Python
    ```
    pyenv install -s $(cat ./.python-version)
    ```

### Ruby

* Configure your shell to enable shims
    ```
    # in e.g. ~/.bash_profile

    if which rbenv > /dev/null; then
      eval "$(rbenv init -)"
    fi
    ```

* Install Ruby
    ```
    rbenv install -s $(cat .ruby-version)
    ```

* Install gems
    ```
    gem update --system
    gem install bundler
    rbenv rehash
    bundle install
    ```

## Per Framework

### React

* Install useful browser plugins

    * [React Developer Tools](https://chrome.google.com/webstore/detail/react-developer-tools/fmkadmapgofadopljbjfkapdkoienihi)
    * [Redux DevTools Extension](https://chrome.google.com/webstore/detail/redux-devtools/lmhkpmbekcpmknklioeibfkpmmfibljd)
