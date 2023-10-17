<template>
  <main>
    <div class="container bg">
      <div class="navBar">
        <div class="logo">
          <a href="#">
            <i class="fas fa-thin fa-user"></i>
          </a>
        </div>
      </div>
      <header>
        <h2></h2>
        <nav class="navigation">
          <a href="/">หน้าหลัก</a>
          <a href="/aboutus">เกี่ยวกับ</a>
          <a href="/service">บริการ</a>
          <a href="/contact">ติดต่อเรา</a>

          <a><input v-model="username" type="text" /></a>
          <a v-if="!isLoggedIn" @click="login">เข้าสู่ระบบ</a>
          <a v-else href="/login">{{ name }}</a>
        </nav>
      </header>

      <div class="wrapper">
        <span class="icon-close"><ion-icon name="close-circle"></ion-icon></span>
        <div class="form-box login">
          <h2>เข้าสู่ระบบ</h2>
          <from action="#">
            <div class="input-box">
              <span class="icon"><ion-icon name="card"></ion-icon></span>
              <input type="id-card" required />
              <label>บัตรประชาชน</label>
            </div>
            <div class="input-box">
              <span class="icon"><ion-icon name="lock-closed"></ion-icon></span>
              <input type="password" required />
              <label> รหัสผ่าน</label>
            </div>
            <div class="remember-forgot">
              <label><input type="checkbox" /> จดจำฉัน</label>
              <a href="#"> ลืมรหัสผ่าน</a>
            </div>
            <button type="submit" class="btn">เข้าสู่ระบบ</button>
            <div class="login-register">
              <p>ยังไม่ได้เป็นสมาชิก?<a href="#" class="register-link"> สมัครสมาชิก</a></p>
            </div>
          </from>
        </div>
        <div class="form-box register">
          <h2>สมัครสมาชิก</h2>
          <from action="#">
            <div class="input-box">
              <span class="icon"><ion-icon name="person"></ion-icon></span>
              <input type="NameLast" required />
              <label>ชื่อ-นามสกุล</label>
            </div>
            <div class="input-box">
              <span class="icon"><ion-icon name="card"></ion-icon></span>
              <input type="id-card" required />
              <label>บัตรประชาชน</label>
            </div>
            <div class="input-box">
              <span class="icon"><ion-icon name="lock-closed"></ion-icon></span>
              <input type="password" required />
              <label> รหัสผ่าน</label>
            </div>
            <button type="submit" class="btn">สมัครสมาชิก</button>
            <div class="login-register">
              <p>เป็นสมาชิกแล้ว?<a href="#" class="login-link" @click="login">เข้าสู่ระบบ</a></p>
            </div>
          </from>
        </div>
      </div>
      <div class="content">
        <div class="bank" style="width: 50%">
          <div class="txt">
            <h2><i class="fas fa-map-marker-alt"></i> Mae Hong Son</h2>
          </div>
          <div class="txt">
            <h1>โครงการธนาคารขยะ</h1>
            <h1>ส่วนตำบลเมืองปอน</h1>
          </div>
          <p>
            Lorem ipsum dolor sit amet, consectetur adipisicing elit. Veniam accusantium ipsam
            repellendus laborum corrupti, obcaecati consequatur incidunt eveniet dolores laudantium,
            dolorum totam officia velit modi consectetur provident facere ipsa architecto!
          </p>
        </div>
        <div class="card">
          <div class="box bg1">
            <h2>A</h2>
          </div>
          <div class="box bg2">
            <h2>B</h2>
          </div>
          <div class="box bg3">
            <h2>C</h2>
          </div>
          <div class="box bg4">
            <h2>D</h2>
          </div>
        </div>
      </div>
    </div>
  </main>
</template>

<script setup>
// import { initializeApp } from 'firebase/app'
// import { getAuth, signInWithEmailAndPassword } from 'firebase/auth'
// import { ref } from 'vue'

// const firebaseConfig = {
//   // ...
// }

// const app = initializeApp(firebaseConfig)

// const auth = getAuth(app)

// const username = ref('')
// const name = ref('')
// const isLoggedIn = ref(false)

// const formLogin = ref({
//   email: '',
//   password: ''
// })

// const userData = [
//   {
//     id: '1',
//     username: 'wave',
//     name: 'Wave Memory'
//   },
//   {
//     id: '2',
//     username: 'panuwat',
//     name: 'Time Panuwat'
//   },
//   {
//     id: '3',
//     username: 'murphy',
//     name: 'Hello Merphy'
//   }
// ]

// function login() {
//   signInWithEmailAndPassword(auth, formLogin.value.email, formLogin.value.password)
//     .then((userCredential) => {
//       // Signed in
//       const user = userCredential.user

//       name.value = user.name
//       // ...
//     })
//     .catch((error) => {
//       const errorCode = error.code
//       const errorMessage = error.message
//     })

// const user = userData.find((user) => user.username === username.value)

// if (user) {
//   isLoggedIn.value = true
//   name.value = user.name
// }
//}
</script>

<style scoped>
box. {
}
</style>
