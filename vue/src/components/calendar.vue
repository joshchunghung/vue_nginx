<script setup>
import VueCal from 'vue-cal'
import 'vue-cal/dist/vuecal.css'
import { ref } from 'vue';
//https://github.com/ddmy/vue3-gantt
const selectedDate = ref(new Date())


</script>
<template>
    <vue-cal :time="false" @cell-click="selectedDate = $event" :selected-date="selectedDate" hide-weekends
        class="vuecal--date-picker" />
    <div>Selected date: '{{ selectedDate.format() }}'</div>
    <!-- <vue-cal xsmall hide-view-selector click-to-navigate :time="false" active-view="month" :disable-views="['week']"
                                                                        :disable-days="[
                                                                            // new Date().subtractDays(2).format(),
                                                                            new Date('2023-04-30').format(),
                                                                            // new Date().addDays(2).format()
                                                                        ]"></vue-cal> -->
</template>