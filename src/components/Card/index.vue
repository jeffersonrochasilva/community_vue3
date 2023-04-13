<template>
  <div
    class="card"
    :style="{
      '--background': props.corFundo,
    }"
  >
    <p class="card__subtitle">Para você começar</p>
    <div class="card__titles">
      <span
        :style="{ '--colorTextTitle': props.colorTextTitle }"
        class="card__titles__title"
        >{{ props.textTitle1 }}</span
      >
      <span
        :style="{ '--colorTextTitle': props.colorTextTitle }"
        class="card__titles__title"
        >R$ {{ subTextTitle }} /mês</span
      >
    </div>
    <button
      :style="{
        '--colorFundoButton': props.corFundoButton,
        '--colorText': props.corButtonWrite,
      }"
    >
      Assinar agora
    </button>
    <v-divider />
    <div style="height: 40%">
      <div class="card__description" v-for="(item, i) in items" :key="i">
        <div class="card__description__camp">
          <v-icon color="green">mdi-check</v-icon>
          <p
            :style="{ '--colorText': props.colorText }"
            class="card__description__camp__text"
          >
            {{ item }}
          </p>
        </div>
        <v-icon :style="{ color: props.colorText }"
          >mdi-minus-circle-outline</v-icon
        >
      </div>
    </div>
  </div>
</template>
<script lang="ts" setup>
const props = defineProps<{
  corFundo: String;
  corFundoButton: String;
  corButtonWrite: String;
  textTitle1: String;
  subTextTitle: String;
  colorTextTitle: String;
  colorText: String;
  items: String[];
}>();
</script>
<style lang="scss" scoped>
p,
span {
  font-family: sans-serif;
}
.card {
  --background: red;
  width: 384px;
  height: 454px;
  border-radius: 5px;
  background: var(--background, blue);
  margin: 32px;
  padding: 50px 32px;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  &__subtitle {
    color: #996dff;
    font-size: 18px;
    font-weight: bold;
  }
  &__titles {
    display: flex;
    justify-content: space-between;
    span {
      --colorTextTitle: #000;
      font-size: 25px;
      font-weight: bold;
      color: var(--colorTextTitle);
    }
  }
  button {
    --colorFundoButton: #303030;
    --borderColor: #303030;
    --colorText: #303030;
    width: 80%;
    height: 45px;
    background: var(--colorFundoButton, red);
    border-radius: 4px;
    border: 1px solid var(--borderColor, red);
    color: var(--colorText, red);
    margin-left: 10%;
  }
  &__description {
    display: flex;
    justify-content: space-between;
    margin-bottom: 15px;
    &__camp {
      display: flex;

      &__text {
        --colorText: red;
        color: var(--colorText);
      }
    }
  }
}
</style>
