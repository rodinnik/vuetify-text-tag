<template>
  <v-app>
    <v-main>
      <tour-view v-for="tour in tours" :key="tour.id" :tour="tour" class="sss"></tour-view>
    </v-main>
  </v-app>
</template>
<script>
import TourView from "@/components/TourView.vue";

export default {
  components: { TourView },
  name: "App",
  data() {
    return {
      tours: [
        {
          id: 0,
          title: "Город сыра и мира",
          tags: [
            { id: 0, text: "5", icon: "mdi-star-outline" },
            { id: 1, text: "Историческая", icon: "" },
            { id: 2, text: "На автобусе", icon: "mdi-bus" },
            { id: 3, text: "28 марта", icon: "" },
            { id: 4, text: "9 часов", icon: "mdi-clock-time-three-outline" },
          ],
        },
        {
          id: 1,
          title: "Экскурсия в национальный парк Куршская коса",
          tags: [
            { id: 0, text: "5", icon: "mdi-star-outline" },
            { id: 1, text: "Обзорная", icon: "" },
            { id: 2, text: "На автобусе", icon: "mdi-bus" },
            { id: 3, text: "25 марта", icon: "" },
            { id: 4, text: "6 часов", icon: "mdi-clock-time-three-outline" },
          ],
        },
        {
          id: 2,
          title: "О кирках, рыцарях и замках",
          tags: [
            { id: 0, text: "5", icon: "mdi-star-outline" },
            { id: 1, text: "Историческая", icon: "" },
            { id: 2, text: "На автобусе", icon: "mdi-bus" },
            { id: 3, text: "29 марта", icon: "" },
            { id: 4, text: "6 часов", icon: "mdi-clock-time-three-outline" },
          ],
        },
        {
          id: 3,
          title: "Экскурсия в янтарный",
          tags: [
            { id: 0, text: "Историческая", icon: "" },
            { id: 1, text: "На автобусе", icon: "mdi-bus" },
            { id: 2, text: "29 марта", icon: "" },
            { id: 3, text: "6 часов", icon: "mdi-clock-time-three-outline" },
            { id: 4, text: "до 49", icon: "mdi-account" },
          ],
        },
      ],
    };
  },
};
</script>
<style scoped>
.sss{
  max-width: 600px;
}
</style>