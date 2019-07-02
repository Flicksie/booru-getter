# Booru-Getter
### A Node.js module for retrieving search information or image urls from Safebooru and Gelbooru

### Usage

##### Safebooru
[A worksafe booru.](https://safebooru.org/) 

```js
const getter = require('booru-getter')

//Searching by tags
getter.get(1, 0, "blue_hair+-red*").then(xml=>{
	//work with XML here.
})

//Retrieving a random image with matching tags
getter.getRandom("blue_hair+red_shirt+-dress*").then(data =>{
 	
	// Object, see below
	
}
```

#### Gelbooru
[A booru that contains NSFW images.](http://gelbooru.com/)

```js
//Searching by tags
getter.getLewd(1, 0, "blue_hair+-red*").then(xml=>{
	//work with XML here.
})

//Retrieving a random image with matching tags
getter.getRandomLewd("blue_hair+red_shirt+-dress*").then(data =>{
 	
	// Object, see below
	
}
```

#### Returning data Object
The fullfilled Promise will return an object with entry info.

example:
```js

{ 
  height: '1024',
  score: '0',
  file_url:
   	'https://safebooru.org/images/2552/b523bd0bc8cfdba7d4cf4aafaa2feeb84c7a9930.jpg',
  parent_id: '',
  sample_url:
   	'https://safebooru.org/images/2552/b523bd0bc8cfdba7d4cf4aafaa2feeb84c7a9930.jpg',
  sample_width: '768',
  sample_height: '1024',
  preview_url:
   	'https://safebooru.org/thumbnails/2552/thumbnail_b523bd0bc8cfdba7d4cf4aafaa2feeb84c7a9930.jpg',
  rating: 's',
  tags:
   	' 1girl ahoge azur_lane bangs bare_shoulders black_ribbon blunt_bangs blush criss-cross_halter dress eyebrows_visible_through_hair eyes_visible_through_hair hair_between_eyes hair_ribbon halterneck hand_up holding holding_stuffed_animal lace lace-trimmed_ribbon lavender_hair long_hair looking_at_viewer parted_bangs parted_lips ren_kun ribbon see-through see-through_silhouette simple_background solo stuffed_alicorn stuffed_animal stuffed_toy tareme unicorn_(azur_lane) very_long_hair violet_eyes white_background white_dress ',
  id: '2659807',
  width: '768',
  change: '1538559013',
  md5: 'dc1d02f7a3f157afe6e83cd9525e7550',
  creator_id: '79',
  has_children: 'false',
  created_at: 'Wed Oct 03 11:30:13 +0200 2018',
  status: 'active',
  source: 'https://twitter.com/Ren_sukiari/status/1046302960378994689',
  has_notes: 'false',
  has_comments: 'false',
  preview_width: '112',
  preview_height: '150' 
}
```
