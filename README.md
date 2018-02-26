#项目初始化
	1.安装vue-cli脚手架工具
		npm install -g vue-cli
	2.初始化项目
		vue init webpack my-project
	3.进入项目
		cd my-project
	4.安装依赖
		npm install
	5.运行项目
		npm run dev
#项目目录结构
	index.html项目根视图
	package.json配置文件
	.postcssrc.js postcss配置文件
	.gitignore 用git上传时忽略的文件
	.editorconfig IDE配置文件
	.babelrc

	static 静态文件目录

#组件的使用
	1.引入组件
		import app from './App'
	2.加载视图
		template: '<App/>'
	3.注册组件
		components: {App}

#模板语法
	mustache模板(双花括号的模板语法)
		表现形式：{{ 语法：变量 }}
		例子：
			{{ hello(已定义的变量) }}
			{{ 1+1 }}
			{{ "哈哈" }}
			{{ 0>10 ? '对的' : '错的' }}
	注意：只能写单行语句，并且不是作用在HTML的属性上边
#Vue组件包括三个部分：
	1.template: 视图
	2.script： 逻辑
	3.style： 样式

#Vue的基本指令
	1.v-html: 渲染文本 <p v-html="hello"></p>
		和双花括号的区别：双花括号只是变量，v-html必须依赖于标签
	2.v-text: 渲染文本 <p v-text="hello"></p>
		和v-html的区别： v-html可以解析html v-text不能
	3.v-bind: 绑定属性 <span v-bind:class="haha">我要888</span>
		想要变成活的属性都可以使用v-bind绑定。

#条件渲染
	1.v-if
	2.v-else
	3.v-show 
	v-if与v-show的区别
		v-if只有在条件为true时才渲染，v-show不管什么时候都渲染，只是进行简单的cdd切换。v-if 有更高的切换开销，而 v-show 有更高的初始渲染开销。因此，如果需要非常频繁地切换，则使用 v-show 较好；如果在运行时条件很少改变，则使用 v-if 较好。 

#列表渲染
	1.v-for:是根据数组的选项列表进行渲染
		<li v-for="(name,index) in names" v-bind:key="index">{{ name }}-{{ index }}</li>
		<li v-for="item in user">
          <span>{{ item.name }}</span>
          <span>{{ item.age }}</span>
        </li>

#事件监听
	v-on：(methods，参数，事件修饰符)
	事件修饰符：stop(阻止事件冒泡)，prevent(阻止默认事件)，once(只生效一次)
				captrue(添加事件监听是采用事件捕获模式，即内部元素触发的事件先在此处理，然后才交由内部元素自身处理)
				self(当事件源是当前元素自身时触发函数)
				enter

#数组更新检测
	变异方法：引起视图的变化push(),pop(),shift(),unshift(),splice(),sort(),reverse()
	替换方法：不会引起视图的变化,filter(), concat() 和 slice()

#计算属性和观察者
	computed
	computed和methods的区别：计算属性是基于它们的依赖进行缓存的。计算属性只有在它的			相关依赖发生改变时才会重新求值。这就意味着只要 message 							还没有发生改变，多次访问 reversedMessage 										计算属性会立即返回之前的计算结果，而不必再次执行函数。

#表单输入绑定
	v-model: 实现数据双向绑定
	watch监听数据
	修饰符：lazy,number,trim

#class与style绑定
	<p v-bind:class="{ active: isActive }">哈哈</p>