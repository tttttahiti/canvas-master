<template>
  <div class="container">
    <div class="inner">
      <div class="preview">
        <canvas ref="canvas" class="canvas" width="600" height="600"></canvas>
      </div>
      <div class="controller">
        <img class="logo" src="~/assets/images/logo.png" alt="canvas" />
        <dl class="controll-list">
          <dt class="controll-list-title">Paint</dt>
          <dd class="controll-list-body">
            color: # <input v-model="color" type="text" class="input" />
            <button class="button">Paint</button>
          </dd>
          <dt class="controll-list-title">Clear</dt>
          <dd class="controll-list-body">
            <button class="button">Clear</button>
          </dd>
          <dt class="controll-list-title">Place Image</dt>
          <dd class="controll-list-body">
            <input type="file" />
            <button class="button">Clear</button>
          </dd>
          <dt class="controll-list-title">Download</dt>
          <dd class="controll-list-body">
            <button class="button">Download</button>
          </dd>
        </dl>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Main',
  data() {
    return {
      canvas: null,
      context: null,
      color: 'ffffff',
      image: null
    }
  }
}
</script>

<style lang="scss">
.container {
  background-color: #ccc;
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
  .inner {
    border-radius: 12px;
    background-color: #fff;
    padding: 24px;
    display: flex;
  }
  .preview {
    margin-right: 24px;
  }
  .controller {
    max-width: 600px;
  }
  .canvas {
    border: 1px solid #ccc;
  }
  .logo {
    display: block;
    margin: 0 auto 24px;
    width: 430px;
    height: 150px;
  }
  .controll-list {
    display: flex;
    align-items: center;
    flex-wrap: wrap;
    text-align: left;
    &-title {
      width: 25%;
      font-size: 14px;
      font-weight: bold;
      padding: 12px 12px 12px 0;
    }
    &-body {
      width: 75%;
      padding: 12px 0;
    }
  }
  .input {
    border: 1px solid #ccc;
    border-radius: 4px;
    height: 40px;
    box-sizing: border-box;
    padding: 8px 12px;
    font-size: 14px;
    width: 120px;
  }
  .button {
    appearance: none;
    border: none;
    border-radius: 4px;
    padding: 0 12px;
    background-color: #3368b1;
    color: #fff;
    font-size: 16px;
    font-weight: bold;
    display: inline-block;
    height: 40px;
    line-height: 40px;
  }
}
</style>
