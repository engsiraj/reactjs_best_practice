# React JS Best Practices

List Contains usefull features, functions, methods Of React and Javascript.

- [import and exports components](#import_export_components)
- [import and exports files and links ](#import_export_file_links)

## import and exports components

First we will create file for adding what we want to export `index.js/ts/jsx` in components folder.

```javascript
//export your component as index.js/ts/jsx file.

export { default as ChannelCard } from "./ChannelCard";
export { default as VideoCard } from "./VideoCard";
export { default as ChannelDetail } from "./ChannelDetail";
export { default as Feed } from "./Feed";

//import from your component as index.js/ts/jsx file.

import { ChannelCard, VideoCard, ChannelDetail, Feed } from "./";
```

## import and exports files and links

First we will create file for adding what we want to export `utils/contant.js/ts/jsx` in utilsfor components.

```javascript
import MusicNoteIcon from "@mui/icons-material/MusicNote";
import HomeIcon from "@mui/icons-material/Home";
import CodeIcon from "@mui/icons-material/Code";
import OndemandVideoIcon from "@mui/icons-material/OndemandVideo";
import SportsEsportsIcon from "@mui/icons-material/SportsEsports";

export const logo = "https://i.ibb.co/s9Qys2j/logo.png";

export const categories = [
  { name: "New", icon: <HomeIcon /> },
  { name: "JS Mastery", icon: <CodeIcon /> },
  { name: "Coding", icon: <CodeIcon /> },
  { name: "ReactJS", icon: <CodeIcon /> },
  { name: "NextJS", icon: <CodeIcon /> },
];

export const demoThumbnailUrl = "https://i.ibb.co/G2L2Gwp/API-Course.png";
export const demoChannelUrl = "/channel/UCmXmlB4-HJytD7wek0Uo97A";
export const demoVideoUrl = "/video/GDa8kZLNhJ4";

//import from your component as utils/constant.js/ts/jsx file.

import {
  demoThumbnailUrl,
  demoVideoUrl,
  demoVideoTitle,
  demoChannelUrl,
  demoChannelTitle,
} from "../utils/constant";
```
