﻿
# to.js

 JavaScript animation framework.

## About

  to.js is a small JavaScript library making CSS3 backed animation
  extremely simple , elegant and powerful. 

## Installation

add the ref in your html file if you don't use amd,cmd or [kmdjs](https://github.com/kmdjs/kmdjs) in your project

    <script src='to.js'></script>


## Example

  For example below we translate to the point `(500px, 200px)`,
  rotate by `180deg`, scale by `.5` within a 2 second
  duration. Once the animation is complete we invoke `to()` to next task ,then fade out the element by setting the `opacity` to `0`, and shrink it with `scale(0.1)`.

    tojs.get('.square')
       .to()
       .x(500,2000)
       .y(200,2000,tojs.bouseOut)
       .rotate(180,2000)
       .scaleX(.5,2000)
       .scaleY(.5,2000)
       .to()
       .alpha(0,500)       
       .scaleX(0.1,500)
       .scaleY(0.1,500)
       .end(function(){

        })
        .start();

## Easing functions

  Built-in easing functions are defined as:

```js
bounceOut:TWEEN.Easing.Bounce.Out,
linear: TWEEN.Easing.Linear.None,
quadraticIn:TWEEN.Easing.Quadratic.In,
quadraticOut:TWEEN.Easing.Quadratic.Out,
quadraticInOut:TWEEN.Easing.Quadratic.InOut,
cubicIn:TWEEN.Easing.Cubic.In,
cubicOut:TWEEN.Easing.Cubic.Out,
cubicInOut:TWEEN.Easing.Cubic.InOut,
quarticIn:TWEEN.Easing.Quartic.In,
quarticOut:TWEEN.Easing.Quartic.Out,
quarticInOut:TWEEN.Easing.Quartic.InOut,
quinticIn:TWEEN.Easing.Quintic.In,
quinticOut:TWEEN.Easing.Quintic.Out,
quinticInOut:TWEEN.Easing.Quintic.InOut,
sinusoidalIn:TWEEN.Easing.Sinusoidal.In,
sinusoidalOut:TWEEN.Easing.Sinusoidal.Out,
sinusoidalInOut:TWEEN.Easing.Sinusoidal.InOut,
exponentialIn:TWEEN.Easing.Exponential.In,
exponentialOut:TWEEN.Easing.Exponential.Out,
exponentialInOut:TWEEN.Easing.Exponential.InOut,
circularIn:TWEEN.Easing.Circular.In,
circularOut:TWEEN.Easing.Circular.Out,
circularInOut:TWEEN.Easing.Circular.InOut,
elasticIn:TWEEN.Easing.Elastic.In,
elasticOut:TWEEN.Easing.Elastic.Out,
elasticInOut:TWEEN.Easing.Elastic.InOut,
backIn:TWEEN.Easing.Back.In,
backOut:TWEEN.Easing.Back.Out,
backInOut:TWEEN.Easing.Back.InOut,
bounceIn:TWEEN.Easing.Bounce.In,
bounceOut:TWEEN.Easing.Bounce.Out,
bounceInOut:TWEEN.Easing.Bounce.InOut,
interpolationLinear:TWEEN.Interpolation.Linear,
interpolationBezier: TWEEN.Interpolation.Bezier,
interpolationCatmullRom: TWEEN.Interpolation.CatmullRom       
```

you can user it such as "tojs.backInOut"


## License

(The MIT License)

Copyright (c) 2011 TJ Holowaychuk &lt;tj@vision-media.ca&gt;

Permission is hereby granted, free of charge, to any person obtaining
a copy of this software and associated documentation files (the
'Software'), to deal in the Software without restriction, including
without limitation the rights to use, copy, modify, merge, publish,
distribute, sublicense, and/or sell copies of the Software, and to
permit persons to whom the Software is furnished to do so, subject to
the following conditions:

The above copyright notice and this permission notice shall be
included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED 'AS IS', WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF
MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT.
IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY
CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT,
TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE
SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
