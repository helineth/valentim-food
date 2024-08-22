<template>
  <q-page class="container q-pa-md row justify-between">
    <q-card class="my-card" flat bordered>
      <q-img
        src="https://minervafoods.com/wp-content/uploads/2023/09/HamburguerAlcatraComBacon_1-scaled.jpg"
      />

      <q-card-section>
        <div class="text-h5 q-mt-sm q-mb-xs">Hambúrguer normal</div>
        <div class="text-caption text-grey">
          Small plates, salads & sandwiches in an intimate setting.
        </div>
      </q-card-section>

      <q-card-actions
        class="flex row justify-center q-gutter-x-lg content-end items-center"
      >
        <q-btn round color="secondary" icon="add" @click="incrementCount()" />
        <p class="text-h5">{{ count }}</p>
        <q-btn round color="primary" icon="remove" @click="decrementCount()" />
        <q-space />
        <q-btn round color="primary" glossy icon="local_grocery_store" />
      </q-card-actions>
    </q-card>
    <q-icon
      name="shopping_cart"
      v-for="size in ['xl']"
      :key="size"
      :size="size"
    />
  </q-page>
</template>

<script setup>
import { computed } from "vue";
import { useCounterStore } from "stores/example-store";

defineOptions({
  name: "DetailPage",
});

const store = useCounterStore();

const count = computed(() => store.counter);

const incrementCount = () => store.increment();
const decrementCount = () => store.counter--;
</script>

<style scoped>
.example-row-all-breakpoints {
  display: flex;
  flex-wrap: wrap;
  gap: 16px;
  justify-content: space-between;
  width: full;
}

.card-container {
  flex: 1 1 calc(33.333% - 16px);
  box-sizing: border-box;
}

.my-card {
  width: 50%;
}
</style>
