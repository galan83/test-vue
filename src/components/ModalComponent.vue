<template>
  <div>
    <q-modal ref="basicModal">
      <h4>Basic Modal</h4>
      <ckeditor v-model="content" :config="config"></ckeditor>
      <button class="primary" @click="$refs.basicModal.close()">Close</button>
    </q-modal>
    <button @click="openModal">Open modal</button>
  </div>
</template>

<script>
  import Ckeditor from 'vue-ckeditor2'

  export default {
    name: 'ModalComponent',
    components: {
      Ckeditor
    },
    data () {
      return {
        config: {
          toolbar: [
            [ 'Bold', 'Italic', 'Underline', 'Strike', 'Subscript', 'Superscript' ]
          ],
          height: 300
        }
      }
    },
    methods: {
      openModal () {
        this.$refs.basicModal.open()
      }
    }
  }
</script>
