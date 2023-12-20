<template>
  <i v-html="svg"></i>
</template>

<script>
import { svgService } from '../services/svg.service.js'

export default {
  name: 'SvgIcon',
  props: {
    iconName: String,
  },
  data() {
    return {
      svg: '',
    }
  },
  mounted() {
    this.svg = svgService.getIcon(this.iconName)
  },
}
</script>
