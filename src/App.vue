<script setup>
function greet() {
  var container = document
    .querySelectorAll(".snap-container .snap-wrapper")
    .forEach((n) => n.classList.remove("snap-wrapper"));
  // var elements = container.getElementsByClassName(".snap-wrapper");
  console.log("element", container);
}
</script>

<template>
  <!-- scroll snap -->
  <div class="">
    <div class="">
      <div
        class="snap-container flex gap-5 snap-x snap-mandatory h-48 w-screen overflow-scroll"
        @mouseover="greet"
      >
        <div
          class="snap-wrapper ml-[500px] snap-center shrink-0 rounded-md shadow-md bg-amber-200 grid w-[400px] h-48 place-items-center text-8xl"
        >
          1
        </div>
        <div
          class="snap-wrapper snap-center shrink-0 rounded-md shadow-md bg-blue-200 grid w-[400px] h-48 place-items-center text-8xl"
        >
          2
        </div>
        <div
          class="snap-wrapper snap-center shrink-0 rounded-md shadow-md bg-orange-200 grid w-[400px] h-48 place-items-center text-8xl"
        >
          3
        </div>
        <div
          class="snap-wrapper snap-center shrink-0 rounded-md shadow-md bg-green-200 grid w-[400px] h-48 place-items-center text-8xl"
        >
          4
        </div>
        <div
          class="snap-wrapper snap-center shrink-0 rounded-md shadow-md bg-amber-200 grid w-[400px] h-48 place-items-center text-8xl"
        >
          5
        </div>
        <div
          class="snap-wrapper snap-center shrink-0 rounded-md shadow-md bg-blue-200 grid w-[400px] h-48 place-items-center text-8xl"
        >
          6
        </div>
        <div
          class="snap-wrapper snap-center shrink-0 rounded-md shadow-md bg-orange-200 grid w-[400px] h-48 place-items-center text-8xl"
        >
          7
        </div>
        <div
          class="snap-wrapper snap-center shrink-0 rounded-md shadow-md bg-green-200 grid w-[400px] h-48 place-items-center text-8xl"
        >
          8
        </div>
      </div>
    </div>
  </div>
</template>
<style scope>
.snap-wrapper {
  white-space: nowrap;
  animation: slide infinite 15s linear;
}

@keyframes slide {
  0% {
    transform: translateX(0);
  }
  100% {
    transform: translateX(-800%);
  }
}

.snap-container:hover > .snap-wrapper {
  animation-play-state: paused;
  animation-fill-mode: forwards;
}
</style>
