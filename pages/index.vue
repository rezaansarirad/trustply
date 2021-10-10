<template>
  <div>
    <Community :communityList="communityList" :countrys="countrys" :checkList="checkList" />
  </div>
</template>


<script>
export default {
  layout: "default",

  data() {
    return {
      checkList: [
        {
          name1: "Germans",
          src1: "germany",
          name2: "Edmonton",
          src2: "canada",
        },
        {
          name1: "Germans",
          src1: "germany",
          name2: "Calgary",
          src2: "canada",
        },
        {
          name1: "Germans",
          src1: "germany",
          name2: "Sherwook ",
          src2: "canada",
        },
        {
          name1: "Germans",
          src1: "germany",
          name2: "Edmonton",
          src2: "canada",
        },
        {
          name1: "Germans",
          src1: "germany",
          name2: "Edmonton",
          src2: "canada",
        },
      ],
      communityList: [
        {
          name1: "Iranians",
          src1: "iran",
          name2: "Edmonton,Alberta,Canada",
          src2: "canada",
        },
        {
          name1: "Brazilians",
          src1: "brezil",
          name2: "Calgary,Alberta,Canada",
          src2: "canada",
        },
        {
          name1: "Irishes",
          src1: "Ireland",
          name2: "Sherwook Park,Alberta,Canada",
          src2: "canada",
        },
        {
          name1: "Americans",
          src1: "america",
          name2: "Edmonton,Alberta,Canada",
          src2: "canada",
        },
        {
          name1: "Spanishes",
          src1: "spanish",
          name2: "Calgary,Alberta,Canada",
          src2: "canada",
        },
        {
          name1: "Germans",
          src1: "germany",
          name2: "Sherwook Park,Alberta,Canada",
          src2: "canada",
        },
      ],

      countrys: [
        {
          name: "German",
          src: "germany",
        },
        {
          name: "Canadian",
          src: "canada",
        },
        {
          name: "Spanish",
          src: "spanish",
        },
        {
          name: "Iranian",
          src: "iran",
        },
        {
          name: "American",
          src: "america",
        },
        {
          name: "German",
          src: "germany",
        },
        {
          name: "Canadian",
          src: "canada",
        },
        {
          name: "Spanish",
          src: "spanish",
        },
        {
          name: "Iranian",
          src: "iran",
        },
        {
          name: "American",
          src: "america",
        },
      ],
    };
  },
};
</script>