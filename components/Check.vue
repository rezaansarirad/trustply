<template>
  <div>
    <v-row>
      <v-col cols="2.5" v-for="(item, c) in checkList" :key="c">
        <div class="d-flex align-center card-design ">
          <div class="d-flex flex-column align-center justify-center">
            <img
              :src="require(`~/assets/images/country/${item.src1}.svg`)"
              class="country-img"
            />
            <p class="name-country">{{ item.name1 }}</p>
          </div>
          <span style="margin: 0px 20px">of</span>
          <div class="d-flex flex-column align-center justify-center">
            <img
              :src="require(`~/assets/images/country/${item.src2}.svg`)"
              class="country-img"
            />
            <p class="name-country">{{ item.name2 }}</p>
          </div>
        </div>
      </v-col>
    </v-row>
  </div>
</template>


<script>
export default {
  props: ["checkList"],
  data() {
    return {};
  },
};
</script>


<style scoped>

.card-design {
  padding: 10px;
  background: #f5f5f5;
  border-radius: 8px;
  border: 1px solid #c3c3c3;
}

.card-design:hover {
  background-color: #189876;
  color: #fff;
  box-shadow: 0 4px 10px 0 rgb(0 0 0 / 50%);
  border: 1px solid #189876;
  border-radius: 8px;
  cursor: pointer;
}
.country-img {
  width: 32px;
  height: 23px;
}
</style>