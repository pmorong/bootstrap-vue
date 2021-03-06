# Navs

> Navigation available in Bootstrap share general markup and styles,
from the base `<b-nav>` class to the `active` and `disabled` states.
Swap modifier props to switch between each style.

```html
<div>
  <b-nav>
    <b-nav-item active>Active</b-nav-item>
    <b-nav-item>Link</b-nav-item>
    <b-nav-item>Another Link</b-nav-item>
    <b-nav-item disabled>Disabled</b-nav-item>
  </b-nav>
</div>

<!-- nav-1.vue -->
```

The base `<b-nav>` component is built with flexbox and provides a strong
foundation for building all types of navigation components. It includes
some style overrides (for working with lists), some link padding for larger
hit areas, and basic disabled styling. No active states are included in the base nav.

### Link Appearance

Two style variations are supported: `tabs` and `pills`, which support `active` state styling.
These variants are mutually exclusive - use only one style or the other.

#### Tabs:

Make the nav look like tabs by setting the prop `tabs`.

```html
<b-nav tabs>
  <b-nav-item active>Active</b-nav-item>
  <b-nav-item>Link</b-nav-item>
  <b-nav-item>Another Link</b-nav-item>
  <b-nav-item disabled>Disabled</b-nav-item>
</b-nav>

<!-- nav-2.vue -->
```

#### Pills:

Use the pill style by setting the prop `pills`.

```html
<b-nav pills>
  <b-nav-item active>Active</b-nav-item>
  <b-nav-item>Link</b-nav-item>
  <b-nav-item>Another Link</b-nav-item>
  <b-nav-item disabled>Disabled</b-nav-item>
</b-nav>

<!-- nav-3.vue -->
```

### Fill and justify

Force your `b-nav` content to extend the full available width.

#### fill:

To proportionately fill all available space with your `<b-nav-item>` components,
set the `fill` prop. Notice that all horizontal space is occupied, but not
every nav item has the same width.

```html
<b-nav fill tabs>
  <b-nav-item active>Active</b-nav-item>
  <b-nav-item>Link</b-nav-item>
  <b-nav-item>Link with a long name </b-nav-item>
  <b-nav-item disabled>Disabled</b-nav-item>
</b-nav>

<!-- nav-4.vue -->
```

#### Justified:

For equal-width elements, set prop `justified` instead. All horizontal space
will be occupied by nav links, but unlike `fill` above, every `<b-nav-item>`
will be the same width.

```html
<b-nav justified tabs>
  <b-nav-item active>Active</b-nav-item>
  <b-nav-item>Link</b-nav-item>
  <b-nav-item>Link with a long name </b-nav-item>
  <b-nav-item disabled>Disabled</b-nav-item>
</b-nav>

<!-- nav-5.vue -->
```

### Vertical variation

By default navs appear on a horizontal line. Stack your navigation by setting
the `vertical` prop.

```html
<b-nav vertical class="w-25">
  <b-nav-item active>Active</b-nav-item>
  <b-nav-item>Link</b-nav-item>
  <b-nav-item>Another Link</b-nav-item>
  <b-nav-item disabled>Disabled</b-nav-item>
</b-nav>

<!-- nav-6.vue -->
```

### Dropdown support

Use `<b-nav-item-dropdown>` to place dropdown items within your nav.

```html
<b-nav pills>
  <b-nav-item active>Active</b-nav-item>
  <b-nav-item>Link</b-nav-item>
  <b-nav-item-dropdown id="nav7_ddown" text="Dropdown" right>
    <b-dropdown-item>one</b-dropdown-item>
    <b-dropdown-item>two</b-dropdown-item>
    <b-dropdown-divider></b-dropdown-divider>
    <b-dropdown-item>three</b-dropdown-item>
  </b-nav-item-dropdown>
</b-nav>

<!-- nav-7.vue -->
```

Refer to [`<b-dropdown>`](../dropdown) for a list of supported sub-components.


### Using in Navbar

When using `<b-nav>` within a `<b-navbar>`, set the `navbar-nav` prop.

### Tabbed content support

See the [`<b-tabs>`](./tabs) component.

### Regarding accessibility

If you’re using `<b-nav>` to provide a navigation bar, be sure to add a
`role="navigation"` to the most logical parent container of `<b-nav>`, or wrap
a `<nav>` element around `<b-nav>`. Do **not** add the role to the `<b-nav>` itself,
as this would prevent it from being announced as an actual list by assistive technologies.

When using a `<b-nav-item-dropdown>` in your `<b-nav>`, be sure to assign a unique `id`
prop value to the `<b-nav-dropdown>` so that the apropriate `aria-*` attributes can
be automatically generated.

### See Also

- [`<b-tabs>`](./tabs) to create tabbable panes of local content, even via dropdown menus.
- [`<b-navbar>`](./navbar) a wrapper that positions branding, navigation, and other elements in a concise header.
- [`<b-dropdown>`](./dropdown) for sub-components that you can place inside `<b-nav-item-dropdown>`
