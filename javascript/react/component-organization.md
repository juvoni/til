# Component organisation

> From  John Cobb - An opinionated guide to React.js best practices and conventions

```
React.createClass({

        propTypes: {},
        mixins : [],

        getInitialState: function() {},
        getDefaultProps: function() {},

        componentWillMount : function() {},
        componentWillReceiveProps: function() {},
        componentWillUnmount : function() {},

        _parseData : function() {},
        _onSelect : function() {},

        render : function() {}

    })
```

I like to declare ``propTypes`` at the top of my component as they are a useful guide to a components expected usage (see section below for more on this), followed by the ``mixins`` because it is handy to initially know exactly what external behaviours the component is using/dependent on.

I choose to split the life-cycle methods into those that occur before an instance of the component is created (e.g. ``getInitialState``, ``getDefaultProps``) and those which occur during the mounting/updating/mounted cycle (e.g. ``componentWillMount``, ``shouldComponentUpdate``). Furthermore, I find that declaring the lifecycle methods in order of execution also makes the component easier to reason about.

I always have my custom methods follow the lifecycle methods and be prefixed with an underscore to make them easier to identify. I’ll usually also group these by utility (parsers, event handlers, etc).

I like the ``render`` method to always be last. The ``render`` method is a mandatory lifecycle method and it’s almost always the function I need to find first when I open a file. Consequently, it’s pragmatic to have it in a consistent location across all of my components.

In general, my mixins will follow the same conventions as regular components.


[Source](https://web-design-weekly.com/2015/01/29/opinionated-guide-react-js-best-practices-conventions/)
