<template>
    <div class="row"> 
        <form>
            <div class="col-sm-8 col-sm-offset-2 col-xs-12 col-md-6 col-md-offset-3 form-group">
                <label>Add New Quote </label>
                <textarea class="form-control" name="" id="" cols="30" rows="3" v-model="quote"></textarea>
            </div>
            <div class="col-sm-8 col-sm-offset-2 col-xs-12 col-md-6 col-md-offset-3 form-group">
                <button class="btn btn-primary" @click.prevent="createNew">Add Quote</button>
                <!-- .prevent stops the default form behavior of submitting form to server (and reloading page) -->
            </div>
        </form>
    </div>
</template>

<script>
    export default {
        data() {
            return {
                quote: ''
            };
        },
        methods: {
            createNew() {
                this.$emit('quoteAdded',this.quote);
                this.quote = '';
            }
        }

    }
</script>

<style scoped>

</style>

