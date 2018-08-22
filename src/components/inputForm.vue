<template>
    <div>
        <form id="application-input">
            <label>Apply Here: </label>
            <textarea v-model="applyInput" id="application-text" rows="8" cols="100"></textarea>
            <input v-on:click.prevent='toggleShow' id="submit" type="submit" value="Submit" />
        </form>
        <div id="preview">
            <p v-show='show' id="message">{{submitMessage}}</p>
        </div>
        <preview :resume="applyInput"/>
    </div>
</template>

<script>
import preview from './preview.vue'
export default {
    name: 'inputForm',
    components: {
        preview
    },
    data(){ 
        return {
            applyInput: '',
            show: false,
            submitMessage: "Your application was submitted!"
        }
    },
    methods: {
        toggleShow: function(){
            console.log('hello')
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
#preview{
    width: 462px;
    height: 18px;
    margin-top: 16px;
    margin-bottom: 16px;
}
</style>
