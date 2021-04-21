<template>
  <div class="about">
    <transition appear="" name="fade"
        @before-enter="beforeEnter"
        @enter="enter"
        @after-enter="afterEnter"
        @before-leave="beforeLeave"
        @leave="leave"
        @after-leave="afterLeave"
    >
      <h1>About</h1>
    </transition>
    <p>
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Cum aperiam
      officia possimus delectus inventore quod quisquam culpa voluptas iusto,
      quae maiores quo dolorum, corporis laboriosam a dolore consequatur
      assumenda nam!
    </p>
    <p>
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Cum aperiam
      officia possimus delectus inventore quod quisquam culpa voluptas iusto,
      quae maiores quo dolorum, corporis laboriosam a dolore consequatur
      assumenda nam!
    </p>
    <p>
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Cum aperiam
      officia possimus delectus inventore quod quisquam culpa voluptas iusto,
      quae maiores quo dolorum, corporis laboriosam a dolore consequatur
      assumenda nam!
    </p>
  </div>
</template>

<script>
import { ref } from '@vue/reactivity';
export default {
  setup() {
      const showTitle = ref(true)
      const beforeEnter = () => {

      }
      const enter = () => {

      }
      const afterEnter = (el) => {
          el.style.color = 'green'
          setTimeout(()=>showTitle.value=false, 2000)
      }

      const beforeLeave = (el) => {
          el.style.color = 'pink'
      }
      const leave = () => {

      }
      const afterLeave = () => {
          setTimeout(()=>showTitle.value=false, 2000)
      }

      return {showTitle, beforeEnter, enter, afterEnter, leave, afterLeave, beforeLeave}
  },
};
</script>

<style>
.about {
  max-width: 600px;
  margin: 20px auto;
}

.fade-enter-from{
    opacity: 0;
}
.fade-enter-active{
    transition: opacity 3s ease;
}
.fade-leave-to{
    opacity: 0;
}
.fade-leave-active{
    transition: opacity 3s ease;
}
</style>
