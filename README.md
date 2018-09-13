# &lt;details-dialog&gt; element

A modal dialog that's opened with a &lt;details> button.

## Installation

```
$ npm install --save details-dialog-element
```

## Usage

```js
import 'details-dialog-element'
```

```html
<details>
  <summary>Open dialog</summary>
  <details-dialog>
    Modal content
    <button type="button" data-close-dialog>Close</button>
  </details-dialog>
</details>
```

## Events

### `details-dialog:will-close`

A `details-dialog:will-close` event is fired when a request to close the dialog
is made either by pressing escape, clicking the close button, clicking outside
the dialog, or when `.toggle(false)` is called on an open dialog.

This event can be cancelled to keep the dialog open.

```js
document.addEventListener('details-dialog:will-close', function(event) {
  if (!confirm("Are you sure?")) {
    event.preventDefault()
  }
})
```

## Browser support

Browsers without native [custom element support][support] require a [polyfill][].

- Chrome
- Firefox
- Safari
- Internet Explorer 11
- Microsoft Edge

[support]: https://caniuse.com/#feat=custom-elementsv1
[polyfill]: https://github.com/webcomponents/custom-elements

## Development

```
npm install
npm test
```

## License

Distributed under the MIT license. See LICENSE for details.
