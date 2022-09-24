---
title: Interactive Menu Icon
tags: Interactivity
expertise: beginner
firstSeen: 2022-09-24T05:02:11+0000
---

Creates a menu icon for any web-page using html and css and very simple java script.

- The container to make the background your desired color
- The class menu to create the menu icon box
- Menu div and menu span create three lines centered at the menu icon
- Menu line-1 moves the line up right 50 pixels
- Menu line-3 moves the line down 40 pixels
- Openmenu line-1, Openmenu line -3, and Openmenu line -2 makes the rotation animations. We made this possible by adding java script in the html ("script")

```HTML
<!DOCTYPE html>
<hmtl>
  <head>
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Interactive Menu Icon</title>
    <link rel="stylesheet" href="style.css" />
  </head>
  <body>
    <div class="container">
      <div class="menu" id="menu">
        <div>
          <span class="line-1"></span>
          <span class="line-2"></span>
          <span class="line-3"></span>
        </div>
      </div>
    </div>
    <script>
      var menu = document.getElementById("menu");

      menu.onclick = function () {
        menu.classList.toggle("openmenu");
      };
    </script>
  </body>
</hmtl>
```

```CSS
* {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}
.container {
  width: 100%;
  height: 100vh;
  background: #1d3c7e;
  display: flex;
  justify-content: center;
  align-items: center;
}
.menu {
  width: 200px;
  height: 200px;
  margin: 8px;
  cursor: pointer;
  border-radius: 5px;
  background-image: linear-gradient(to right, #16f0d3, #1fecdb);
}
.menu div {
  width: 120px;
  height: 120px;
  margin: 40px;
  position: relative;
}
.menu span {
  width: 100px;
  height: 10px;
  background: #fff;
  display: block;
  border-radius: 5px;
  position: absolute;
  left: 50%;
  top: 50%;
  transition: transform 0.5s, width 0.5s;
  transform: translate(-50%, -50%);
}
.menu .line-1 {
  transform: translate(-50%, -50px);
}
.menu .line-3 {
  transform: translate(-50%, 40px);
}
.openmenu .line-1 {
  transform: translate(-50%, -50%) rotate(-45deg);
}
.openmenu .line-3 {
  transform: translate(-50%, -50%) rotate(45deg);
}
.openmenu .line-2 {
  width: 0;
}
```
