## React LifeCycles

React is divided into 3 parts
- Mounting
- Updating
- UnMounting

### Mounting Phase
- Constructor
    - since react is still javascript, constructor will still run during the initialization of the component
- Static GetDerivedStateFromProps
    - DO NOT USE. It is a last resort to change state before the render as quoted in the react docs here: https://reactjs.org/docs/react-component.html#static-getderivedstatefromprops
- render
    - returns JSX in order for React to inject into the DOM

### Updating
- Static GetDerivedStateFromProps
    - We still don't use, it's pretty blah, bad news bear
- shouldComponentUpdate
    - This is used in order to compare old props and state with new props and state in order to prevent a unnecessary re-render.
- render
    - Re-renders with the new information
- getSnapshotBeforeUpdate
    - is invoked right before the most recently rendered output is committed to e.g. the DOM. It enables your component to capture some information from the DOM (e.g. scroll position) before it is potentially changed. Any value returned by this lifecycle will be passed as a parameter to componentDidUpdate().
- componentDidUpdate
    - used for things like focusing on a specific form input or doing the effect of scrolling down a window

### Unmounting

- componentWillUnmount
    - This is the only lifecycle event in the unmounting stage, this is used to clean up any events, animations, intervals, etc...
