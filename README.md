# uxcore-tooltip

---

## TL;DR

tooltip ui component for react

#### setup develop environment

```sh
$ git clone https://github.com/uxcore/uxcore-tooltip
$ cd uxcore-tooltip
$ npm install
$ gulp server
```

## Usage

```js
import Tooltip from 'uxcore-tooltip';

ReactDOM.render(
	<Tooltip
		placement="top"
		trigger="hover"
		overlay={title}
		<span>tooltip</span>
	</Tooltip>, document.getElementById('target'));
```

### demo
http://uxcore.github.io/uxcore/components/tooltip/

## API

### props

|参数|类型|默认值|说明|
|---|----|---|------|
|overlayClassName | string | uxcore | additional className added to popup overlay |
|trigger | string[] | ['hover'] | which actions cause tooltip shown. enum of 'hover','click','focus' |
|mouseEnterDelay | number | 0 | delay time to show when mouse enter.unit: s. |
|mouseLeaveDelay | number | 0.1 | delay time to hide when mouse leave.unit: s. |
|overlayStyle | Object |  | additional style of overlay node |
|wrapStyle | Object |  | additional style of wrap node |
|prefixCls | String | kuma-tooltip | prefix class name |
|onVisibleChange | Function |  | call when visible is changed |
|visible | boolean |  | whether tooltip is visible |
|defaultVisible | boolean |  | whether tooltip is visible initially |
|placement | String|Object |  | one of ['left','right','top','bottom', 'topLeft', 'topRight', 'bottomLeft', | 'bottomRight'] or alignConfig of [dom-align](https://github.com/yiminghe/dom-align)
|align | Object: alignConfig of [dom-align](https://github.com/yiminghe/dom-align) |  | only valid when placement's type | is String. value will be merged into placement's align config. note: can only accept offset and targetOffset
|overlay | React.Element |  | popup content |
|getTooltipContainer | function |  | function returning html node which will act as tooltip contaier |
