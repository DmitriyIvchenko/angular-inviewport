# Angular InViewport
[![Build Status][travis-badge]][travis-badge-url]

A simple lightweight library for [Angular (2+)][angular] with no external dependencies that detects when an element is within the browser viewport and adds a `in-viewport` or `not-in-viewport` class to the element.

This is a simple library for [Angular][angular], implemented in the [Angular Package Format v4.0](https://docs.google.com/document/d/1CZC2rcpxffTDfRDs6p1cfbmKNLA6x5O-NtkJglDaBVs/edit#heading=h.k0mh3o8u5hx).


## Install

`npm i angular-inviewport --save`

`app.module.ts`
```ts
import { InViewportModule } from 'angular-inviewport';

@NgModule({
  imports: [
    /** other imports **/
    InViewportModule,
    /** other imports **/
  ],
  /** other ngModule code **/
})
export class AppModule { }
```


## Example

```html
<p class="foo" inViewport>Amet tempor excepteur occaecat nulla.</p>
```

```css
.foo {
  transition: transform .35s ease-out;
}

.foo.not-in-viewport {
  transform: translateY(-30px);
}

.foo.in-viewport {
  transform: translateY(0);
}
```

[travis-badge]: https://travis-ci.org/edoparearyee/angular-inviewport.svg?branch=master
[travis-badge-url]: https://travis-ci.org/edoparearyee/angular-inviewport
[angular]: https://angular.io/
