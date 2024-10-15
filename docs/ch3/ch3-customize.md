## 3. Customizing Charts
- Titles and legends
- Axis configuration
- Colors and themes
- Tooltips and labels

### 1. Titles and Legends:

- Title Configuration:
```js
title: {
    text: 'Product Sales Analysis',
    subtext: 'Monthly Data Overview',
    left: 'center',
    top: 10,
    textStyle: {
        fontSize: 24,
        fontWeight: 'bold'
    },
    subtextStyle: {
        fontSize: 14
    }
}
```
- Legend Configuration:
```js
legend: {
    data: ['Laptops', 'Smartphones', 'Tablets'],
    orient: 'horizontal',
    bottom: 10,
    textStyle: {
        fontSize: 12
    },
    selectedMode: 'multiple'
}
```

### 2. Axis Configuration:

- X-axis Configuration:
```js
xAxis: {
    type: 'category',
    boundaryGap: false,
    data: ['Jan', 'Feb', 'Mar', ...],
    axisLabel: {
        rotate: 45,
        fontSize: 10
    },
    axisTick: {
        alignWithLabel: true
    },
    axisLine: {
        lineStyle: {
            color: '#5793f3'
        }
    }
}
```
- Y-axis Configuration:
```js
yAxis: {
    type: 'value',
    name: 'Units Sold',
    nameLocation: 'middle',
    nameGap: 50,
    nameTextStyle: {
        fontSize: 14,
        fontWeight: 'bold'
    },
    splitLine: {
        lineStyle: {
            type: 'dashed'
        }
    }
}
```

### 3. Colors and Themes:
- Color Palette:
```js
color: ['#5470c6', '#91cc75', '#fac858']
```

- Series Styling:
```js
areaStyle: {
    opacity: 0.3
}
```

### 4. Tooltips and Labels:
- Tooltip Configuration:
```js
tooltip: {
    trigger: 'axis',
    axisPointer: {
        type: 'cross',
        label: {
            backgroundColor: '#6a7985'
        }
    },
    formatter: function(params) {
        // Custom formatting logic
    }
}
```
- Data Labels:
```js
label: {
    show: true,
    position: 'top',
    formatter: '{c} units'
}
```