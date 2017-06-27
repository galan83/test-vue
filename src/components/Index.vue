<template>
  <q-layout>
    <div slot="header" class="toolbar">
      <q-toolbar-title :padding="0">
        Test ckeditor
      </q-toolbar-title>
    </div>

    <div class="layout-view">
      <ckeditor v-model="content" :config="config"></ckeditor>
      <modal-component></modal-component>
    </div>
  </q-layout>
</template>

<script>
import Ckeditor from 'vue-ckeditor2'
import ModalComponent from 'components/ModalComponent'

export default {
  components: {
    Ckeditor,
    ModalComponent
  },
  data () {
    return {
      content: '',
      config: {
        toolbar: [
          [ 'Bold', 'Italic', 'Underline', 'Strike', 'Subscript', 'Superscript' ]
        ],
        height: 300
      }
    }
  }
}
</script>
