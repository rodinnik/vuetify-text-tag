<template>
  <v-container ref="containerTagList" v-resize="getResizeMain">
    <v-row justify="space-around">
      <template v-for="(tag, index) in tags" >
        <div :key="tag.id">
          <v-icon v-if="tag.icon">{{ tag.icon }}</v-icon
          >{{ tag.text }}
        </div>
        <v-icon
          v-if="index !== Object.keys(tags).length - 1"
          :key="tag.id + '_sep'"
          >mdi-circle-medium</v-icon
        ></template
      > 
    </v-row>
    {{ widthMain }}
  </v-container>
</template>
<script>
export default {
  name: "TagList",
  props: {
    tags: Array,
  },
  data() {
    return {
      widthMain: null,
    };
  },
  mounted() {
    this.getResizeMain();
  },
  methods: {
    getResizeMain() {
      this.widthMain = this.$refs.containerTagList.clientWidth;
    },
    getResizeEl(){
    }
  },
};
</script>