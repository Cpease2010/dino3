<template>
<div>
    <section id="job-details">
        <h2>Job Details</h2>
        <h4>{{listing.title}}</h4>
        <p>{{listing.description}}</p>
    </section>
    </div>
</template>

<script>
export default {
    name: 'jobDetails',
    data(){
        return {
            listing: [],
            apiURL: '../../static/listing.json'
        }
    },
    mounted(){
        fetch(this.apiURL)
            .then(result => result.json())
            .then(result => {
                console.log(result);
                
                this.listing = result
            })
    }
}
</script>


<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
main section {
  grid-column: 2/3;
}
</style>
