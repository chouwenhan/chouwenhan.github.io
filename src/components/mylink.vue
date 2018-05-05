<template>
    <div class="flex width-100 margin-auto text-align-center flex-justify-center flex-items-center flex-content-center" style="height: 4vh">
        <a target="_blank" href="https://github.com/chouwenhan">
          <Icon type="social-github" size="30" color="white" style="margin:0vw 1vw"></Icon>
        </a>
        <a target="_blank" href="https://www.facebook.com/profile.php?id=100001439120213">
          <Icon type="social-facebook" size="30" color="white" style="margin:0vw 1vw"> </Icon>
        </a>
        <a target="_blank" href="Mailto:a29554483@gmail.com">
          <Icon type="social-googleplus" size="30" color="white" style="margin:0vw 1vw"></Icon>
        </a>
    </div>
</template>
<script>
// import comE from '../util/CommtEmit.js'
export default {
  data () {
    return {
      author: 'Hank',
    }
  },
  methods: {
    goback: function () {
      window.history.back()
    },
    emitA: function () {
      comE.$emit('id-selected', 1)
    },
    emitP: function () {
      this.$emit('ee', 'cc' )
    }
  },
  components: {
  },
  name: 'mylink'
}
</script>
<style>
.flex {
  display: -webkit-flex;
}
.width-100 {
  width: 100%;
}
.text-align-center {
  justify-content: center;
  align-items: center;
}
</style>