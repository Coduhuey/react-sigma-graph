# react-sigma-graph

A react component that allows simple integration of [sigma.js](http://sigmajs.org/) visualizations. You provide your data defined as an array of nodes and edges, and that's it. This library automatically uses d3 to compute the layout the of the graph. It also integrates several sigma.js plugins, such as [animate](https://github.com/jacomyal/sigma.js/tree/master/plugins/sigma.plugins.animate), [edge labels](https://github.com/jacomyal/sigma.js/tree/master/plugins/sigma.renderers.edgeLabels), and [snapshot](https://github.com/jacomyal/sigma.js/tree/master/plugins/sigma.renderers.snapshot) to allow downloading images of the graph.

## Example Usage

```js
import React, { Component } from 'react';

import Graph from 'react-sigma-graph';

class App extends Component {
  render() {
    var _data = {
      nodes: [
        { id: 'a', category: 'cat', name: 'Garfield' },
        { id: 'b', category: 'dog', name: 'Pluto' }
      ],
      edges: [
        { source: 'a', target: 'b', label: 'friend', type: 'arrow' }
      ]
    };
    return (
      <Graph data={_data}/>
    );
  }
}

export default App;
```

WORK IN PROGRESS
