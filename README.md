# Overview
The picker component based on vue.js

# Install

```Bash
npm install vue-3d-picker --save
```

```JavaScript
import Picker from 'picker';
```

# Base Usage
```HTML
<picker v-model="visible" :data-items="items" @change="onValuesChange">
	<div class="top-content" slot="top-content">Top of the content.</div>
	<div class="bottom-content" slot="bottom-content">Bottom of the content.</div>
</picker>
```

```JavaScript
export default {
  methods: {
    onValuesChange(result, pickerEl, reset) {
      let year = result[0], month = result[1];
      // result -> The selected data
      // pickerEl -> DOM ?
      // reset -> Reset the data on the picker component ?
    }
  },

  data() {
    return {
      visible: true,
      items: [
        {
          values: ['2000', '2001', '2002', '2003', '2004', '2005', '2006', '2007'],
        }, {
          values: ['1', '2', '3', '4', '5', '6', '7', '8', '9', '10', '11', '12'],
        }
      ]
    }
  }
}
```

# Options

Picker Options:

| Option | Description |
| ----- | ----- |
| v-model | Boolean(default: false) Picker show and hide. |
| :data-items | Array(default: []) The configuration on the items. |
| @change | Function() Listening when data changes. |


Picker Items Options:

| Option | Description |
| ----- | ----- |
| index | item default index position. |
| values | values of this item. |
| width | The width of the item. The unit is %.|




