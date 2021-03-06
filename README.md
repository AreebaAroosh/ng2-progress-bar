# ngx-progress-bar

Simple progress bar control for your angular2 applications using bootstrap3. Does not depend of jquery. 
If you don't want to use it without bootstrap - simply create proper css classes. 
Please star a project if you liked it, or create an issue if you have problems with it.

## Installation

1. Install npm module:
    
    `npm install ngx-progress-bar --save`

2. If you are using system.js you may want to add this into `map` and `package` config:

    ```json
    {
        "map": {
            "ngx-progress-bar": "node_modules/ngx-progress-bar"
        },
        "packages": {
            "ngx-progress-bar": { "main": "index.js", "defaultExtension": "js" }
        }
    }
    ```
## Usage

```typescript
<progress-bar [value]="50" [max]="100" title="Text to be put in the progress bar"></progress-bar>
```

* `value` is a progress number
* `max` is a maximal number of the progress. By default is 100.
* `title` is a text that will be shown in the progress bar. This is optional.

## Sample

```typescript
import {Component} from "@angular/core";
import {ProgressBarModule} from "ngx-progress-bar";

@Component({
    selector: "app",
    template: `
    <div class="container">
        <progress-bar [value]="50" [max]="100"></progress-bar>
    </div>
    `
})
export class App {

}

@NgModule({
    imports: [
        // ...
        ProgressBarModule
    ],
    declarations: [
        App
    ],
    bootstrap: [
        App
    ]
})
export class AppModule {

}
```

Take a look on samples in [./sample](https://github.com/pleerock/ngx-progress-bar/tree/master/sample) for more examples of
usages.
