# jquery-custom-select
Custom Select jQuery Plugin

[![npm version](https://img.shields.io/npm/v/jquery-custom-select.svg)](https://npmjs.com/package/jquery-custom-select)

Simple plugin creates custom select instead of default `<select>`.

### Usage

```js
$('select').customSelect();
```

Selectors naming of custom select based on BEM. Here is HTML structure of block (open dropdown state):

```html
<div class="custom-select custom-select--active">
  <button class="custom-select__option custom-select__option--value" type="button">...</button>
  <div class="custom-select__dropdown">
    <button class="custom-select__option" type="button">...</button>
    <button class="custom-select__option" type="button">...</button>
    <button class="custom-select__option" type="button">...</button>
  </div>
</div>
```

Note, plugin does not contain any additional CSS except of base, which includes only dropdown positioning, reset of options & input.

### Options

Name | Type | Default | Description
---- | ---- | ------- | -----------
`block` | string | `'custom-select'` | Class name (BEM block name)
`hideCallback` | Function | `false` | Fires after dropdown closes
`includeValue` | boolean | `false` | Shows chosen value option in dropdown, if enabled also cancels dropdown options rerender
`keyboard` | boolean | `true` | Enables keyboard control
`modifier` | string | `false` | Additional class, e.g. BEM modifier
`placeholder` | string | `false` | Custom select placeholder hint, can be an HTML string (appears if there is no explicitly selected options)
`search` | boolean | `false` | Adds input to search options
`showCallback` | Function | `false` | Fires after dropdown opens
`transition` | number &#124;&#124; string | `100` | jQuery slideUp/Down speed

### Demo

You can view demo [here](https://kvlsrg.github.io/jquery-custom-select/).
