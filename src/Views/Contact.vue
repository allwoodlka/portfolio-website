<template>
  <page-title title="Get in Touch"></page-title>
  <p>If you want to get in touch with me, fill out this form with your information and I'll receive it in an email shortly after</p>
  <p>Don't forget to include a way for me to contact you back!</p>
  <br />

  <form name="ask-question"
        method="post" netlify netlify-honeypot="bot-field">
    <input type="text" name="name" />
    <input type="radio" name="panelist" />
    <textarea name="question"></textarea>
    <button type="submit">Send</button>
  </form>



  <form ref="formref" name="contact" method="POST" data-netlify-recaptcha="true" data-netlify="true">
    <div class="p-fluid p-formgrid p-grid">
      <div class="p-field p-col-6">
        <label for="name">Name</label>
        <InputText id="name" type="text" />
      </div>
      <div class="p-field p-col-6">
        <label for="contact">Preferred Contact</label>
        <InputText id="contact" type="text" />
      </div>
      <div class="p-field p-col-12">
        <label for="message">Message</label>
        <Textarea id="message" rows="4" />
      </div>
      <div class="p-col-6">
        <div data-netlify-recaptcha="true"></div>
      </div>
      <div class="p-col-6">
        <Button @click="submitForm" label="Send" icon="pi pi-envelope" iconPos="right" style="max-width: 100%"/>
      </div>
    </div>
  </form>
</template>

<script>

import PageTitle from "../components/PageTitle";


export default {
  name: 'Contact',
  components: {
    PageTitle,
  },
  methods: {
    submitForm(){
      this.$refs.formref.submit();
    }
  }
}
</script>

<style>

</style>
