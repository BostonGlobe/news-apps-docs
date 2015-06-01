# Style Guide

## Buttons
To create a button, add the `btn` classn to any `a` or `button` element. This base class must be used alongside an [ordinality](#ordinality) modifier (and must serve as the base for all other modifiers).

##### Ordinality
To indicate the a button represents a primary action, add the `btn--primary` class alongside `btn`. The available classnames are `btn--primary`, `btn--secondary`, and `btn--accent`. Accent buttons provide some extra visual weight over the other two and should be used *sparingly*.
```html
<button class="btn btn--primary">Primary Button</a>
<a href="#" class="btn btn--primary">Primary Button</a>

<button class="btn btn--secondary">Secondary Button</a>
<a href="#" class="btn btn--secondary">Secondary Button</a>

<button class="btn btn--accent">Accent Button</a>
<a href="#" class="btn btn--accent">Accent Button</a>
```

##### Disabled
To indicate that a button is disabled, add the `btn--disabled` class alongside `btn` and an [ordinality](#ordinality) modifier.
```html
<button class="btn btn--primary btn--disabled">Disabled Button</a>
```

##### Disabled
To indicate that a button is disabled, add the `btn--disabled` class alongside `btn` and an [ordinality](#ordinality) modifier.
```html
<button class="btn btn--primary btn--disabled">Disabled Button</a>
```

##### Sizes
To change the size of a button, add the `btn--small` or `btn--large` class alongside `btn` and an [ordinality](#ordinality) modifier. The default size is regular.
```html
<button class="btn btn--primary btn--small">Small Button</button>
<button class="btn btn--primary">Regular Button</button>
<button class="btn btn--primary btn--large">Large Button</button>
```

##### Widths
The width-modifying class changes the button to be relative to the width of its container. To create a button that takes up the full width of its container, add the `btn--full` class alongside `btn` and an [ordinality](#ordinality) modifier. To create a button that takes up half the width of its container, add the `btn--half` class alongside `btn` and an [ordinality](#ordinality) modifier.
```html
<button class="btn btn--primary btn--full">Full-width Button</button>
<button class="btn btn--primary btn--half">Regular Button</button>
<button class="btn btn--primary btn--large">Large Button</button>
```

##### Widths
The width-modifying class changes the button to be relative to the width of its container. To create a button that takes up the full width of its container, add the `btn--full` class alongside `btn` and an [ordinality](#ordinality) modifier. To create a button that takes up half the width of its container, add the `btn--half` class alongside `btn` and an [ordinality](#ordinality) modifier.
```html
<button class="btn btn--primary btn--full">Full-width Button</button>
<button class="btn btn--primary btn--half">Regular Button</button>
<button class="btn btn--primary btn--large">Large Button</button>
```
