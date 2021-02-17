# Overview

Generally handling state in an app is hard. The `useQuery` attempts to make things easier.

### Example

```vue

<template>
  <div>
   
  </div>
</template>

<script>
import { useQuery } from 'vue-query';

export default {
  name: 'SomeComponent',

  setup() {
    const {
      data: people,
      isIdle,
      isError,
      isSuccess,
      isLoading,
    } = useQuery('star-wars-people', () => fetch('https://swapi.dev/api/people').then(response => response.json()));

    return {
      people,
      isIdle,
      isError,
      isLoading,
      isSuccess,
    }
  }
}
</script>
```
