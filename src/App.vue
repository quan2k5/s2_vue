<script setup>
    import Ex1 from'./components/Ex1.vue'
    import Ex2 from './components/Ex2.vue'
    import Ex3 from './components/Ex3.vue'
    import Ex4 from'./components/Ex4.vue'
    import Ex5 from './components/Ex5.vue'
    import Ex6 from'./components/Ex6.vue'
    import Ex7 from './components/Ex7.vue'
    import Ex8 from './components/Ex8.vue'
    import Ex9 from './components/Ex9.vue'
    import Ex10 from './components/Ex10.vue'
    // V-bind 
    const imgURL = "https://giaydabongtot.com/wp-content/uploads/2020/10/Hinh-nen-ronaldo-cr7-may-tinh-laptop-3-scaled.jpg"
    const size = "30px"
    const color = "red"

    // V-if
    const isIf = false
    const isIf2 = true

    const age = 5

    // V-show
    const isShow = true

    // V-for
    const student = [
        {
            name: "quân lê",
            age: 19
        },
         {
            name: "ựdfdc",
            age: 18
        }
    ]

    //V-modal
    import { ref } from 'vue';
    const text = ref("")

    const handleChange = (event) => {
        console.log(); 
        text.value = event.target.value
    }
    const count=ref(0);
    // khai báo hàm tăng count
    const increase=()=>{
      count.value+=1;
    }
    // gọi hàm
    const handleClick=(mess)=>{
      console.log(mess);
      


    }
</script>

<template>
<div> 
    <h1>Lý thuyết</h1>
    <p>Binding Property
        
    </p>
    <ol>
        <li>v-bind
            <div>
                <img :src="imgURL"  alt="img1">
                <img v-bind:src="imgURL" alt="">
                <p v-bind:style="{fontSize: size, color: color}">Text Example</p>
            </div>
        </li>
        *******************************************************************************
        <li>v-if, v-else, v-else-if</li>
            <div>
                <!-- Trường hợp false thì không render ra DOM  -->
                <p v-if="isIf">Hiển thị nội dung false</p>
                <p v-if="isIf2">Hiển thị nội dung true</p>
            </div>
            <ul>
                <li v-if="age > 30">Trung niên</li>
                <li v-else-if="age>18">Thanh niên</li> 
                <li v-else-if="age > 6">Trưởng thành</li>
                <li v-else>Trẻ em</li>
            </ul>
        *********************************************************************************
        <li>v-show</li>
            <div>
                <!-- Trường hợp false thì vẫn render ra DOM nhưng không hiển thị -->
                <p v-if="isShow">Hiển thị nội dung true</p>
            </div>
        ********************************************************************************
        <li>v-for</li>
        <ul>
            <li v-for="(std, index) in student" :key="std.id">{{index+1}} {{std.name}}</li>
        </ul>
        ********************************************************************************
        <li>v-model</li>
        <p>Cách 1</p>
        <div>
            <input type="text" v-model="text">
            <p>Gía trị bạn nhập: {{text}}</p>
        </div>
        <p>Cách 2</p>
        <div>
            <input :value="text" type="text" @input="handleChange">
            <p>Gía trị bạn nhập: {{text}}</p>
        </div>
        <div>{{count}}</div>
        <button @click="increase">ấn</button>
        <p>event</p>
        <div @click="()=>{handleClick('hello')}">edfv</div>
        <p>Bài 1</p>
        <ex-1></ex-1>
        <p>Bài 2</p>
        <ex-2></ex-2>
        <p>Bài 3</p>
        <ex-3></ex-3>
        <p>Bài 4</p>
        <ex-4></ex-4>
        <p>Bài 5</p>
        <ex-5></ex-5>
        <p>Bài 6</p>
        <ex-6></ex-6>
        <p>Bài 7</p>
        <ex-7></ex-7>
        <p>Bài 8</p>
        <ex-8></ex-8>
        <p>Bài 9</p>
        <ex-9></ex-9>
        <p>Bài 10</p>
        <ex-10></ex-10>
    </ol>
  </div>
 
</template>

<style scoped>
    img {
        width: 100px;
        height: 100px;
    }
</style>