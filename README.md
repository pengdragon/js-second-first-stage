<!DOCTYPE html>
<html lang="zh">
<head>
	<meta charset="UTF-8" />
	<meta name="viewport" content="width=device-width, initial-scale=1.0" />
	<meta http-equiv="X-UA-Compatible" content="ie=edge" />
	<title>Document</title>
	<style>
		#box{height: 400px;
		width:400px;
		border:2px solid black;
		position: relative;
		margin:100px auto;
		}
		#min_box{height: 100px;
		width:100px;
		background: blue;
		position: absolute;
		left:0px;
		top:0px;
		}
	</style>
</head>
<body>
	<div id="box">
		<div id="min_box"></div>
	</div>
	<script type="text/javascript">	
		function $(ele){
			return document.getElementById(ele);
		}
		var $box = $('box');
		var $min_box = $('min_box');
		var $x = $box.offsetLeft;
		var $y = $box.offsetTop;
		var max = $box.clientWidth-$min_box.offsetWidth;
		var may = $box.clientHeight-$min_box.offsetHeight;
			$min_box.onmousedown = function(e){
				e = e||window.event;
				var _x = e.offsetX;
				var _y = e.offsetY;
				window.onmousemove = function(e){
					e = e||window.event;
					console.log(1);
					var x = e.clientX-_x-$x;
					var y = e.clientY-_y-$y;
					if(x<0)
					x=0;
					else if(x>max)
					x=max;
					if(y<0)
					y=0;
					else if(y>may)
					y=may;
					$min_box.style.left=x+'px';
					$min_box.style.top=y+'px';	
				}	
			}
			document.onmouseup=function(){
				window.onmousemove= null;
				}			
	</script>
</body>
</html>
