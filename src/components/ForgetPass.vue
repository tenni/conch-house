<template>
	<div>
		<v-header></v-header>
		<div class="forgetp_con">
			<div class="forgetp_con_user">
		  		<input type="text" class="phonenum"  placeholder="请输入手机号" v-model="phonenum"/>
		  		<span class="getyzm">获取验证码</span>
		  	</div>
		  	<div class="forgetp_con_yzm">
		  		<input type="text" class="yzm"  placeholder="请输入短信验证码" v-model="dxyzm"/>
		  	</div>
		  	<div class="forgetp_con_pass">
		  		<input type="text" class="pass"  placeholder="请输入新密码（最少8位数，数字+子母）" v-model="password"/>
		  	</div>
			<mt-button type="primary" size="large">提交</mt-button>	
		</div>		
	</div>
</template>

<script>
	
	import Header from "./Header"
	export default{
		name:"ForgetPass",
		data:function(){
			return{
				phonenum:"",
				password:"",
				dxyzm:""
			}	
		},
		components:{
			"v-header":Header
		},
		mounted(){			
//			location.reload()
//			this.$router.go(0)
//			this.$router.push({path:"/forgetpass"})
		}
	}
</script>

<style>
.forgetp_con{
	padding: 0 50px;
	margin-top: 156px;
}
.forgetp_con_user,.forgetp_con_pass,.forgetp_con_yzm{
	height: 103px;
	line-height: 130px;
	border-bottom-width: thin;
	border-bottom-style: solid;
	border-bottom-color: rgba(0,0,0,0.8);
}
.forgetp_con input{
	width: 80%;
	border: 0;
	outline: none;
	font-size:28px;
	font-weight:normal;
	color:rgba(0,0,0,1);
	opacity: 0.3;
}
.getyzm{
	height:28px;
	font-size:28px;
	font-weight:normal;
	color:rgba(0,0,0,0.5);
	margin-left: -8%;
}
.mint-button{
	height:94px;
	background:rgba(255,144,18,1);
	border-radius:47px;
	font-size: 36px;
}
.mint-button--large{
	margin-top: 119px;
}

</style>