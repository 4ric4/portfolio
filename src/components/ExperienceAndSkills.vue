<template>
    <section class="text-white mt-18" id="skills">
        <div class="absolute right-o top-[100rem] h-full justify-end">
            <span class="flex opacity-20">
                <span class="w-16 h-32 rounded-l-full flex bg-primary blur-2x1"></span>
                <span class="w-16 h-32 rounded-r-full flex bg-[#f88fc2] blur-2xl mt-14"></span>
            </span>
        </div>
        <div class="md:grid md:grid-cols-2 gap-8 items-center py-8 px-4 xl:gap-15 xl:px-16">
            <div class="mt-4 md:mt-0 text-left flex flex-col z-10 h-full w-[80%]">
                <h2 class="text-4xl font-bold text-white text-left mb-4">My
                    <span class="text-transparent bg-clip-text bg-gradient-to-t from-primary to-secondary">Skills</span>
                </h2>
                <div class="mt-8" v-for="skill in Skills" :key="skill.id">
                    <div class="flex items-end justify-between" data-aos="fade-right">
                        <h4 class="font-semibold uppercase text-white">
                            {{ skill.name }}
                        </h4>
                        <h3 class="text-2xl font-bold text-white">{{ skill.width }}</h3>
                    </div>
                    <div class="mt-2 h-1 w-full bg[#131d30] rounded-full">
                        <div class="h-1 rounded-full bg-primary" :style="`width :${skill.width}`"></div>
                    </div>
                </div>
            </div>
            <div data-aos="flip-left">
                <h2 class="class=text-4xl font-bold text-white text-left mb-8 md:text-center md:mt-0 mt-8">My Experiences</h2>
                <div class="space-y-8 py-8" data-aos="fade-left">
                    <div v-for="element in Experinces" :key="element.id"
                    class="flex items-center rounded-xl p4 bg-[#11a3e] shadow-lg border border-[#1f1641]"
                    >
                    <div class="w-1/4">
                        <img src="https://img.icons8.com/ios-filled/100/ffffff/lawyer.png" alt="lawyer">
                    </div>
                    <div class="w-3/4 pl-4">
                        <h3 class="text-2xl font-semibold uppercase text-transparent bg-clip-text bg-gradient-to-r from-primary to-secondary">
                            {{ element.title }}
                        </h3>
                        <p class="text-white">{{ element.company }}</p>
                        <p class="text-white">{{ element.year }}</p>
                        <p class="text-white">{{ element.description }}</p>
                            
                    </div>
                </div>
                </div>
            </div>
        </div>
        
    </section>
</template>
<script setup>
import { ref } from 'vue';
const Skills =ref([
    {
        id: 1,
        name: 'HTML',
        width: '90%'
    },
        {
        id: 2,
        name: 'Python',
        width: '70%'
    },
        {
        id: 3,
        name: 'Php',
        width: '98%'
    },
        {
        id: 4,
        name: 'java',
        width: '85%'
    },

]);
const Experinces = ref([
    {
        id: 1,
        title: 'Frontend Developer',
        company: 'Google',
        year: '2019-2021',
        description: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Error, quibusdam voluptate? Laudantium reiciendis quo eveniet autem, distinctio nulla vel dignissimos recusandae cupiditate, obcaecati, veniam dolorem sunt! Vero totam voluptas modi.'
    },
    {
        id: 2,
        title: 'Backend Developer',
        company: 'Facebook',
        year: '2017-2019',
        description: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Error, quibusdam voluptate? Laudantium reiciendis quo eveniet autem, distinctio nulla vel dignissimos recusandae cupiditate, obcaecati, veniam dolorem sunt! Vero totam voluptas modi.'
    },
    {
        id: 3,
        title: 'Fullstack Developer',
        company: 'Amazon',
        year: '2015-2017',
        description: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Error, quibusdam voluptate? Laudantium reiciendis quo eveniet autem, distinctio nulla vel dignissimos recusandae cupiditate, obcaecati, veniam dolorem sunt! Vero totam voluptas modi.'
    },
]);
</script>
