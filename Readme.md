# React-electron-contextmenu
Makes it super easy to create context menus in your React powered Electron apps. TypeScript supported!

## Installation
```bash
npm install react-electron-contextmenu --save
```

## Usage

Import the component:
```ts
import ContextMenuArea from "react-electron-contextmenu";
```

Wrap the component you want to use as the right click area in the `<ContextMenuArea>` component and use in render method:
```tsx
render() {
  const menuItems = [
    {
      label: "A menu item",
      submenu: [
        { label: "Submenu item", click: () => alert("I was clicked!") },
        {
          label: "Submenu item #2",
          click: () => alert("I was also clicked!")
        }
      ]
    },
    {
      label: "Another menu item",
      click: () => alert("I was clicked!")
    }
  ];
  return (
    <ContextMenuArea menuItems={menuItems}>
      <div>Right click me to show a context menu!</div>
    </ContextMenuArea>
  );
}
```

React-electron-context menu uses the menu template format from electron, see samples here:  
<https://electronjs.org/docs/api/menu#examples>
