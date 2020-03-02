# isValidCoords

[![Build Status](https://travis-ci.com/fitiskin/is-valid-coords.svg?branch=master)](https://travis-ci.com/fitiskin/is-valid-coords)
![](https://badgen.net/github/license/fitiskin/is-valid-coords)

Simple dependency-free utility to provide coordinates validation written in TypeScript.

## Install

**npm**

```sh
npm install --save is-valid-coords
```

**yarn**

```sh
yarn add is-valid-coords
```

## Usage

```javascript
import isValidCoords from "is-valid-coords";

const latitude = 55.7558;
const longitude = 37.6173;

// true
isValidCoords(latitude, longitude);
isValidCoords(0, 0);

// false
isValidCoords(null);
isValidCoords(100, 500);
```

## Overloads

```javascript
// two arguments
isValidCoords(55.7558, 37.6173);

// array
isValidCoords([55.7558, 37.6173]);

// string
isValidCoords("55.7558, 37.6173");

// plain object with keys:
// - latitude, lat
// - longitude, lng, lon, long
isValidCoords({
  latitude: 55.7558,
  longitude: 37.6173
});
```
