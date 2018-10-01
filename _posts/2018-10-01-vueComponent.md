---
title: Vue.js의 Component
date: 2018-10-01
categories: Javascript
---

## **Component**

*컴포넌트는 코드를 재사용 가능할 수 있도록 하는 인스턴스이다.* :satisfied:

### (1) 전역 컴포넌트

전역 컴포넌트 등록에는 Vue.component(tagName, options)가 필요하다. 이후 Vue 인스턴스 내 어디에서나 컴포넌트를 사용할 수 있다.

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
    

### (2) 지역 컴포넌트

지역 컴포넌트의 경우 해당 인스턴스나 컴포넌트 범위 내에서만 사용할 수 있도록 해준다. 

    <script>
        const Child = {
            template: '<div>지역 컴포넌트</div>'
        }

        new Vue({
            components: {
                'my-compt': Child
            }
        })
    </script>


### (3) 장단점

장점: 코드 재사용이 편리하고, 특정 부분 수정을 하기에도 용이하다.

단점:

## **Props**
