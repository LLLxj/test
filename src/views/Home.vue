<template>
  <div>
    <B :toB="data1" :toC="data2" @getB="getB" @getC="getC" v-on:test1="onTest1" v-on:test2="onTest2"/>
  </div>
</template>

<script>
import B from './b'
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'

export default {
  name: 'Home',
  components: {
    HelloWorld, B
  },
  data () {
    return {
      data1: '1111',
      data2: '2222'
    }
  },
  created() {
    var a = this.deepClone({ a: '1', b: '2' })
    // var a = this.deepClone(b)
    console.log(a)
  },
  methods: {
    getB() {
      console.log('b组件传值')
    },
    getC() {
      console.log('c组件传值')
    },
    onTest1(data) {
      console.log('我来自:' + data)
    },
    onTest2(data) {
      console.log('我来自:' + data)
    },
    deepClone(source) {
			const targetSource = Object.constructor === Array ? [] : {}
			for (var keys in source) {
				if (source.hasOwnProperty(keys)) {
					if (source[keys] && typeof source[keys] === 'object') {
						targetSource[keys] = source[keys].constructor === Array ? [] : {}
						targetSource[keys] = deepClone(source[keys])
					} else {
						targetSource[keys] = source[keys]
					}
				}
			}
			return targetSource
    },
    mvvm () {
      Object.defineProperty(data, 'text', {
        set (value) {
          input.value = value
          this.value = value
        }
      })
      input.onchange = function (e) {
        data.text = e.target.value
      }
    }
  }
}
</script>
