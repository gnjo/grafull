# grafull
grayscale to fullcolor

# filter to grayscale
```js
function _grayscale(data,w,h) {
  for (let i = 0; i < data.length; i += 4) {
    // (r+g+b)/3
    const color = (data[i] + data[i+1] + data[i+2]) / 3;
    data[i] = data[i+1] = data[i+2] = color;
  }

  return data;
}
```
avarage to hsl
```js
0-255 =>0-360
av=...
gain= 255/360
d=~~(av*gain)
rgba(av,av,av,1)=>hsl(d%,s,l)
hsl(d%,s,l)=>rgba
```
