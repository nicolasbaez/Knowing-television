# Knowing-television
We are not alone

![buh](https://github.com/nicolasbaez/Knowing-television/blob/main/xp007.gif)
```javascript
w = 500;
h = 255;
k = 0;
setup = (_) => createCanvas(w, w, WEBGL);
draw = (_) => {
  colorMode(HSB, 7);
  rotateZ(0.6);
  rotateY(1.5);
  background(0);
  stroke(1);
  line(0, 0, -w, 0, 0, w);
  for (i = 0; i < w * 0.3; i += 15)
    for (j = k; j < 7 + k; j += 0.15) {
      strokeWeight(0.8);
      stroke(j, 7 - j, 7);
      point(i * cos(j + i * h), i * sin(j + i * h));
    }
  k += 0.001;
};
function keyPressed() {
  if (key === "s") {
    saveGif("xp007.gif", 700, { delay: 0, units: "frames" });
  }
}
