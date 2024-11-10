<template>
    <div class="  p-8 mr-80 ml-52 px-270">
        <h6 class="font-bold">This course includes:</h6>
        <div class="flex gap-8">
            <div>
                <p>

                    1 hour on-demand video
                </p>
                <p>2 Access on mobile and TV</p>
            </div>
            <div>
               
                <p>
                    <Icon name="hugeicons:award-01" /> Certificate of completion
                </p>
            </div>
        </div>

        <div pt-3>
            <h4 class="font-bold text-xl mt-9 mb-3">Course content</h4>
        </div>

        <div class="flex justify-between">
            <p class="font-thin">
                {{ sections.length }} sections • {{ totalLectures }} lectures • {{ formattedTotalTime }}
            </p>
            <div>
                <button @click="toggleCollapse" class="text-violet-0 font-bold p-2 rounded">
                    {{ showAll ? 'Collapse all sections' : 'Expand all sections' }}
                </button>

            </div>
        </div>

        <div class="border pb-8 pr-2">
            <transition name="fade">
                <div class="mt-6">
                    <div v-for="(section, index) in (showAll ? sections : limitedSections)" :key="index"
                        class="section">
                        <div class="collapsible cursor-pointer p-2 mt-2 rounded flex justify-between pr-6 bg-gray-0"
                            @click="toggleSection(index)">
                            <div>
                                <span class="pr-3 font-bold">{{ section.isActive ? 'v' : '^' }}</span>
                                <span class="font-bold">{{ section.title }}</span>
                            </div>
                            <span>
                                {{ section.contents.length }} lectures • {{ formatTime(section.contents.reduce((total,
                                item) => total + item.duration, 0)) }}
                            </span>
                        </div>

                        <transition name="fade">
                            <div v-if="section.isActive" class="content mt-2 p-2 rounded">
                                <div v-for="(content, i) in section.contents" :key="i"
                                    class="flex justify-between pr-6 ">
                                    <p class="font-light">{{ content.title }}</p>
                                    <p class="text-neutral-500  font-thin">{{ formatTime(content.duration) }}</p>
                                </div>
                            </div>
                        </transition>
                    </div>
                </div>
            </transition>
        </div>
    </div>
</template>

<script>
export default {
    name: 'CollapsableCard',
    data() {
        return {
            showAll: false, // Controls if all sections are shown or only the first two
            sections: [
                {
                    title: 'Welcome to How to Understand Customer Needs',
                    contents: [
                        { title: 'Welcome to How to Understand Customer Needs', duration: 330 }, // duration in seconds
                       
                    ],
                    isActive: false,
                },
                {
                    title: 'Customer Satisfaction',
                    contents: [
                        { title: 'The Service Profit Chain', duration: 1200 },
                        { title: 'The Relationship Between Employee and Customer Satisfaction', duration: 900 },
                        
                    ],
                    isActive: false,
                },
                {
                    title: 'Internal and External Customers',
                    contents: [
                        { title: 'A Focus on the Internal Customer', duration: 800 },
                        { title: 'Identifying External Customer Needs', duration: 620 },
                        { title: 'Why Employee Satisfaction is Key for Customer Satisfaction', duration: 420 },
                        { title: 'A Quote from Mark Cuban', duration: 620 },
                    ],
                    isActive: false,
                },

                {
                    title: 'The Modern Day Customer',
                    contents: [
                        { title: 'Identifying the Modern Day Customer', duration: 1200 },
                        { title: 'Strategies for the Modern Day Customer', duration: 900 },
                        { title: 'The Modern Shopper - Some Stats', duration: 420 },
                        { title: 'Expectations of Our Customers', duration: 620 },
                        { title: 'Why Exceed Customer Expectations', duration: 1200 },
                        { title: 'Personalised Customer Experience', duration: 900 },
                        { title: 'Rogue Wallet Gets it Right', duration: 420 },
                        { title: 'Personalising for Your Customers', duration: 620 },
                        { title: 'Buying Habits of Contemporary Customers', duration: 1200 },
                        { title: 'The Link Between Decision Making and Emotions', duration: 900 },
                        { title: 'Explore More', duration: 420 },



                        
                    ],
                    isActive: false,
                },
                {
                    title: 'What is Your Day Customer ?',
                    contents: [
                        { title: 'What is Your Day Customer ?', duration: 1200 },
                   
            
                    ],
                    isActive: false,
                },
                {
                    title: 'Congratualtions! You now Know how to Understand Customer <br> Needs',
                    contents: [
                        { title: 'How to Understand Customer Needs', duration: 1200 },
                   
            
                    ],
                    isActive: false,
                },
                

            ],
        };
    },
    computed: {
        limitedSections() {
            return this.sections.slice(0, 6);
        },
        totalLectures() {
            return this.sections.reduce((total, section) => total + section.contents.length, 0);
        },
        totalTime() {
            return this.sections.reduce((total, section) => {
                return total + section.contents.reduce((sectionTotal, content) => sectionTotal + content.duration, 0);
            }, 0);
        },
        formattedTotalTime() {
            return this.formatTime(this.totalTime);
        },
    },
    methods: {
        toggleSection(index) {
            this.sections[index].isActive = !this.sections[index].isActive;
        },
        toggleCollapse() {
            this.showAll = !this.showAll;
            this.sections.forEach(section => {
                section.isActive = this.showAll;
            });
        },
        formatTime(seconds) {
            const mins = Math.floor(seconds / 60);
            const secs = seconds % 60;
            return `${String(mins).padStart(2, '0')}:${String(secs).padStart(2, '0')}`;
        },
    },
};
</script>