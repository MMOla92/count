<template>
  <div>
    <h1
      style="
        color: black;
        text-align: center;
        font-family: Arial, Helvetica, sans-serif;
        font-size: 40px;
      "
    >
      Timer
    </h1>
    <div
      style="
        text-align: center;
        font-family: Arial, Helvetica, sans-serif;
        font-size: 20px;
      "
    >
      The count is: {{ count }}
    </div>

    <button
      style="
        padding: 10px;
        width: 300px;
        text-align: center;
        position: center;
        right: 0;
        left: 0;
      "
      @click="increase"
      :disabled="count >= 10"
    >
      +1
    </button>
    <br />
    <br />

    <button
      style="
        padding: 10px;
        width: 300px;
        text-align: center;
        position: center;
        right: 0;
        left: 0;
      "
      @click="decrease"
    >
      -1
    </button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      count: 0,
    };
  },
  methods: {
    increase() {
      if (this.count < 10) this.count++;
    },
    decrease() {
      if (this.count > 0) this.count--;
    },
  },
};
</script>

<style>
* {
  background: white;
}

#h1 {
  margin-left: 0;
  margin-right: 0;
}

#button-click {
  box-sizing: border-box;
}
</style>
