<template>
  <div class="py-24 sm:py-32 bg-gray-50" id="testimonials">
    <div class="mx-auto px-4 sm:px-6 lg:px-8 max-w-7xl gap-16 sm:gap-y-24 flex flex-col">
      <div class="text-center flex flex-col items-center">
        <div class="mb-2 text-base/7 font-semibold text-primary">Testimonials</div>
        <h2 class="text-3xl font-bold tracking-tight text-gray-900 dark:text-white sm:text-4xl lg:text-5xl">How people are
          using the take a break app.</h2>
        <p class="mt-6 text-lg/8 text-gray-600 dark:text-gray-300">Proident sunt exercitation minim laborum enim
          laboris labore esse.</p>
      </div>
      <div class="column-1 md:columns-2 lg:columns-3 gap-8 space-y-8">
        <div v-for="testimonial in testimonials " class="break-inside-avoid">
          <div
            class="overflow-hidden rounded-lg divide-y divide-gray-200 dark:divide-gray-800 ring-1 ring-gray-200 dark:ring-gray-800 shadow bg-white dark:bg-gray-900 relative group">

            <div class="flex-1 px-4 py-5 sm:p-6">
              <div class="flex py-2">
                <Icon class="text-primary h-6 w-6" v-for="i in testimonial.stars" name="ph:star-fill" />
              </div>
              <q class="italic text-lg text-gray-500 dark:text-gray-400">{{ testimonial.quote }}</q>
            </div>
            <div class="px-4 py-4 sm:px-6">
              <div class="flex items-center gap-3"><span
                  class="relative inline-flex items-center justify-center flex-shrink-0 rounded-full h-10 w-10 text-base"><img
                    class="rounded-full h-10 w-10 text-base" :alt="testimonial.name" :src="testimonial.avatar"
                    loading="lazy"></span>
                <div class="text-sm">
                  <p class="font-medium text-gray-900 dark:text-white">{{ testimonial.name }}</p>
                  <p class="text-gray-500 dark:text-gray-400">{{ testimonial.position }}</p>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
interface Testimonial {
  stars: number,
  name: string,
  position: string,
  quote: string,
  avatar: string,
}

const testimonials: Array<Testimonial> = [
  {
    stars: 5,
    name: "Emily Chang",
    position: "Student",
    quote: "I've tried several meditation apps, and this one stands out for its simplicity and effectiveness. The variety of meditation styles keeps things interesting, and the progress tracker motivates me to stay consistent. It's like having a personal zen coach in my pocket!",
    avatar: "https://i.pravatar.cc/300?img=5",
  },
  {
    stars: 4,
    name: "Alex Rodriguez",
    position: "Tech Professional",
    quote: "As someone constantly juggling deadlines and high-pressure situations, this meditation app has been a game-changer. The quick, focused sessions help me reset and approach challenges with a calmer mindset. The interface is user-friendly, making it easy to integrate into my busy schedule.",
    avatar: "https://i.pravatar.cc/300?img=11",
  },
  {
    stars: 5,
    name: "Sophie Thompson",
    position: "Yoga Instructor",
    quote: "The meditation app has transformed my daily routine. The variety of guided sessions caters to my mood, and the soothing voices make it a truly immersive experience. My mindfulness practice has reached new heights, thanks to this app!",
    avatar: "https://i.pravatar.cc/300?img=23",
  }
]
</script>