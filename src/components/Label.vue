<template>
  <div class="relative w-4/12 inline-block mt-20 mb-20" >
    <!-- add-in picture and some contents -->
    <div class="h-95">
      <img src="./picture.png" class="mx-auto mt-4 w-8/12">
      <div class="text-center m-4 text-xl leading-7 font-bold text-blue-900" >NGUYEN HAI PHONG</div>
    </div>
    <!-- Loop the personal information -->
    <div class="ml-4">
      <div v-for="information in informations" :key="information">
        <img :src="`${information.picLinks}`" class="h-5 w-5 inline-block mr-1">
        <div class="inline-block">
          {{ information.values }}
        </div>
      </div>
    </div>
    <!-- Loop the details information -->
    <div class="ml-4">
      <div class="mt-3" v-for="detail in details" :key="detail">
        <div class="ml-4 text-xl leading-10 font-bold text-blue-900">{{ detail.values }}</div>
        <div class="leading-normal text-sm" v-for="detail in detail.contents"
        :key="detail">
          <img src="https://img.icons8.com/material-two-tone/24/000000/double-right.png" class="h-3 w-3 inline-block"/> {{ detail.content_name }}</div>
      </div>
    </div>
  </div>
</template>

<script>

export default {
  name: 'Label',
  data() {
    return {
      informations: [
        {
          picLinks: 'https://img.icons8.com/ios/50/000000/calendar--v1.png',
          values: '02/12/1999',
        },
        {
          picLinks: 'https://img.icons8.com/external-flatart-icons-outline-flatarticons/50/000000/external-male-basic-ui-elements-flatart-icons-outline-flatarticons.png',
          values: 'Male',
        },
        {
          picLinks: 'https://img.icons8.com/ios/50/000000/apple-phone.png',
          values: '(+81)70-2362-1575',
        },
        {
          picLinks: 'https://img.icons8.com/ios/50/000000/email-open.png',
          values: 'nguyen.hai.phong.uv@tut.jp',
        },
        {
          picLinks: 'https://img.icons8.com/wired/64/000000/home.png',
          values: 'Toyohashi University of Technology, 1-1 Hibarigaoka, Tenpaku town, Toyohashi city, Aichi prefecture',
        },
      ],
      details: [
        {
          values: 'PROGRAMING SKILLS',
          contents: [
            {
              content_name: 'Python',
            },
            {
              content_name: 'Javascript',
            },
            {
              content_name: 'C++',
            },
            {
              content_name: 'Vuejs',
            },
            {
              content_name: 'Nodejs',
            },
            {
              content_name: 'Robot Operating System (ROS)',
            },
          ],
        },
        {
          values: 'OTHER SKILLS',
          contents: [
            {
              content_name: '2D Drawing: AutoCAD',
            },
            {
              content_name: '3D Drawing: Solid Work, Fusion360',
            },
          ],
        },
        {
          values: 'CERTIFICATES',
          contents: [
            {
              content_name: 'JLPT: N1',
            },
            {
              content_name: 'TOEIC L&R: 715',
            },
            {
              content_name: 'Paiza: rank B',
            },
            {
              content_name: 'Codelearn: C++ Advanced',
            },
          ],
        },
      ],
    };
  },
};
</script>
