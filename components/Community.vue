<template>
  <div>
    <v-container>
      <v-row>
        <v-col cols="6">
          <div class="bottom30">
            <h1>Find your community</h1>
          </div>
          <div class="card-design d-flex flex-column">
            <div class="d-flex justify-space-between align-center">
              <div>
                <h2 class="title-national">1.Choose your nationality</h2>
                <span class="des-national"
                  >or nationality you are interested in viewing their
                  businesses</span
                >
              </div>
              <div>
                <v-icon>search</v-icon>
              </div>
            </div>
            <div
              class="d-flex flex-row flex-wrap pa-2 justify-center align-center"
            >
              <v-col
                cols="2.5"
                v-for="(country, i) in countrys"
                :key="i"
                class="mb-3 d-flex justify-center align-center"
              >
                <div class="d-flex flex-column p-2 flag">
                  <img
                    :src="require(`~/assets/images/country/${country.src}.svg`)"
                    class="country-img"
                  />
                  <p>{{ country.name }}</p>
                </div>
              </v-col>
              <a href="/">show all nationality</a>
            </div>
          </div>
        </v-col>
        <v-col cols="6">
          <div class="bottom10">
            <p class="title-matters">why community matters?</p>
            <span class="des-matters"
              >Your community is important since you can find a group of people
              with the same language, common culture and similar needs.</span
            >
          </div>
          <div class="card-design d-flex flex-column">
            <div class="d-flex justify-space-between align-center">
              <div>
                <h2 class="title-national">2.Set the location</h2>
                <span class="des-national">
                  you are interested in viewing their businesses</span
                >
              </div>
              <div>
                <v-icon>search</v-icon>
              </div>
            </div>
            <div>
              <iframe
                src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3236.129212314583!2d51.42853341540221!3d35.79676108016764!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x3f8e06756350db0d%3A0x6c937bdd2863f26b!2sTehran%20Province%2C%20Tehran%2C%20District%201%2C%20Akbari%20St%2C%20German%20Embassy%20Garden%2C%20Iran!5e0!3m2!1sen!2s!4v1633320660256!5m2!1sen!2s"
                width="540"
                height="250"
                style="border: 0; object: fit"
                allowfullscreen=""
                loading="lazy"
              >
                <div>
                  <span>Use my current location</span>
                </div>
              </iframe>
            </div>
          </div>
        </v-col>
        <v-col cols="12">
          <div class="card-design d-flex flex-column">
            <div class="d-flex flex-column">
              <h2 class="title-national">3.Pick a community</h2>
              <span class="des-national">
                When you choose a community, we show its businessers</span
              >
            </div>
            <v-row class="pa-3">
              <v-col
                cols="6"
                v-for="(item, a) in communityList"
                :key="a"
                class="d-flex"
              >
                <div class="d-flex flag-community align-center">
                  <img
                    :src="require(`~/assets/images/country/${item.src1}.svg`)"
                    class="country-img"
                  />
                  <p class="margin10">{{ item.name1 }}</p>
                  <span style="margin: 0px 20px">of</span>
                  <img
                    :src="require(`~/assets/images/country/${item.src2}.svg`)"
                    class="country-img"
                  />
                  <p class="margin10">{{ item.name2 }}</p>
                </div>
              </v-col>
            </v-row>
          </div>
        </v-col>
        <div>
          <p class="title-check">Some other cool communities to check</p>
          <Check :checkList="checkList" />
        </div>
      </v-row>
    </v-container>
  </div>
</template>

<script>
import Check from "./Check.vue";
export default {
  components: { Check },
  props: ["countrys", "communityList", "checkList"],
  data() {
    return {};
  },
};
</script>
<style scoped>
a {
  text-decoration: none;
}
.bottom30 {
  margin-bottom: 30px;
}
.bottom10 {
  margin-bottom: 10px;
}
.margin10 {
  margin: 0px 10px;
}
.title-check{
  font-family: vazir-bold;
  font-weight: bold;
  font-size: 15px;
  margin-left:12px;
}

.title-matters {
  font-family: vazir-bold;
  font-weight: bold;
  font-size: 15px;
  margin-bottom: 0;
}
.des-matters {
  font-size: 12px;
  color: #c3c3c3;
}
.card-design {
  background-color: #fff;
  box-shadow: 0px 1px 20px 4px #bcbaba47;
  border-radius: 10px;
  border: 1px solid #00000026;
  padding: 10px;
}
.title-national {
  font-family: vazir-bold;
  font-weight: bold;
  font-size: 15px;
}
.des-national {
  font-size: 13px;
  color: #c3c3c3;
}
.country-img {
  width: 32px;
  height: 23px;
}
.flag {
  margin-left: 10px;
  padding: 5px;
}
.flag:hover {
  background-color: #189876;
  color: #fff;
  box-shadow: 0 4px 10px 0 rgb(0 0 0 / 50%);
  border-radius: 5px;
  cursor: pointer;
}
.flag-community {
  margin: 5px;
  padding: 5px;
}
.flag-community:hover {
  background-color: #189876;
  color: #fff;
  box-shadow: 0 4px 10px 0 rgb(0 0 0 / 50%);
  border-radius: 5px;
  cursor: pointer;
}
</style>