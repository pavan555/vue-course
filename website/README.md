You can run these examples on https://play.vuejs.org/



### Attribute Bindings
In Vue, mustaches are only used for text interpolation. To bind an attribute to a dynamic value, we use the v-bind directive:

Bind attributes Directive
```vue
<div v-bind:attribute="variable"></div>
```

A directive is a special attribute that starts with the v- prefix. They are part of Vue's template syntax. Similar to text interpolations, directive values are JavaScript expressions that have access to the component's state.

The part after the colon (:id) is the "argument" of the directive. Here, the element's id attribute will be synced with the dynamicId property from the component's state.

> Because v-bind is used so frequently, it has a dedicated shorthand syntax:

```vue
<div :id="dynamicId"></div>
```


Event Directives

Modifiers -> available on event directives after attaching the event with dot notation, like preventing redirection in a hyperlink tag, like below
```vue

<a href="google.com" target="_blank" v-on:click="blockLeave()"> Go to google </a>
<a href="google.com" target="_blank" v-on:click.prevent="blockLeave()"> Go to google </a>
```


```vue
v-on:[dynamic argument here]="method_name" or expression
or @[dynamic_argument]
```


```vue
<script setup>
  import {ref} from 'vue';
  const count = ref(0)
  const event = ref("click")
</script>

<template>
  <h1 v-on:click="count++">Count {{count}}</h1>
  <h1 @[event]="count++">Counter Dynamic {{count}}</h1>
</template>
```

