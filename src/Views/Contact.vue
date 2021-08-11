<template>
  <page-title title="Get in Touch"></page-title>
  <p>If you want to get in touch with me, fill out this form with your information and I'll receive it in an email shortly after</p>
  <p>Don't forget to include a way for me to contact you back!</p>
  <br />

  <form ref="formref" name="contactform" method="POST" id="contactForm" netlify netlify-honeypot="liam">
    <input type="hidden" name="form-name" value="contactform" />
    <div class="p-fluid p-formgrid p-grid">
      <div class="p-field p-col-6">
        <label for="name">Name</label>
        <InputText id="name" type="text" v-model="nameVal" :class="nameClass" />
        <input type="text" name="name" :value="nameVal" class="p-d-none" />
        <span style="color: orangered" v-if="nameErrorMessage">{{ nameErrorMessage }}</span>
      </div>
      <div class="p-field p-col-6">
        <label for="contact">Preferred Contact</label>
        <InputText id="contact" type="text" v-model="contactVal" :class="contactClass" />
        <input type="text" name="contact" :value="contactVal" class="p-d-none" />
        <span style="color: orangered" v-if="contactErrorMessage">{{ contactErrorMessage }}</span>
      </div>
      <div class="p-field p-col-12">
        <label for="message">Message</label>
        <Textarea id="message" rows="6" v-model="messageVal" :class="messageClass" style="resize: vertical"/>
        <textarea name="message" :value="messageVal" class="p-d-none"/>
        <span style="color: orangered" v-if="messageErrorMessage">{{ messageErrorMessage }}</span>
      </div>
      <div class="p-col-6">
        <input name="liam" class="p-d-none" />
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
      nameVal: "",
      nameClass: "",
      nameErrorMessage: false,
      contactVal: "",
      contactClass: "",
      contactErrorMessage: false,
      messageVal: "",
      messageClass: "",
      messageErrorMessage: false,
    }
  },
  methods: {
    submitForm(){
      if(this.validateForm()){
        this.$refs.formref.submit();
      }
    },
    validateForm(){
      if(this.nameVal.length < 3){
        this.nameClass = "p-invalid";
        this.nameErrorMessage = "Name is too short.";
      }else{
        this.nameClass = "";
        this.nameErrorMessage = false;
      }
      if(this.contactVal.length < 6){
        this.contactClass = "p-invalid";
        this.contactErrorMessage = "Contact method too short.";
      }else{
        this.contactClass = "";
        this.contactErrorMessage = false;
      }
      if(this.messageVal.length < 10){
        this.messageClass = "p-invalid";
        this.messageErrorMessage = "Message too short.";
      }else{
        this.messageClass = "";
        this.messageErrorMessage = false;
      }
      if(this.messageErrorMessage || this.contactErrorMessage || this.nameErrorMessage){
        return false;
      }else{
        return true;
      }
    }
  }
}
</script>

<style>
</style>
