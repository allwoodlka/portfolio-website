<template>
  <page-title title="Get in Touch"></page-title>
  <p>If you want to get in touch with me, fill out this form with your information and I'll receive it in an email shortly after</p>
  <p>Don't forget to include a way for me to contact you back!</p>
  <br />

  <form ref="formref" name="contactform" method="POST" id="contactForm" netlify data-netlify-recaptcha="true">
    <input type="hidden" name="form-name" value="contactform" />
    <div class="p-fluid p-formgrid p-grid">
      <div class="p-field p-col-6">
        <label for="name">Name</label>
        <InputText id="name" type="text" v-model="nameVal" />
        <input type="text" name="name" :value="nameVal" class="p-d-none" />
      </div>
      <div class="p-field p-col-6">
        <label for="contact">Preferred Contact</label>
        <InputText id="contact" type="text" v-model="contactVal" />
        <input type="text" name="contact" :value="contactVal" class="p-d-none" />
      </div>
      <div class="p-field p-col-12">
        <label for="message">Message</label>
        <Textarea id="message" rows="4" v-model="messageVal" />
        <textarea name="message" :value="messageVal" class="p-d-none" />
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
  data(){
    return{
      nameVal: null,
      contactVal: null,
      messageVal: null,

    }
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
