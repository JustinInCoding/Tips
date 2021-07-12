不能直接修改 css ，需要定义变量，绑定属性来做判断，比如说ipad 和 iOS

```html
<button class={{largeButton}} disabled={{!isVinValid}} onclick={this.turnToFactoryCheck}>
  xxxxxx
</button>
```



```js
largeButton: api.uiMode === "pad" ? "large-button" : "large-button-iphone",
```



```css
	.large-button {
		height: 44px;
		width: 50%;
		font-size: 16px;
	}

	.large-button-iphone {
		height: 44px;
		width: 60%;
		font-size: 12px;
	}

	.large-button:disabled,
	.large-button-iphone:disabled {
		color: lightgray;
		border: 1px solid lightgray;
	}
```

