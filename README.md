# html-
html5+js写的计算机

下面是代码
<html>
	<head>
    <meta http-equiv="Content-Type" content="text/html; charset=utf-8" />
    <title></title>
    </head>
    <style>
    	#div1{
			width:400px;
			height:450px;
			background:#CCC;
			margin:20px auto;
		}
		#tex{
			width:360px;
			height:80px;
			background:white;
			text-align:center;
			margin-top:30px;
			font-size:35px;
			line-height:30px;
		}
		#div2{
			width:400px;
			height:350px;
		}
		#div2 div{
			width:60px;
			height:40px;
			background:gray;
			float:left;
			margin:10px 20px;
			text-align:center;
			padding-top:20px;
		}
    </style>
    <script>
    	window.onload = function(){
			var oDiv = document.getElementById('tex');
			var oDiv1 = document.getElementById('div2');
			var aDiv2 = oDiv1.getElementsByTagName('div');
			
			for(var i = 0;i<aDiv2.length; i++){
				aDiv2[i].index = i;
			}
			
			
			int();
			for(var i = 0;i<aDiv2.length;i++) {
				aDiv2[i].index = i+1;
				aDiv2[i].onmouseover = function(){
					int();
					this.style.background = 'yellow';
					
				}
				aDiv2[i].onclick = function(){
					this.style.background = 'black';
					this.style.color = 'pink';
					
					if([i].index%4 != 0) {
						
						if(this.index ==14 || this.index ==15) {
							oDiv.value='';
						} else {
							oDiv.value=oDiv.value + this.innerHTML;	
						}
					}
				}
			}
				
			function int(){
				for(var i = 0;i<aDiv2.length;i++) {
					aDiv2[i].style.background = 'gray';
					aDiv2[i].style.color = 'black';
				}
			}
		}
    </script>
    <body>
    	<div id="div1">
        	<center><input type="text" id="tex"></center>
            <div id="div2">
            	<div >7</div>
                <div >8</div>
                <div >9</div>
                <div >/</div>
                <div >4</div>
                <div >5</div>
                <div >6</div>
                <div >*</div>
                <div >1</div>
                <div >2</div>
                <div >3</div>
                <div >-</div>
                <div >0</div>
                <div >c</div>
                <div >=</div>
                <div >+</div>
			</div>
        </div>
    </body>
</html>
