<script setup>
import FormInput from './FormInput.vue';
import FormTextarea from './FormTextarea.vue';
import FormResponse from './FormResponse.vue';
import Button from './Button.vue';
</script>

<template>
  <section class="py-10">
    <form class="flex flex-col items-center bg-gray-100 py-4" action="">
      <FormInput
        id="first_name"
        label="First name"
        placeholder="Your name"
        pattern="^[a-zA-Z- .,&]*$"
        :isRequired="true"
      />
      <FormInput
        id="last_name"
        label="Last name"
        placeholder="Your family name"
        pattern="^[a-zA-Z- .,&]*$"
        :isRequired="true"
      />
      <FormInput
        id="company"
        label="Company / Organization"
        placeholder="Your business or employer"
        pattern="^[0-9a-zA-Z- .,&+!?()@#*$%]*$"
        :isRequired="true"
      />
      <FormInput
        id="email"
        type="email"
        label="Email"
        placeholder="Enter your email address"
        pattern="^[a-zA-Z0-9-._%#*+&]{1,}@{1}[a-zA-Z0-9-._]{1,}[.]{1,}[a-zA-Z0-9]{1,}$"
        :isRequired="true"
      />
      <FormInput
        id="phone"
        type="tel"
        label="Phone"
        placeholder="Enter your telephone number"
        pattern="^[0-9()+ -]*$"
      />
      <FormTextarea
        id="message"
        label="Message"
        placeholder="Type your message..."
      />
      <FormInput
        id="newsletter"
        type="checkbox"
        label="Yes, I would like to stay updated"
      />
      <Button text="Send" />
    </form>
    <FormResponse />
  </section>
</template>
