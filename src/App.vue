<template>
  <div class="app">
    <JobList :jobs="jobs" />
  </div>
</template>

<script lang="ts">
import { defineComponent, reactive, toRefs, ref } from 'vue';
import JobList from './components/JobsList.vue'
import Job from './types/Job'

export default defineComponent({
  name: 'App',
  components: {JobList},
  setup() {

    // reactive way
    // const state = reactive({
    //   name: 'Link',
    //   age: 25 as string | number,
    // });

    // state.name = 99 // cannot change type
    // state.age = '12'

    // return {
    //   ...toRefs(state),
    // };

    // const name = ref('Link')
    // const age = ref<number | string>(25)

    // return {
    //   name, age
    // }

    const jobs = ref<Job[]>([
      { title: 'farm worker', location: 'lon lon ranch', salary: 30000, id: '1'},
      { title: 'quarryman', location: 'death mountain', salary: 102000, id: '2'},
      { title: 'flute player', location: 'the lost woods', salary: 100000, id: '3'},
      { title: 'fisher man', location: 'lake hylia', salary: 212000, id: '3'},
      { title: 'prison guard', location: 'gerudo valley', salary: 300200, id: '3'}
    ])

    return {
      jobs
    }

  },

});
</script>

<style></style>
