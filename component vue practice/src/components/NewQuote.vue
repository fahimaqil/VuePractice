<template>
    <div class="row">
        <form>
      <div class="col-sm-8 clo-sm-offset-2 colxs-12 col-md-6 col-md-offset-3">
            <label>Quote</label>
            <textarea class="form-control" rows="3" v-model="quote"></textarea>
            <button class="btn btn-primary" @click.prevent="createNew">Add Quote</button>
      </div>
      </form>
    </div>
</template>

<script>
    export default {
        data:function(){
            return{
                quote:''
            };
        },
        methods:{
            createNew(){
                this.$emit('quoteAdded',this.quote);
                this.quote='';
            }
        }
        
    }
</script>

<style>
</style>
