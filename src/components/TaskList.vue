<template>
  <PureTaskList :tasks="tasks" v-on="$listeners" @archive-task="archiveTask" @pin-task="pinTask" />
</template>

<script>
import PureTaskList from './PureTaskList.vue'
import { mapActions, mapState } from 'vuex'

export default {
  name: 'TaskList',
  components: { PureTaskList },
  methods: mapActions(['archiveTask', 'pinTask']),
  computed: mapState(['tasks']),
}
</script>
