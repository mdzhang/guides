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

* Setup laptop by following instructions [here](https://github.com/mdzhang/laptop)

## Per Language

### Javascript

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

* Install Python
    ```
    pyenv install -s $(cat ./.python-version)
    ```

### Ruby

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
