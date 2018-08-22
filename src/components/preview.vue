<template>
    <div>
        <button v-on:click="toggleShow" id="preview-toggle">Show Preview</button>
        <section v-show="show" id="application-preview">{{resume}}</section>
    </div>
</template>

<script>
export default{
    name: 'preview',
    props: ['resume'],
    data(){ 
        return {
            show: false,
        }
    },
    methods: {
        toggleShow: function(){
            this.show = !this.show
        }
    }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
#application-preview {
    border-radius: 6px;
    box-shadow: 0 2px 4px 0 rgba(0, 0, 0, 0.3);
    border: 1px solid darkgrey;
    min-height: 100px;
    margin-top: 20px;
    padding: 10px;
}
</style>
