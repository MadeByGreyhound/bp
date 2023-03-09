# @greyhoundstudio/bp

A simple @bp media query mixin for SASS.

Include it in your package with `@use`:

```sass
@use '@greyhoundstudio/bp' as *;
```

Use it like...

```sass
@include bp(sm, md) {
  body {
    font-size: 1.6rem;
  }
}
```

to generate...

```css
@media only screen and (min-width: 480px) and (max-width: 767px) {
  body {
    font-size: 1.6rem;
  }
}
```

You can provide just the `$min` argument, or both `$min` and `$max`. You can also provide unit-less values which will be interpreted as pixels, or any other CSS unit.

```sass
@include bp(768) {
  body {
    font-size: 1.6rem;
  }
}

@include bp(48rem) {
  body {
    font-size: 1.6rem;
  }
}
```

You can also configure your own pre-defined breakpoints.

```sass
@use '@greyhoundstudio/bp' as * with(
  $breakpoints: (
    "sm": 480px,
    "md": 768px,
    "lg": 1024px
  )
);
```
