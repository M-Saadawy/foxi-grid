# Getting Started

## Installation

### NPM

```bash
npm install foxi-grid
```

### Yarn

```bash
yarn add foxi-grid
```

## Usage

### Basic Setup

1. Import the grid system in your SASS file:

```scss
@import "foxi-grid/src/foxi-grid";
```

2. Start using the grid classes in your HTML:

```html
<div class="container">
  <div class="row">
    <div class="col-md-6">Column 1</div>
    <div class="col-md-6">Column 2</div>
  </div>
</div>
```

### Custom Configuration

Create a custom configuration file (e.g., `_custom-grid.scss`):

```scss
// Custom variables
$grid-columns: 15;
$grid-gutter-width: 2rem;

// Custom breakpoints
$grid-breakpoints: (
  xs: 0,
  sm: 480px,
  md: 768px,
  lg: 1024px,
  xl: 1280px,
  xxl: 1536px
);

// Import Foxi Grid after variables
@import "foxi-grid/src/foxi-grid";
```

## Basic Concepts

### Container Types

```html
<!-- Fixed width container -->
<div class="container">
  <!-- Responsive max-width -->
</div>

<!-- Fluid container -->
<div class="container-fluid">
  <!-- Full width -->
</div>
```

### Grid System

```html
<!-- Basic grid -->
<div class="container">
  <div class="row">
    <div class="col-12 col-md-6 col-lg-4">
      <!-- Responsive column -->
    </div>
  </div>
</div>

<!-- Auto-layout -->
<div class="row">
  <div class="col">Auto width</div>
  <div class="col-6">Fixed width</div>
  <div class="col">Auto width</div>
</div>
```

### Responsive Utilities

```html
<!-- Responsive visibility -->
<div class="d-none d-md-block">
  <!-- Hidden on mobile, visible on desktop -->
</div>

<!-- Responsive spacing -->
<div class="mt-2 mt-md-3 mt-lg-4">
  <!-- Different margins at different breakpoints -->
</div>

<!-- Responsive flexbox -->
<div class="d-flex flex-column flex-md-row">
  <!-- Stack on mobile, row on desktop -->
</div>
```

## Best Practices

1. Always use `.container` or `.container-fluid` as the outermost wrapper
2. Place `.row` elements directly inside containers
3. Place columns (`.col-*`) directly inside rows
4. Use responsive classes for better mobile experience
5. Avoid deeply nested grids when possible

## Examples

### Basic Layout

```html
<div class="container">
  <!-- Header -->
  <div class="row">
    <div class="col-12">
      <header>...</header>
    </div>
  </div>

  <!-- Main content -->
  <div class="row">
    <div class="col-12 col-md-8">
      <main>...</main>
    </div>
    <div class="col-12 col-md-4">
      <aside>...</aside>
    </div>
  </div>

  <!-- Footer -->
  <div class="row">
    <div class="col-12">
      <footer>...</footer>
    </div>
  </div>
</div>
```

### Complex Layout

```html
<div class="container">
  <div class="row">
    <!-- Main content area -->
    <div class="col-12 col-lg-8">
      <div class="row">
        <div class="col-md-6">
          <!-- Article 1 -->
        </div>
        <div class="col-md-6">
          <!-- Article 2 -->
        </div>
      </div>
    </div>

    <!-- Sidebar -->
    <div class="col-12 col-lg-4">
      <!-- Sidebar content -->
    </div>
  </div>
</div>
```

## Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)
- Opera (latest)
- Mobile browsers (iOS Safari, Android Chrome)

## Troubleshooting

### Common Issues

1. Columns overflowing:
   - Make sure you're using `.row` to wrap columns
   - Check for padding/margin on child elements

2. Uneven column heights:
   - Use `.h-100` on column content
   - Consider using flexbox utilities

3. Unexpected margins:
   - Remember that `.row` has negative margins
   - Use `.no-gutters` to remove gutters if needed

### Solutions

```html
<!-- Fix uneven heights -->
<div class="row">
  <div class="col">
    <div class="h-100">Equal height content</div>
  </div>
  <div class="col">
    <div class="h-100">Equal height content</div>
  </div>
</div>

<!-- Remove gutters -->
<div class="row g-0">
  <div class="col">No gutter content</div>
  <div class="col">No gutter content</div>
</div>
```