AnimateSCSS
===========

As the name suggests, _AnimateSCSS_ is the Sass version of [Dan Eden's](http://daneden.me/) popular [Animate.css](https://github.com/daneden/animate.css/blob/master/animate.css). The code is exactly the same, but now powered by the features that come with Sass.

Each animation is split into a partial, animations are controlled through mixins, and variables are used within the keyframes for easy editing of animation values, like start/end positions and rotation.

## Why? ##
I love Animate.css, digging into it properly for the first time back in October '12 when I building [ghostgames.com](http://ghostgames.com/).

But...  
I needed to experiment, so I downloaded the minified dev version... __48kB__.  
I needed to edit some of the values, so had to use the full dev version... __61kB__.

The filesizes of these dev files were becoming a burden to the development...so I brought in Sass to help.

With _AnimateSCSS_, you've got full access to all of the animations in *Animate.css*, but you __choose__ – on the fly – which are loaded into your CSS file. Not using any of the bouncing animations? Comment them out and your project won't be weighed down by their code. An added benefit is there is no "dev" and "final" version; just make sure any animations you don't use are commented out...you don't need the [custom build](http://daneden.me/animate/build/).

_AnimateSCSS_ makes editing the default animation values easy. Dive into your chosen animation, and at the top are the variables used in the animation. Edit, save, and they're changed throughout...no more copy/pasting through `-webkit-`, `-moz-`, `-o-` and regular.

_AnimateSCSS_ also gives you greater control. The durations and delays of any animation can be controlled with the included mixins. It's also really easy on the eye:

    h1 {
        @include animation(fadeInDown);
        @include duration(1s);
        @include delay(2s);
    }

####Usage:####

* Download, drop into your Sass section of your project, and `@import` the `_config` file.
* Dive into `_config` and uncomment the animation you want to use.
* Apply the animation to your element, and control it's duration and delay through the supplied mixins.
