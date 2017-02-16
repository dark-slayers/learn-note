# 数组
## 数组合并
concat() 方法用于连接两个或多个数组。
**该方法不会改变现有的数组，而仅仅会返回被连接数组的一个副本。**
<pre>
<code>
	`let a=[0,1,3];
  var b=[2,4,6,8,10];
  a.concat(b);
  console.log("a:"+a);
  //a=[0,1,3];
  a=a.concat(b);
  console.log("a:"+a);
  //a=[0,1,3,2,4,6,8,10];`
</code>
</pre>
---
