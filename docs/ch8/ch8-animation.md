## 8. Animation and Transitions
- Enable/disable animations
- Customizing animation effects
- Transition between chart types

### Enabling/Disabling Animations:

- The `animation` option can be set to `true` or `false` to enable or disable animations globally.
- `animationDuration` sets the duration of animations in milliseconds.
- `animationEasing` determines the easing function for animations. ECharts provides various easing functions like 'linear', 'quadraticIn', 'quadraticOut', 'quadraticInOut', 'cubicIn', 'cubicOut', 'cubicInOut', etc.
- `animationThreshold` is useful for performance optimization. It disables animations when the number of elements exceeds the specified threshold.

```js
// 1. Enabling/Disabling Animations
var option = {
    animation: true,  // Enable animations (default)
    animationDuration: 1000,  // Duration of animations in milliseconds
    animationEasing: 'cubicOut',  // Easing function for animations
    animationThreshold: 2000,  // Disable animations when number of elements exceeds this threshold
};
```


### Customizing Animation Effects:

- In this example, we're customizing animations for individual data items in a bar chart.
- `animationDelay` is a function that returns the delay for each data item. Here, each bar starts animating 100ms after the previous one.
- `animationDurationUpdate` is similar, but it's used when updating the chart. Each bar's update animation lasts longer than the previous one.

```js
// 2. Customizing Animation Effects
var option = {
    series: [{
        type: 'bar',
        data: [120, 200, 150, 80, 70, 110, 130],
        animationDelay: function (idx) {
            return idx * 100;
        },
        animationDurationUpdate: function (idx) {
            return idx * 100 + 300;
        }
    }]
};
```


### Transitions Between Chart Types:

- This example shows how to smoothly transition from one chart type to another.
- We start with a bar chart and set some animation options.
- To change to a line chart, we simply change the `type` property and call `setOption()`. ECharts will automatically create a smooth transition between the two chart types.
```js
// 3. Transitions Between Chart Types
var option = {
    series: [{
        type: 'bar',
        data: [120, 200, 150, 80, 70, 110, 130],
        animationDuration: 1500,
        animationEasing: 'elasticOut'
    }]
};

// To change to a line chart:
option.series[0].type = 'line';
myChart.setOption(option);
```