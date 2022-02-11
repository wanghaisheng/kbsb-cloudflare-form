<template>
  <div class="">
    <label class="mr-4" for="first_name">First name</label>
    <input
      class="inline-block bg-gray-300 my-2 p-2"
      type="text"
      id="first_name"
      name="first_name"
      minlength="2"
      required
      pattern="^[a-zA-Z- .,&]*$"
      placeholder="First name"
    />
  </div>
</template>

<script></script>
