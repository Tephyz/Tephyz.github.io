<script>
  import "../app.css";

  let y = 0;
  let innerWidth = 0;
  let innerHeight = 0;

  function goTop() {
      document.body.scrollIntoView();
  }

  // Sample tabs array for demonstration (if not already defined in Header)
  let tabs = [
      { name: "Home", link: "/" },
      { name: "Portfolio", link: "/portfolio" },
      { name: "About", link: "/about-me" },
      { name: "Contact", link: "/contact" }
      
  ];
</script>

<div class="relative flex flex-col max-w-[1900px] max-auto w-full text-sm sm:text-base min-h-screen">
  <!-- Top Scroll Button -->
  <div class={"fixed botton-0 w-full duration-200 flex p-10 z-[10] " + 
      ( y > 0 
          ? "opacity-full pointer-events-auto" 
          : "pointer-events-none opacity-0")}
  > 
      <button on:click={goTop} class="ml-auto rounded-full bg-slate-900 text-violet-400 px-3 sm:px-4 hover:bg-slate-800 cursor-pointer">
          <i class="fa-solid fa-arrow-up grid place-items-center aspect-aquare"></i>
      </button>
  </div>

  <!-- Header Code -->
  <header 
      class={'sticky z-[10] top-0 duration-200 px-6 flex items-center justify-between border border-solid ' + 
      ( y > 0 
          ? " py-4 bg-slate-950 border-violet-950" 
          : " py-6 bg-transparent border-transparent")}
  >
      <h1 class="font-medium">
          <b class="font-bold poppins">Stephany</b> Galo
      </h1>
      <div class="sm:flex ml-auto pr-4 items-center gap-4 hidden">
          {#each tabs as tab, index}  
              <a href={tab.link} class="duration-200 hover:text-violet-400">
                  <p>{tab.name}</p>
              </a>
          {/each}
      </div>
      <a 
          href="/" 
          target="_self"
          class="blueShadow relative overflow-hidden px-5 py-2 group rounded-full bg-white 
          text-slate-950"
      > 
          <div 
              class="absolute top-0 right-full w-full h-full bg-violet-400 opacity-20 group-hover:translate-x-full z-0 duration-200"
          />
          <h4 class="relative z-9">Get in touch</h4>
      </a>
  </header>

  
  <slot />

</div>

<svelte:window bind:scrollY={y} bind:innerHeight bind:innerWidth />
