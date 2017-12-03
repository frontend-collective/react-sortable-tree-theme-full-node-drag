# React Sortable Tree Full Node Drag Theme
<img alt="theme appearance" src="https://user-images.githubusercontent.com/4413963/33521792-61dc2c50-d81f-11e7-8ab1-359661a11ca4.png" width="500">

## Features
* No drag handles. You can click anywhere on a node to drag it.

## Usage

```sh
npm install --save react-sortable-tree-theme-full-node-drag
```

```jsx
import React, { Component } from 'react';
import SortableTree from 'react-sortable-tree';
import FileExplorerTheme from 'react-sortable-tree-theme-full-node-drag';

export default class Tree extends Component {
  constructor(props) {
    super(props);

    this.state = {
      treeData: [{ title: 'src/', children: [ { title: 'index.js' } ] }],
    };
  }

  render() {
    return (
      <div style={{ height: 400 }}>
        <SortableTree
          treeData={this.state.treeData}
          onChange={treeData => this.setState({ treeData })}
          theme={FileExplorerTheme}
        />
      </div>
    );
  }
}
```
