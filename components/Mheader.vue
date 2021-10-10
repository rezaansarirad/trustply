<template>
  <v-container>
    <v-app-bar app fixed elevation="0" right id="navBar" class="header">
      <v-row>
        <v-col cols="4" class="d-flex justify-start align-center">
          <img
            src="~/assets/images/logo.png"
            alt="logo trustply"
            width="190px"
          />
        </v-col>
        <v-col cols="4" class="d-flex justify-center align-center top30">
          <v-combobox
            dense
            outlined
            solo
            label="I need to"
            :items="items"
          ></v-combobox>
        </v-col>
        <v-col cols="4" class="d-flex justify-end align-center">
          <img
            src="~/assets/images/profile.jpeg"
            width="50px"
            height="50px"
            alt=" profile user"
            class="profile-style"
          />
        </v-col>
      </v-row>
    </v-app-bar>
  </v-container>
</template>








<script>
export default {
  data() {
    return {
      items: [
        "Exchange my money ",
        "Check currency rates ",
        "Find a local business ",
      ],
    };
  },
  // mounted() {
  //   window.addEventListener("scroll", function () {
  //     window.pageYOffset
  //       ? document.getElementById("navBar").classList.add("sticky")
  //       : document.getElementById("navBar").classList.remove("sticky");
  //   });
  // },
};
</script>













<style  scoped>
.header {
  background-image: linear-gradient(180deg, #082839, #536674);
  width: 100%;
}

.profile-style {
  width: 50px;
  height: 50px;
  border-radius: 50%;
}
.top30 {
  margin-top: 30px;
}
</style>


