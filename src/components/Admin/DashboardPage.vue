<script setup lang="ts">
import AttendanceChart from "./DashboardPage/AttendanceChart.vue";
import AttendanceTime from "@/components/Admin/DashboardPage/AttendanceTime.vue";
</script>
<template>
 <div class="grid grid-cols-2 gap-4">
    <div id="default-carousel" class="w-full mt-5" data-carousel="slide">
    <!-- Carousel wrapper -->
    <div class="relative w-full h-auto mx-auto overflow-hidden rounded-lg md:h-full">
         <!-- Item 1 -->
        <div class="hidden duration-700 ease-in-out" data-carousel-item>
            <img src="../../assets/beach.jpg" class="w-screen h-auto " alt="...">
        </div>
        <!-- Item 2 -->
        <div class="hidden duration-700 ease-in-out" data-carousel-item>
            <img src="../../assets/beach2.jpg" class="w-screen h-auto " alt="...">
        </div>
        <!-- Item 3 -->
        <div class="hidden duration-700 ease-in-out" data-carousel-item>
            <img src="../../assets/capitol.jpg" class="w-screen h-auto " alt="...">
        </div>
        <!-- Item 4 -->
        <div class="hidden duration-700 ease-in-out" data-carousel-item>
            <img src="../../assets/download (1).jpg" class="w-screen h-auto " alt="...">
        </div>
        <!-- Item 5 -->
    
    </div>
    
    <!-- Slider indicators -->
</div>
<div class="z-50 w-full">
  <AttendanceChart />
</div>

<div class="z-50 w-full">
  <AttendanceTime />
</div>

</div>



  

  
 
</template>