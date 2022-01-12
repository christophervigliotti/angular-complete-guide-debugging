# Section 2: Debugging

*This is one of several repos that I created for the course "Angular - The Complete Guide (2022 Edition)".  For a complete list of repos created for this course: https://gist.github.com/christophervigliotti/92e5b3b93cbe9d630d8e9d81b7eb6636 .*

## 63. Debugging Code in the Browser Using Sourcemaps

https://www.udemy.com/course/the-complete-guide-to-angular-2/learn/lecture/6656260


### The Error

No error...but last server cnanot be deleted

### The Solution

change `const position = id + 1;` to `const position = id;`

## 62. Understanding Angular Error Messages

https://www.udemy.com/course/the-complete-guide-to-angular-2/learn/lecture/6656252

### The Error

when clicking the Add Server button

```
core.js:6210 ERROR TypeError: Cannot read properties of undefined (reading 'push')
    at AppComponent.push.Sy1n.AppComponent.onAddServer (app.component.ts:12)
    at AppComponent_Template_button_click_5_listener (template.html:5)
    at executeListenerWithErrorHandling (core.js:15279)
    at wrapListenerIn_markDirtyAndPreventDefault (core.js:15317)
    at HTMLButtonElement.<anonymous> (dom_renderer.ts:66)
    at ZoneDelegate.invokeTask (zone.js:421)
    at Object.onInvokeTask (core.js:28578)
    at ZoneDelegate.invokeTask (zone.js:420)
    at Zone.runTask (zone.js:188)
    at ZoneTask.invokeTask [as invoke] (zone.js:503)
```

### The Solution

changed this...

```
export class AppComponent {
  servers;
```

...to this...

```
export class AppComponent {
  servers = [];
```
