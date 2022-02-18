<script setup>
import FormInput from './FormInput.vue';
import FormTextarea from './FormTextarea.vue';
import FormResponse from './FormResponse.vue';
import Button from './Button.vue';

function submitForm() {
  console.log('Submitted');
  // Todo: refactor submit, remove form action
  // https://kbsb-cloudflare-form-worker.kaboom.workers.dev
  // @submit.prevent="submitForm"
}
</script>

<script>
export default {
  mounted() {
    const captcha = document.createElement('script');
    captcha.setAttribute('src', 'https://js.hcaptcha.com/1/api.js');
    document.head.appendChild(captcha);
  },
};
</script>

<template>
  <section class="py-10">
    <form
      class="flex flex-col items-center bg-gray-100 py-4"
      action="https://kbsb-cloudflare-form-worker.kaboom.workers.dev"
      method="POST"
    >
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
        id="newsletter"
        type="checkbox"
        label="Yes, I would like to stay updated"
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
      <div
        class="h-captcha"
        data-sitekey="d34868ed-69b1-4794-9516-5e3f0f802bd0"
      ></div>
      <Button type="submit" text="Send" />
      <div>
        This site is protected by
        <a href="https://www.hCaptcha.com">hCaptcha</a> and its
        <a href="https://www.hcaptcha.com/privacy">Privacy Policy</a> and
        <a href="https://www.hcaptcha.com/terms">Terms of Service</a> apply.
      </div>
    </form>
    <FormResponse />
  </section>
</template>
