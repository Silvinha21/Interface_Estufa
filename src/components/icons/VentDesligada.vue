<template>
  <svg-icon type="mdi" :path="path"></svg-icon>
</template>

<script>
import SvgIcon from '@jamescoyle/vue-icon';
import { mdiFanOff } from '@mdi/js';

export default {
  name: "my-component",
  components: {
    SvgIcon
  },
  data() {
    return {
       path: mdiFanOff,
    }
  }
}
</script>