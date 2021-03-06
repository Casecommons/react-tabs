# Changelog

### Next Major

#### Breaking Changes

- `activeTabClassName` was renamed to `selectedTabClassName`
- `selectedTabClassName` and `disabledTabClassName` moved from `<TabList />` to `<Tabs />`
- `className` property on all components now overwrites the default classes instead of adding a second class name

```js
// 0.8
<Tabs className="tabs">
    <TabList className="list">
        <Tab className="tab" />
    </TabList>
    <TabPanel className="panel" />
</Tabs>

// Same effect in 1.0
<Tabs className={['tabs', 'ReactTabs']}>
    <TabList className={['list', 'ReactTabs__TabList']}>
        <Tab className={['tab', 'ReactTabs__Tab']} />
    </TabList>
    <TabPanel className={['panel', 'ReactTabs__TabPanel']} />
</Tabs>
```

- `selectedIndex` now enables controlled mode, which disables internal management of the active tab. If you were using `selectedIndex` to set the initial displayed tab use `defaultIndex`
- No styles do get added by default anymore. If you want to use the default styles you need to add them yourself. See README.

#### New Features

- `selectedTabPanelClassName` was added to add `<Tabs />` to change the class name of the current selected TabPanel
- `defaultIndex` was added to set the initial displayed tab
- Add function `resetIdCounter` to reset the id-counter for isomorphic apps.

```js
const reactTabs = require('react-tabs');

...
reactTabs.resetIdCounter();
render();
```

#### Bug Fixes

-

#### Internal

- Refactor components to use native classes
- Refactor to not use react-dom

### 0.8.3 (Apr 19, 2017)

- Fix deprecation warnings with react 15.5

### 0.8.2 (Oct 19, 2016)

- Fix UMD build (#143)

### 0.8.0 (Sep 14, 2016)

- Allow other components inside TabList (#123)

### 0.7.0 (Jul 05, 2016)

- Feature/add custom active and disabled class (#108)
- Remove aria-expanded attribute (#71)
- Fix warning with react 15.2

### 0.6.2 (Jun 24, 2016)

- Fix bower bundling (#111, #112)

### 0.6.1 (Jun 23, 2016)

- Allow setState in onSelect (#51, #110)

### 0.6.0 (Jun 20, 2016)

- Add a cancel option to tab change event handler (#73)
- DOMNode.setAttribute() expects the second param to be string (#75, #76)
- Allow passing through custom attributes (#93)
- Fix nesting of multiple instances of react-tabs (#103)

### 0.5.5 (Jun 13, 2016)

- Fix main exports of react tabs which were broken in 0.5.4

### 0.5.4 (Jun 10, 2016)

- Update to support react 15 (#94)

### 0.5.3 (Feb 01, 2016)

- use correct spelling of aria-labelledby (#67)

### 0.5.2 (Jan 29, 2016)

- Server Side Rendering won't work with default styles (#45)

### 0.5.1 (Oct 22, 2015)

- Removing ReactDOM from bundle

### 0.5.0 (Oct 22, 2015)

- Fix conditional rendering of tabs (#37)
- New configuration to disable styling via jss (#25)
- Avoid white on white Tab labels (#40)
- Support react 0.14 (#43)
- Issue when conditionally rendering Tab/TabPanel (#37)

### 0.4.1 (Sep 09, 2015)

- Do not bundle react into dist (#26)

### 0.4.0 (Aug 18, 2015)

- Support rendering of hidden Tabs (#28)
- Support supplying array of child nodes to Tab (#27)

### 0.3.0 (Aug 11, 2015)

- Support for disabling tabs

### 0.2.1 (Jun 26, 2015)

- Bower support (#22)
- Issue with React being included twice (#23)

### 0.2.0 (Jun 07, 2015)

- Allowing children of Tab to select Tab (#9)
- Only render the selected TabPanel
- Upgrading to React 0.13
- Removing JSX
- Fixing issue with focus management (#7)
- Fixing issue caused by no children being provided (#6)
- Fixing issue that made dynamic Tabs difficult

### 0.1.2 (Jul 23, 2014)

- Making Tab and TabPanel to be stateless
- Throwing Error when Tab count and TabPanel count aren't equal

### 0.1.1 (Jul 19, 2014)

- Fixing warning: Invalid access to component property
- Fixing style weirdness in Firefox

### 0.1.0 (Jul 18, 2014)

- Initial release
