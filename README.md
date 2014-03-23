gaffa-concat
============

concat view for gaffa

## Install:

    npm i gaffa-concat

## Add to gaffa:

    gaffa.actions.constructors.concat = require('gaffa-concat');

## Example

Assuming a model such as:

    {
        targetArray: [0,1,2],
        sourceArray: [3,4,5]
    }

Set up the action

    var concatItems = new concat();
    concatItems.source.binding = '[sourceArray]';
    concatItems.target.binding = '[targetArray]';

After being triggered, the model will look like:

    {
        targetArray: [0,1,2,3,4,5],
        sourceArray: [3,4,5]
    }

# API

## Properties (instanceof Gaffa.Property)

### target

A binding to an array to concat into

### source

A binding to an array to concat from

### clone

Default: true;

Whether to clone the items in the source array.