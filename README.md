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
