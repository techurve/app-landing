<template>
  <div class="bg-white" id="faq">
    <div class="mx-auto max-w-7xl px-6 py-16 sm:py-24 lg:px-8">
      <h2 class="text-2xl font-bold leading-10 tracking-tight text-gray-900">Frequently asked questions</h2>
      <p class="mt-6 max-w-2xl text-base leading-7 text-gray-600">Have a different question and can’t find the answer
        you’re looking for? Reach out to our support team by <a href="#"
          class="font-semibold text-primary-600 hover:text-primary-500">sending us an email</a> and we’ll get back to you
        as
        soon as we can.</p>
      <div class="mt-20">
        <dl class="space-y-16 sm:grid sm:grid-cols-2 sm:gap-x-6 sm:gap-y-16 sm:space-y-0 lg:grid-cols-3 lg:gap-x-10">
          <div v-for="faq in faqs" :key="faq.id">
            <dt class="text-base font-semibold leading-7 text-gray-900">{{ faq.question }}</dt>
            <dd class="mt-2 text-base leading-7 text-gray-600">{{ faq.answer }}</dd>
          </div>
        </dl>
      </div>
    </div>
  </div>
</template>

<script setup>
const faqs = [
  {
    id: 1,
    question: "How do I get started with the take a break app?",
    answer: "Getting started is easy! Simply download the app from the app store, create an account, and explore our library of guided meditation sessions. You'll find a variety of options to suit your preferences and goals.",
  },
  {
    id: 2,
    question: "Can I use the meditation app as a beginner?",
    answer: "Absolutely! The app is designed for users of all experience levels. We offer beginner-friendly sessions to help you ease into meditation and build a consistent practice. You'll find guidance and support every step of the way.",
  },
  {
    id: 3,
    question: "Is there a cost associated with the meditation app?",
    answer: "The basic version of the app is free and includes a variety of meditation sessions. We also offer a premium subscription with additional features and a wider range of content. You can choose the option that best fits your needs.",
  },
  {
    id: 4,
    question: "Are the meditation sessions guided or unguided?",
    answer: "Our app offers both guided and unguided meditation sessions. You can choose based on your preference. The guided sessions provide step-by-step instructions, while unguided sessions allow for a more independent practice with ambient sounds or music.",
  },
  {
    id: 5,
    question: "Can I use the meditation app offline?",
    answer: "Yes, you can! Once you've downloaded the meditation sessions, you can access them offline. This is perfect for times when you don't have an internet connection or want to meditate in a peaceful, disconnected environment.",
  },
  {
    id: 6,
    question: "How long are the typical meditation sessions?",
    answer: "Our meditation sessions vary in length to accommodate different schedules and preferences. You'll find sessions ranging from quick 5-minute mindfulness exercises to longer, more immersive sessions. Choose what fits your time and needs best!",
  }
  // More questions...
]
</script>