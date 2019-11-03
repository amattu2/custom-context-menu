# Introduction
This is a simple HTML/CSS custom context menu design. I've built a simple JavaScript function to handle building the context menu, but usage is optional. 

# Usage
Included Function
```
createContextMenu(event, parent, options);
```

> event

This accepts the JavaScript click event, and collects the X and Y coordinate to place the context menu

> parent

This accepts the context menu element. [Eg. ocument.getElementById('custom-context-menu')]

> options

This accepts a array of the menu options. See below for an example


A basic option array would be:
```
[{
    icon: "open_in_new", // Material icon 
    text: "Export", // Title displayed next to icon
    action: function() { console.log("Export") } // Action (optional) fires when clicked
}]
```

An advanced option array would be:
```
[{
  icon: "add", // Material icon
  text: "Add", // Title displayed next to icon
  menu: [
    {
      icon: "person",
      text: "Package",
      action: function() { console.log("Add package") }
    },
    {
      icon: "person",
      text: "Part Line"
    },
    {
      icon: "person",
      text: "Part Line"
    }
  ]
}]
```
Providing a array inside the "menu" element builds a submenu (see example)

To include a separator line between elements:
```
  {
    line: "1"
}
```

# Preview
![preview image](https://github.com/amattu2/custom-context-menu/blob/master/demo.jpg)
