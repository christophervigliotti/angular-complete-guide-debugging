# 62. Understanding Angular Error Messages

https://www.udemy.com/course/the-complete-guide-to-angular-2/learn/lecture/6656252

## The Error

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

## The Fix

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