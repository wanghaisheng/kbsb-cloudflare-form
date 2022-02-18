<script setup>
import FormInput from './FormInput.vue';
import FormTextarea from './FormTextarea.vue';
import Button from './Button.vue';
</script>

<template>
  <section class="py-10">
    <form class="flex flex-col items-center bg-gray-100 py-4" action="">
      <FormInput
        id="first_name"
        label="First name"
        :isRequired="true"
        placeholder="Your name"
        pattern="^[a-zA-Z- .,&]*$"
      />
      <FormInput
        id="last_name"
        label="Last name"
        :isRequired="true"
        placeholder="Your family name"
      />
      <FormInput
        id="company"
        label="Company / Organization"
        :isRequired="true"
        placeholder="Your business or employer"
      />
      <FormInput
        id="email"
        label="Email"
        placeholder="Enter your email address"
      />
      <FormInput
        id="phone"
        label="Phone"
        placeholder="Enter your telephone number"
      />
      <FormInput
        type="checkbox"
        label="Yes, I would like to receive the newsletter"
      />
      <FormTextarea label="Message" />
      <Button text="Send" />
    </form>
  </section>
</template>
