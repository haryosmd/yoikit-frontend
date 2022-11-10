<script setup>
defineProps({
  // Props here
  placeholder: String,
  id: String,
  type: String,
  name: String,
  forLabel: String,
  labelName: String,
  modelValue: String,
})
defineEmits([ 'update:modelValue' ]) // <-- this is the important part

</script>

<template>
  <div class="mb-4">
    <label class="block mb-1" :for="forLabel">{{ labelName }}</label>
    <input :placeholder="placeholder" :id="id" :type="type" :name="name" :value="modelValue"
      @input="$emit('update:modelValue', $event.target.value)"
      class="block w-full py-3 mt-2 border border-gray-300 rounded-full shadow-sm px-7 focus:border-yellow-300 focus:outline-none focus:ring focus:ring-yellow-200 focus:ring-opacity-50 disabled:bg-gray-100" />
  </div>
</template>