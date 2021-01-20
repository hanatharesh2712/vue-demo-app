<template>
  <div class="home">
     <chat-window :current-user-id="currentUserId" :rooms="rooms" :messages="messages" />
     <HelloWorld msg="Welcome to Your Vue.js + TypeScript App"/>
  </div>
</template>

<script lang="ts">
import Vue from 'vue';
import HelloWorld from '@/components/HelloWorld.vue'; // @ is an alias to /src
import ChatWindow from 'vue-advanced-chat';
import 'vue-advanced-chat/dist/vue-advanced-chat.css';

export default Vue.extend({
  name: 'Home',
  components: {
    HelloWorld,
    ChatWindow,
  },
  data() {
    return {
      rooms: [],
      messages: [],
      currentUserId: 1234,
    };
  },
});
</script>
