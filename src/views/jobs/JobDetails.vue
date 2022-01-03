<template lang="">
    <div>
        <h1><b>Job Details</b></h1>
        <p>The Job Id is {{$route.params.id}}</p>
    </div>
</template>
<script>
    import {toRefs, reactive} from 'vue'
export default {
    setup() {
        const state = reactive({
            
        });

        return toRefs(state)
    }
}
</script>
<style lang="">
    
</style>