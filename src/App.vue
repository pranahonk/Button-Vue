<style>
.box {
  width: 120px;
  text-align: center;
  display: inline-block;
}

.divider {
  display: block;
  margin-top: 15px;
}
</style>


<template>
  <div>
    <div class="divider">
      <div v-for="(item, index) in buttonType" :key="index" class="box">
        <Button :label="item.label" :type="item.type" :size="item.size" :Outline="item.outline"/>
        <div>{{item.size}}</div>
      </div>
    </div>
  </div>
</template>

<script>
import Button from "./components/Button.vue";

export default {
  components: {
    Button: Button
  },
  data() {
    return {
      buttonType: [
        {
          type: "primary",
          label: "Primary",
          outline: false,
          size: "normal"
        },
        { type: "primary", label: "Primary", outline: true, size: "normal" },
        { type: "primary", label: "Primary", outline: false, size: "large" },
        { type: "primary", label: "Primary", outline: false, size: "small" }
      ]
    };
  }
};
</script>
