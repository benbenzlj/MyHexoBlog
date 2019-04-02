---
title: VueJs验证组件Vuelidate 使用
date: 2017-07-28 13:17:57
tags: ['Vue.js','验证组件','Vuelidate']
---

# Vuelidate是Vue.js的一个验证组件，简单，轻量级，基于对象 #
----

# 项目地址 #
* [源码](http://www.baidu.com)
* [demo](https://monterail.github.io/vuelidate)

# 安装 #
```javascript
npm install vuelidate --save
```
# 在Vue中使用 #
```javascript
import Vue from 'vue'
import Vuelidate from 'vuelidate'
Vue.use(Vuelidate)
```
# 使用 #
## 简单验证
```javascript
import { required, minLength, between } from 'vuelidate/lib/validators'
export default {
  data () {
    return {
      name: '',
      age: 0
    }
  },
  validations: {
    name: {
      required,
      minLength: minLength(4)
    },
    age: {
      between: between(20, 30)
    }
  }
}
```
## 2