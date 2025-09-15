# Foxi Grid System

A highly customizable SASS grid system with responsive features and utility classes.

## Installation

```bash
npm install foxi-grid
```

## Usage

Import the grid system in your SASS file:

```scss
@import "foxi-grid/src/foxi-grid";
```

## Features

- Responsive 12-column grid system
- Flexible containers (fixed and fluid)
- Customizable breakpoints (xs, sm, md, lg, xl, xxl)
- Comprehensive utility classes
- Built with Flexbox
- Easy to customize
- No JavaScript dependencies

## Grid System

### Containers

Three types of containers available:

```html
<!-- Fixed width container -->
<div class="container">
  <!-- Content -->
</div>

<!-- Fluid container (full width) -->
<div class="container-fluid">
  <!-- Content -->
</div>
```

### Grid Basics

#### Basic Grid Columns
```html
<!-- Equal width columns -->
<div class="row">
  <div class="col">Equal Column</div>
  <div class="col">Equal Column</div>
</div>

<!-- Specific width columns -->
<div class="row">
  <div class="col-6">Half width</div>
  <div class="col-6">Half width</div>
</div>

<!-- Mixed columns -->
<div class="row">
  <div class="col-4">One third</div>
  <div class="col-8">Two thirds</div>
</div>
```

#### Responsive Grid
```html
<!-- Responsive breakpoints -->
<div class="row">
  <div class="col-12 col-sm-6 col-md-4 col-lg-3">
    <!-- Full width on xs, half on sm, third on md, quarter on lg -->
  </div>
</div>
```

#### Column Ordering
```html
<!-- Order modification -->
<div class="row">
  <div class="col order-2">Second</div>
  <div class="col order-1">First</div>
  <div class="col order-3">Third</div>
</div>

<!-- Responsive ordering -->
<div class="row">
  <div class="col order-md-2 order-1">First on mobile, second on desktop</div>
  <div class="col order-md-1 order-2">Second on mobile, first on desktop</div>
</div>
```

### Column Offset

```html
<!-- Basic offset -->
<div class="row">
  <div class="col-4 offset-4">Centered 4 columns</div>
</div>

<!-- Responsive offset -->
<div class="row">
  <div class="col-md-6 offset-md-3 col-sm-8 offset-sm-2">
    <!-- Different centering for different screens -->
  </div>
</div>

<!-- Multiple offsets -->
<div class="row">
  <div class="col-4">Column</div>
  <div class="col-4 offset-4">Offset Column</div>
</div>
```

## Utility Classes

### Flexbox Utilities

#### Flex Container
```html
<!-- Display flex -->
<div class="d-flex">Flex container</div>
<div class="d-inline-flex">Inline flex container</div>

<!-- Flex direction -->
<div class="flex-row">Row direction</div>
<div class="flex-column">Column direction</div>
<div class="flex-row-reverse">Reversed row</div>
<div class="flex-column-reverse">Reversed column</div>

<!-- Flex wrap -->
<div class="flex-wrap">Wrap items</div>
<div class="flex-nowrap">No wrap</div>
<div class="flex-wrap-reverse">Reverse wrap</div>
```

#### Justify Content
```html
<div class="justify-content-start">Start</div>
<div class="justify-content-end">End</div>
<div class="justify-content-center">Center</div>
<div class="justify-content-between">Space between</div>
<div class="justify-content-around">Space around</div>
<div class="justify-content-evenly">Space evenly</div>
```

#### Align Items
```html
<div class="align-items-start">Start</div>
<div class="align-items-end">End</div>
<div class="align-items-center">Center</div>
<div class="align-items-baseline">Baseline</div>
<div class="align-items-stretch">Stretch</div>
```

#### Individual Item Alignment
```html
<div class="align-self-start">Self start</div>
<div class="align-self-end">Self end</div>
<div class="align-self-center">Self center</div>
<div class="align-self-baseline">Self baseline</div>
<div class="align-self-stretch">Self stretch</div>
```

### Spacing Utilities

#### Margin
```html
<!-- All sides -->
<div class="m-0">No margin</div>
<div class="m-1">Small margin</div>
<div class="m-3">Medium margin</div>
<div class="m-5">Large margin</div>

<!-- Directional -->
<div class="mt-3">Top margin</div>
<div class="mb-3">Bottom margin</div>
<div class="ms-3">Start margin</div>
<div class="me-3">End margin</div>

<!-- Horizontal/Vertical -->
<div class="mx-auto">Horizontally centered</div>
<div class="my-3">Vertical margin</div>

<!-- Responsive margins -->
<div class="m-sm-3 m-md-4 m-lg-5">Responsive margins</div>
```

#### Padding
```html
<!-- All sides -->
<div class="p-0">No padding</div>
<div class="p-1">Small padding</div>
<div class="p-3">Medium padding</div>
<div class="p-5">Large padding</div>

<!-- Directional -->
<div class="pt-3">Top padding</div>
<div class="pb-3">Bottom padding</div>
<div class="ps-3">Start padding</div>
<div class="pe-3">End padding</div>

<!-- Horizontal/Vertical -->
<div class="px-3">Horizontal padding</div>
<div class="py-3">Vertical padding</div>

<!-- Responsive padding -->
<div class="p-sm-3 p-md-4 p-lg-5">Responsive padding</div>
```

### Display Utilities
```html
<!-- Responsive display -->
<div class="d-none d-md-block">Hidden on small, visible on medium+</div>
<div class="d-block d-md-none">Visible on small, hidden on medium+</div>

<!-- Display variations -->
<div class="d-inline">Inline</div>
<div class="d-block">Block</div>
<div class="d-inline-block">Inline block</div>
<div class="d-flex">Flex</div>
<div class="d-inline-flex">Inline flex</div>
<div class="d-none">None</div>

<!-- Responsive display types -->
<div class="d-block d-sm-flex d-md-grid">
  Changes display type at different breakpoints
</div>
```

## Customization

### Grid System
```scss
// Custom grid variables
$grid-columns: 15; // Change number of columns
$grid-gutter-width: 2rem; // Change gutter width
$grid-row-columns: 8; // Change number of row columns

// Custom breakpoints
$grid-breakpoints: (
  xs: 0,
  sm: 480px,
  md: 768px,
  lg: 1024px,
  xl: 1280px,
  xxl: 1536px
);

// Custom container max-widths
$container-max-widths: (
  sm: 420px,
  md: 720px,
  lg: 960px,
  xl: 1200px,
  xxl: 1400px
);

// Custom spacing
$spacer: 1rem;
$spacers: (
  0: 0,
  1: ($spacer * .25),
  2: ($spacer * .5),
  3: $spacer,
  4: ($spacer * 1.5),
  5: ($spacer * 3),
  6: ($spacer * 4),
  7: ($spacer * 5)
);

// Import Foxi Grid after variables
@import "foxi-grid/src/foxi-grid";
```

## Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)
- Opera (latest)
- Mobile browsers (iOS Safari, Android Chrome)

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License

MIT License - See LICENSE file for details