```css
/* 兼容iphone4/4s：*/

@media (device-height:480px) and (-webkit-min-device-pixel-ratio:2){ }

/* 兼容iphone5 ：*/

@media (device-height:568px) and (-webkit-min-device-pixel-ratio:2){ }

/* 兼容iphone6，iphone7，iphone8s ：*/

@media (device-height:667px) and (-webkit-min-device-pixel-ratio:2){ }

/* 兼容iphone6 Plus,iphone7 Plus,iphone8 Plus：*/

@media (device-height:736px) and (-webkit-min-device-pixel-ratio:2){ }

/* 兼容iphoneX：*/

@media only screen and (device-width: 375px) and (device-height: 812px) and (-webkit-device-pixel-ratio: 3){ }

/* 兼容ipad ：*/

@media only screen and (min-device-width : 768px) and (max-device-width : 1024px){ /* style */ }

/* 兼容ipad横屏 */

@media only screen and (min-device-width : 768px) and (max-device-width : 1024px) and (orientation : landscape){ /* style */ }

/* 兼容ipad竖屏 ：*/

@media only screen and (min-device-width : 768px) and (max-device-width : 1024px) and (orientation : portrait){ /* style */ }
```

> 生效需要 `<meta name="viewport" content="width=device-width, initial-scale=1.0"/>`

