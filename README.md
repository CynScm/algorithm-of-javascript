##Q1 判断一个单词是否是回文？
###回文是指把相同的词汇或句子，在下文中调换位置或颠倒过来，产生首尾回环的情趣，叫做回文，也叫回环。比如 mamam redivider .
很多人拿到这样的题目非常容易想到用for 将字符串颠倒字母顺序然后匹配就行了。其实重要的考察的就是对于reverse的实现。其实我们可以利用现成的函数，将字符串转换成数组，这个思路很重要，我们可以拥有更多的自由度去进行字符串的一些操作。
```javascript
function checkPalindrom(str) {  
    return str == str.split('').reverse().join('');
}
```
##Q2 去掉一组整型数组重复的值
###比如输入: [1,13,24,11,11,14,1,2] 
###输出: [1,13,24,11,14,2]
###需要去掉重复的11 和 1 这两个元素。
```javascript
  	var arr=[1,13,24,11,11,14,1,2];
	var arr1=[];
	var hashArr=[];
	for(var i=0;i<arr.length;i++)
		if(!hashArr[arr[i]])
		{
			hashArr[arr[i]]=1;
			arr1.push(arr[i]);
	}
	console.log(arr1);
```
