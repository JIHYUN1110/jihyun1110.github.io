---
title: Vue.js의 Component/Props/Events
date: 2018-10-01
categories: Javascript
---

## **Component** :wave:

*컴포넌트는 코드를 재사용 가능할 수 있도록 하는 인스턴스이다.*

### (1) 전역 컴포넌트

전역 컴포넌트 등록에는 Vue.component(tagName, options)가 필요하다. 이후 Vue 인스턴스 내 어디에서나 컴포넌트를 사용할 수 있다.

'''html
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
'''
    

### (2) 지역 컴포넌트

지역 컴포넌트의 경우 해당 인스턴스나 컴포넌트 범위 내에서만 사용할 수 있도록 해준다. 

'''html
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
'''

### (3) 장단점

장점: 코드 재사용이 편리하고, 특정 부분 수정을 하기에도 용이하다.

단점:

## **Props** :wave:

*Props는 부모-자식 간 관계에서 부모가 자식에게 데이터를 '아래로' 전달하는 개념이다.*

- 상위의 데이터를 하위 컴포넌트에서 바로 참조할 수 없기 때문에 props 옵션을 사용한다.
- 하위 컴포넌트에서는 미리 받아올 props를 명시한다.
- v-bind로 동적 props를 나타낼 수 있는데, 상위에서 데이터가 업데이트 되면 하위에서도 반영되게 해준다.

## **Events :wave:

*Events emitting 을 통해서 부모-자식 간 관계에서 자식이 부모에게 '위로' 메시지를 전달할 수 있다.*



