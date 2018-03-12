# Web-Interface-Library
A typescript and SCSS based web interface library. Allows easy creation of web pages dynamically on runtime.

### Creating a div element and adding it to the page.
```javascript
let myDiv = Interface.Create({type: 'div'});
document.body.appendChild(myDiv);
```

### Creating an example page header with tabs and adding it to the page.
```javascript
let aboutTab = null;
let blogTab = null;
let myHeader = Interface.Create({type: 'div', className: 'Header', elements: [
  //Create the title bar
  {type: 'div', className: 'TitleBar', text: 'Welcome to my page'},
  //Create the tab bar
  {type: 'div', className: 'TabBar', elements: [
      //Create the items in the tab bar
      aboutTab = Interface.Create({type: 'div', className: 'AboutTab', text: 'About', onClick: this.aboutClicked}),
      blogTab = Interface.Create({type: 'div', className: 'BlogTab', text: 'Blog', onClick: this.blogClicked}),
  ]}
]});
//Add to page
document.body.appendChild(myHeader);
```
