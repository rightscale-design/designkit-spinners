# Designkit Spinners

Sass module for css only spinners.

## Install

```bash
npm i designkit-spinners
```

## Markup

```html
<!-- Fading Dots Spinner -->
<div class="spinner-dots"></div>

<!-- Spinning Disc -->
<div class="spinner-disc"></div>

<!-- Spinning Disc Options -->
<div class="spinner-disc spinner-disc-md"></div>

<div class="spinner-disc spinner-disc-sm"></div>

<div class="spinner-disc spinner-disc-thick"></div>

<div class="spinner-disc spinner-disc-thicker"></div>
```

## CSS

```css
/*
//
// Designkit-Spinners
// --------------------------------------------------
*/
@-webkit-keyframes spinner-disc-rotate {
  0% {
    -webkit-transform: rotateZ(-360deg);
  }
  100% {
    -webkit-transform: rotateZ(0deg);
  }
}

@-moz-keyframes spinner-disc-rotate {
  0% {
    -moz-transform: rotateZ(-360deg);
  }
  100% {
    -moz-transform: rotateZ(0deg);
  }
}

@keyframes spinner-disc-rotate {
  0% {
    -webkit-transform: rotateZ(-360deg);
    -moz-transform: rotateZ(-360deg);
    -ms-transform: rotateZ(-360deg);
    -o-transform: rotateZ(-360deg);
    transform: rotateZ(-360deg);
  }
  100% {
    -webkit-transform: rotateZ(0deg);
    -moz-transform: rotateZ(0deg);
    -ms-transform: rotateZ(0deg);
    -o-transform: rotateZ(0deg);
    transform: rotateZ(0deg);
  }
}

@-webkit-keyframes spinner-dots-fade {
  0%,
  80%,
  100% {
    opacity: 1;
  }
  40% {
    opacity: .2;
  }
}

@-moz-keyframes spinner-dots-fade {
  0%,
  80%,
  100% {
    opacity: 1;
  }
  40% {
    opacity: .2;
  }
}

@keyframes spinner-dots-fade {
  0%,
  80%,
  100% {
    opacity: 1;
  }
  40% {
    opacity: .2;
  }
}

.spinner-disc {
  display: block;
  width: 10px;
  height: 10px;
}

.spinner-disc:after {
  position: relative;
  display: block;
  width: 20px;
  height: 20px;
  content: '';
  border-style: solid;
  border-width: 1px;
  border-top-color: #000;
  border-right-color: #ddd;
  border-bottom-color: #ddd;
  border-left-color: #000;
  border-radius: 100%;
  opacity: .5;
  -webkit-animation: spinner-disc-rotate 0.6s linear infinite;
  -moz-animation: spinner-disc-rotate 0.6s linear infinite;
  animation: spinner-disc-rotate 0.6s linear infinite;
}

.spinner-disc.spinner-disc-sm:after {
  width: 10px;
  height: 10px;
}

.spinner-disc.spinner-disc-md:after {
  width: 16px;
  height: 16px;
}

.spinner-disc.spinner-disc-thick:after {
  border-width: 2px;
}

.spinner-disc.spinner-disc-thicker:after {
  border-width: 3px;
}

.spinner-disc {
  position: absolute;
  top: calc(50% - 11px);
  left: calc(50% - 11px);
}

.spinner-dots,
.spinner-dots:before,
.spinner-dots:after {
  width: 16px;
  height: 16px;
  background-color: #000;
  border-radius: 50%;
  -webkit-animation: spinner-dots-fade 1s infinite ease-in-out;
  -moz-animation: spinner-dots-fade 1s infinite ease-in-out;
  animation: spinner-dots-fade 1s infinite ease-in-out;
  -webkit-animation-fill-mode: both;
  -moz-animation-fill-mode: both;
  animation-fill-mode: both;
}

.spinner-dots {
  -webkit-animation-delay: -0.16s;
  -moz-animation-delay: -0.16s;
  animation-delay: -0.16s;
  -webkit-transform: translateZ(0);
  -moz-transform: translateZ(0);
  -ms-transform: translateZ(0);
  -o-transform: translateZ(0);
  transform: translateZ(0);
}

.spinner-dots:before, .spinner-dots:after {
  position: absolute;
  top: 0;
  content: '';
}

.spinner-dots:before {
  left: -24px;
  -webkit-animation-delay: -0.32s;
  -moz-animation-delay: -0.32s;
  animation-delay: -0.32s;
}

.spinner-dots:after {
  left: 24px;
}

.spinner-dots {
  position: absolute;
  top: calc(50% - 8px);
  left: calc(50% - 8px);
}
```

## Author

Jason Melgoza

## License

The MIT License (MIT)

Copyright (c) 2016 RightScale

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
