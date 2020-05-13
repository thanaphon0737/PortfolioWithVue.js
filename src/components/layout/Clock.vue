<template>
  <div class="clock" id="clock">

      <slot>Now</slot> : {{time}}

    </div>
</template>

<script>
import moment from 'moment'
    
export default {
    name :'Clock',
    mounted() {
        setInterval(() =>{
            this.time = moment(Date()).format('MM/DD/YYYY hh:mm:ss')
        },100)
    },
    data() {
        return {
            time: ""
        }
    },

}
</script>

<style scoped>
    .clock{
        font-size: 12px;
    }
</style>