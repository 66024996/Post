<script setup>
import HelloWorld from './components/HelloWorld.vue'
import TheWelcome from './components/TheWelcome.vue'
</script>
<template>
  <div class="container">
    
    <div class="post" v-for="(post, index) in posts" :key="index">
      <h2>{{ post.title }}</h2>
      <p>{{ post.content }}</p>
    </div>
    <button class="btn-create" @click="goToCreatePage">+ ตั้งกระทู้</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      posts: [
        { title: 'หอพักAAกว้างไหมคะ'},
        { title: 'แนะนำหอพักหน้าม.พะเยาหน่อยครับ'},
        { title: 'จะต่อสัญญาต้องเตรียมอะไรบ้างคับ'},
        { title: 'ยีนยืนเหงาๆ ในมือของเขามีทินเนอร์ '},
        { title: 'หยงหลงทางกางใบเรือ'},
        { title: 'หอพักไหนที่เลี้ยงแมวได้บ้าง'},
        { title: 'พี่ต๋าอยู่หอไหน มีใครรู้บ้างคะ'},
        { title: 'พี่กำปั้นย้ายไปอยู่หอไหน มีใครทราบบ้างครับ'},
        { title: 'มีใครสนใจซื้อไมค์ไหม่ให้พี่กิ๊กบ้าง'},
        { title: 'ทำไมเก๊ะไม่พูดเลย'},
        { title: 'ปั่นลึกล้ำสุดหยั่งถึงคณึงหา'}
        
      ]
    };
  },
  methods: {
    goToCreatePage() {
      window.location.href = '';
    }
  }
};
</script>

<style scoped>
.container {
  max-width: 800px;
  margin: 0 auto;
  padding: 20px;
}

.post {
  background-color: #D9E8F5;
  padding: 10px;
  margin-bottom: 30px;
  border-radius: 5px;
  box-shadow: 10px 8px 5px #8888;
}

.btn-create {
  position: fixed;
  top: 20px;
  right: 20px;
  background-color: #0075BE;
  color: #fff;
  padding: 10px 20px;
  border: none;
  border-radius: 5px;
  cursor: pointer;
}
</style>
