---
id: get-started
title: Get Started
sidebar_label: Quick start
---

The library is built in Reason, so we are assuming you are all set with the Reason configuration, if not please check out [Reason docs](https://reasonml.github.io) to learn how to get started with Reason.

## Install the library

```sh
yarn add reroute
# or
npm install reroute --save
```

## Add it to your config

In your `bsconfig.json` add it to the dependecies:

```json
"bs-dependencies": [
  "reason-react",
  "reroute"
]
```

## Usage

First we need to create the navigation based on our needs.
In `Navigation.re`, we will create our `Config` module and pass it to a `CreateNavigation` functor:

**Navigation.re**:

```reason
module Config = {
  type route =
    | Home
    | About
    | Contact;
};

include ReRoute.CreateNavigation(Config);
```

That's it! Now you are ready to use ReRoute in your React Native application.