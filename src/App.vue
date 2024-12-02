<template>
  <form class="group">
    <fieldset
      v-for="step in 3"
      :id="`step-${step}`"
      class="bg-amber-200 place-content-center justify-items-center target:visible relative hidden group-[:not(:has(:target))]:[&[id='step-1']]:block target:block h-0 [&[id='step-1']]:h-screen target:h-screen"
    >
      <legend class="contents text-7xl font-bold font-mono">
        <h1>Step {{ step }}</h1>
      </legend>
      <a
        v-if="step > 1"
        :href="`#step-${step - 1}`"
        class="rounded-full bg-slate-950 text-emerald-50 p-4 absolute bottom-2 min-w-12 leading-0 aspect-square left-2 place-content-center text-2xl"
      >
        <span class="sr-only">Previous</span>
        &larr;
      </a>
      <a
        v-if="step <= 3"
        :href="`#step-${step + 1}`"
        class="rounded-full bg-slate-950 text-emerald-50 p-4 absolute bottom-2 min-w-12 leading-0 aspect-square right-2 place-content-center text-2xl"
      >
        <span class="sr-only">Next</span>
        &rarr;
      </a>
    </fieldset>
  </form>
</template>
