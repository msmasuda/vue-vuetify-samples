<template>
  <v-layout justify-start row>
    <draggable :options="{ group: 'tasks' }"
      element="div"
      class="pa-5"
      v-for="(list, key, index) in tasks" :key="index">
        <v-card v-for="(item, key, index) in list" :key="index" class="pa-2">
          <v-card-title>
            <div>
              <span class="grey--text">{{ item }}</span>
            </div>
          </v-card-title>
          <v-card-actions>
            <v-btn outline color="orange" href="/DraggableSample">見る</v-btn>
          </v-card-actions>
        </v-card>
    </draggable>
  </v-layout>
</template>

<script>
import draggable from 'vuedraggable';

export default {
  name: 'container',
  components: {
    draggable,
  },
  data() {
    return {
      items: [
        ['task1-1', 'task1-2', 'task1-3', 'task1-4'],
        ['task2-1', 'task2-2', 'task2-3', 'task2-4'],
        ['task3-1', 'task3-2', 'task3-3', 'task3-4']
      ]
    }
  },
  computed: {
    tasks: {
      get() {
        return this.items
      },
      set(value) {
        this.items = value
      }
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
