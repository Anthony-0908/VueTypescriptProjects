<template>
    <div class="job-list" > 
        <ul> 
            <li v-for="job in jobs" :key="job.id">
                <h2>{{job.title}} in {{job.location}}</h2>
                <div class="salary">
                    <p>{{job.salary}}</p>
                </div>
                <div class="description ">
                    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Sunt eos eveniet, voluptas ipsa dolorem aspernatur mollitia facere animi aliquid. Veritatis, ex ut doloribus cupiditate praesentium porro labore odio neque harum.</p>
                </div>
            </li>
           
        </ul>
    </div>
</template>

<script lang="ts">
import {defineComponent, PropType} from 'vue';
import Job from '@/types/Job';
export default defineComponent ({
    props: {
        jobs: {
            required:true,
            type: Array as PropType<Job[]>
        }
    }
})
</script>

<style scoped>
.job-list {
    max-width: 960px;
    margin: 40px auto;
  }
  
  .job-list ul {
    padding: 0;
  }
  
  .job-list li {
    list-style-type: none;
    background: white;
    padding: 16px;
    margin: 16px 0;
    border-radius: 4px;
  }
  
  .job-list h2 {
    margin: 0 0 10px;
    text-transform: capitalize;
  }
  
  .salary {
    display: flex;
  }
  
  .salary img {
    color: #17bf66;
  }
  
  .salary p {
    color: #17bf66;
    font-weight: bold;
    margin: 10px 14px;
  }
</style>