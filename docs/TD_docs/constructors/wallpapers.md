---
title: wallpapers
description: Contains list of wallpapers
---
## Constructor: wallpapers  
[Back to constructors index](index.md)



Contains list of wallpapers

### Attributes:

| Name     |    Type       | Required | Description |
|----------|:-------------:|:--------:|------------:|
|wallpapers|Array of [wallpaper](../constructors/wallpaper.md) | Yes|List of wallpapers|



### Type: [Wallpapers](../types/Wallpapers.md)


### Example:

```
$wallpapers = ['_' => 'wallpapers', 'wallpapers' => [wallpaper]];
```  

[PWRTelegram](https://pwrtelegram.xyz) json-encoded version:

```
{"_": "wallpapers", "wallpapers": [wallpaper]}
```


Or, if you're into Lua:  


```
wallpapers={_='wallpapers', wallpapers={wallpaper}}

```


