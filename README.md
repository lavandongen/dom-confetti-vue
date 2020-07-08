# Vue Confetti (TypeScript)
Move the `.vue` file to your components folder and import it as usual. Then wherever you import the file position the pixel wherever you want it. And pass a config if you want.

## Example
import and cofigure the confetti canon.
```ts
import { Component, Vue } from 'vue-property-decorator';

import ConfettiCanon from '@/components/ConfettiCanon.vue'

@Component({
	components: {
		ConfettiCanon
	}
})
export default class Results extends Vue {
	confettiConfig: any = {
		angle: '45',
		spread: '70',
		startVelocity: '100',
		elementCount: '90',
		dragFriction: '0.13',
		duration: 4000,
		stagger: '2',
		width: '12px',
		height: '12px',
		colors: ['#FF4767', '#1AA8B5']
	}
}
```
For more options and the explainations of all settings check the official documentation [here](https://github.com/daniel-lundin/dom-confetti#interface).

Then include that it with the config (if you have a config) in the `<template>`.
```html
<confetti-canon :config="confettiConfig" />
```

## Requirements
This file uses `TypeScript` make sure your Vue project runs using TypeScript using the `Class-Style` based implementation.

If you wish to use this without TypeScript, [Claudia Ochoa](https://github.com/claudia-ochoa) made a conversion from this to vanilla Vue that can be found here: https://github.com/claudia-ochoa/vue-confetti

## Credits
This file was converted from [dom confetti](https://github.com/daniel-lundin/dom-confetti) and all credit goes to [Daniel Lundin](https://github.com/daniel-lundin).

All I did was convert them from one to the other.
