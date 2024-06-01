<h1 align='center'>
  Music Player
</h1>

<p align='center'>
  <a href='https://www.npmjs.com/package/mixmotion-player' target="_blank">
    <img src='https://img.shields.io/npm/v/mixmotion-player.svg' alt='Latest npm version'>
  </a>
    <a href='https://github.com/lewhunt/mixmotion/blob/main/LICENSE' target="_blank">
      <img src='https://img.shields.io/badge/License-GPLv3-yellow.svg' alt='GPLv3 License'>
  </a>
    <a href='https://www.npmjs.com/package/mixmotion-player' target="_blank">
    <img src='https://img.shields.io/npm/dm/mixmotion-player.svg' alt='Monthly npm downloads'>
  </a>

</p>

<p align='center'>
An immersive music player with Mixcloud integration and dynamic visual effects</p>

[![https://lewhunt.github.io/mixmotion/](https://lewhunt.github.io/assets/readme/mm-player-example.jpg)](https://lewhunt.github.io/mixmotion/)

<p align='center'><i>Click the image to try out the app</i>

## How to use

For casual users who just want to discover some new music with fullscreen visuals, hit the image above or link below to launch the Mixmotion web app on your mobile, desktop or TV device.

### [:point_right: Try out the App :point_left:](https://lewhunt.github.io/mixmotion/)

On playback, you'll enter an immersive lean-back mode, with a huge variety of dynamic backgrounds appearing after a few seconds of user inactivity. Below is a quick video of the app transitioning between playback modes:

https://github.com/lewhunt/mixmotion/assets/9886284/95a2116f-5e4c-47fc-af65-6e65a53a0048

More screenshots and videos at the end of this doc.

<hr>

## Installation

Developers can also install Mixmotion Player as an open source component to use in React apps. Quickest install method is via the npm i command below. Alternatively, integrate it manually by grabbing the lib folder in this repo along with the associated dependencies.

```bash
npm install
```

```bash
npm run dev
```

### Basic Usage

Import the player and render MixmotionPlayer in your own app with a Mixcloud URL. It will use default settings for the other non declared props.

```jsx
import { useEffect, useState } from "react";
import { MixmotionPlayer } from "mixmotion-player";

function Demo() {
  const [url, setUrl] = useState("");

  useEffect(() => {
    setUrl("https://www.mixcloud.com/discover/trance/?order=latest");
  }, []);

  return <MixmotionPlayer url={url} />;
}

export default Demo;
```

### Advanced Usage

The <a href='https://github.com/lewhunt/mixmotion/blob/main/src/DemoAdvanced.tsx'>advanced demo</a> and official <a href='https://lewhunt.github.io/mixmotion/'>web app</a> illustrate how the component can be customised further. Props are specified for custom buttons, video backgrounds and local data (saved items). A complete list of props are detailed further down this page.

```jsx
<MixmotionPlayer
  url={url}
  showsData={getSavedData}
  customButtons={customButtons}
  backdropVideoList={backdropVideoList}
  enableBackdropVideo={true}
></MixmotionPlayer>
```

<hr>

## Why Another Music Player?

There are plenty of web players and widgets already available from the likes of Soundcloud and Mixcloud that you can integrate into your app.

Mixmotion offers something different; an immersive, full-screen playback experience with unique visual effects, while still providing free access to Mixcloud's vast music catalogue.