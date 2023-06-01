<template>
	<div class="w-full md:w-1/2">
	  <div class="leading-loose max-w-xl m-4 p-7 bg-secondary-light dark:bg-secondary-dark rounded-xl shadow-xl text-left">
		<p class="font-general-medium text-primary-dark dark:text-primary-light text-2xl mb-8">Contact Form</p>
		<form id="contactForm" class="font-general-regular space-y-7" @submit.prevent="submitForm">
    <FormInput label="Full Name" inputIdentifier="name" ref="nameInput" />
    <FormInput label="Email" inputIdentifier="email" inputType="email" ref="emailInput" />
    <FormInput label="Subject" inputIdentifier="subject" ref="subjectInput" />
    <FormTextarea label="Message" textareaIdentifier="message" ref="messageInput" />
  
		  <div>
			<Button
			title="Send Message"
        class="px-4 py-2.5 text-white tracking-wider bg-indigo-500 hover:bg-indigo-600 focus:ring-1 focus:ring-indigo-900 rounded-lg duration-500"
        type="submit"
        aria-label="Send Message"
			/>
		  </div>
		</form>
	  </div>
	</div>
  </template>
  
  <script>
  import Button from '../reusable/Button.vue';
  import FormInput from '../reusable/FormInput.vue';
  import FormTextarea from '../reusable/FormTextarea.vue';
  
  export default {
	components: { Button, FormInput, FormTextarea },
	methods: {
		submitForm() {
      const form = document.getElementById('contactForm');
      const url = 'https://formspree.io/f/mnqykqnj';
      form.setAttribute('action', url);
      form.setAttribute('method', 'POST');

      // Menggunakan this.$refs untuk mengakses nilai input
      const name = this.$refs.nameInput.value;
      const email = this.$refs.emailInput.value;
      const subject = this.$refs.subjectInput.value;
      const message = this.$refs.messageInput.value;

      console.log('Nama:', name);
      console.log('Email:', email);
      console.log('Subject:', subject);
      console.log('Message:', message);

      form.submit();
	  },
	},
  };
  </script>
  
  <style lang="scss" scoped></style>
  