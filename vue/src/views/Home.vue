<template>
 <div class="body">
 
 
 <div v-for="i in arr">
 	{{i.state}}	
 	{{i.shuxue}} 
 	{{i.yunwen}} 
 	{{i.yingyu}} 
 	{{i.wuli}} 
 	{{i.huaxue}} 
 	{{i.zhengzhi}} 
 	{{i.lishi}} 
 	{{i.tiyu}}
 <br />
 <br />
 </div>
 <button @click="xiugai"> 修改 </button>   
 	<button @click="zengjia">增加</button>
 	
 	
 	
 </div>
</template>
<script>	
 export default {
 	created(){
 		this.$http.get('http://localhost:3010/').then(e=>this.arr=e.body)
 	},
 	data(){
 		return {
 			arr:[],
// 			xiugai:"",
// 			zengjia:""
 		}
 	},
 	methods:{
        xiugai(){
        	this.$http.get('http://localhost:3010/').then(e=>this.arr=e.body)
        },
        
        zengjia(){
        	this.$http.get('http://localhost:3010/').then(e=>this.arr=e.body)
        }
        
        
        },
 }
</script>
