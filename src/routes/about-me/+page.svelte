<script>
         let benefits = [
          {name: 'Hometown', description: 'Hello!! Im Stephany Galo 21 years old I live in Morong Bataan'},
          {name: 'About Me', description: ' I am now studying at Gordon College as a 3rd year student Major in Information in technology. Im happy go lucky fersown that brings happiness haha. And im interested in playing online games like valorant and mobile legends.'},
          {name: 'Goal', description: 'My goal is to become a rich auntie for my future niece Keke. kidding aside I want to finish my college and go abroad to help my parents and to buy what I want. And build a computer shop here in my hometown.'},
     ]
</script>
<section id="about" class="py-20 pt-10 lg:pt-16 lg:py-32 flex flex-col
gap-16 sm:gap-20 md:gap-24 relative">
       <div class="flex flex-col gap-2 text-center relative before:absolute before:top-0
       before:left-0 before:w-2/3 before:h-1.5 before:bg-violet-500 after:absolute after:bottom-0
       after:right-0 after:w-2/3 after:h-1.5 after:bg-violet-700 py-4"
       >
       <h6 class="text-lg sm:text-xl md:text-2xl">Want to know more?</h6>
       <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
        A bit <span class="poppins text-violet-700"> about </span> me.</h3>
      </div>
      <p class="mx-auto poppins fontsemi text-lg sm:text-xl md:text-2xl">I am Stephany Galo </p>
      <div class="flex flex-col gap-20 w-full mx-auto max-w-[800px]">
           {#each benefits as benefit, index}
           <div class="flex gap-6 sm:gap-8">
              <p class="poppins text-4xl sm:text-5xl md:text-6xl text-slate-500
                      font-semibold">
                           0{index+1}
                    </p>
                    <div class="flex flex-col gap-6 sm:gap-8">
                      <h3 class="text-2xl sm:text-3xl md:text-5xl">
                          {benefit.name}
                      </h3>
                      <p>{benefit.description}</p>
                    </div>
           </div>
           {/each}

      </div>



</section>