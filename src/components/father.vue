<template>
<div>
    <button @click="clickParent">{{yuandou}}

    </button>
    <son ref="mychild" :shuxing = "yuandou" @event="getuser"  >
      <div slot="body" slot-scope="slotProps"  v-if="slotProps.todo.is" >i love you {{slotProps.todo.num}}
          <div v-for="(item,index) in slotProps.todo.todo" :key="index">{{item.asd}}</div>
      </div>
      <div>asdsadsdasdaasd</div> 
      <div></div> 
    </son>
    
  </div>
</template>

<script>
 import son from './son';
export default {
    data() {
      return {
            // radio:'',
            c_zfb: true,
            c_wx: false,
            money: 'true',
            orderlist: [],
            rmb: '10',
            yuandou: '1000',
            access_code: '',
            userid: '',
            appVersion:'',
            isDisable: false,
            yuandouyue:'',
            channelList:'',
            zfbpay:'',
            wxpay:''
        }
    },
    name: "parent",
    components: {
      son:son
    },
    methods: {
      clickParent(e) {
        this.yuandou = 10
        this.$refs.mychild.parentHandleclick(e);
      },
      getuser(e){
        console.log(e)
      }
    },
    watch:{
      yuandou (val){
        alert('watch')
      }
    }
}
</script>

<style>

</style>
