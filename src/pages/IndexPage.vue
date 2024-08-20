<template>
  <q-page>
    <ExampleComponent title="Example component" active :items="items" />
  </q-page>
</template>

<script setup>
import ExampleComponent  from "src/components/ExampleComponent.vue";
defineOptions({
  name: "IndexPage",
});

const items = [
  {
    id:"1",
    name: "Hambúrguer normal",
    description: "Small plates, salads & sandwiches in an intimate setting.",
    image:
      "https://minervafoods.com/wp-content/uploads/2023/09/HamburguerAlcatraComBacon_1-scaled.jpg",
    price: "2.500,00 Kz",
  },
  {
    id: "2",
    name: "Hambúrguer duplo",
    description: "Small plates, salads & sandwiches in an intimate setting.",
    image:
      "https://img.freepik.com/fotos-premium/hamburguer-de-carne-com-hamburguer-duplo-e-duas-camadas-de-delicioso-queijo-derretido-por-cima_124507-37487.jpg",
    price: "5.500,00 Kz",
  },
  {
    id: "3",
    name: "Dose de batatas",
    description: "Small plates, salads & sandwiches in an intimate setting.",
    image:
      "https://conteudo.imguol.com.br/c/entretenimento/a0/2018/02/26/batata-frita-1519671488107_v2_4x3.jpg",
    price: "800,00 Kz",
  },
  {
    id: "4",
    name: "Dose de banana",
    description: "Small plates, salads & sandwiches in an intimate setting.",
    image:
      "https://www.laylita.com/receitas/wp-content/uploads/2014/08/Chifles-Salgadinhos-de-banana-verde-frita.jpg",
    price: "900,00 Kz",
  },
  {
    id: "5",
    name: "Fahita de frango",
    description: "Small plates, salads & sandwiches in an intimate setting.",
    image:
      "https://i.ytimg.com/vi/lMvHQPBOAfg/hq720.jpg?sqp=-oaymwEhCK4FEIIDSFryq4qpAxMIARUAAAAAGAElAADIQj0AgKJD&rs=AOn4CLBHhpVPfdNr7N3nPJuUWnHm0WJHTA",
    price: "3.500,00 Kz",
  },
  {
    id: "6",
    name: "Fahita de carne",
    description: "Small plates, salads & sandwiches in an intimate setting.",
    image: "https://sandar.co.ao/upload/1687950688-images%20CAR.jpg",
    price: "4.000,00 Kz",
  },
  {
    id: "7",
    name: "Bolo no pote de chocolate",
    description: "Small plates, salads & sandwiches in an intimate setting.",
    image:
      "https://guiadacozinha.com.br/wp-content/uploads/2019/10/bolo-leite-ninho-nutella-potinho-768x619.jpg",
    price: "1.500,00 Kz",
  },
  {
    id: "8",
    name: "Bolo no pote outros sabores",
    description: "Small plates, salads & sandwiches in an intimate setting.",
    image:
      "https://assets.delirec.com/images%2F92IzaQ9utTd5FOLcoq7OazC92HG3%2Frecipe%2Fc03a8604-f383-48fd-bb97-53cc842ae367-Bolo-no-Pote-gallery-0",
    price: "1.300,00 Kz",
  },
];
</script>
