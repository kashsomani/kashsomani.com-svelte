<script>
  import { fade } from "svelte/transition"
  // $: flags = [false, false, false]
  // let counter = 0
  // let next = ()=>{
  //   flags[counter++] = true;
  // }
  $: borderActive = false
</script>

<div
  class=" detail px-4 text-primary py-8 text-center {borderActive ? 'detail-active' : ''}"
  id="experience"
  transition:fade={{ y: 200, duration: 1000 }}
  on:introend={() => (borderActive = true)}
>
  <div class="detail-header">
    <h1 class="text-2xl font-semibold lg:text-4xl">Experience</h1>
  </div>
  <div class="grid grid-cols-1  gap-0 place-items-center lg:text-xl">
    <div>
      <div class="pt-16" id="techstart">
        <h1 class="text-lg xl:text-2xl text-tertiary font-semibold">
          TECHSTART INTERN (WEB DEVLOPMENT)
        </h1>
        <p class="text-xs font-semibold lg:text-lg xl:text-xl">LIBERTY MUTUAL, PORTSMOUTH, NH</p>
        <div class="text-left px-4 md:text-lg xl:text-2xl ">
          <p>
            <span class="text-tertiary">•</span> Developed REST APIs to facilitate the
            construction of a company made ticket management system
          </p>
          <p>
            <span class="text-tertiary">•</span> Constructed a frontend UI in Vue.js
            to enable users to query and test the built APIs
          </p>
          <p>
            <span class="text-tertiary">•</span> The work included constant collaboration
            with other team members, and I had the experience to work in AGILE for the
            first time
          </p>
        </div>
      </div>
    
      <div class="pt-4" id="learners">
        <h1 class="text-lg xl:text-2xl text-tertiary font-semibold">
          COMPUTER SCIENCE TEACHER
        </h1>
        <p class="text-xs font-semibold lg:text-lg xl:text-xl">LEARNERS ACADEMY, MUMBAI, INDIA</p>
        <div class="text-left px-4 md:text-lg xl:text-2xl">
          <p>
            <span class="text-tertiary">•</span> Taught core Java to 9th and 10th graders
          </p>
          <p>
            <span class="text-tertiary">•</span> Administered and graded tests. Aided
            students with ICSE board projects
          </p>
          <p>
            <span class="text-tertiary">•</span> Designed a new course structure to comply
            with the changing ICSE syllabus
          </p>
        </div>
      </div>
    
      <div class="pt-4" id="web-dev">
        <h1 class="text-lg xl:text-2xl text-tertiary font-semibold">
          WEB DEVELOPER
        </h1>
        <p class="text-xs font-semibold lg:text-lg xl:text-xl">LEARNERS ACADEMY, MUMBAI, INDIA</p>
        <div class="text-left px-4 md:text-lg xl:text-2xl">
          <p>
            <span class="text-tertiary">•</span> Created and Deployed the company's main website
          </p>
          <p><span class="text-tertiary">•</span> Used Svelte and Firebase for the first time</p>
          <p>
            <span class="text-tertiary">•</span> Ensured that component based architure was followed to ease development with colleague 
          </p>
        </div>
      </div>
      <div class="pt-4" id="uca">
        <h1 class="text-lg xl:text-2xl text-tertiary font-semibold">
          UNDERGRATUATE COURSE ASSISTANT
        </h1>
        <p class="text-xs font-semibold lg:text-lg xl:text-xl">UNIVERSITY OF MASSACHUSETTS - AMHERST</p>
        <div class="text-left px-4 md:text-lg xl:text-2xl">
          <p>
            <span class="text-tertiary">•</span> Developing content in coordination with
            instructors to better help students grasp basic concepts.
          </p>
          <p><span class="text-tertiary">•</span> Leading lab assignments</p>
          <p>
            <span class="text-tertiary">•</span> Leading small group discussions
          </p>
          <p>
            <span class="text-tertiary">•</span> Grading class assignments (including
            exams)
          </p>
        </div>
      </div>
    </div>
  </div>

</div>