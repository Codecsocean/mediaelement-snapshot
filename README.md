# Mediaelement Snapshot

## Overview

Mediaelement Snapshot plugin creates a button in the player controls allows to take video snapshots with different image types (jpeg, png).

## Installation

Download plugin files and place the js files after the main [Mediaelement](https://github.com/mediaelement/mediaelement/) player js `mediaelement-and-player.min.js` file:

```HTML
<!-- Include main mediaelement player file -->
<script src="/path/to/mediaelement-and-player.min.js"></script>
<!-- Include snapshot main plugin file -->
<script src="/path/to/snapshot/snapshot.min.js"></script>
<!-- Include snapshot Translation file -->
<script src="/path/to/snapshot/snapshot-i18n.js"></script>

```
Place plugin main CSS style after the main player stylesheet

```HTML

<!-- Include main mediaelement player stylesheet file -->
<link rel="stylesheet" href="/path/to/mediaelementplayer.min.css">
<!-- Include snapshot main stylesheet file -->
<link rel="stylesheet" href="/path/to/snapshot/snapshot.min.css">

```

Add plugin keyword to the features list

```Javascript
features: [..., 'snapshot']
```

That's it !, for more details about [install mediaelement plugin](https://github.com/mediaelement/mediaelement-plugins#installation).

## Usage

Example initialize Snapshot plugin

```Javascript

var player = new MediaElementPlayer(document.querySelector('video'), {

  features:['play', 'playpause', volume', 'progress', 'snapshot', fullscreen'],

       snapType:'jpeg',
       snapQuality: 0.5, //half quality
       snapShot: true,
            
       snapSuccess: function(snap){
          console.log(snap.url); //return snap object
       },

       snapError: function(){
          console.log('snapshot error !');
       }
       
 });

```

## API

| Parameter 	| Type 	       | Default | Description |
| ----------- | ------------ | --------| -----------
| snapShot    | boolean      | true    | rgergergerg
| snapType    | string       | png     | gergergerge
| snapQuality | number|float | 1       | gergergerge
| snapWidth   | number       | null    | gergergerge
| snapHeight  | number       | null    | gergergerge
| snapSuccess | callback     | null    | gergergerge
| snapError   | callback     | null    | gergergerge

## Support

Having trouble with this plugin? [create an issue](https://github.com/Codecsocean/mediaelement-snapshot/issues) describing the problem that you have encountered.
 
