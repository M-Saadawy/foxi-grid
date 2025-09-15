# Grid System

## Overview

Foxi Grid is a flexible, responsive grid system built with SASS. It provides a robust foundation for creating complex layouts with ease.

## Core Concepts

### Container

Containers are the most basic layout element and are required when using the grid system. Choose from:

- `.container` - Fixed-width container with responsive breakpoints
- `.container-fluid` - Full-width container spanning the entire viewport

```html
<div class="container">
  <!-- Content here -->
</div>
```

### Row

Rows are horizontal groups of columns that ensure proper alignment and padding. Use `.row` to create a row:

```html
<div class="container">
  <div class="row">
    <!-- Columns here -->
  </div>
</div>
```

### Columns

Columns are the basic unit of content organization within a row. Key features:

- 12-column system by default (customizable)
- Responsive classes for different breakpoints
- Auto-layout options
- Nesting support

#### Basic Column Classes

- `.col` - Equal width column
- `.col-{number}` - Specific width column (1-12)
- `.col-auto` - Width based on content

#### Responsive Column Classes

- `.col-{breakpoint}-{number}`
  - xs: Extra small (< 576px)
  - sm: Small (≥ 576px)
  - md: Medium (≥ 768px)
  - lg: Large (≥ 992px)
  - xl: Extra large (≥ 1200px)
  - xxl: Extra extra large (≥ 1400px)

## Examples

### Basic Grid

```html
<div class="container">
  <div class="row">
    <div class="col-md-6">Half width on medium screens</div>
    <div class="col-md-6">Half width on medium screens</div>
  </div>
</div>
```

### Auto-layout

```html
<div class="row">
  <div class="col">Equal Width</div>
  <div class="col">Equal Width</div>
  <div class="col">Equal Width</div>
</div>
```

### Mixed Column Sizes

```html
<div class="row">
  <div class="col">Auto Width</div>
  <div class="col-6">Half Width</div>
  <div class="col">Auto Width</div>
</div>
```

### Nesting

```html
<div class="row">
  <div class="col-sm-9">
    Level 1: .col-sm-9
    <div class="row">
      <div class="col-8 col-sm-6">Level 2: .col-8 .col-sm-6</div>
      <div class="col-4 col-sm-6">Level 2: .col-4 .col-sm-6</div>
    </div>
  </div>
</div>
```

## Customization

### SASS Variables

```scss
// Grid columns
$grid-columns: 12 !default;
$grid-gutter-width: 1.5rem !default;
$grid-row-columns: 6 !default;

// Breakpoints
$grid-breakpoints: (
  xs: 0,
  sm: 576px,
  md: 768px,
  lg: 992px,
  xl: 1200px,
  xxl: 1400px
) !default;

// Container max-widths
$container-max-widths: (
  sm: 540px,
  md: 720px,
  lg: 960px,
  xl: 1140px,
  xxl: 1320px
) !default;
```

### Custom Column Count

```scss
// Override default column count
$grid-columns: 15;

// Import grid system
@import "foxi-grid/src/foxi-grid";
```

### Custom Breakpoints

```scss
// Override default breakpoints
$grid-breakpoints: (
  xs: 0,
  sm: 480px,
  md: 720px,
  lg: 1024px,
  xl: 1366px,
  xxl: 1600px
);

// Override container max-widths accordingly
$container-max-widths: (
  sm: 450px,
  md: 680px,
  lg: 960px,
  xl: 1280px,
  xxl: 1500px
);
```