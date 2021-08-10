<template>
  <page-title title="Get in Touch"></page-title>
  <p>If you want to get in touch with me, fill out this form with your information and I'll receive it in an email shortly after</p>
  <p>Don't forget to include a way for me to contact you back!</p>
  <br />


  <form name="contact" method="POST" data-netlify="true">
    <p>
      <label>Your Name: <input type="text" name="name" /></label>
    </p>
    <p>
      <label>Your Email: <input type="email" name="email" /></label>
    </p>
    <p>
      <label>Your Role: <select name="role[]" multiple>
        <option value="leader">Leader</option>
        <option value="follower">Follower</option>
      </select></label>
    </p>
    <p>
      <label>Message: <textarea name="message"></textarea></label>
    </p>
    <p>
      <button type="submit">Send</button>
    </p>
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
