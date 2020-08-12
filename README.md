# [@st-lib/render](https://www.npmjs.com/package/@st-lib/render) [@st-lib/events](https://www.npmjs.com/package/@st-lib/events) bindings.

```ts
import { render, text } from '@st-lib/render'
import { button } from '@st-lib/render-html'
import { onClick } from '@st-lib/render-events'

window.onload = () => {
	render(document.body, () => {
		button(null, () => {
			onClick(() => {
				console.log('click')
			})
			text(null, 'click me?')
		})
	})
}
```

```ts
import { render, text } from '@st-lib/render'
import { onDocumentScroll, onWindowResize } from '@st-lib/render-events'

window.onload = () => {
	render(document.body, () => {
		onDocumentScroll(() => {
			console.log(document.scrollTop)
		}, true)

		onWindowResize(() => {
			console.log(window.innerWidth, window.innerHeight)
		}, true)


		text(null, 'lorem ipsum' /* ... */)
	})
}
```
