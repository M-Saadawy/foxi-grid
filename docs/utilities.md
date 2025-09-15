# Utilities

## Spacing Utilities

Foxi Grid provides comprehensive spacing utilities for margin and padding.

### Margin Classes

Format: `.m{side}-{size}`

Sides:
- `t` - Top
- `b` - Bottom
- `s` - Start
- `e` - End
- `x` - Left and Right
- `y` - Top and Bottom
- No side specified - All sides

Sizes:
- `0` - 0
- `1` - 0.25rem
- `2` - 0.5rem
- `3` - 1rem
- `4` - 1.5rem
- `5` - 3rem

Examples:
```html
<div class="mt-3">Margin top 1rem</div>
<div class="mx-auto">Horizontally centered</div>
<div class="m-0">No margin</div>
<div class="mb-4">Margin bottom 1.5rem</div>
```

### Padding Classes

Format: `.p{side}-{size}`

Uses the same sides and sizes as margin utilities.

Examples:
```html
<div class="pt-3">Padding top 1rem</div>
<div class="px-2">Horizontal padding 0.5rem</div>
<div class="p-5">Padding 3rem all around</div>
```

### Responsive Spacing

Add breakpoints to create responsive spacing:

```html
<div class="mt-2 mt-md-3 mt-lg-4">
  <!-- Different top margins at different breakpoints -->
</div>
```

## Flexbox Utilities

### Display Flex

- `.d-flex` - Display flex
- `.d-inline-flex` - Display inline-flex

### Flex Direction

- `.flex-row` - Row (default)
- `.flex-row-reverse` - Row reverse
- `.flex-column` - Column
- `.flex-column-reverse` - Column reverse

### Flex Wrap

- `.flex-wrap` - Wrap
- `.flex-nowrap` - No wrap
- `.flex-wrap-reverse` - Wrap reverse

### Justify Content

- `.justify-content-start` - Start
- `.justify-content-end` - End
- `.justify-content-center` - Center
- `.justify-content-between` - Space between
- `.justify-content-around` - Space around
- `.justify-content-evenly` - Space evenly

### Align Items

- `.align-items-start` - Start
- `.align-items-end` - End
- `.align-items-center` - Center
- `.align-items-baseline` - Baseline
- `.align-items-stretch` - Stretch

### Align Self

- `.align-self-start` - Start
- `.align-self-end` - End
- `.align-self-center` - Center
- `.align-self-baseline` - Baseline
- `.align-self-stretch` - Stretch

### Examples

```html
<!-- Basic flex container -->
<div class="d-flex justify-content-between align-items-center">
  <div>Item 1</div>
  <div>Item 2</div>
</div>

<!-- Responsive flex direction -->
<div class="d-flex flex-column flex-md-row">
  <div>Stack on mobile, row on desktop</div>
  <div>Stack on mobile, row on desktop</div>
</div>

<!-- Complex flex layout -->
<div class="d-flex flex-wrap justify-content-around align-items-center">
  <div class="align-self-start">Item 1</div>
  <div>Item 2</div>
  <div class="align-self-end">Item 3</div>
</div>
```

## Display Utilities

### Display Values

- `.d-none` - Display none
- `.d-inline` - Display inline
- `.d-inline-block` - Display inline-block
- `.d-block` - Display block
- `.d-table` - Display table
- `.d-table-cell` - Display table-cell
- `.d-flex` - Display flex
- `.d-inline-flex` - Display inline-flex
- `.d-grid` - Display grid
- `.d-inline-grid` - Display inline-grid

### Responsive Display

Add breakpoints to create responsive displays:

```html
<!-- Hidden on small, visible on medium -->
<div class="d-none d-md-block">
  Visible on medium and up
</div>

<!-- Visible on small, hidden on medium -->
<div class="d-block d-md-none">
  Visible on small only
</div>

<!-- Change display type at different breakpoints -->
<div class="d-block d-sm-flex d-lg-grid">
  Different display types per breakpoint
</div>
```

## Customization

### Custom Spacing Scale

```scss
$spacer: 1rem;
$spacers: (
  0: 0,
  1: ($spacer * .25),
  2: ($spacer * .5),
  3: $spacer,
  4: ($spacer * 1.5),
  5: ($spacer * 3),
  6: ($spacer * 4),  // Custom larger sizes
  7: ($spacer * 5)
);
```

### Custom Display Classes

```scss
$displays: none, inline, inline-block, block, table, table-row, table-cell, 
          flex, inline-flex, grid, inline-grid;
```