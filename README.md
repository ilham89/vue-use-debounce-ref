# debounce-vue

## Installation

### Using npm

```shell
npm i vue-use-debounce-ref
```

### Using yarn

```shell
yarn add vue-use-debounce-ref
```

## Usage

### Vue

```jsx
<template>
    <div>
        <label>Search</label>
        <input v-model="input" type="text" />
        <div>Value: {{ input }}</div>
  </div>
</template>
<script>
import { watch } from 'vue'
import useDebouncedRef from "vue-use-debounce-ref";
export default {
    setup() {
        const input = useDebouncedRef('', 1000)

        watch(input, newData => {
            console.log({ newData })
             // init an API request
        })
    return {
        input,
    }
  },
}
</script>
```
