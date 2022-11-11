<template>
  <div>
    {{ tour.title }}
    <tag-list :tags="tour.tags"/>
    <v-divider />
  </div>
</template>
<script>
import TagList from "@/components/TagList.vue";
export default {
  components: { TagList },
  name: "TourView",
  props: {
    tour: Object,
  },
};
</script>