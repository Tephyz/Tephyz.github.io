<script>
    import Step from "./Step.svelte";

    let steps = [
      {name: 'EVENT SNAP', icon: 'fa-solid fa-calendar-days'},
      {name: 'Calculator', icon: 'fa-solid fa-calculator'},
      {name: 'E-commerce', icon: 'fa-brands fa-shopify'},


    ];
</script>

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