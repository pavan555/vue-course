You can run these examples on https://play.vuejs.org/



### Attribute Bindings
In Vue, mustaches are only used for text interpolation. To bind an attribute to a dynamic value, we use the v-bind directive:

```vue
<div v-bind:attribute="variable"></div>
```

A directive is a special attribute that starts with the v- prefix. They are part of Vue's template syntax. Similar to text interpolations, directive values are JavaScript expressions that have access to the component's state.

The part after the colon (:id) is the "argument" of the directive. Here, the element's id attribute will be synced with the dynamicId property from the component's state.

> Because v-bind is used so frequently, it has a dedicated shorthand syntax:

```vue
<div :id="dynamicId"></div>
```
