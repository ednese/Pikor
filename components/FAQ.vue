<script setup lang="ts">
const faqs = [
  {
    question: "Comment Pikor sélectionne-t-il les articles ?",
    answer: "Notre intelligence artificielle analyse une large variété de sources fiables pour identifier les actualités les plus pertinentes et intéressantes, qui vous sont ensuite présentées de manière claire et concise."
  },
  {
    question: "Pikor est-il gratuit à utiliser ?",
    answer: "Oui, Pikor est entièrement gratuit. Tous nos contenus sont disponibles directement sur notre compte Instagram, sans frais ni abonnement."
  },
  {
    question: "Sur quels sujets Pikor propose-t-il des résumés ?",
    answer: "Pikor couvre une large gamme de sujets : actualité mondiale, technologie, culture, économie et bien plus encore, pour que vous restiez informé des sujets qui comptent."
  }
];
</script>

<template>
  <section id="faq" class="text-black py-20">
    <Container>
      <SectionTitle>
        Questions fréquentes
        <template #description>Tout ce que vous devez savoir pour profiter pleinement de Pikor.</template>
      </SectionTitle>
      
      <div class="flex flex-wrap justify-center gap-8 mt-12">
        <div 
          v-for="(faq, index) in faqs" 
          :key="index"
          :class="[
            'bg-gray-100 p-6 rounded-lg w-full max-w-[600px]',
            { 'md:w-[calc(50%-1rem)]': index < 2,
              'md:w-full': index === 2 }
          ]"
        >
          <h3 class="text-xl font-bold mb-2">{{ faq.question }}</h3>
          <p class="text-gray-600">
            {{ faq.answer }}
          </p>
        </div>
      </div>
    </Container>
  </section>
</template>