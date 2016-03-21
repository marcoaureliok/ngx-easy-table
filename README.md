# ng2-table

[![NPM](https://nodei.co/npm/ng2-easy-table.png)](https://npmjs.org/package/ng2-easy-table)

Early alpha version. Do not add it to page, it is highly unstable


This table always will be easy to add to every page.
You need to add only `<ng2-table></ng2-table>` to your html page
```html
<div class="row">
    <div class="col-sm-12">
        <ng2-table></ng2-table>
    </div>
</div>
```

Don't forget to add styles:
```
<link rel="stylesheet" href="node_modules/bootstrap/dist/css/bootstrap.min.css">
<link rel="stylesheet" href="node_modules/font-awesome/css/font-awesome.min.css">
```

![table](http://i.imgur.com/ya2Woj3.png "table")

To customize your table add `ConfigService` to the bootstrap :
```
bootstrap(AppComponent, [FiltersService, ConfigService]);
```
and create this service:
```
import {Injectable} from "angular2/core";
@Injectable()
export class ConfigService {
    public searchEnabled = true;
    public orderEnabled = true;
    // etc.
}
```

###Available config settings:

| field    |      type      |  options | example |
|----------|:--------------:|:--------:|---------|
| searchEnabled | bool | true false | public searchEnabled = true; |
| orderEnabled | bool | true false | public orderEnabled = true; |
| resourceUrl | string | | public resourceUrl = "http://beta.json-generator.com/api/json/get/Ey-KcWd6g"; |