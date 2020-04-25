<template>
  <div>  
    <h1>Clicked {{ timesClicked }} times.</h1>
    <button @click="iAmClicked()">Click me!</button>
  </div>
</template>
 
<script>
    test1 : 0;
    export default {
        
        data() {
            return {timesClicked: 0}
        },
        methods: {
            iAmClicked() {
                this.timesClicked ++ ;
            }
        }
    };
</script>