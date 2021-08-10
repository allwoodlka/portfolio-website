<template>
  <page-title title="About Myself"></page-title>
  <Fieldset legend="Liam Allwood">
    <div class="p-grid">
      <div class="p-md-6 p-sm-12">
        <img alt="user header" src="../assets/myself.png" class="my-image"/>
      </div>
      <div class="p-md-6 p-sm-12">
        <p><b>BSc. majoring in Statistics and minoring in Information Systems.</b></p>
        <p>I'm a recent graduate from the University of Canterbury in Christchurch, New Zealand.</p>
        <p>I've spent a good part of my undergraduate studies using R, SQL, ArcGIS, Excel, Tableau and more to analyse and present data.</p>
        <p>Another passion of mine is designing and creating information systems to capture and process data from the real world. Incorporating good design principals to make the most user-friendly applications</p>
        <p>In addition to my study, I have shorn sheep as a job for 3 summers, I am always looking for ways to capture and analyse data related to my work, hence a lot of my projects featured within this portfolio are related to the shearing and agricultural industry.</p>
        <p>Take a look around, this is my compilation of projects that showcase some of my skills and interests.</p>
      </div>
    </div>

  </Fieldset>
</template>

<script>

import PageTitle from "../components/PageTitle";


export default {
  name: 'Home',
  components: {
    PageTitle,
  }
}
</script>

<style>

</style>
