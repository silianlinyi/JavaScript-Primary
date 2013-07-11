## Window事件

Window事件是指事件的发生与浏览器窗口本身而非窗口中显示的任何特定文档内容相关。

### 1.load事件

当文档和其所有外部资源（比如图片）完全加载并显示给用户时就会触发它。onload监听window对象的load事件。

<pre>
window.onload = function(args) {
    return console.log("load event trigger");
};
</pre>

### 2.unload事件

unload事件和load事件相对，当用户离开当前文档转向其他文档时会触发它。unload事件处理程序可以用于保存用户的状态，但它不能
用于取消用户转向其他地方。

### 3.beforeunload事件

beforeunload事件和unload事件类似，但它能提供询问用户是否确定离开当前页面的机会。如果beforeunload的处理程序返回字符串，
那么在新页面加载之前，字符串会出现在展示给用户确认的对话框上，这样用户将有机会取消其跳转而留在当前页。

<pre>
window.onbeforeunload = function(args) {
    return '确定要离开该页面吗？';
};
</pre>

### 4.blur事件

当浏览器窗口从操作系统中得到或失去键盘焦点时会触发blur事件。

<pre>
window.onblur = function(args) {
    console.log("window blur event trigger");
};
</pre>

### 5.resize事件

当用户调整浏览器窗口大小时会触发resize事件。

> 注意：window.resize事件默认情况会触发两次。

<pre>
window.onresize = function(args) {
    console.log("window resize event trigger");
};
</pre>

### 6.scroll事件

当用户滚动滚动条时会触发scroll事件。scroll事件也能在任何可以滚动的文档元素上触发，比如那些设置CSS的overflow属性的元素。
传递给resize和scroll事件处理程序的事件对象是一个非常普通的Event对象，它没有指定调整大小或发生滚动的详细信息属性。



