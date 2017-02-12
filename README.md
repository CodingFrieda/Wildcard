# Wildcard (WIP)

[![Travis Build Status](https://travis-ci.org/electerious/Wildcard.svg?branch=master)](https://travis-ci.org/electerious/Wildcard) [![Coverage Status](https://coveralls.io/repos/github/electerious/Wildcard/badge.svg?branch=master)](https://coveralls.io/github/electerious/Wildcard?branch=master) [![Dependencies](https://david-dm.org/electerious/Wildcard.svg)](https://david-dm.org/electerious/Wildcard#info=dependencies)

Your self-hosted placeholder microservice of choice.

## Contents

- [Description](#description)
	- [What is Wildcard?](#what-is-wildcard)
	- [Whyt Wildcard?](#why-wildcard)
- [How to use](#how-to-use)
	- [With Now](#with-now)
	- [With Docker](#with-docker)
	- [Manually](#manually)
- [API](#api)
- [Options](#options)
	- [Port](#port)

## Description

### What is Wildcard?

Wildcard is similar to [Unsplash It](https://unsplash.it) and other placeholder services. The main difference is that Wildcard was built to be the self-hosted. You decide where to run it and which images it should serve. A simple REST API provides you with an access to all images placed in `images/`. Requesting specific or random placeholders in different sizes and variations (greyscaled, blurred or cropped) is just a matter of the URL.

### Why Wildcard?

I've used a lot of placeholder images on sites (front-ends without real content) I've built. My favorite placeholder service suddenly shut down and my front-ends started to look odd. I don't think it's necessary to depend on such a service, so I started to develop Wildcard as a self-hosted alternative.

## How to use

1. Place all photos you want to use as placeholders in `images/`. Wildcard supports JPEG and PNG.
2. Deploy your personal Wildcard on [now](#with-now), run it with [Docker](#with-docker) or go the [manual way](#manually).

### With Now

Deploy Wildcard with [now](https://zeit.co/now) installed on your system.

```
now
```

### With Docker

Start Wildcard with [Docker](https://docker.com) installed on your system.

```sh
docker run -p 2015:3000 -v /path/to/images/:/srv/app/data/ electerious/Wildcard
```

This command will…

- …map the internal port (`3000`) to port `2015` on your system (`-p`).
- …allow Wildcard to use the images from your system located at `/path/to/images/` (`-v`).
- …use and run the newest version of Wildcard (`electerious/Wildcard`).

### Manually

Make sure to install and update all dependencies before you setup Wildcard.

- [Node.js](https://nodejs.org/en/) (v7.5.0 or newer)
- [npm](https://www.npmjs.com)

Install all dependencies using `npm`.

```sh
npm install
```

Start the server.

```sh
npm start
```

## API

## Options

### Port

The port Wildcard is listening on.

```sh
PORT=3000
```