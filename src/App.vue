<template>
  <div class="absolute bg-gray-200">
    <div class="relative mx-auto h-full w-6/12 bg-white">
      <Detail :backgrounds="backgrounds"/>
      <Label :informations="informations" :skills="skills"/>
    </div>
  </div>
</template>

<script>
import Detail from './components/Detail.vue';
import Label from './components/Label.vue';

export default {
  name: 'App',
  components: {
    Detail,
    Label,
  },
};
</script>
