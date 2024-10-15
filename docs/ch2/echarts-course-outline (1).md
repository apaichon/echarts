# ECharts.js Course Outline

[Previous sections remain unchanged]

## 2. Basic Concepts

### 2.1 Chart Types Overview
- Introduction to common chart types supported by ECharts:
  1. Line Charts: For showing trends over time
  2. Bar Charts: For comparing quantities across categories
  3. Pie Charts: For showing composition or proportion
  4. Scatter Charts: For showing distribution or correlation
  5. Candlestick Charts: For financial data
  6. Radar Charts: For multivariate data on a two-dimensional chart
  7. Treemap: For hierarchical data
  8. Sunburst: For hierarchical data with a radial layout
  9. Heatmap: For visualizing data through color variations
  10. Graph: For relationship networks
- Brief explanation of when to use each chart type
- Introduction to more advanced chart types (to be covered in detail later)

### 2.2 ECharts DOM Element
- Explanation of the role of the DOM element in ECharts
- How to prepare an HTML element for ECharts:
  ```html
  <div id="main" style="width: 600px;height:400px;"></div>
  ```
- Importance of setting dimensions for the container element
- Considerations for responsive design (detailed coverage in a later section)

### 2.3 ECharts Instance
- Detailed explanation of what an ECharts instance represents
- How to create an ECharts instance:
  ```javascript
  var myChart = echarts.init(document.getElementById('main'));
  ```
- Options for the `init` method:
  - DOM element
  - Theme (optional)
  - Device pixel ratio (optional)
- Key methods of an ECharts instance:
  - `setOption(option)`: Setting chart configuration
  - `getOption()`: Getting current configuration
  - `resize()`: Resizing the chart
  - `dispatchAction()`: Triggering chart actions programmatically
  - `on()` / `off()`: Event handling

### 2.4 Basic Configuration Structure
- Overview of the ECharts option object structure
- Key components of the configuration:
  1. Title: `title: {}`
  2. Legend: `legend: {}`
  3. Tooltip: `tooltip: {}`
  4. Axis (for Cartesian charts): `xAxis: {}`, `yAxis: {}`
  5. Series: `series: []`
- Example of a basic configuration:
  ```javascript
  var option = {
    title: { text: 'My First Chart' },
    tooltip: {},
    legend: { data: ['Sales'] },
    xAxis: { data: ["shirt","cardigan","chiffon","pants","heels","socks"] },
    yAxis: {},
    series: [{
      name: 'Sales',
      type: 'bar',
      data: [5, 20, 36, 10, 10, 20]
    }]
  };
  ```
- Explanation of how these components work together

### 2.5 Series and Data Formats
- Detailed explanation of the `series` configuration
- Different types of series (corresponding to chart types)
- Data formats for different series types:
  1. Simple array format: `[value1, value2, ...]`
  2. Object array format: `[{name: 'A', value: 10}, ...]`
  3. Two-dimensional array: `[[x1, y1], [x2, y2], ...]`
- Introduction to the `dataset` component for more flexible data handling:
  ```javascript
  dataset: {
    source: [
      ['product', '2015', '2016', '2017'],
      ['Matcha Latte', 43.3, 85.8, 93.7],
      ['Milk Tea', 83.1, 73.4, 55.1],
      ['Cheese Cocoa', 86.4, 65.2, 82.5],
      ['Walnut Brownie', 72.4, 53.9, 39.1]
    ]
  }
  ```
- Explanation of how to reference dataset in series configuration

This expanded "Basic Concepts" section provides a comprehensive introduction to the fundamental elements of working with ECharts. It covers the essential knowledge needed to start creating charts, from understanding different chart types to configuring data and options. This foundation will prepare learners for more advanced topics in subsequent sections of the course.

[Subsequent sections of the course outline remain unchanged]
