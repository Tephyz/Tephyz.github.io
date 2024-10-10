<script>
    import Step from "./Step.svelte";

    let steps = [
      {name: 'EVENT SNAP', icon: 'fa-solid fa-calendar-days'},
      {name: 'Calculator', icon: 'fa-solid fa-calculator'},
      {name: 'E-commerce', icon: 'fa-brands fa-shopify'},


    ];
    
     let benefits = [
          {name: 'Hometown', description: 'Hello!! Im Stephany Galo 21 years old I live in Morong Bataan'},
          {name: 'About Me', description: ' I am now studying at Gordon College as a 3rd year student Major in Information in technology. Im happy go lucky fersown that brings happiness haha. And im interested in playing online games like valorant and mobile legends.'},
          {name: 'Goal', description: 'My goal is to become a rich auntie for my future niece Keke. kidding aside I want to finish my college and go abroad to help my parents and to buy what I want. And build a computer shop here in my hometown.'},
     ]
</script>

<main class="flex flex-col flex-1 p-4">
    <section 
        id="introPage" class="grid grid-cols-1 lg:grid-cols-2 gap-10 py-8 sm:py-14">
        <div 
              class="flex flex-col lg:justify-center text-center lg:text-left gap-6 md:gap-8 
              lg:gap-10">

          <h2 class="font-semibold text-4xl sm:text-5xl md:text-6xl">
            Hi! I'm <span class="poppins text-violet-400">Stephany</span> Galo <br/> Major in
            <span class="poppins text-violet-400">Information Technology</span>
          </h2>
          
          <a class="blueShadow mx-auto lg:mr-auto text-base sm:text-lg md:text-xl poppins
          relative overflow-hidden px-6 py-3 group rounded-full bg-white text-slate-950">
            <div 
              class="absolute top-0 right-full w-full h-full bg-violet-400 opacity-20 group-hover:translate-x-full z-0 duration-200"></div>
            <h4 class="relative z-9">Get in touch &rarr;</h4>
          </a>
        </div>
        <div class="relative shadow-2xl flex justify-center bg-slate-950 overflow-hidden">
             <img src="images/Profile.png" alt="Profile image"
             class="object-cover z-[2] max-h-[70vh]"/>
        </div>
      </section>


      <section id="projects" class="py-20 lg:py-32 flex flex-col gap-24">
        <div class="flex flex-col gap-2 text-center"></div>
            
            <h3 class="font-semibold text-3xl sm:text-4 md:text-5xl">
                Curious to <span class="poppins text-violet-400">see</span> my
                work?
            </h3>
            <a href="https://youtu.be/_6q3ocr9I5Q?si=lsmCy-wXfeByXgPe"
            target="_blank" class="mx-auto px-4 py-2 rounded-md border
            border-solid border-white flex items-center gap-2 -mb-4 sm:-mb-0
            -mt-10 hover:border-violet-700 duration-200">
                <i class="fa-regular fa-circle-play"></i>
                <p>Watch the video</p>
          </a>
          <div class="grid grid-cols-1 lg:grid-cols-3 gap-12 lg:gap-10">
            <Step step={steps[0]}>
              <strong class="text-violet-400"></strong>
                <p>Event Snap aims to attendance tracking for various activities by implementing a sophisticated Registration Attendance System. 
                  This system utilizes image processing technology to automate the registration and verification process seamlessly.
                   Attendees will interact with a user-friendly interface that simplifies the selection of events, departments and courses.</p>
            </Step>
            <Step step={steps[1]}>
              <strong class="text-violet-400"></strong>
                <p>is an mobile application that created with Python and JavaScript</p>
            </Step>
            <Step step={steps[2]}>
              <strong class="text-violet-400"></strong>
              <p>An e-commerce platform is a digital marketplace where businesses and consumers can buy and sell products or services online.
                 These platforms typically provide features like product catalogs, shopping carts, payment gateways, 
                 order tracking, and customer reviews. </p>
            </Step>
          </div>
      </section>
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
</main>