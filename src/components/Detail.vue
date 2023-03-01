<template>
  <div class="h-full bg-white">
    <!-- <Label :informations="informations" :skills="skills"/> -->
    <div class="relative float-right h-full bg-white w-8/12">
      <!-- loop background informations -->
      <div class="m-4" v-for="objective in objectives" :key="objective">
        <div class="text-2xl leading-10 font-bold text-blue-900 ml-4">{{ objective.tag }}</div>
        <div class="rounded-lg bg-gray-200">
          <!-- loop contents of background informations -->
          <div class="p-2 text-sm">{{ objective.contents }}</div>
        </div>
      </div>
      <div class="m-4" v-for="background in backgrounds" :key="background">
        <div class="text-2xl leading-10 font-bold text-blue-900 ml-4">{{ background.tag }}</div>
        <div class="rounded-lg bg-gray-200">
          <!-- loop contents of background informations -->
          <div v-for="detail in background.contents" :key="detail" class="p-2 text-sm">
            <div class="font-bold text-yellow-700 inline-block mr-1">{{ detail.name }}</div>
            <div class="font-bold inline-block">{{ detail.info }}</div>
            <div class="font-bold text-blue-400">{{ detail.place }}</div>
            <div v-for="property in detail.details" :key="property">
              <img src="https://img.icons8.com/ios/50/null/checkmark--v1.png" class="h-3 w-3 inline-block"/>
              {{ property.detail }}
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
// import Label from './Label.vue';

export default {
  name: 'Detail',
  components: {
    // Label,
  },
  tag: 'Detail',
  data() {
    return {
      objectives: [
        {
          tag: 'OBJECTIVE',
          contents: 'Expand knowledge about autonomous vehicles. With experience in Mechanical Engineering and Team Management, I aim to become a young Front Project Manager. Completing projects not only in software but also in hardware, meeting customer expectations.',
        },
      ],
      backgrounds: [
        {
          tag: 'EDUCATION',
          contents: [
            {
              name: 'Japanese | ',
              info: 'October 2018 ~ March 2020',
              place: 'Kamimura Gakuen College - Graduated',
              details: [
                {
                  detail: 'Achievement: Excellence Award',
                },
              ],
            },
            {
              name: 'Mechanical Engineering | ',
              info: 'April 2020 ~ March 2024',
              place: 'Toyohashi University of Technology - 3rd year.',
            },
          ],
        },
        {
          tag: 'WORK EXPERIENCE',
          contents: [
            {
              name: 'Quality Controller | ',
              info: ' February 2022 ~ Current',
              place: 'HACHIX Cooperation',
              details: [
                {
                  detail: 'Ensure project quality through GUI testing and Unit Test.',
                },
                {
                  detail: 'Apply automated testing tools',
                },
                {
                  detail: 'Achievement: Predicted the maximum load capacity of the system. Helped minimize the risk of system crashes due to excessive traffic.',
                },
              ],
            },
            {
              name: 'Fresher Developer | ',
              info: 'February 2022 ~ Current',
              place: 'HACHIX Cooperation',
              details: [
                {
                  detail: 'Update features and fix issues for the factory management project.',
                },
                {
                  detail: 'Developed front-end for several projects using Vue.js',
                },
              ],
            },
          ],
        },
        {
          tag: 'PERSONAL PROJECT',
          contents: [
            {
              name: 'Online CV:',
              info: 'https://github.com/kazetut/Online-CV',
            },
            {
              name: 'Knock Knock Arduino:',
              info: 'https://github.com/kazetut/Knock-Knock-Arduino',
            },
            {
              name: 'Line Detection:',
              info: 'https://github.com/kazetut/Line-Detection',
            },
          ],
        },
        {
          tag: 'SOCIAL ACTIVITIES',
          contents: [
            {
              name: 'Vice President, External Relations Leader |',
              info: 'April 2021 ~ March 2022',
              place: 'Viettagse Youth and Student Association in Tokai, Japan (VYSA Tokai)',
              details: [
                {
                  detail: 'Mainly responsible for organizing events for Viettagse people in the Tokai region of Japan. Such as Badminton Tourtagnt, Lunar New Year.',
                },
                {
                  detail: 'Invite guests to collaborate in recording sharing sessions about Startup, Learning, and Living experiences in Japan',
                },
              ],
            },
          ],
        },
      ],
    };
  },
};
</script>
