
# to.js

 JavaScript animation framework.

##demo
http://htmlcssjs.duapp.com/transformjs/

## About

  to.js is a small JavaScript library making animation
  extremely simple , elegant and powerful.  ==>[demo](http://htmlcssjs.duapp.com/tojs/)

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

  tojs's easing functions are mapped to tweenjs's easing functions:

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

## Effect

tojs provide some convenient methods(shake、rubber、bounceIn、flipInX、zoomOut). you can use them like this: 

```js
tojs.get('.square').shake().start();
```

you can also add the effect to  your animation :

```js
tojs.get('.square')
    .to()
    .x(500,2000)
    .y(200,2000,tojs.bouseOut)
    //here 
    .shake()
    .to()
    .alpha(0,500)       
    .scaleX(0.1,500)
    .scaleY(0.1,500)
    .end(function(){

    })
    .start();
```

## License

(The MIT License)
