<template>
  <div class="">
    <input
      :type="type"
      :id="id"
      :name="id"
      :minlength="minLength"
      :maxlength="maxLength"
      :required="isRequired"
      :placeholder="placeholder"
      :pattern="pattern"
    />
  </div>
</template>

<script>
export default {
  props: {
    id: String,
    type: {
      type: String,
      default: 'text',
      validator(value) {
        // The value must match one of these strings
        return ['text', 'tel', 'email', 'checkbox'].includes(value);
      },
    },
    label: String,
    placeholder: String,
    isRequired: {
      type: Boolean,
      default: false,
    },
    minLength: {
      type: String,
      default: '2',
    },
    maxLength: {
      type: String,
      default: '',
    },
    pattern: String,
  },
};
</script>
