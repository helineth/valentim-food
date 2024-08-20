<template>
  <div

    class=" example-row-all-breakpoints"
  >
    <div
      v-for="item in props.items"
      :key="item?.id"
      class="q-pa-md "
    >
      <q-card class="my-card" flat bordered>
        <q-img
          style="max-height: 237px; min-height: 237px"
          :src="item?.image"
        />

        <q-card-section>
          <q-btn
            fab
            color="primary"
            icon="place"
            class="absolute"
            style="top: 0; right: 12px; transform: translateY(-50%)"
          />

          <div class="row no-wrap items-center">
            <div class="col text-h6 ellipsis">{{ item?.name }}</div>
            <div
              class="col-auto text-grey text-caption q-pt-md row no-wrap items-center"
            >
              <q-icon name="place" />
              250 ft
            </div>
          </div>
        </q-card-section>

        <q-card-section class="q-pt-none">
          <div class="text-subtitle1">{{ item.price }}</div>
          <div class="text-caption text-grey">
            {{ item.description }}
          </div>
        </q-card-section>

        <q-separator />

        <q-card-actions>
          <q-btn flat round icon="event" />

          <q-btn flat color="primary" to="/detail"> Reservar </q-btn>
        </q-card-actions>
      </q-card>
    </div>
  </div>
</template>

<script setup>
defineOptions({
  name: "ExampleComponent",
});

const props = defineProps({
  title: {
    type: String,
    default: "",
  },

  items: {
    type: Array,
    default: () => [],
  },
});
</script>

<style scoped>
.example-row-all-breakpoints {
  display: flex;
  flex-wrap: wrap;
  gap: 16px;
justify-content: space-between;
  width: full ;
}

.card-container {
  flex: 1 1 calc(33.333% - 16px);
  box-sizing: border-box;

}

.my-card {
  width: 100%;
}

</style>
