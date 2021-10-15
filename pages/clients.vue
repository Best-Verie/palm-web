<template>
  <div>
    <a-row>
      <a-col :md="12" :lg="12" :xl="12">
        <div class="client-img">
          <img :src="require('../static/client.png')"/>
        </div>
      </a-col>
      <a-col :md="12" :lg="12" :xl="12" class="client-desc">
        <h3>What our clients say!</h3>
        <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Vitae magnam culpa tempora? Eligendi ab esse maiores architecto consequatur maxime magni, reiciendis vel perferendis, delectus corporis, dolor dicta quidem enim sed.</p>
        <!-- <a-button class="indicators">
          <a-row>
          <a-col :md="12" :lg="6" :xl="6">
            <a-icon type="left" />
          </a-col>
          <a-col :md="12" :lg="6" :xl="6">
          <a-icon type="right" />
          </a-col>
          </a-row>
        </a-button> -->
      </a-col>
    </a-row>
  </div>
</template>

<script>
export default {
  name: "Clients",
};
</script>

<style scoped>
.client-img{
  background-color: #EDF5FB ;
  padding: 0.2em;
  width: 30em;
  /* opacity: ; */
 } 
.client-img img{
  width: 20em;
  margin-left: 3em;
}
.client-desc p{
  margin-top: 4em;
  width: 30em;
}
.client-desc h3{
  font-weight: bold;
}
.indicators a-icon{
  padding: 15px;
}
</style>
