<div align="center">
<h1>React Canvas Draw</h1>
</div>

> A simple yet powerful canvas-drawing component for React ([Demo](https://embiem.github.io/react-canvas-draw/))

[![npm package][npm-badge]][npm] [![downloads][downloads-badge]][npmtrends] [![MIT License][license-badge]][license] [![PRs Welcome][prs-badge]][prs]

[![Watch on GitHub][github-watch-badge]][github-watch] [![Star on GitHub][github-star-badge]][github-star]

## Installation

Install via NPM:

```
npm install @krajncdev/react-canvas-draw --save
```

or YARN:

```
yarn add @krajncdev/react-canvas-draw
```

## Original repository

This is an extended version of the [react-canvas-draw](https://www.npmjs.com/package/react-canvas-draw) repository.

## Usage

```javascript
import React from 'react';
import ReactDOM from 'react-dom';
import CanvasDraw from 'react-canvas-draw';

ReactDOM.render(<CanvasDraw />, document.getElementById('root'));
```

For more examples, like saving and loading a drawing ==> look into the [`/demo/src` folder](https://github.com/embiem/react-canvas-draw/tree/master/demo/src).

### Props

These are the defaultProps of CanvasDraw. You can pass along any of these props to customize the CanvasDraw component. Examples of how to use the props are also shown in the [`/demo/src` folder](https://github.com/embiem/react-canvas-draw/tree/master/demo/src).

```javascript
  static defaultProps = {
    onChange: null,
    loadTimeOffset: 5,
    lazyRadius: 30,
    brushRadius: 12,
    brushColor: "#444",
    catenaryColor: "#0a0302",
    gridColor: "rgba(150,150,150,0.17)",
    backgroundColor: "#ffffff",
    containImg: true,
    hideGrid: false,
    canvasWidth: 400,
    canvasHeight: 400,
    disabled: false,
    imgSrc: "",
    saveData: null,
    immediateLoading: false,
    hideInterface: false,
    gridSizeX: 25,
    gridSizeY: 25,
    gridLineWidth: 0.5,
    hideGridX: false,
    hideGridY: false,
    enablePanAndZoom: false,
    mouseZoomFactor: 0.01,
    zoomExtents: { min: 0.33, max: 3 },
    clampLinesToDocument: false,
  };
```

### Functions

Useful functions that you can call, e.g. when having a reference to this component:

- `getSaveData()` returns the drawing's save-data as a stringified object
- `loadSaveData(saveData: String, immediate: Boolean)` loads a previously saved drawing using the saveData string, as well as an optional boolean flag to load it immediately, instead of live-drawing it.
- `getDataURL({fileType: String, useBgImage: Boolean, backgroundColour: String, resetView: Boolean})` will export the canvas to a data URL, which can subsequently be used to share or manipulate the image file.
- `clear()` clears the canvas completely, including previously erased lines, and resets the view. After a clear, `undo()` will have no effect.
- `eraseAll()` clears the drawn lines but retains their data; calling `undo()` can restore the erased lines. _Note: erased lines are not included in the save data._
- `resetView()` resets the canvas' view to defaults. Has no effect if the `enablePanAndZoom` property is `false`.
- `undo()` removes the latest change to the drawing. This includes everything drawn since the last MouseDown event.

## Local Development

This repo was kickstarted by nwb's awesome [react-component starter](https://github.com/insin/nwb/blob/master/docs/guides/ReactComponents.md#developing-react-components-and-libraries-with-nwb).

You just need to clone it, yarn it & start it!

## Acknowledgement

The [lazy-brush](https://github.com/dulnan/lazy-brush) project as well as its demo app by [dulnan](https://github.com/dulnan) have been a heavy influence.

I borrowed a lot of the logic and actually used lazy-brush during the push to v1 of react-canvas-draw. Without it, react-canvas-draw would most likely still be pre v1 and wouldn't feel as good.

## Contributors

Thanks goes to these wonderful people ([emoji key](https://github.com/kentcdodds/all-contributors#emoji-key)):

<!-- ALL-CONTRIBUTORS-LIST:START - Do not remove or modify this section -->
<!-- prettier-ignore -->
| [<img src="https://avatars3.githubusercontent.com/u/3866457?v=4" width="100px;"/><br /><sub><b>Martin Beierling-Mutz</b></sub>](https://embiem.me)<br />[💻](https://github.com/embiem/react-canvas-draw/commits?author=embiem "Code") [📖](https://github.com/embiem/react-canvas-draw/commits?author=embiem "Documentation") [💡](#example-embiem "Examples") [🤔](#ideas-embiem "Ideas, Planning, & Feedback") | [<img src="https://avatars0.githubusercontent.com/u/4155003?v=4" width="100px;"/><br /><sub><b>Jan Hug</b></sub>](http://www.janhug.info)<br />[🤔](#ideas-dulnan "Ideas, Planning, & Feedback") | [<img src="https://avatars0.githubusercontent.com/u/127794593?v=4" width="100px;"/><br /><sub><b>Jaka Krajnc</b></sub>](http://www.krajnc)<br />[💻](#code "Code") |
| :---: | :---: | :---: |

<!-- ALL-CONTRIBUTORS-LIST:END -->

This project follows the [all-contributors](https://github.com/kentcdodds/all-contributors) specification. Contributions of any kind welcome!

## License

MIT, see [LICENSE](https://github.com/embiem/react-canvas-draw/blob/master/LICENSE) for details.

[build-badge]: https://img.shields.io/travis/embiem/@krajncdev/react-canvas-draw/master.png?style=flat-square
[build]: https://travis-ci.org/embiem/react-canvas-draw
[npm-badge]: https://img.shields.io/npm/v/@krajncdev/react-canvas-draw.png?style=flat-square
[npm]: https://www.npmjs.com/package/@krajncdev/react-canvas-draw
[npm]: https://www.npmjs.com/
[node]: https://nodejs.org
[downloads-badge]: https://img.shields.io/npm/dm/@krajncdev/react-canvas-draw.svg?style=flat-square
[npmtrends]: http://www.npmtrends.com/react-canvas-draw
[license-badge]: https://img.shields.io/npm/l/@krajncdev/react-canvas-draw.svg?style=flat-square
[license]: https://github.com/embiem/react-canvas-draw/blob/master/LICENSE
[prs-badge]: https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat-square
[prs]: http://makeapullrequest.com
[github-watch-badge]: https://img.shields.io/github/watchers/embiem/react-canvas-draw.svg?style=social
[github-watch]: https://github.com/embiem/@krajncdev/react-canvas-draw/watchers
[github-star-badge]: https://img.shields.io/github/stars/embiem/react-canvas-draw.svg?style=social
[github-star]: https://github.com/embiem/@krajncdev/react-canvas-draw/stargazers
