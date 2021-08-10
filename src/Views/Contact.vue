<template>
  <page-title title="Get in Touch"></page-title>
  <p>If you want to get in touch with me, fill out this form with your information and I'll receive it in an email shortly after</p>
  <p>Don't forget to include a way for me to contact you back!</p>
  <br />
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
      <span style="color: orangered">Todo: ReCaptcha Here</span>
      <form action="?" method="POST">
        <div class="g-recaptcha" data-sitekey="6Leioe4bAAAAAGAtLiuxpWkt1mgccmO-9knqDt3p"></div>
        <br/>
        <input type="submit" value="Submit">
      </form>
    </div>
    <div class="p-col-6">
      <Button label="Send" icon="pi pi-envelope" iconPos="right" style="max-width: 100%"/>
    </div>
  </div>
</template>

<script>

import PageTitle from "../components/PageTitle";


export default {
  name: 'Contact',
  components: {
    PageTitle,
  }
}
</script>

<style>

</style>
