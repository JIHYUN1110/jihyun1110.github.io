---
title: Vue.js의 Component
date: 2018-10-01
categories: Javascript
---

# **Component :satisfied:

(1) 전역 컴포넌트

    <div id="example">
        <my-compt></my-compt>
    </div>

    <script>
        Vue.component('my-compt', {
            template: '<div>전역 컴포넌트</div>'
        })

        new Vue({
            el: '#example'
        })
    </script>
    

(2) 지역 컴포넌트





# **Props
