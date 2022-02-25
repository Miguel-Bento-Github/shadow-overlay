# Shadow Overlay

ES Module `modern.js` 3.51KB <br>
CommonJS `legacy.js` 6.44KB <br>

<br><br>

<hr>
<br><br>

## Installation

`npm i -D shadow-overlay`<br>

`pnpm i -D shadow-overlay`<br>

`yarn add -D shadow-overlay`

<br><br>

<hr>
<br><br>

## Markup mode

### Element Attributes list

| attribute  | usage                                                                   |
| ---------- | ----------------------------------------------------------------------- |
| opacity    | `number`                                                                |
| color      | Any css valid `color` unit                                              |
| margin     | Any css `size` unit                                                     |
| gutters    | Any css `size` unit                                                     |
| disabled   | https://developer.mozilla.org/en-US/docs/Web/HTML/Attributes/disabled   |
| controller | Similar to disabled, `controller='true'` or just `controller` will work |

### HTML example

You can use the custom element by using import the main.js file in your `<head>`<br>
The attribute `type` should be `module`

```html
<!DOCTYPE html>
<html>
  <head>
    <script
      type="module"
      src="./node_modules/shadow-overlay/dist/module.js"
    ></script>
  </head>
  <body>
    <grid-overlay></grid-overlay> --> custom element 🎉
  </body>
</html>
```

The custom attribute list above contains all attributes that can be passed to the overlay

```html
<grid-overlay color="red"></grid-overlay> --> I'm a red grid now! ⭕⭕⭕⭕
```

<br><br>

<hr>
<br><br>

## Scripting mode

### Methods

### Basic usage

Import the overlay and start the instance

```ts
import { overlay } from 'shadow-overlay'
overlay.start()
```

### Methods usage

#### Start

```ts
overlay.start()
```

#### Opacity

```ts
overlay.setOpacity(0.4)
```

#### Color

```ts
overlay.setColor('red')
overlay.setColor('ff0000')
overlay.setColor('hsl(0, 100%, 50%)')
overlay.setColor('rgb(255, 0, 0)')
```

#### Margin and Gutters

```ts
overlay.setMargin('16px')
overlay.setMargin('1em')
overlay.setMargin('1rem')
overlay.setMargin('5ch')
overlay.setMargin('5%')
```

#### Disabled and Controller

```ts
overlay.disabled = true
overlay.disabled = 'true'
overlay.disabled = false
overlay.disabled = 'false'
overlay.disabled = undefined
```
