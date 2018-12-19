<template>
    <div>
        <div class="231"><slot name = "body" :todo="obj"></slot></div>
        <slot  ></slot>
    </div>
</template>

<script>
export default {
    data(){
        return {
            obj:{
                num:'12',
                sas:'123',
                is:true,
                todo:{
                    key:{asd:1312},
                    asd:{asd:3121}
                }
            },
            
        }
    },
    name: "son",
    props: ['shuxing'],
    methods: {
      parentHandleclick(e) {    
            alert('子组件属性改变啦')
        this.$emit('event',this.obj)
      }
    }
  }
</script>

<style>

</style>
