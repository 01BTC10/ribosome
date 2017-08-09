# RIBOSOMEJS [![Build Status](https://travis-ci.org/01BTC10/ribosomejs.svg?branch=master)](https://travis-ci.org/01BTC10/ribosomejs)

## A simple generic code generation tool.

Forked from [here](https://github.com/sustrik/ribosome/)
This repository include only the javascript binary, javascript tests and javascript examples. The main goal of this fork is to add a javascript only npm package.

## Installation

```sh
$ npm install -g ribosomejs
```

## Usage

```sh
$ ribosomejs examples/errors.dna
```

## Example

This example uses JavaScript as the control language:

readysteady.js.dna:
```
.#include <stdio.h>
.
.int main() {
var i;
for (i=3; i>0; i--) {
.    printf("@{i}!\n");
}
.    printf("Go!\n");
.    return 0;
.}
```

To generate the code do the following:

```
$ ribosome.js readysteady.js.dna
```

The script produces the following output (which happens to be a C program):

```
#include <stdio.h>

int main() {
    printf("3!\n");
    printf("2!\n");
    printf("1!\n");
    printf("Go!\n");
    return 0;
}
```

[Original documentation](http://sustrik.github.io/ribosome/).
