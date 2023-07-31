<template>
     <div class="modal" v-if="visible">
    <div class="modal-content">
        
      <slot></slot>
    </div>
  </div>
</template>

<script>

export default{
    name: 'Modal',
    components:{
    },
    props:{
        visible: Boolean,

    },

}
</script>

<style >
@import '../style.css';




</style>