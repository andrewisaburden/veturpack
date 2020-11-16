<template>
    <div>
      Test
    </div>
</template>
<script lang="ts">
import Vue from 'vue';
import {
    Component,
    Prop,
    PropSync,
} from 'vue-property-decorator';

@Component({})
export default class Child extends Vue {
    @Prop({ required: true, type: String }) readonly foo!: string;

    @PropSync('foo', { type: String }) fooLocal: string;
}
</script>
