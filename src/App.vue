<template>
  <select id="language-select" v-model="locale">
    <option value="zh">简体中文</option>
    <option value="en">English</option>
    <option value="ptBR">Brazilian Portuguese</option>
  </select>
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
      :ctm="true"
      :locale="en"
      :timetravel="true"
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
      locale: "en",
      mm: [
        {
          name: "Start"
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
  top: 60px;
  bottom: 0px;
}
</style>
