<template>
<FirstComponent v-bind:weather = "weather"/>

</template>

<script>
import FirstComponent from './components/myComponent.vue';

export default{
  name:'app',
  components:{
    FirstComponent
  },
  data: () => ({
    weather:{
      temperatureReal: 1,
      temperatureFeel: '-3.2',
      humidity: 6,
      wind: 20
    }
  })  
}
</script>



