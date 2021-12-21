# grid-mixins

Install with [npm](https://www.npmjs.com/):

```bash
npm install grid-mixins
```

## Example usage

### SCSS

```scss
@use "grid-mixins" as grid;

.container {
  @include grid.make-container();
}

.row {
  @include grid.make-row();
}

.main {
  @include grid.make-col-ready();

  @include media-breakpoint-up(sm) {
    @include grid.make-col(6);
  }

  @include media-breakpoint-up(lg) {
    @include grid.make-col(8);
  }
}

.sidebar {
  @include grid.make-col-ready();

  @include media-breakpoint-up(sm) {
    @include grid.make-col(6);
  }

  @include media-breakpoint-up(lg) {
    @include grid.make-col(4);
  }
}
```

### HTML

```html
<div class="container">
  <div class="row">
    <div class="main">...</div>
    <div class="sidebar">...</div>
  </div>
</div>
```
