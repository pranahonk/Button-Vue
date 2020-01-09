<style>
[type="button"],
[type="reset"],
[type="submit"],
button {
  -webkit-appearance: button;
}

button,
select {
  text-transform: none;
  overflow: visible;
}

.btn {
  display: inline-block;
  font-weight: 400;
  color: #212529;
  text-align: center;
  vertical-align: middle;
  cursor: pointer;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
  background-color: transparent;
  border: 1px solid transparent;
  padding: 0.375rem 0.75rem;
  font-size: 1rem;
  line-height: 1.5;
  border-radius: 0.25rem;
  transition: color 0.15s ease-in-out, background-color 0.15s ease-in-out,
    border-color 0.15s ease-in-out, box-shadow 0.15s ease-in-out;
}

.btn-large {
  padding: 0.5rem 1rem;
  font-size: 1.25rem;
  line-height: 1.5;
  border-radius: 0.3rem;
}

.btn-small {
  padding: 0.25rem 0.5rem;
  font-size: 0.875rem;
  line-height: 1.5;
  border-radius: 0.2rem;
}

.btn-primary {
  color: #fff;
  background-color: #007bff;
  border-color: #007bff;
}

.btn-outline-primary {
  color: #007bff;
  border-color: #007bff;
}

.btn-primary:hover {
  color: #fff;
  background-color: #0069d9;
  border-color: #0062cc;
}

.btn-secondary {
  color: #fff;
  background-color: #6c757d;
  border-color: #6c757d;
}

.btn-outline-secondary {
  color: #6c757d;
  border-color: #6c757d;
}

.btn-secondary:hover {
  color: #fff;
  background-color: #5a6268;
  border-color: #545b62;
}

.btn-success {
  color: #fff;
  background-color: #28a745;
  border-color: #28a745;
}

.btn-success:hover {
  color: #fff;
  background-color: #218838;
  border-color: #1e7e34;
}

.btn-outline-success {
  color: #28a745;
  border-color: #28a745;
}
</style>

<template>
  <button
    class="btn"
    @click="clickHandler"
    :class="[Outline ? 'btn-outline-' + 
    type : 
    'btn-' + type, 
    'btn-' + size]"
    :style="{'background-color': Outline ?  
    'transparent' 
    : null }"
    :disabled="disabled"
  >{{label}}</button>
</template>



<script>
export default {
  name: "OpenSOurceButton",
  props: {
    label: {
      type: String,
      default: "default"
    },
    disabled: {
      type: Boolean,
      default: false
    },
    type: {
      type: String,
      default: ""
    },
    size: {
      type: String,
      default: ""
    },
    Outline: {
      type: Boolean,
      default: false
    }
  },
  methods: {
    clickHandler() {
      this.$emit("click");
    }
  }
};
</script>


