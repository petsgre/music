## Web pages based on HTML 5 < audio > music player

> [demo](https://www.166zx.com/ "demo")

## Requirements

- vue ^2.3.3
- vue-resource ^1.3.4
- v-click-outside ^0.0.8

## Installation

	npm install vue-music --save

## Usage

	<template>
	  <div id="app">
	    <Music :protocol="protocol"></Music>
	  </div>
	</template>
	<script>
	import Music from 'vue-music'
	export default {
	  name: 'app',
	   data(){
		return{
		  protocol:"http"
		}
	  },
	  components: {
	    Music
	  }
	}
	</script>

## api

protocol


	protocol:"http"  required,string


## Function

- play/pause，Previous，Next

play/pause：

> watch a toggle，named**audioToggle**，control by toggle typed boolean

Previous/Next：

> function named 'play()' to play music，3 arguments('random play'，'The list of play'，'single cycle') to change **Play mode**


- range

watch the event named **timeupdate** to modify the range，useing input new attribute range，by Two-way binding

- play time

as same as range,do not describe again,you can modify the attribute named duration

- voice

as same as range , modify the attribute 'range'

- play mode

3 condition：single cycle、The list of play、random play
detail to see play list tips

- play list

> play mode need to use play list,i save the list to localstorage(like Netease Cloud Music),if there is no one in list,it will play the music that named 'faded'(i like it,very rhythmical)

### because my server is closed, the music api is not useful,i'm so sorry about that.
