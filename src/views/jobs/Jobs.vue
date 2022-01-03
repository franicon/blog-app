<template lang="">
    <div class="">
        <h1>Jobs</h1>
        <div v-for="job in jobs" :key="job.id">
            <router-link  :to="{name: 'JobDetails', params:{id: job.id}}">{{ job.title }}</router-link>
        </div>
    </div>
</template>
<script>
    import {toRefs, reactive} from 'vue'
export default {
        setup() {
            const state = reactive({
                jobs:[
                    {title: 'Ux Designer', id: 1, details:'lorem'},
                    {title: 'Front End Developer', id: 2, details:'lorem'},
                    {title: 'Backend Developer', id: 3, details:'lorem'},
                ]
            });
            return toRefs(state)
        },
}
</script>
<style lang="">
    
</style>