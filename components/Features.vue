<script setup lang="ts">
const features = [
  {
    title: 'Simplifier votre accès à l\'actualité',
    description:
      'Notre intelligence artificielle filtre et synthétise des milliers d\'articles chaque jour pour vous proposer uniquement les informations essentielles. Vous accédez ainsi à un contenu clair et précis en un clin d\'œil.',
    image: '/img/feature_1.jpg',
    alt: 'Feature 1',
    layout: 'imageFirst',
    fullWidth: false,
  },
  {
    title: 'Restez informé de l\'actu accessible partout',
    description:
      'Avec Pikor découvrez des articles courts et percutants disponibles directement sur Instagram. Que vous soyez chez vous, dans les transports ou en pause, l\'information est toujours à portée de main.',
    image: '/img/feature_2.jpg',
    alt: 'Feature 2',
    layout: 'imageFirst',
    fullWidth: false,
  },
  {
    title: 'Un contenu concis et percutant pour aller à l\'essentiel',
    description:
      'Pikor utilise les dernières avancées en matière d\'intelligence artificielle pour rendre l\'actualité plus accessible. Chaque article est synthétisé pour vous offrir une lecture rapide, tout en conservant l\'essence de l\'information.',
    image: '/img/feature_3.jpg',
    alt: 'Feature 3',
    layout: 'textFirst',
    fullWidth: true,
  },
];
</script>

<template>
  <section id="features" class="bg-white text-black py-20">
    <Container class="max-w-[928px]">
      <SectionTitle>
        Découvrez Pikor
        <template #description>
          Découvrez l'avenir de l'informations avec Pikor, votre application de référence pour des résumés de contenu concis et pertinents.
        </template>
      </SectionTitle>

      <div class="grid grid-cols-1 md:grid-cols-2 gap-8 mt-12">
        <div
          v-for="(feature, index) in features"
          :key="index"
          :class="[
            'p-6 lg:p-10 bg-gray-100 rounded-lg',
            feature.fullWidth ? 'md:col-span-2' : ''
          ]"
        >
          <div v-if="feature.layout === 'textFirst'" class="flex flex-col md:flex-row md:items-center">
            <div class="md:w-1/2">
              <h3 class="text-xl mb-4">{{ feature.title }}</h3>
              <p class="text-gray-600 mb-4 md:mb-0">{{ feature.description }}</p>
            </div>
            <div class="md:w-1/2 md:pl-6">
              <img :src="feature.image" :alt="feature.alt" class="rounded-lg w-full" />
            </div>
          </div>
          <div v-else>
            <h3 class="text-xl mb-4">{{ feature.title }}</h3>
            <p class="text-gray-600 mb-4">{{ feature.description }}</p>
            <img :src="feature.image" :alt="feature.alt" class="rounded-lg w-full" />
          </div>
        </div>
      </div>
    </Container>
  </section>
</template>
