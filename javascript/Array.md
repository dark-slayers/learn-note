# 数组
## 数组合并
concat() 方法用于连接两个或多个数组。<br>
**该方法不会改变现有的数组，而仅仅会返回被连接数组的一个副本。**
<pre>
<code>
  let a=[0,1,3];
  var b=[2,4,6,8,10];
  a.concat(b);
  console.log("a:"+a);
  //a=[0,1,3];
  a=a.concat(b);
  console.log("a:"+a);
  //a=[0,1,3,2,4,6,8,10];
</code>
</pre>
---
## 数组创建
<pre>
<code>
	let array=new Array();
	let array=new Array(3);
	let array=[1,'A',3];
	let array=[];
	let array={};
	let array=new Array(1,2,3);
</code>
</pre>
---
## 数组拆分
<pre>
<code>
	let data = [1,2,3,4,5,6,7,8,9];
	let result = [];
	for(let i=0,len=data.length;i&lt;len;i+=3){
 		result.push(data.slice(i,i+3));
	}
</code>
</pre>
---
