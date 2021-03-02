<template>
    <div>
        <ul v-for="(project,index) in filteredProjects" :key="index" >
            <li>
                <div>
                    {{ project.projectName }} developer is 
                {{ project.developer }}
                </div>
            </li>
        </ul>
    </div>
</template>

<script>

export default {
    name: 'App',
    data() {
        return {
            projects: [
                {
                    projectName:'eghtesadnews',
                    developer:'Sara',
                    yearStart:'1390'
                },
                {
                    projectName:'rokna',
                    developer:'Ehsan',
                    yearStart:'1391'
                },
                {
                    projectName:'eghtesadonline',
                    developer:'Sara',
                    yearStart:'1391'
                },
                {
                    projectName:'gostaresh',
                    developer:'Ehsan',
                    yearStart:'1392'
                },
            ],
            filteredProjects:[]
        }
    },
    methods: {
        developerName(developer) {
            this.filteredProjects = this.projects.filter(project => project.developer === developer);
            console.log(this.filteredProjects);
        }
    },
    mounted() {
        this.developerName('Sara');
    }
}
</script>

<style>
</style>
