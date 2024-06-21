<template>
  <div>
    <q-toolbar class="navbar">
      <q-toolbar-title class="text-white">UAS PBK LAB</q-toolbar-title>
      <q-btn-dropdown flat label="Tugas" color="white" text-color="white" dense>
        <q-list style="min-width: 180px">
          <q-item v-for="task in tasks" :key="task.id" clickable v-ripple @click="openTask(task.url)">
            <q-item-section>{{ task.name }}</q-item-section>
          </q-item>
        </q-list>
      </q-btn-dropdown>
    </q-toolbar>
  </div>

  
</template>
<script>
export default {
  name: 'Navbar',
  data() {
    return {
      tasks: [
        { id: 1, name: 'Tugas 1', url: 'https://abihtugas.vercel.app/' },
        { id: 2, name: 'Tugas 2', url: 'https://tugas2-seven.vercel.app/' },
        { id: 3, name: 'Tugas 3', url: 'https://ikhlasul-qalbi-tugas3-eta.vercel.app/' },
        { id: 4, name: 'Tugas 4', url: 'https://qalbi-tgs4.vercel.app/' },
        { id: 5, name: 'Tugas 5', url: 'https://qalbi-tgss5.vercel.app/' },
        { id: 6, name: 'Tugas 6', url: 'https://tugass-6.vercel.app/' },
        { id: 7, name: 'Tugas 7', url: 'https://tugaslastprakqalbi.vercel.app/' },
      ],
    };
  },
  methods: {
    openTask(url) {
      window.open(url, '_blank');
    },
  },
};
</script>
<style scoped>
.navbar {
  background-color: #333;
  color: white;
}

.text-white {
  color: white;
}

.q-btn-dropdown .q-item-section {
  font-size: 16px;
}

.q-toolbar-title {
  font-size: 20px;
  font-weight: bold;
}
</style>
