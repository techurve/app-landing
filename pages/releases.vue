<template>
  <div class="mt-16 mx-auto w-2/4">
    <div class="mb-20 flex justify-between items-center">
      <div>
        <h1 class="text-5xl font-bold text-gray-700">What's New</h1>
        <p>Do we have a cooling cream</p>
      </div>
      <Icon class="h-28 w-28 text-gray-300" name="uim:layer-group" />
    </div>
    <div class="flex flex-col gap-5 mb-10">
      <ContentList path="/releases" v-slot="{ list }">
        <div class="flex items-center gap-4" v-for="article in list" :key="article._path">
          <img class="border rounded-lg w-72 h-32 object-cover" src="/take_a_break.png" />
          <div>
            <h2 class="text-2xl font-bold text-gray-800">{{ article.title }}</h2>
            <p class="text-gray-600 text-sm mt-2">{{ article.description }}</p>
          </div>
        </div>
      </ContentList>
    </div>
  </div>
</template>
