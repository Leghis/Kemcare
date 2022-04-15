<template>
  <div class="bg-white">
    <div class="max-w-2xl mx-auto py-16 px-4 sm:py-24 sm:px-6 lg:max-w-7xl lg:px-8">
      <h2 class="text-xl font-bold text-gray-900">Catalogue</h2>

      <div class="mt-8 grid grid-cols-1 gap-y-12 sm:grid-cols-2 sm:gap-x-6 lg:grid-cols-4 xl:gap-x-8">
        <div v-for="product in products" :key="product.id">
          <div class="relative">
            <div class="relative w-full h-72 rounded-lg overflow-hidden">
              <img :src="product.imageSrc" :alt="product.imageAlt" class="w-full h-full object-center object-cover" />
            </div>
            <div class="relative mt-4">
              <h3 class="text-sm font-medium text-gray-900">{{ product.name }}</h3>
              <p class="mt-1 text-sm text-gray-500">{{ product.description }}</p>
            </div>
            <div class="absolute top-0 inset-x-0 h-72 rounded-lg p-4 flex items-end justify-end overflow-hidden">
              <div aria-hidden="true" class="absolute inset-x-0 bottom-0 h-36 bg-gradient-to-t from-black opacity-50" />
              <p class="relative text-lg font-semibold text-white">{{ product.price }}</p>
            </div>
          </div>
          <div class="mt-6">
            <a :href="product.href" class="relative flex bg-gray-100 border border-transparent rounded-md py-2 px-8 items-center justify-center text-sm font-medium text-gray-900 hover:bg-gray-200"
            >Ajouter au panier<span class="sr-only">, {{ product.name }}</span></a
            >
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "ProductComposant",
  data(){
    return{
      products : [
        {
          id: 1,
          name: 'Huile a cheveux',
          description: 'Huile pour aider a la croissance des cheveux',
          href: '#',
          imageSrc: 'https://firebasestorage.googleapis.com/v0/b/kem-care.appspot.com/o/SectionPromoImages%2Fphoto06.jpg?alt=media&token=b5c82b16-f7f7-4411-978b-d933ac28870b',
          imageAlt: 'Front of zip tote bag with white canvas, black canvas straps and handle, and black zipper pulls.',
          price: '7000 FCFA',
        },
        {
          id: 1,
          name: 'Huile a cheveux',
          description: 'Huile pour aider a la croissance des cheveux',
          href: '#',
          imageSrc: 'https://firebasestorage.googleapis.com/v0/b/kem-care.appspot.com/o/SectionPromoImages%2Fphoto07.jpg?alt=media&token=d7975bd3-1f82-4b10-8de0-6684d6bd1a8e',
          imageAlt: 'Front of zip tote bag with white canvas, black canvas straps and handle, and black zipper pulls.',
          price: '7000 FCFA',
        },
        {
          id: 1,
          name: 'Huile a cheveux',
          description: 'Huile pour aider a la croissance des cheveux',
          href: '#',
          imageSrc: 'https://firebasestorage.googleapis.com/v0/b/kem-care.appspot.com/o/SectionPromoImages%2Fphoto05.jpg?alt=media&token=828c290e-c16a-4ca9-afe0-f30795cf30df',
          imageAlt: 'Front of zip tote bag with white canvas, black canvas straps and handle, and black zipper pulls.',
          price: '7000 FCFA',
        },
        {
          id: 1,
          name: 'Huile a cheveux',
          description: 'Huile pour aider a la croissance des cheveux',
          href: '#',
          imageSrc: 'https://firebasestorage.googleapis.com/v0/b/kem-care.appspot.com/o/SectionPromoImages%2Fphoto06.jpg?alt=media&token=b5c82b16-f7f7-4411-978b-d933ac28870b',
          imageAlt: 'Front of zip tote bag with white canvas, black canvas straps and handle, and black zipper pulls.',
          price: '7000 FCFA',
        },
        {
          id: 1,
          name: 'Huile a cheveux',
          description: 'Huile pour aider a la croissance des cheveux',
          href: '#',
          imageSrc: 'https://firebasestorage.googleapis.com/v0/b/kem-care.appspot.com/o/SectionPromoImages%2Fphoto04.jpg?alt=media&token=8517f256-9403-4a57-a6cc-65d9a346f6c3',
          imageAlt: 'Front of zip tote bag with white canvas, black canvas straps and handle, and black zipper pulls.',
          price: '7000 FCFA',
        },
        {
          id: 1,
          name: 'Huile a cheveux',
          description: 'Huile pour aider a la croissance des cheveux',
          href: '#',
          imageSrc: 'https://firebasestorage.googleapis.com/v0/b/kem-care.appspot.com/o/SectionPromoImages%2Fphoto03.jpg?alt=media&token=0ae57e05-50da-408b-8525-e88f75aa7ddc',
          imageAlt: 'Front of zip tote bag with white canvas, black canvas straps and handle, and black zipper pulls.',
          price: '7000 FCFA',
        },
        {
          id: 1,
          name: 'Huile a cheveux',
          description: 'Huile pour aider a la croissance des cheveux',
          href: '#',
          imageSrc: 'https://firebasestorage.googleapis.com/v0/b/kem-care.appspot.com/o/SectionPromoImages%2Fphoto02.jpg?alt=media&token=cb8e84aa-3282-4e63-a809-81757c48d32a',
          imageAlt: 'Front of zip tote bag with white canvas, black canvas straps and handle, and black zipper pulls.',
          price: '7000 FCFA',
        },
        {
          id: 1,
          name: 'Huile a cheveux',
          description: 'Huile pour aider a la croissance des cheveux',
          href: '#',
          imageSrc: 'https://firebasestorage.googleapis.com/v0/b/kem-care.appspot.com/o/SectionPromoImages%2Fphoto01.JPG?alt=media&token=ad1f3e33-a622-40aa-ad0a-85923a8595b5',
          imageAlt: 'Front of zip tote bag with white canvas, black canvas straps and handle, and black zipper pulls.',
          price: '7000 FCFA',
        },
        // More products...
      ]
    }
  }
}
</script>

<style scoped>

</style>