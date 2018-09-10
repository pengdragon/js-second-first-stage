<!DOCTYPE html>
<html>
	<head>
		<meta charset="UTF-8">
		<title></title>
	</head>
	<body>
		<script type="text/javascript">//淘宝面试题
            //  3. 有一个字符串 '/location.html?name=xiaolan&age=18&height=180',通过一系列转换为对象
            // {name: 'xiaolan', age: 18, height: 180}
           /* var str = '/location.html?name=xiaolan&age=18&height=180';
             var _name = str.substr(15,4);
             var _xiaolan = str.substr(20,7);
             var _age = str.substr(28,3);
             var _18 = str.substr(32,2);
             var _height = str.substr(35,6);
             var _180 = str.substr(42,3);
             console.log(_name+':'+_xiaolan+','+_age+':'+_18+','+_height+':'+_180);
			var obj={
			}
			obj[_name]=_xiaolan;
			obj[_age]=_18;
			obj[_height]=_180;
			console.log(obj);*/
			var obj ={
				
			}
			var str = '/location.html?name=xiaolan&age=18&height=180';
			str = str.substring(str.indexOf('?')+1);
			console.log(str);
			str = str.split("&");
			for(var i =0; i<str.length;i++){
				var _str = str[i];
				_str =_str.split("=");
				if(i>0){
					_str[1]=Number(_str[1]);
				}
				obj[_str[0]]=_str[1];
				
			}
			console.log(obj);
			
		</script>
	</body>
</html>
