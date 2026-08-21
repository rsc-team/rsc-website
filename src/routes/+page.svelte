<script>
   let sponsors = [
      {url:"/sponsors/rusoe.png",alt:"Rutgers School of Eningeering"},
      {url:"/sponsors/airtech.png",alt:"Rutgers School of Eningeering"},
      {url:"/sponsors/badger.png",alt:"Rutgers School of Eningeering"},
      {url:"/sponsors/bayarea.png",alt:"Rutgers School of Eningeering"},
      {url:"/sponsors/climate.png",alt:"Rutgers School of Eningeering"},
      {url:"/sponsors/endurans.png",alt:"Rutgers School of Eningeering"},
      {url:"/sponsors/gobain.png",alt:"Rutgers School of Eningeering"},
      {url:"/sponsors/gs.png",alt:"Rutgers School of Eningeering"},
      {url:"/sponsors/komo.png",alt:"Rutgers School of Eningeering"},
      {url:"/sponsors/lockheed.png",alt:"Rutgers School of Eningeering"},
      {url:"/sponsors/maxeon.png",alt:"Rutgers School of Eningeering"},
      {url:"/sponsors/mrg.png",alt:"Rutgers School of Eningeering"},
      {url:"/sponsors/pcbway.png",alt:"Rutgers School of Eningeering"},
      {url:"/sponsors/pmc.png",alt:"Rutgers School of Eningeering"},
      {url:"/sponsors/tripower.png",alt:"Rutgers School of Eningeering"},
      {url:"/sponsors/viking.png",alt:"Rutgers School of Eningeering"}
      
   ]
</script>

<div class="h-full w-full align-middle">

   <!-- Logo/Welcome Screen -->
   <div class="relative w-full h-150 lg:h-200 drop-shadow-lg">
      <div class="absolute z-2 user-none w-full h-full max-w-content"> </div>
      <video class="absolute user-none w-full h-full object-cover brightness-50 overflow-hidden" autoplay muted loop>
         <source src="assets/tempbg.mp4" type="video/mp4">
      </video>
      <div class="relative max-w-content justify-center z-2 w-auto top-[50%] translate-y-[-50%] lg:translate-y-[-50%] mx-auto">
         <img class="hidden" src="assets/rscsplash.png" alt="Rutgers Solar Car Logo">
         <p class="text-center  text-red font-sweetsquare font-black drop-shadow-logo text-4xl lg:text-5xl sm:text-5xl ">
            Making fast, sustainable, solar-powered cars
         </p>
      </div>
   </div>


   <!-- About the team -->
   <div class="drop-shadow-lg items-center  overflow-hidden w-full h-250 xl:h-200  bg-gray-600 bg-[url(/assets/sidgrind.webp)]  bg-blend-multiply  bg-position-[13%_70%] bg-no-repeat lg:bg-position-[20%_75%] xl:bg-cover xl:bg-position-[20%_95%] 2xl:bg-position[20%_10%]  flex flex-col justify-center">
      <div class="flex items-center align-middle mt-50 lg:-mt-20 flex-nowrap  flex-col-reverse lg:flex-row xl:pr-25 h-full w-full xl:max-w-content justify-center">
         <img src="assets/sun.webp" alt="Rutgers Solar Car Sun" class="relative top-20 sm:static  xl:static self-center  w-100 h-100">
         <div class="w-full text-xl xl:text-4xl sm:text-3xl flex flex-col self-center mt-20 justify-center text-left p-10 xl:w-200 sm:w-150  drop-shadow-small lg:drop-shadow-med  text-white font-sweetsquare font-black ">
            <p class="pb-15">
               Rutgers Solar Car is a nonprofit, passionate, student-led organization committed to advancing innovation, sustainability, and collaboration in solar-powered vehicle development
            </p>
            <p>
               Through the design, manufacturing, and testing of solar vehicles, we work on developing competitive, road-legal, fully solar-powered race cars.
            </p>
            <a href="/team" class="mt-10 h-10 transition-all not-hover:drop-shadow-logo xl:order-3 self-center w-60">
               <button class="transition-all hover:text-navy text-white  hover:bg-white cursor-pointer p-3 w-full font-black  bg-red text-4xl solar-clip-rectangle">
                  <p class="w-full h-full transition-all  group-hover:drop-shadow-med">Learn More</p>
               </button>
            </a> 
         </div>
      </div>
   </div>

   <!-- Sponsors Preview -->
   <div class="flex flex-col overflow-hidden h-45 bg-navy place-content-center">
      <p class="font-black text-gold text-center pb-5 text-2xl drop-shadow-med">Backed by trusted sponsors</p>
      <div class="self-center relative overflow-hidden whitespace-nowrap  max-w-content [mask-image:_linear-gradient(to_right,_transparent_0,_white_128px,white_calc(100%-128px),_transparent_100%)]">
         {#each {length:2} as _, i}
            <div class="inline-block animate-scrolling w-max">
               {#each sponsors as sponsor}
                  <img class="mx-4 inline h-25" src={sponsor.url} alt={sponsor.alt}>
               {/each}
            </div>
         {/each}
      </div>
   </div>

 </div>
