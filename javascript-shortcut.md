title: "一些js的简便写法"
date: 2015-03-17 23:51:20
tags: [javascript, codes, shortcut]
---

## 没有考究性能，只是感到有趣

### 获取当前是星期几
##### 说明:
  这个方法是无意中看到的，后面是变形
   
    function getDay(date) {
        var weeks = ['日', '一', '二', '三', '四', '五', '六'];
        return weeks[new Date(date).getDay()];
    }
    function getDay(date) {
        var weeks = "日一二三四五六";
        return weeks[new Date(date).getDay()];
    }
    function getDay(date) {
        var weeks = "日一二三四五六";
        return weeks.charAt(new Date(date).getDay());
    }

### 把object的属性放在一个数组里
##### 说明:
   注意for循环，是没有循环体的，利用的是for(key in obj)，会遍历obj属性且对key赋值

        function attr2Arr(obj) {
            var result = [];
            for (result[result.length] in obj);
            return result;
        }
     
### 数组遍历新写法，可以省几个字符
##### 说明:
   for循环中间体实际上是一个对结果取bool值的过程，既然这样，可以这样写，
   另外一点值得说明的是，for循环只要求有两个分号，不对分号间是否有表达式做要求
    
        function reverseLoop(arr) {
            for (var i = arr.length;i--;) {
                console.log(i, arr[i]);
            }
        }
     

     
  
  