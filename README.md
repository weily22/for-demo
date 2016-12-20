# for-demo
Details about the for loop

* 普通for循环
* for-in
* forEach
* for-of

**普通for循环**
demo1.html
当要循环的数组长度固定不变化时，最好将数组长度用变量存储起来，这样会获得更好的效率。

**for-in**
demo2.html
for-in可以遍历数组的内容，可以循环对象的属性。
实际上，for-in循环遍历的是对象的属性，而不是数组的索引。
array在Javascript中是一个对象，它的索引是属性名。
for-in遍历的可枚举的属性，所以不会遍历array对象的length属性。

**for-in的性能**
demo2.html
for-in每次操作都会同时查找实例或者原型属性，会产生更多开销，因此要比其他循环体类型慢，一般速度为其他类型循环的1/7。
除非明确需要迭代一个属性数量未知的对象，否则应避免使用for-in循环。

**forEach**
demo3.html
forEach是ES5中新引入的循环。
forEach为数组中含有有效值得每一项执行一次callback函数，如果是已删除或者未赋值的项将被跳过(不包括undefined或null的项)。
callback(item, index, self)
item:    当前项的值
index:    当前项的索引（number类型）
self:    对象本身
forEach遍历的范围在第一次调用callback前就会确定。在forEach被调用后，添加到数组中的项不会被访问到。

**for-of**
demo4.html
for-of，可以正确响应break,continue,return
for-of循环支持数组 ， 类数组对像 ，字符串遍历 ，MAP遍历，Set遍历
for-of不支持普通对象
