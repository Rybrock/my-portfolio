<script>
  import "../app.css";
  import Header from "../components/Header.svelte";
  import Footer from "../components/Footer.svelte";

  export let children;

  let y = 0;
  let innerHeight = 0;
  let innerWidth = 0;

  function toTop() {
    document.body.scrollIntoView();
  }
</script>

<div class="relative flex flex-col max-w-[1400px] mx-auto text-sm sm:text-base min-h-screen">
  <div class={"fixed bottom-0 w-full duration-200 flex p-10 z-[10] " + (y > 0 ? "opacity-full pointer-events-auto" : "pointer-events-none opacity-0")}>
    <button onclick={toTop} name="arrow-up" aria-label="arrow-up" class="ml-auto rounded-full bg-slate-900 text-sky-400 px-3 sm:px-4 hover:bg-slate-800 cursor-pointer">
      <i class="fa-solid fa-arrow-up grid place-items-center aspect-square" />
    </button>
  </div>
  <Header {y} />
  {@render children()}

  <Footer />
</div>

<svelte:window bind:scrollY={y} bind:innerHeight bind:innerWidth />