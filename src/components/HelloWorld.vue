<template>
  <div>
      <div id="header">
        <div class="tab">聊天</div>
        <div class="tab">个人中心</div>
      </div>

      <div id="body">
        <div class="tabs">
          <h2 style="text-align: center;height:60px;line-height:60px">会话</h2>
          <ul>
            <li>小明</li>
            <li>小王</li>
            <li>小张</li>
            <li>小黄</li>
            <li>小明</li>
            <li>小王</li>
            <li>小张</li>
            <li>小黄</li>
          </ul>
        </div>
      </div>
    </div>
</template>

<script>
	import io from 'socket.io-client'
	
	const socket = io();
	const adminSocket = io('/admin')
	
	export default {
		name: 'HelloWorld',
	}         
</script>


<style scoped>
    *{
			margin:0;
			padding:0;
		}
		ul,li,ol{
			list-style: none;
		}
		body{
			width:100%;
			height:100%;
		}
		#header{
			width:80%;
			height:100px;
			margin:0 auto;
		}
		#header .tab{
			min-width: 150px;
			float:left;
			width:50%;
			text-align: center;
			line-height: 100px;
			background:blue;
			color:#fff;
			font-size:30px;
			opacity: 0.5;
		}
		#body{
			width:80%;
			height:600px;
			background:red;
			margin:0 auto;
			opacity: 0.5;		
		}
		#body .tabs{
			min-width: 100px;
			width:20%;
			height:100%;
			float:left;
			background:yellow;
		}
		#body .tabs ul li{
			width:100%;
			height:50px;
			line-height: 50px;
			text-align:center;
			background:#000;
			color:#fff;
		}
</style>
