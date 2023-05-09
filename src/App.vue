<template>
  <div class="box-form">
    <div class="box-form__progress">

      <div class="task" v-for="(task, key) in tasks" :key="key">
        <div class="task__number task__active" v-if="key===0">{{ key+1 }}</div>
        <div class="task__number" v-else>{{ key+1 }}</div>
        <div class="task__text">
          <span>STEP {{ key+1 }}</span>
          <p>{{ task }}</p>
        </div>
      </div>

      <NavDecoration />

    </div>
    <div class="box-form__content">
      <GlobalInfoForm />
    </div>
  </div>
</template>

<script setup lang="ts">
import NavDecoration from './components/NavDecoration.vue';
import GlobalInfoForm from './components/GlobalInfoForm.vue';

const tasks = ['Your info', 'Select plan', 'Add-ons', 'Summary'];
</script>

<style lang="scss">
html, body {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  background-color: color(neutral, magnolia);
  height: 100%;
}

#app {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100%;
  font-family: $font-family;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  font-size: $base-font-size;
}

.box-form {
  width: 45%;
  display: flex;
  background-color: color(neutral, white);
  border-radius: 15px;
  padding: 1rem;
  gap: 2rem;

  &__progress {
    position: relative;
    flex: 1;
    background: color(primary, purplish-blue);
    display: flex;
    flex-direction: column;
    padding: 2rem;
    border-radius: 15px;
    gap: 2rem;
    overflow: hidden;

    .task {
      display: flex;
      align-items: flex-start;
      gap: 1rem;

      &__number {
        border: 1px solid color(neutral, white);
        color: color(neutral, white);
        padding: 0.4em;
        border-radius: 50%;
        width: 1.5em;
        height: 1.5em;
        line-height: 1.5em;
        text-align: center;
        font-weight: 700;
      }

      &__active {
        background: color(primary, light-blue);
        color: color(primary, marine-blue)
      }

      &__text {
        span {
          color: color(primary, pastel-blue);
          font-size: 11px;
        }

        p {
          margin: 3px 0 0 0;
          color: color(neutral, magnolia);
          text-transform: uppercase;
          font-size: 14px;
          font-weight: 600;
        }
      }
    }
  }

  &__content {
    flex: 3;
    height: 550px;
  }
}
</style>
