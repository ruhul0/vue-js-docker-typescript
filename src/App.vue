 <template>
  <div class="app">
    <p>{{ name }} - {{ age }}</p>
    <button @click= "changeName('test')">change names </button>
    <button @click= "changeAge(30)">change age </button>
    <!-- <p>{{ jobs[0] }}</p> -->
  </div>
</template>

<script lang="ts">

// let age: string | number = 27

import { defineComponent, reactive, ref, toRefs } from 'vue';
import Job from './components/types/Job'

export default defineComponent({
  name: 'App',
  components: {},
  setup(){

    // reactive 
    // const state = reactive({
    //   name: 'Link' as String,
    //   age: 25 as string | number
    // })

    // state.name = "ruhul"
    // state.age = 27

    // return { ...toRefs(state) }

    const name = ref('Link')
    const age = ref<number | string>(25)

    return {name,age}

    // const jobs = ref<Job[]>([
    //   {
    //     title:"developer",
    //     location: "dhaka",
    //     salary: 300000,
    //     id: '1'
    //   },
    //   {
    //     title:"developer",
    //     location: "dhaka",
    //     salary: 10000,
    //     id: '2'
    //   },
    //   {
    //     title:"developer",
    //     location: "dhaka",
    //     salary: 15000,
    //     id: '3'
    //   },
    //   {
    //     title:"developer",
    //     location: "dhaka",
    //     salary: 20000,
    //     id: '4'
    //   }
    // ])
  },
  methods: {
    changeName(name:string) {
      this.name = name;
      return name
    },
    changeAge(age:string | number){
      this.age = age
      return age
    }
  }
});
</script>

<style>

</style>
