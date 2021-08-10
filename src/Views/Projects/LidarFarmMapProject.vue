<template>
  <page-title title="Processing Opensource Lidar Data into High Quality Farm Maps"></page-title>
  <div class="p-grid">
    <div class="p-d-lg-none p-col-3"></div>
    <div class="p-col-6">
      <img alt="Lidar Farm Map" src="../../assets/map.png" style="max-width:100%" class="p-shadow-3">
    </div>
    <div class="p-d-lg-none p-col-3"></div>
    <div class="p-lg-6 p-sm-12">
      <Fieldset legend="About This Project">
        <p>While working on a large farm in Banks Peninsula, I was tasked with spraying gorse in hard to reach places. Because of the sheer size of this farm, navigating to and tracking areas that had been sprayed already was a challenge for a contractor like myself.</p>
        <p>There were existing maps of this farm, along with rough boundary lines, but they were low quality and the boundaries were fairly inaccurate.</p>
        <p>I decided to improve the quality of these maps using high resolution <InformationalText content="Lidar" overlayContent="Lidar is a remote sensing method used to make 3D representations of areas on the earth's surface. It works by firing a laser at many points on the terrain and calculating the distance to each point from the return time of the lasers reflection. The resulting dara is a 3D point-cloud of the terrain."/> data of the area.</p>
        <br />
      </Fieldset>
    </div>
    <div class="p-col-12">
      <Panel header="Sourcing Data">
        <p>A decent portion of New Zealand has been mapped using high resolution Lidar (~6 elevation points / square metre) and the information is openly available online. I found the data I needed for this project via <a href="https://www.linz.govt.nz/data/linz-data/elevation-data" target="_blank">Land Information New Zealand</a>.</p>
      </Panel>
      <Panel header="Processing the Data">
        <p>Lidar data are actually a collection points in 3D space. When viewing millions of points at once the result is a pseudo 3 dimensional surface.</p>
        <video controls style="max-width: 100%" autoplay muted loop>
          <source src="../../assets/3dLidarScreencapture.webm" type="video/webm">
          <p>Your browser does not support video</p>
        </video>
        <p>To transform this data into a 2D surface, I made use of <a href="https://www.opentopography.org/" target="_blank">Open Topography's</a> free tools to render the Lidar data as a 2D surface. Ideal for our map.</p>
        <img alt="2D Render of Lidar Data" src="../../assets/lidar-farm-map-project/lidar-2d-render.png" style="max-width:100%" class="p-shadow-3">
      </Panel>
      <Panel header="Adding Map Features">
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.
          Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.
          Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat
          cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</p>
      </Panel>
      <Panel header="Comparison">
        <div class="p-grid">
          <div class="p-col-6">
            <img alt="Lidar Farm Map" src="../../assets/lidar-farm-map-before.png" style="max-width: 100%" class="p-shadow-2">
          </div>
          <div class="p-col-6">
            <img alt="Lidar Farm Map" src="../../assets/lidar-farm-map-after.png" style="max-width: 100%" class="p-shadow-2">
          </div>
        </div>
      </Panel>
      <Panel header="Using The Map">
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.
          Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.
          Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat
          cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</p>
      </Panel>
    </div>
  </div>

</template>

<script>

import PageTitle from "../../components/PageTitle";
import InformationalText from "../../components/InformationalText";


export default {
  name: 'Home',
  components: {
    PageTitle,
    InformationalText
  },
  mounted() {
    window.scrollTo({top: 0, behavior: 'smooth'}); // Scroll to top as SPA keeps scroll history on page-change
  },
  data(){
    return{

    }
  }
}
</script>

<style>

</style>
