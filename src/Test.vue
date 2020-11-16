<template>
  <child
      :foo.sync="foo"
  >
  </child>
</template>

<script lang="ts">
import {
    Component,
    Vue,
} from 'vue-property-decorator';
import Child from './Child.vue';

@Component({
    components: {
        Child,
    },
})
export default class Parent extends Vue {
  foo = 'hi';
}
</script>

