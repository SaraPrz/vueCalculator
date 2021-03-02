<template>
  <div id="app">
    <CalculateMethod></CalculateMethod>
    <CalculateComputed></CalculateComputed>
    <ProjectsList></ProjectsList>
    <projectListComputed></projectListComputed>
    <projectListSearch></projectListSearch>
  </div>
</template>

<script>

import CalculateMethod from './components/CalculateMethod'
import CalculateComputed from './components/CalculateComputed'
import ProjectsList from './components/ProjectsList'
import projectListComputed from './components/projectListComputed'
import projectListSearch from './components/projectListSearch'

export default {
  name: 'App',
  components: {
    CalculateMethod,
    CalculateComputed,
    ProjectsList,
    projectListComputed,
    projectListSearch
  }
}
</script>

<style>
</style>
