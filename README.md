# React AUI &middot; [![GitHub license](https://img.shields.io/badge/license-MIT-blue.svg)](https://github.com/iZemil/react-aui/blob/master/LICENSE) ![GitHub code size in bytes](https://img.shields.io/github/languages/code-size/izemil/react-aui)

[React AUI library Storybook Components](https://izemil.github.io/react-aui/)

## Development

-   run storybook dev server `npm run dev`
-   [commit changes and push](https://semantic-release.gitbook.io/semantic-release/), github actions and semantic realease deploy changes to npm and update github pages automatically

## Production

-   Install [npm package](https://www.npmjs.com/package/react-aui) `npm i react-aui`
-   Init AUIProvider into root of your project:

```jsx
import { IAUI, darkTheme, lightTheme } from 'react-aui';

\// also you can create your own themes, see IAUI
const theme: IAUI = {
	...darkTheme,
	mode: 'myTheme',
	colors: {
		...darkTheme.colors,
		\// for example, change some colors
		bg: '#36393f',
		text: '#ffffff',
	},
};
const App = () => {
	return (
		<AUIProvider themes={[theme, lightTheme, darkTheme]} active={0}>
			{/* your frontend components */}
		</AUIProvider>
	);
};
```
