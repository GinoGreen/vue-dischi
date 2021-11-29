<template>
   <select 
      class="form-select"
      v-model="genr"
      @change="$emit('sendGenr', genr)"
   >
      <option value="selected" selected>Seleziona il genere musicale</option>
      <option value="Rock">Rock</option>
      <option value="Pop">Pop</option>
      <option value="Jazz">Jazz</option>
      <option value="Metal">Metal</option>
   </select>
</template>

<script>
export default {
   name: 'Select',
   data(){
      return {
         // default genr
         genr: 'selected'
      }
   }
}
</script>

<style lang="scss">

   .form-select {
      display: inline-block;
      width: 300px !important;
   }
</style>