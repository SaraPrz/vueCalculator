<template>
    <div>
        <input type="text" v-model="developerName">
        <ul v-for="(project,index) in filteredProjects" :key="index" >
            <li>
                <div>
                {{ project.developer }} get
                    {{ project.projectName }} since {{ project.yearStart }}
                </div>
            </li>
        </ul>
    </div>
</template>

<script>

export default {
    name: 'SearchList',
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
                {
                    projectName:'mosalas',
                    developer:'Fatemeh',
                    yearStart:'1393'
                },
                {
                    projectName:'pendaronline',
                    developer:'Ehsan',
                    yearStart:'1392'
                },
            ],
        developerName:''
        }
    },
    computed : {
        filteredProjects() {
            return this.projects.filter(project => project.developer === this.developerName);
        }
    },
}
</script>

<style>
</style>
