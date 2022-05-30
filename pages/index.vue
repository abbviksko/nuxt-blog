<template>
<body>

     <div>


       <div>

         <div>
            <img src="../static/images/namnlos.png">
         </div>
             <div class="z-10 justify-center items-center flex flex-col text-5xl font-mono right-1/4 h-24 " style="background-color:#dfdfdf;" >
             <img class="right-64 top-18vh h-16" src="../static/images/rubrik.png" alt="">



               <h2 style="height:20px; width:30%;" class="under"></h2>
             </div>





           <div class=" z-10 absolute">

        <div style="margin-top:10vh;" >

        <div class="flex justify-start" style="margin-left:5%;">
          <me/>
        </div>

        <div class="flex justify-end" style="margin-right:5%; margin-top:3%;">
          <lucas/>
        </div>

      </div >
      <div class="mt-16">
      <blogpath/>
     </div>
            </div>

         <div>
          <img class="z-0 relative" src="../static/images/background3.png">
           <img class="z-0 relative" src="../static/images/background4.png">

        </div>

        <!-- <div style="background-image: url(../static/images/background2.png); width:100%" class="bg-fixed top-151 left-0 z-0">
          <img src="../static/images/background2.png">
        </div> -->



       </div>






</div>
</body>

</template>

 <style>
 body{
   /* background-color:#dfdfdf */
   background:url(../static/images/background-picture.jpg) fixed center;
   /* max-width:max-content; */
   width: 100%;


 }



.halfmoonShape {
width: full;
}

 </style>

<script>
import lucas from '../components/lucas.vue'
import me from '../components/me.vue'

export default {
  name: 'IndexPage',
  components: {
    me,

    lucas,

}
}

</script>








