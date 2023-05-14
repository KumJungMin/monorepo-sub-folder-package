<template>
  <label class="checkbox">
    <input
      type="checkbox"
      v-model="props.isChecked"
      :disabled="props.isDisabled"
    />
    <span class="checkmark"></span>
    <slot></slot>
  </label>
</template>

<script setup>
import { ref } from "vue";

const props = defineProps({
  isChecked: {
    type: Boolean,
    default: false,
  },
  isDisabled: {
    type: Boolean,
    default: false,
  },
});
</script>
<style scoped>
.checkbox {
  display: inline-block;
  position: relative;
  padding-left: 24px;
  margin-bottom: 8px;
  cursor: pointer;
  font-size: 14px;
}

.checkbox input {
  position: absolute;
  opacity: 0;
  cursor: pointer;
}

.checkmark {
  position: absolute;
  top: 0;
  left: 0;
  height: 16px;
  width: 16px;
  background-color: #f0f0f0;
}

.checkbox input:checked ~ .checkmark {
  background-color: #2196f3;
}

.checkmark:after {
  content: "";
  position: absolute;
  display: none;
}

.checkbox input:checked ~ .checkmark:after {
  display: block;
}

.checkbox .checkmark:after {
  left: 5px;
  top: 1px;
  width: 3px;
  height: 7px;
  border: solid white;
  border-width: 0 2px 2px 0;
  transform: rotate(45deg);
}
</style>
