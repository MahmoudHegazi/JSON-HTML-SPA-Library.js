# Unreal World Engine — UI DOM Framework

**Unreal World Engine** is a lightweight, JSON-driven UI framework designed for building web app layouts without enforcing any logic or interactivity. It allows you to construct entire UI worlds using declarative JSON configurations while leaving all behavior and app logic to the developer.

## ✨ Features

- ⚙️ **Zero-JavaScript Logic Requirements**: The framework handles rendering only. Developers manage actions and logic separately.
- 🧠 **Pure UI Focus**: No state, no logic — just structure, layout, and interaction hooks.
- 🔄 **JSON-Defined Views**: Exportable and importable JSON schemas define views, components, navigation, and more.
- 🌐 **Single-Page Navigation**: Internal view switching with DOM rendering; no page reloads.
- 🌟 **Responsive Design**: Bootstrap-powered grid system with additional layout options.
- 📅 **onClickAction Support**: Hook user actions declaratively without embedding JS logic inside components.

## 📁 Example JSON Schema

```json
{
  "id": "goto_map_maker",
  "target": "main",
  "targetType": "component",
  "text": "Map Maker",
  "onClickAction": "openMapEditor"
}
```

And your app handles it like this:

```js
window.onUIAction = function(action, item) {
  if (action === 'openMapEditor') {
    // Handle opening map editor UI
  }
};
```

## 🚀 Quick Start

1. Include the engine script in your HTML:

```html
<script src="path/to/unreal-world-engine.js"></script>
```

2. Define your layout using JSON:

```js
const app = {
  appId: 'app',
  views: [
    {
      id: 'main_view',
      type: 'view',
      nav: { items: [/* ... */] },
      childs: [/* ... */]
    }
  ]
};
```

3. Load the app:

```js
window.onload = () => {
  renderApp(app);
};
```

## 📊 Use Cases

- No-code or low-code layout builders
- Game or world editor interfaces
- JSON-based UI scene exporters
- Prototype-to-production layout transitions
- SPA frontends that separate layout from logic

## 📖 Documentation

- [ ] JSON Schema Reference
- [ ] Built-in Bootstrap Themes
- [ ] Event Hooks & Action Handling
- [ ] Embedding & Export

## 📚 License

MIT License

## 🙌 Made With

- JavaScript (ES5+ compatible)
- Bootstrap 4 / 5
- jQuery Slim (for basic compatibility)

## ✨ Credits

Created with vision and precision by [YourName].

---

> "You build the world. You control the logic. This is just the stage."

---

Need help? Open an issue or message me directly.

---

