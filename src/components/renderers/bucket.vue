<template>
  <div>
    <component-renderer v-for="field in fields" v-bind:key="field.id" :field="field"/>
  </div>
</template>

<script>
import componentRenderer from "@/components/component-renderer";

export default {
  name: 'bucket',
  components: {
    componentRenderer
  },
  props: {
    fields: {
      type: Array,
      required: false
    }
  }
};
</script>

<style>
div[data-field-type="bucket"] {
  min-height: 50px;
  background-color: green;
}
</style>