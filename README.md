**THE PROJECT IS UNDER DEVELOPMET**

# Grafana icon

## Abstract

The module gives a way to render and edit icons in your Grafana pluging.
It is distributed via AngularJS directives.

### Icon
Directive for showing icon on your page. 
It adds div with customizable:
* height
* width
* icon
* icon size
* icon color
* visibility


Icon would try to scale to parent block.

Icon size is given as % of div height. If icon is too wide - it would scale to fit div.
### Icon editor
Directive for editing icon content.
### Icon size editor 
Directive for editing icon size.

## Usage

### Installation
### Usage from client code
#### Directives registering
In your *module.js*
```javascript
import { iconDirective } from './icon/directives/icon';
import { editorIconDirective } from './icon/directives/editor-icon';
import { editorIconSizeDirective } from './icon/directives/editor-icon-size';

angular.module('grafana.directives').directive('icon', iconDirective);
angular.module('grafana.directives').directive('iconEditor', editorIconDirective);
angular.module('grafana.directives').directive('iconSizeEditor', editorIconSizeDirective);
```
#### Using
In your html
```html
<icon
  class="icon"
  width="ctrl.panelWidth"
  height="ctrl.panelHeight"
  content="ctrl.iconContent"
  size="ctrl.iconSize"
  color="ctrl.iconColor"
  visible="ctrl.iconVisible"
/>
```
Icon will be updated each time any of arguments updates.
## Changelog


## Other 

* [Project proposal](https://github.com/CorpGlory/grafana-icon/blob/master/proposal.md)
