```javascript
(ret, err) => {
  if (ret && ret.eventType === 'success') {
    console.log(this.vin)
    this.vin = ret.content;
  } else if (err) {
    alert(JSON.stringify(err));
  }
});
```

> 使用箭头