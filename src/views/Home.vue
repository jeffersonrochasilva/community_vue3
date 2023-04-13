<template>
  <div class="home">
    <Card
      :corFundo="card"
      :corFundoButton="corFundoButtonWrite"
      :corButtonWrite="corButtonNoWrite"
      :textTitle1="textTitle1"
      :subTextTitle="subTextTitle1"
      :colorTextTitle="colorTextTitle1"
      colorText="#000"
      :items="itemsOne"
    />
    <Card
      :corFundo="cardCenter"
      :corFundoButton="corFundoButtonNoWrite"
      :corButtonWrite="corButtonWrite"
      :textTitle1="textTitle2"
      :subTextTitle="subTextTitle2"
      :colorTextTitle="colorTextTitle2"
      colorText="#cdcdcd"
      :items="itemsTwo"
    />
    <Card
      :corFundo="card"
      :corFundoButton="corFundoButtonWrite"
      :corButtonWrite="corButtonNoWrite"
      :textTitle1="textTitle3"
      :subTextTitle="subTextTitle3"
      :colorTextTitle="colorTextTitle1"
      colorText="#000"
      :items="itemsThree"
    />
  </div>
</template>

<script lang="ts" setup>
import Card from "@/components/Card/index.vue";
import { Ref, ref } from "vue";
const card: Ref<string> = ref("#FFFFFF");
const cardCenter: Ref<string> = ref("#0F172A");
const corFundoButtonWrite: Ref<string> = ref("#FFF");
const corFundoButtonNoWrite: Ref<string> = ref("#996DFF");
const corButtonWrite: Ref<string> = ref("#fff");
const corButtonNoWrite: Ref<string> = ref("#0F172A");
const textTitle1: Ref<string> = ref("Essentials");
const textTitle2: Ref<string> = ref("Ultimate");
const textTitle3: Ref<string> = ref("Interprise");
const subTextTitle1: Ref<string> = ref("19,97");
const subTextTitle2: Ref<string> = ref("29,97");
const subTextTitle3: Ref<string> = ref("");
const colorTextTitle1: Ref<string> = ref("#000");
const colorTextTitle2: Ref<string> = ref("#fff");
const itemsOne: Ref<string[]> = ref(["Até 3 usuários", "Autoatendimento"]);
const itemsTwo: Ref<string[]> = ref([
  "Usuários ilimitados",
  "Suporte 24/7",
  "CSM Dedicado",
  "Treinamentos",
]);
const itemsThree: Ref<string[]> = ref([
  "Plano customizado especialmente para a necessidade de seu negocio",
]);
</script>
<style lang="scss" scoped>
.home {
  width: 100%;
  height: 100vh;
  background: #f8fafc;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-wrap: wrap;

  h1 {
    color: red;
  }
}
</style>
