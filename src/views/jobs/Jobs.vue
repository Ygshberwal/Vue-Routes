<template>
    <h1>Jobs</h1>
    <div v-for="job in jobs" :key="job.id" class="job">
        <router-link :to="{ name: 'JobDetails', params:{id: job.id} }">
            <h2>{{ job.title }}</h2>
        </router-link>
        
    </div>
</template>

<script>
import JobDetails from './JobDetails.vue';

export default{
    
    data(){
        return {
            jobs:[
                {title:'Web Developer', id:1, details:"A Web Developer is a professional who is responsible for the design and construction of websites. They ensure that sites meet user expectations by ensuring they look good, run smoothly and offer easy access points with no loading issues between pages or error messages."},
                {title:'Web Designer', id:2, details:"A Web Designer is a professional who works for corporations across industries, but they can also be employed by web design agencies or self-employed individuals. Their job entails monitoring user feedback and performing routine updates to website layouts as needed; this may include coding new pages with particular care when necessary – all in order that the company’s brand identity remains intact."},
                {title:'App Developer', id:3, details:"An Application Developer is a professional responsible for designing and coding functional software programs and applications. They collaborate with teams to set specifications, write high-quality code, conduct testing, and troubleshoot applications."}
            ]
        }
    }
}
</script>


<style>
.job h2{
    background: #f4f4f4;
    padding: 20px; 
    border-radius: 10px;
    margin: 10px auto; 
    max-width: 600px; 
    cursor: pointer;
    color:#444
}
.job h2:hover {
    background:#ddd;
}
 a{
    text-decoration: none;
}
</style>