
<template>
  <div>
    <slot></slot>
  </div>
</template>

<script>
export default {
  props: {

  },
  data () {

  },
  methods: {
    supportSticky () {
      let vendorList = ['', '-webkit-', '-ms-', '-moz-', '-o-'],
          vendorListLength = vendorList.length,
          stickyElement = document.createElement('div')

      for (let i = 0; i < vendorListLength; i++) {
        stickyElement.style.position = vendorList[i] + 'sticky'
        if (stickyElement.style.position !== '') {
          return true
        }
      }
      return false
    }
  },
  mounted () {

  }
}
</script>