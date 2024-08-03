<script setup>
import Card from '@/components/Card.vue'


</script>

<template>
   <section class="py-4 bg-black/20">
      <div class="container-xl lg:container m-auto">
        <div class="grid grid-cols-1 md:grid-cols-2 gap-4 p-4 rounded-lg">
          <Card bg="bg-white" title="For Developers" subtitle="Browser Our Vue Jobs and start your career today" href="/jobs" buttonValue="Browse Jobs"/>
          <Card bg="bg-green-100" title="For Employers" subtitle="List your job to find the perfect develope for the role" href="/add/job" buttonValue="Add Jobs" buttonBg="bg-green-500" hover="bg-green-600"/>
        </div>
      </div>
    </section>
</template>