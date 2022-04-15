<template>
  <div class="home">
    <SectionComponent/>
    <ProductComposant/>
    <div class="bg-white">
      <div class="max-w-7xl mx-auto px-4 py-24 sm:px-6 lg:px-8">
        <div class="bg-gray-200 rounded-2xl px-6 py-16 sm:p-16">
          <div class="max-w-xl mx-auto lg:max-w-none">
            <div class="text-center">
              <h2 class="text-xl font-extrabold tracking-tight text-gray-900">Nous avons bâti notre entreprise sur le service à la clientèle</h2>
            </div>
            <div class="mt-12 max-w-sm mx-auto grid grid-cols-1 gap-y-10 gap-x-8 sm:max-w-none lg:grid-cols-3">
              <div v-for="incentive in incentives" :key="incentive.name" class="text-center sm:flex sm:text-left lg:block lg:text-center">
                <div class="sm:flex-shrink-0">
                  <div class="flow-root">
                    <img class="w-16 h-16 mx-auto" :src="incentive.imageSrc" alt="" />
                  </div>
                </div>
                <div class="mt-3 sm:mt-0 sm:ml-6 lg:mt-6 lg:ml-0">
                  <h3 class="text-sm font-medium text-gray-900">
                    {{ incentive.name }}
                  </h3>
                  <p class="mt-2 text-sm text-gray-500">
                    {{ incentive.description }}
                  </p>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import SectionComponent from "@/components/SectionComponent";
import recycling from '../assets/img/recycling.svg'
import ProductComposant from "@/components/ProductComposant";
export default {
  name: 'HomeView',
  data(){
    return{
      incentives : [
        {
          name: 'Livraison Rapide',
          imageSrc: 'https://tailwindui.com/img/ecommerce/icons/icon-shipping-simple.svg',
          description: "Une fois votre produit commandé vous serez livrer rapidement",
        },
        {
          name: 'Service client disponible',
          imageSrc: 'https://tailwindui.com/img/ecommerce/icons/icon-warranty-simple.svg',
          description: "Notre service client est disponible pour vous a tout l'heure de la journée",
        },
        {
          name: 'Remise',
          imageSrc: recycling,
          description:
              "Pour chaque bouteille que vous nous faites revenir nous vous faisons une réductions de 5% sur vos prochains achat de produit",
        },
      ]
    }
  },
  components: {
    SectionComponent,
    ProductComposant
  }
}
</script>
