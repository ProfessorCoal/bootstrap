---
layout: docs
title: Customization options
description: Customize Bootstrap with Sass variables, easily toggling global preferences with a quick recompile.
group: getting-started
---

With Bootstrap 4, we've added a handful of global options for easily customizing all the components in your project. These options are handled by Sass variables. Simply change a variable's value and recompile with the included Gruntfile.

## Available variables

<<<<<<< HEAD
Bootstrap 4 ships with a `_custom.scss` file for easy overriding of default variables in `/scss/_variables.scss`. Copy and paste relevant lines from there into the `_custom.scss` file, modify the values, and recompile your Sass to change our default values. **Be sure to remove the `!default` flag from override values.**
=======
You can find and customize these variables in our `_variables.scss` file.
>>>>>>> 153630e06119bd0eba602920f6a2254be243dbd5

| Variable                    | Values                             | Description                                                             |
| --------------------------- | ---------------------------------- | ----------------------------------------------------------------------- |
| `$spacer`                   | `1rem` (default), or any value > 0 | Specifies the default spacer value for our spacer utilities.            |
| `$enable-flex`              | `true` or `false` (default)        | Swaps `float` and `display: table` styles for `display: flex`.          |
| `$enable-rounded`           | `true` (default) or `false`        | Enables predefined `border-radius` styles on various components.        |
| `$enable-shadows`           | `true` or `false` (default)        | Enables predefined `box-shadow` styles on various components.           |
| `$enable-gradients`         | `true` or `false` (default)        | Enables predefined gradients via `background-image` various components. |
| `$enable-transitions`       | `true` (default) or `false`        | Enables predefined `transition`s on various components. |
| `$enable-hover-media-query` | `true` or `false` (default)        | ... |
| `$enable-grid-classes`      | `true` (default) or `false`        | Enables the generation of CSS classes for the grid system (e.g. `.col-md-1` etc.). |

## Color palette

Bootstrap's color palette includes a numerical range of shades for each base color, heavily inspired by [Google's color palette](https://www.google.com/design/spec/style/color.html#color-color-palette). Base colors, which utilize Sass color functions to generate each additional shade, are indicated at the top of each stacked palette.

<div class="row">
  <div class="col-sm-6 col-md-4 color-palette">
    <div class="color-slab color-slab-base foreground-500">500</div>
    <div class="color-slab foreground-100">100</div>
    <div class="color-slab foreground-200">200</div>
    <div class="color-slab foreground-300">300</div>
    <div class="color-slab foreground-400">400</div>
    <div class="color-slab foreground-500">500</div>
    <div class="color-slab foreground-600">600</div>
    <div class="color-slab foreground-700">700</div>
    <div class="color-slab foreground-800">800</div>
    <div class="color-slab foreground-900">900</div>
  </div>
  <div class="col-sm-6 col-md-4 color-palette">
    <div class="color-slab color-slab-base primary-500">
      500
    </div>
    <div class="color-slab primary-100">100</div>
    <div class="color-slab primary-200">200</div>
    <div class="color-slab primary-300">300</div>
    <div class="color-slab primary-400">400</div>
    <div class="color-slab primary-500">500</div>
    <div class="color-slab primary-600">600</div>
    <div class="color-slab primary-700">700</div>
    <div class="color-slab primary-800">800</div>
    <div class="color-slab primary-900">900</div>
  </div>
  <div class="col-sm-6 col-md-4 color-palette">
    <div class="color-slab color-slab-base success-500">500</div>
    <div class="color-slab success-100">100</div>
    <div class="color-slab success-200">200</div>
    <div class="color-slab success-300">300</div>
    <div class="color-slab success-400">400</div>
    <div class="color-slab success-500">500</div>
    <div class="color-slab success-600">600</div>
    <div class="color-slab success-700">700</div>
    <div class="color-slab success-800">800</div>
    <div class="color-slab success-900">900</div>
  </div>
  <div class="col-sm-6 col-md-4 color-palette">
    <div class="color-slab color-slab-base info-500">500</div>
    <div class="color-slab info-100">100</div>
    <div class="color-slab info-200">200</div>
    <div class="color-slab info-300">300</div>
    <div class="color-slab info-400">400</div>
    <div class="color-slab info-500">500</div>
    <div class="color-slab info-600">600</div>
    <div class="color-slab info-700">700</div>
    <div class="color-slab info-800">800</div>
    <div class="color-slab info-900">900</div>
  </div>
  <div class="col-sm-6 col-md-4 color-palette">
    <div class="color-slab color-slab-base warning-500">500</div>
    <div class="color-slab warning-100">100</div>
    <div class="color-slab warning-200">200</div>
    <div class="color-slab warning-300">300</div>
    <div class="color-slab warning-400">400</div>
    <div class="color-slab warning-500">500</div>
    <div class="color-slab warning-600">600</div>
    <div class="color-slab warning-700">700</div>
    <div class="color-slab warning-800">800</div>
    <div class="color-slab warning-900">900</div>
  </div>
  <div class="col-sm-6 col-md-4 color-palette">
    <div class="color-slab color-slab-base danger-500">500</div>
    <div class="color-slab danger-100">100</div>
    <div class="color-slab danger-200">200</div>
    <div class="color-slab danger-300">300</div>
    <div class="color-slab danger-400">400</div>
    <div class="color-slab danger-500">500</div>
    <div class="color-slab danger-600">600</div>
    <div class="color-slab danger-700">700</div>
    <div class="color-slab danger-800">800</div>
    <div class="color-slab danger-900">900</div>
  </div>
</div>

### Using the variables

The Bootstrap color palette is built with variables, a Sass map, and some functions. Generic variables are included for a standard set of colors (e.g., `$red` or `$blue`). A subset of those variables are then referenced into the `$theme-colors` Sass map, allowing for easy generation of themed component modifier classes with the `theme-color` or `theme-color-level` functions.

Modify the source color variables and reassign values to the theme colors in `$theme-colors` as you like.

{% highlight sass %}
// Declare all colors
$red: #d9534f !default;
$pink: #ff5b77 !default;
$purple: #613d7c !default;
$blue: #0275d8 !default;
$teal: #5bc0de !default;
$green: #5cb85c !default;
$yellow: #ffd500 !default;
$orange: #f0ad4e !default;
$gray: #6f6f81 !default;
$white: #fff !default;

// Declare a subset of colors for semantic/contextual usage
$theme-colors: (
  "primary": $blue,
  "secondary": $gray,
  "success": $green,
  "info": $teal,
  "warning": $orange,
  "danger": $red,
  "foreground": $gray,
  "background": $white
) !default;

<<<<<<< HEAD
| Variable                    | Values                             | Description                                                                            |
| --------------------------- | ---------------------------------- | -------------------------------------------------------------------------------------- |
| `$spacer`                   | `1rem` (default), or any value > 0 | Specifies the default spacer value for our spacer utilities.                           |
| `$enable-rounded`           | `true` (default) or `false`        | Enables predefined `border-radius` styles on various components.                       |
| `$enable-shadows`           | `true` or `false` (default)        | Enables predefined `box-shadow` styles on various components.                          |
| `$enable-gradients`         | `true` or `false` (default)        | Enables predefined gradients via `background-image` styles on various components.      |
| `$enable-transitions`       | `true` (default) or `false`        | Enables predefined `transition`s on various components.                                |
| `$enable-hover-media-query` | `true` or `false` (default)        | ...                                                                                    |
| `$enable-grid-classes`      | `true` (default) or `false`        | Enables the generation of CSS classes for the grid system (e.g., `.container`, `.row`, `.col-md-1`, etc.).     |
=======
// Allow us to reference the `$theme-colors` map color names (e.g., "primary")
@function theme-color($key: "primary") {
  @return map-get($theme-colors, $key);
}

// Allow us to reference mixed shades of the colors in `$theme-colors`
@function theme-color-level($color-name: "primary", $level: 0) {
  $color: theme-color($color-name);
  $color-base: if($level > 0, black, white);

  @if $level < 0 {
    // Lighter values need a quick double negative for the Sass math to work
    @return mix($color-base, $color, $level * -1 * $theme-color-interval);
  } @else {
    @return mix($color-base, $color, $level * $theme-color-interval);
  }
}

// Example: Use `theme-color-level` function to generate color shade variables
$primary: theme-color-level("primary", 0) !default;
$primary-100: theme-color-level("primary", -9.5) !default;
$primary-200: theme-color-level("primary", -7) !default;
$primary-300: theme-color-level("primary", -4) !default;
$primary-400: theme-color-level("primary", -2) !default;
$primary-500: $primary !default;
$primary-600: theme-color-level("primary", 2) !default;
$primary-700: theme-color-level("primary", 4) !default;
$primary-800: theme-color-level("primary", 6) !default;
$primary-900: theme-color-level("primary", 8) !default;
{% endhighlight %}
>>>>>>> 153630e06119bd0eba602920f6a2254be243dbd5
