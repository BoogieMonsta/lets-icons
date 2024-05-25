# Lets Icons

A tree-shakeable icon set, available as a framework-agnostic npm package.

## Purpose

The Lets Icons set, designed by [Leonid Tsvetkov](https://www.figma.com/community/file/886554014393250663/free-icon-pack-1800-icons), is a remarkable collection of icons available through the npm package provided by Iconify.

However, the Iconify method requires importing the entire Lets Icons set, even if you only need a few icons for your application.

For developers aiming to keep their applications lean and efficient, this is a deal-breaker, as it can lead to unnecessary bloat, slower load times, and degraded performance.

This library addresses this issue by supporting tree-shaking, allowing you to import only the specific Lets Icons you need by their names, and nothing more.

To keep things simple, efficient and flexible, the icons are all in SVG format, ready to be displayed and/or modified.

## Name Conformance

The original Lets Icons names presented a few compatibility issues with JavaScript rules:

- The names are in kebab case
- Some names started with a number
- Some names matched protected keywords (e.g., the icon "export")

To resolve these issues, each icon name has been:

- converted from `kebab-case` to `snake_case`
- prefixed with `li_` (for "lets icons")

Note: Converting the names from kebab-case to camelCase was not feasible due to naming conflicts on case-insensitive file systems (ex: `liSunLight.ts` and `liSunlight.ts` cannot coexist in the same directory). Therefore, I opted to convert the names to snake_case for practicality, despite it being unconventional.

## Usage

1. Install this package into your application
2. Go [find the icon you want to use](https://icon-sets.iconify.design/lets-icons/), and copy its name
3. Import the icon you want to use in your application
4. Display the svg icon according to your frontend framework's best practices

### Example

First, I install the package:

```shell
npm install lets-icons
```

Now, let's say I want to use the icon `subttasks-alt-duotone`.

As explained above, the name to import will be in snake_case, and it will be prefixed by li_, so I can import the icon like this:

```javascript
import { li_subttasks_alt_duotone } from 'lets-icons';
```

Then, I just need to display the SVG icon, usually by putting it into the inner HTML of a div. Just keep in mind that your frontend framework might need to sanitize the DOM first.
