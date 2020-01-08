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
      <div v-for="(item, index) in buttonType.primary" :key="index" class="box">
        <Button
          :label="item.type.charAt(0).toUpperCase() + item.type.slice(1, item.type.length)"
          :type="item.type"
          :size="item.size"
          :Outline="item.outline"
        />
        <div>{{item.size}}</div>
      </div>
    </div>
    <div class="divider">
      <div v-for="(item, index) in buttonType.secondary" :key="index" class="box">
        <Button
          :label="item.type.charAt(0).toUpperCase() + item.type.slice(1, item.type.length)"
          :type="item.type"
          :size="item.size"
          :Outline="item.outline"
        />
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
        buttonType: {
          primary: [
            {
              type: "primary",
              outline: false,
              size: "normal"
            },
            {
              type: "primary",
              outline: true,
              size: "normal"
            },
            {
              type: "primary",
              outline: false,
              size: "large"
            },
            {
              type: "primary",
              outline: false,
              size: "small"
            }
          ],
          secondary: [
            {
              type: "secondary",
              outline: false,
              size: "normal"
            },
            {
              type: "secondary",
              outline: true,
              size: "normal"
            },
            {
              type: "secondary",
              outline: false,
              size: "large"
            },
            {
              type: "secondary",
              outline: false,
              size: "small"
            }
          ]
        }
      };
    }
  };
</script>
