<template>
  <div id="mmcontainer">
    <mindmap
      v-model="mm"
      :edit="true"
      :drag="true"
      :x-gap="84"
      :y-gap="18"
      :branch="5"
      :zoom="true"
      :center-btn="true"
      :fit-btn="true"
      :add-node-btn="true"
      :download-btn="true"
      :sharp-corner="false"
      :ctm="false"
    ></mindmap>
  </div>
</template>

<script>
import mindmap from "vue3-mindmap";
import "@/mmstyle.css";

export default {
  name: "App",
  components: {
    mindmap
  },
  data() {
    return {
      mm: [
        {
          name: "werqer",
          children: [
            {
              name: "asdfasdfasd",
              children: [{ name: "HTML & CSS" }, { name: "JavaScript" }]
            },
            {
              name: "asdfasdfasdf",
              collapse: true,
              children: [{ name: "asdfasdfasd" }]
            },
            { name: "asdfasdfasd", left: true }
          ]
        }
      ]
    };
  }
};
</script>
<style>
#mmcontainer {
  position: absolute;
  left: 0px;
  right: 0px;
  top: 0px;
  bottom: 0px;
}

.Mindmap_text_fgvb6 {
  fill: #f00 !important;
  background-color: blue;
  border: 10px solid red;
}
</style>
