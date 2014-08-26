<p>大家好！今天我正式发布我的OOP框架<span style="color: #000000; font-size: 18px;">YOOP</span>！该框架将帮助开发者更好地进行面向对象编程。</p>
<p>当前版本号：v1.1</p>
<h1>介绍</h1>
<p>该框架包含接口、抽象类、类。</p>
<p>接口Interface可以继承多个接口，可以定义方法、属性。</p>
<p>抽象类AClass可以继承多个接口、一个抽象类，可以定义构造函数、公有成员、私有成员、保护成员、静态成员、虚方法、抽象成员。</p>
<p>类Class可以继承多个接口、一个抽象类或类，可以定义构造函数、公有成员、私有成员、保护成员、静态成员、虚方法。&nbsp;</p>
<h2><span style="background-color: #ffffff; color: #000000;">子类调用父类成员</span></h2>
<p>在子类中，可以使用this.base()来调用父类同名方法。也可以使用this.baseClass来访问父类的原型。</p>
<h2><span style="background-color: #ffffff; color: #000000;">主要的语法规则</span></h2>
<p>如果企图声明虚属性，会抛出异常。</p>
<h3>类Class：</h3>
<ol>
<li>创建实例时调用构造函数。</li>
<li>验证是否实现了接口的方法、属性，如果没有实现会抛出异常。</li>
<li>验证是否实现了父类的抽象成员，如果没有实现会抛出异常。</li>
<li>只能继承一个类（AClass或Class），否则抛出异常.</li>
<li>不能定义抽象成员，否则抛出异常。</li>
</ol>
<h3>抽象类AClass：</h3>
<ol>
<li>可以声明构造函数，供子类Class调用。</li>
<li>抽象类如果继承类Class，会抛出异常。</li>
<li>不用实现接口，可以交给子类Class实现。</li>
<li>不用实现父类抽象成员，可以交给子类Class实现。</li>
<li>只能继承一个抽象类AClass，否则抛出异常。</li>
</ol>
<h3>接口Interface：</h3>
<ol>
<li>接口只能继承接口，否则抛出异常。&nbsp;</li>
</ol>
<p>使用YOOP</p>
<p>YOOP支持AMD、CMD、CommonJS规范，可在Sea.js、node.js中使用：</p>
<div class="cnblogs_code">
<pre><span style="color: #0000ff;">var</span> yoop = require(<span style="color: #800000;">"</span><span style="color: #800000;">./YOOP.js</span><span style="color: #800000;">"</span><span style="color: #000000;">);

yoop.Class({});</span></pre>
</div>
<p>也可以<span style="font-size: 14px; line-height: 1.5;">通过script标签在页面上直接引用</span></p>
<p><span style="font-size: 14px; line-height: 1.5;">页面上引用script：</span></p>
<div class="cnblogs_code">
<pre><span style="color: #0000ff;">&lt;</span><span style="color: #800000;">script </span><span style="color: #ff0000;">src</span><span style="color: #0000ff;">="./YOOP.js"</span><span style="color: #0000ff;">&gt;&lt;/</span><span style="color: #800000;">script</span><span style="color: #0000ff;">&gt;</span></pre>
</div>
<p>然后通过命名空间YYC来使用：</p>
<div class="cnblogs_code">
<pre>YYC.Class({});</pre>
</div>
<h1>用法</h1>
<h2>接口</h2>
<h3>定义接口</h3>
<p>只有方法：</p>
<div class="cnblogs_code">
<pre><span style="color: #0000ff;">var</span> A = YYC.Interface(<span style="color: #800000;">"</span><span style="color: #800000;">method1</span><span style="color: #800000;">"</span>, <span style="color: #800000;">"</span><span style="color: #800000;">method2</span><span style="color: #800000;">"</span>);</pre>
</div>
<p>只有属性：</p>
<div class="cnblogs_code">
<pre><span style="color: #0000ff;">var</span> A = YYC.Interface([], [<span style="color: #800000;">"</span><span style="color: #800000;">attribute1</span><span style="color: #800000;">"</span>, <span style="color: #800000;">"</span><span style="color: #800000;">attribute2</span><span style="color: #800000;">"</span>]);</pre>
</div>
<p>既有方法又有属性：</p>
<div class="cnblogs_code">
<pre><span style="color: #0000ff;">var</span> A = YYC.Interface([<span style="color: #800000;">"</span><span style="color: #800000;">method1</span><span style="color: #800000;">"</span>, <span style="color: #800000;">"</span><span style="color: #800000;">method2</span><span style="color: #800000;">"</span>], [<span style="color: #800000;">"</span><span style="color: #800000;">attribute1</span><span style="color: #800000;">"</span>, <span style="color: #800000;">"</span><span style="color: #800000;">attribute2</span><span style="color: #800000;">"</span>]);</pre>
</div>
<h3>继承接口</h3>
<div class="cnblogs_code">
<pre><span style="color: #0000ff;">var</span> A = YYC.Interface([<span style="color: #800000;">"</span><span style="color: #800000;">method1</span><span style="color: #800000;">"</span>, <span style="color: #800000;">"</span><span style="color: #800000;">method2</span><span style="color: #800000;">"</span>],[<span style="color: #800000;">"</span><span style="color: #800000;">attribute1</span><span style="color: #800000;">"</span>, <span style="color: #800000;">"</span><span style="color: #800000;">attribute2</span><span style="color: #800000;">"</span><span style="color: #000000;">]);
</span><span style="color: #0000ff;">var</span> B = YYC.Interface(A, <span style="color: #800000;">"</span><span style="color: #800000;">m1</span><span style="color: #800000;">"</span>, <span style="color: #800000;">"</span><span style="color: #800000;">m2</span><span style="color: #800000;">"</span><span style="color: #000000;">);
</span><span style="color: #0000ff;">var</span> C = YYC.Interface([A], [<span style="color: #800000;">"</span><span style="color: #800000;">m1</span><span style="color: #800000;">"</span>, <span style="color: #800000;">"</span><span style="color: #800000;">m2</span><span style="color: #800000;">"</span>], [<span style="color: #800000;">"</span><span style="color: #800000;">a1</span><span style="color: #800000;">"</span>, <span style="color: #800000;">"</span><span style="color: #800000;">a2</span><span style="color: #800000;">"</span><span style="color: #000000;">]);
</span><span style="color: #0000ff;">var</span> D = YYC.Interface([A, B], [<span style="color: #800000;">"</span><span style="color: #800000;">m1</span><span style="color: #800000;">"</span>, <span style="color: #800000;">"</span><span style="color: #800000;">m2</span><span style="color: #800000;">"</span>], [<span style="color: #800000;">"</span><span style="color: #800000;">a1</span><span style="color: #800000;">"</span>, <span style="color: #800000;">"</span><span style="color: #800000;">a2</span><span style="color: #800000;">"</span>]);</pre>
</div>
<h2>抽象类</h2>
<h3>定义抽象类</h3>
<div class="cnblogs_code" onclick="cnblogs_code_show('74d2895c-4a23-4e35-9396-13051e6c6202')"><img id="code_img_closed_74d2895c-4a23-4e35-9396-13051e6c6202" class="code_img_closed" src="http://images.cnblogs.com/OutliningIndicators/ContractedBlock.gif" alt="" /><img id="code_img_opened_74d2895c-4a23-4e35-9396-13051e6c6202" class="code_img_opened" style="display: none;" onclick="cnblogs_code_hide('74d2895c-4a23-4e35-9396-13051e6c6202',event)" src="http://images.cnblogs.com/OutliningIndicators/ExpandedBlockStart.gif" alt="" />
<div id="cnblogs_code_open_74d2895c-4a23-4e35-9396-13051e6c6202" class="cnblogs_code_hide">
<pre><span style="color: #0000ff;">var</span> A =<span style="color: #000000;"> YYC.AClass({
    Init: </span><span style="color: #0000ff;">function</span> () { <span style="color: #008000;">//</span><span style="color: #008000;">构造函数</span>
<span style="color: #000000;">    },
    Protected: {    </span><span style="color: #008000;">//</span><span style="color: #008000;">保护成员</span>
        Abstract: { <span style="color: #008000;">//</span><span style="color: #008000;">保护抽象成员</span>
<span style="color: #000000;">        },
        Virtual: {  </span><span style="color: #008000;">//</span><span style="color: #008000;">保护虚方法</span>
<span style="color: #000000;">        },
        P_proA: </span><span style="color: #0000ff;">true</span>,   <span style="color: #008000;">//</span><span style="color: #008000;">保护属性</span>
       P_proM: <span style="color: #0000ff;">function</span> () { }    <span style="color: #008000;">//</span><span style="color: #008000;">保护方法</span>
<span style="color: #000000;">    },
    Public: {   </span><span style="color: #008000;">//</span><span style="color: #008000;">公有成员</span>
        Abstract: { <span style="color: #008000;">//</span><span style="color: #008000;">公有抽象成员</span>
<span style="color: #000000;">        },
        Virtual: {  </span><span style="color: #008000;">//</span><span style="color: #008000;">公有虚方法</span>
<span style="color: #000000;">        },
        pubM: </span><span style="color: #0000ff;">function</span> () { },  <span style="color: #008000;">//</span><span style="color: #008000;">公有方法</span>
      pubA: 0    <span style="color: #008000;">//</span><span style="color: #008000;">公有属性</span>
<span style="color: #000000;">    },
    Private: {  </span><span style="color: #008000;">//</span><span style="color: #008000;">私有成员</span>
        _priA: "",   <span style="color: #008000;">//</span><span style="color: #008000;">私有属性</span>
        _priM: <span style="color: #0000ff;">function</span> () { } <span style="color: #008000;">//</span><span style="color: #008000;">私有方法</span>
<span style="color: #000000;">    },
    Abstract: { </span><span style="color: #008000;">//</span><span style="color: #008000;">公有抽象成员</span>
<span style="color: #000000;">    },
    Virtual: {  </span><span style="color: #008000;">//</span><span style="color: #008000;">公有虚方法</span>
<span style="color: #000000;">    }
});</span></pre>
</div>

<h3>继承抽象类</h3>
<div class="cnblogs_code" onclick="cnblogs_code_show('86502fa7-140a-46a9-9ca3-cc15a69312c9')"><img id="code_img_closed_86502fa7-140a-46a9-9ca3-cc15a69312c9" class="code_img_closed" src="http://images.cnblogs.com/OutliningIndicators/ContractedBlock.gif" alt="" /><img id="code_img_opened_86502fa7-140a-46a9-9ca3-cc15a69312c9" class="code_img_opened" style="display: none;" onclick="cnblogs_code_hide('86502fa7-140a-46a9-9ca3-cc15a69312c9',event)" src="http://images.cnblogs.com/OutliningIndicators/ExpandedBlockStart.gif" alt="" />
<div id="cnblogs_code_open_86502fa7-140a-46a9-9ca3-cc15a69312c9" class="cnblogs_code_hide">
<pre><span style="color: #0000ff;">var</span> A =<span style="color: #000000;"> YYC.AClass({});
</span><span style="color: #0000ff;">var</span> B =<span style="color: #000000;"> YYC.AClass(A, {});
</span><span style="color: #0000ff;">var</span> C = YYC.AClass({Class: A}, {}); </pre>
</div>

<h3>继承接口</h3>
<div class="cnblogs_code" onclick="cnblogs_code_show('9e2698d9-dc7f-4d21-ac3c-9365f4b1430c')"><img id="code_img_closed_9e2698d9-dc7f-4d21-ac3c-9365f4b1430c" class="code_img_closed" src="http://images.cnblogs.com/OutliningIndicators/ContractedBlock.gif" alt="" /><img id="code_img_opened_9e2698d9-dc7f-4d21-ac3c-9365f4b1430c" class="code_img_opened" style="display: none;" onclick="cnblogs_code_hide('9e2698d9-dc7f-4d21-ac3c-9365f4b1430c',event)" src="http://images.cnblogs.com/OutliningIndicators/ExpandedBlockStart.gif" alt="" />
<div id="cnblogs_code_open_9e2698d9-dc7f-4d21-ac3c-9365f4b1430c" class="cnblogs_code_hide">
<pre><span style="color: #0000ff;">var</span> A = YYC.Interface(<span style="color: #800000;">"</span><span style="color: #800000;">m1</span><span style="color: #800000;">"</span><span style="color: #000000;">);
</span><span style="color: #0000ff;">var</span> B = YYC.Interface(<span style="color: #800000;">"</span><span style="color: #800000;">m2</span><span style="color: #800000;">"</span><span style="color: #000000;">);
</span><span style="color: #0000ff;">var</span> C =<span style="color: #000000;"> YYC.AClass({ Interface: A }, {
    Public: {
        m1: function () { }
    }
});
</span><span style="color: #0000ff;">var</span> D =<span style="color: #000000;"> YYC.AClass({ Interface: [A, B] }, {
    Public: {
        m1: function () { },
        m2: function () { }
    }
});</span></pre>
</div>

<h3>继承接口和抽象类</h3>
<div class="cnblogs_code" onclick="cnblogs_code_show('4a15c29d-3313-4198-a7e9-79a429b0deb0')"><img id="code_img_closed_4a15c29d-3313-4198-a7e9-79a429b0deb0" class="code_img_closed" src="http://images.cnblogs.com/OutliningIndicators/ContractedBlock.gif" alt="" /><img id="code_img_opened_4a15c29d-3313-4198-a7e9-79a429b0deb0" class="code_img_opened" style="display: none;" onclick="cnblogs_code_hide('4a15c29d-3313-4198-a7e9-79a429b0deb0',event)" src="http://images.cnblogs.com/OutliningIndicators/ExpandedBlockStart.gif" alt="" />
<div id="cnblogs_code_open_4a15c29d-3313-4198-a7e9-79a429b0deb0" class="cnblogs_code_hide">
<pre><span style="color: #0000ff;">var</span> A = YYC.Interface(<span style="color: #800000;">"</span><span style="color: #800000;">m1</span><span style="color: #800000;">"</span><span style="color: #000000;">);
</span><span style="color: #0000ff;">var</span> B = YYC.Interface([<span style="color: #800000;">"</span><span style="color: #800000;">m2</span><span style="color: #800000;">"</span>], [<span style="color: #800000;">"</span><span style="color: #800000;">a</span><span style="color: #800000;">"</span><span style="color: #000000;">]);
</span><span style="color: #0000ff;">var</span> C =<span style="color: #000000;"> YYC.AClass({});
</span><span style="color: #0000ff;">var</span> D =<span style="color: #000000;"> YYC.AClass({ Interface: [A, B], Class: C }, {
    Public: {
        m1: function () { },
        a: </span><span style="color: #800080;">0</span><span style="color: #000000;">
    }
});</span></pre>
</div>

<h2>类</h2>
<h3>定义类</h3>
<div class="cnblogs_code" onclick="cnblogs_code_show('9e441a77-56a3-4ab3-84c3-75f649488695')"><img id="code_img_closed_9e441a77-56a3-4ab3-84c3-75f649488695" class="code_img_closed" src="http://images.cnblogs.com/OutliningIndicators/ContractedBlock.gif" alt="" /><img id="code_img_opened_9e441a77-56a3-4ab3-84c3-75f649488695" class="code_img_opened" style="display: none;" onclick="cnblogs_code_hide('9e441a77-56a3-4ab3-84c3-75f649488695',event)" src="http://images.cnblogs.com/OutliningIndicators/ExpandedBlockStart.gif" alt="" />
<div id="cnblogs_code_open_9e441a77-56a3-4ab3-84c3-75f649488695" class="cnblogs_code_hide">
<pre><span style="color: #0000ff;">var</span> A =<span style="color: #000000;"> YYC.Class({
                Init: function () { </span><span style="color: #008000;">//</span><span style="color: #008000;">构造函数</span>
<span style="color: #000000;">                },
                Protected: {    </span><span style="color: #008000;">//</span><span style="color: #008000;">保护成员</span>
                    Virtual: {  <span style="color: #008000;">//</span><span style="color: #008000;">保护虚方法</span>
<span style="color: #000000;">                    },
                    P_proA: </span><span style="color: #0000ff;">true</span>,   <span style="color: #008000;">//</span><span style="color: #008000;">保护属性</span>
                    P_proM: function () { }    <span style="color: #008000;">//</span><span style="color: #008000;">保护方法</span>
<span style="color: #000000;">                },
                Public: {   </span><span style="color: #008000;">//</span><span style="color: #008000;">公有成员</span>
                    Virtual: {  <span style="color: #008000;">//</span><span style="color: #008000;">公有虚方法</span>
<span style="color: #000000;">                    },
                    pubM: function () { },  </span><span style="color: #008000;">//</span><span style="color: #008000;">公有方法</span>
                    pubA: <span style="color: #800080;">0</span>    <span style="color: #008000;">//</span><span style="color: #008000;">公有属性</span>
<span style="color: #000000;">                },
                Private: {  </span><span style="color: #008000;">//</span><span style="color: #008000;">私有成员</span>
                    _priA: <span style="color: #800000;">""</span>,   <span style="color: #008000;">//</span><span style="color: #008000;">私有属性</span>
                    _priM: function () { } <span style="color: #008000;">//</span><span style="color: #008000;">私有方法</span>
<span style="color: #000000;">                },
                Virtual: {  </span><span style="color: #008000;">//</span><span style="color: #008000;">公有虚方法</span>
<span style="color: #000000;">                }
            });</span></pre>
</div>

<h3>继承抽象类</h3>
<div class="cnblogs_code" onclick="cnblogs_code_show('9384a505-35bc-44d2-aa46-b5e0deed39f9')"><img id="code_img_closed_9384a505-35bc-44d2-aa46-b5e0deed39f9" class="code_img_closed" src="http://images.cnblogs.com/OutliningIndicators/ContractedBlock.gif" alt="" /><img id="code_img_opened_9384a505-35bc-44d2-aa46-b5e0deed39f9" class="code_img_opened" style="display: none;" onclick="cnblogs_code_hide('9384a505-35bc-44d2-aa46-b5e0deed39f9',event)" src="http://images.cnblogs.com/OutliningIndicators/ExpandedBlockStart.gif" alt="" />
<div id="cnblogs_code_open_9384a505-35bc-44d2-aa46-b5e0deed39f9" class="cnblogs_code_hide">
<pre><span style="color: #0000ff;">var</span> A =<span style="color: #000000;"> YYC.AClass({});
</span><span style="color: #0000ff;">var</span> B =<span style="color: #000000;"> YYC.AClass(A, {});
</span><span style="color: #0000ff;">var</span> C = YYC.AClass({ Class: A }, {});</pre>
</div>

<h3>继承类</h3>
<div class="cnblogs_code" onclick="cnblogs_code_show('976ac329-56ac-4f09-811f-66706040d12f')"><img id="code_img_closed_976ac329-56ac-4f09-811f-66706040d12f" class="code_img_closed" src="http://images.cnblogs.com/OutliningIndicators/ContractedBlock.gif" alt="" /><img id="code_img_opened_976ac329-56ac-4f09-811f-66706040d12f" class="code_img_opened" style="display: none;" onclick="cnblogs_code_hide('976ac329-56ac-4f09-811f-66706040d12f',event)" src="http://images.cnblogs.com/OutliningIndicators/ExpandedBlockStart.gif" alt="" />
<div id="cnblogs_code_open_976ac329-56ac-4f09-811f-66706040d12f" class="cnblogs_code_hide">
<pre><span style="color: #0000ff;">var</span> A =<span style="color: #000000;"> YYC.Class({});
</span><span style="color: #0000ff;">var</span> B =<span style="color: #000000;"> YYC.Class(A, {});
</span><span style="color: #0000ff;">var</span> C = YYC.Class({ Class: A }, {});</pre>
</div>

<h3>继承接口</h3>
<div class="cnblogs_code" onclick="cnblogs_code_show('30e4055d-da03-44ae-85cc-0501a94069a4')"><img id="code_img_closed_30e4055d-da03-44ae-85cc-0501a94069a4" class="code_img_closed" src="http://images.cnblogs.com/OutliningIndicators/ContractedBlock.gif" alt="" /><img id="code_img_opened_30e4055d-da03-44ae-85cc-0501a94069a4" class="code_img_opened" style="display: none;" onclick="cnblogs_code_hide('30e4055d-da03-44ae-85cc-0501a94069a4',event)" src="http://images.cnblogs.com/OutliningIndicators/ExpandedBlockStart.gif" alt="" />
<div id="cnblogs_code_open_30e4055d-da03-44ae-85cc-0501a94069a4" class="cnblogs_code_hide">
<pre><span style="color: #0000ff;">var</span> A = YYC.Interface(<span style="color: #800000;">"</span><span style="color: #800000;">m1</span><span style="color: #800000;">"</span><span style="color: #000000;">);
</span><span style="color: #0000ff;">var</span> B = YYC.Interface(<span style="color: #800000;">"</span><span style="color: #800000;">m2</span><span style="color: #800000;">"</span><span style="color: #000000;">);
</span><span style="color: #0000ff;">var</span> C =<span style="color: #000000;"> YYC.Class({ Interface: A }, {
    Public: {
        m1: function () { }
    }
});
</span><span style="color: #0000ff;">var</span> D =<span style="color: #000000;"> YYC.Class({ Interface: [A, B] }, {
    Public: {
        m1: function () { },
        m2: function () { }
    }
});</span></pre>
</div>

<h3>继承接口和抽象类/类</h3>
<div class="cnblogs_code" onclick="cnblogs_code_show('8dc18103-1f27-4cb1-8bab-d06523bedfcc')"><img id="code_img_closed_8dc18103-1f27-4cb1-8bab-d06523bedfcc" class="code_img_closed" src="http://images.cnblogs.com/OutliningIndicators/ContractedBlock.gif" alt="" /><img id="code_img_opened_8dc18103-1f27-4cb1-8bab-d06523bedfcc" class="code_img_opened" style="display: none;" onclick="cnblogs_code_hide('8dc18103-1f27-4cb1-8bab-d06523bedfcc',event)" src="http://images.cnblogs.com/OutliningIndicators/ExpandedBlockStart.gif" alt="" />
<div id="cnblogs_code_open_8dc18103-1f27-4cb1-8bab-d06523bedfcc" class="cnblogs_code_hide">
<pre><span style="color: #0000ff;">var</span> A = YYC.Interface(<span style="color: #800000;">"</span><span style="color: #800000;">m1</span><span style="color: #800000;">"</span><span style="color: #000000;">);
</span><span style="color: #0000ff;">var</span> B = YYC.Interface([<span style="color: #800000;">"</span><span style="color: #800000;">m2</span><span style="color: #800000;">"</span>], [<span style="color: #800000;">"</span><span style="color: #800000;">a</span><span style="color: #800000;">"</span><span style="color: #000000;">]);
</span><span style="color: #0000ff;">var</span> C =<span style="color: #000000;"> YYC.AClass({});
</span><span style="color: #0000ff;">var</span> D =<span style="color: #000000;"> YYC.Class({});
</span><span style="color: #0000ff;">var</span> E =<span style="color: #000000;"> YYC.AClass({ Interface: [A, B], Class: C }, {
    Public: {
        m1: function () { },
        a: </span><span style="color: #800080;">0</span><span style="color: #000000;">
    }
});
</span><span style="color: #0000ff;">var</span> F =<span style="color: #000000;"> YYC.AClass({ Interface: [A, B], Class: D }, {
    Public: {
        m1: function () { },
        a: </span><span style="color: #800080;">0</span><span style="color: #000000;">
    }
});</span></pre>
</div>

<h2>构造函数</h2>
<div class="cnblogs_code" onclick="cnblogs_code_show('1f31e68a-88be-4e95-85a9-35fcd59c1d1c')"><img id="code_img_closed_1f31e68a-88be-4e95-85a9-35fcd59c1d1c" class="code_img_closed" src="http://images.cnblogs.com/OutliningIndicators/ContractedBlock.gif" alt="" /><img id="code_img_opened_1f31e68a-88be-4e95-85a9-35fcd59c1d1c" class="code_img_opened" style="display: none;" onclick="cnblogs_code_hide('1f31e68a-88be-4e95-85a9-35fcd59c1d1c',event)" src="http://images.cnblogs.com/OutliningIndicators/ExpandedBlockStart.gif" alt="" />
<div id="cnblogs_code_open_1f31e68a-88be-4e95-85a9-35fcd59c1d1c" class="cnblogs_code_hide">
<pre><span style="color: #0000ff;">var</span> A =<span style="color: #000000;"> YYC.Class({
　　Init: function(t){
　　　　</span><span style="color: #0000ff;">this</span>.value =<span style="color: #000000;"> t;
　　}
});
</span><span style="color: #0000ff;">var</span> a = <span style="color: #0000ff;">new</span> A(<span style="color: #800080;">100</span><span style="color: #000000;">);
console.log(a.value);　　</span><span style="color: #008000;">//</span><span style="color: #008000;">100</span></pre>
</div>

<h2>静态成员</h2>
<p>使用&ldquo;类.静态成员&rdquo;的形式来调用静态成员。这里静态成员实质是类（function，function也是对象）的成员。</p>
<p>注意！静态方法中的this指向类，不是指向类的实例！</p>
<div class="cnblogs_code" onclick="cnblogs_code_show('5b868112-991a-4f5f-8bce-cabd0c7c48aa')"><img id="code_img_closed_5b868112-991a-4f5f-8bce-cabd0c7c48aa" class="code_img_closed" src="http://images.cnblogs.com/OutliningIndicators/ContractedBlock.gif" alt="" /><img id="code_img_opened_5b868112-991a-4f5f-8bce-cabd0c7c48aa" class="code_img_opened" style="display: none;" onclick="cnblogs_code_hide('5b868112-991a-4f5f-8bce-cabd0c7c48aa',event)" src="http://images.cnblogs.com/OutliningIndicators/ExpandedBlockStart.gif" alt="" />
<div id="cnblogs_code_open_5b868112-991a-4f5f-8bce-cabd0c7c48aa" class="cnblogs_code_hide">
<pre><span style="color: #0000ff;">var</span> A =<span style="color: #000000;"> YYC.Class({
    Static: {
        a: </span>100<span style="color: #000000;">,
        method1: </span><span style="color: #0000ff;">function</span><span style="color: #000000;"> () {
            </span><span style="color: #0000ff;">return</span> 200<span style="color: #000000;">;
        },
        method2: </span><span style="color: #0000ff;">function</span><span style="color: #000000;"> () {
             </span><span style="color: #0000ff;">this</span>.k = 300<span style="color: #000000;">;
        }
    }
});

A.method2();

console.log(A.a);   </span><span style="color: #008000;">//</span><span style="color: #008000;">100</span>
console.log(A.method1());    <span style="color: #008000;">//</span><span style="color: #008000;">200</span>
console.log(A.k);   <span style="color: #008000;">//</span><span style="color: #008000;">300</span></pre>
</div>

<h2>类的成员互相调用</h2>
<p>使用this来调用。</p>
<div class="cnblogs_code" onclick="cnblogs_code_show('2fa57eb4-faee-463b-b0f3-ed5329d090c0')"><img id="code_img_closed_2fa57eb4-faee-463b-b0f3-ed5329d090c0" class="code_img_closed" src="http://images.cnblogs.com/OutliningIndicators/ContractedBlock.gif" alt="" /><img id="code_img_opened_2fa57eb4-faee-463b-b0f3-ed5329d090c0" class="code_img_opened" style="display: none;" onclick="cnblogs_code_hide('2fa57eb4-faee-463b-b0f3-ed5329d090c0',event)" src="http://images.cnblogs.com/OutliningIndicators/ExpandedBlockStart.gif" alt="" />
<div id="cnblogs_code_open_2fa57eb4-faee-463b-b0f3-ed5329d090c0" class="cnblogs_code_hide">
<pre><span style="color: #0000ff;">var</span> A =<span style="color: #000000;"> YYC.Class({
    Private: {
        _a: </span><span style="color: #800080;">100</span><span style="color: #000000;">
    },
    Public: {
        method: function (t) {
            </span><span style="color: #0000ff;">return</span> <span style="color: #0000ff;">this</span><span style="color: #000000;">._a;
        }
    }
});
</span><span style="color: #0000ff;">var</span> a = <span style="color: #0000ff;">new</span><span style="color: #000000;"> A();
console.log(a.method);  </span><span style="color: #008000;">//</span><span style="color: #008000;">100</span></pre>
</div>

<h2>子类调用父类</h2>
<p>使用this.base()可调用父类同名函数。</p>
<p>使用this.baseClass.xx.call(this, xx)可调用父类的成员。</p>
<div class="cnblogs_code" onclick="cnblogs_code_show('1f442ed7-4339-49f7-abb1-7f1f1563cca6')"><img id="code_img_closed_1f442ed7-4339-49f7-abb1-7f1f1563cca6" class="code_img_closed" src="http://images.cnblogs.com/OutliningIndicators/ContractedBlock.gif" alt="" /><img id="code_img_opened_1f442ed7-4339-49f7-abb1-7f1f1563cca6" class="code_img_opened" style="display: none;" onclick="cnblogs_code_hide('1f442ed7-4339-49f7-abb1-7f1f1563cca6',event)" src="http://images.cnblogs.com/OutliningIndicators/ExpandedBlockStart.gif" alt="" />
<div id="cnblogs_code_open_1f442ed7-4339-49f7-abb1-7f1f1563cca6" class="cnblogs_code_hide">
<pre><span style="color: #0000ff;">var</span> A =<span style="color: #000000;"> YYC.AClass({
                    Init: function () {
                        </span><span style="color: #0000ff;">this</span>.p = <span style="color: #800080;">100</span><span style="color: #000000;">;
                    },
                    Public: {
                        method1: function () {
                            </span><span style="color: #0000ff;">this</span>.m = <span style="color: #800080;">300</span><span style="color: #000000;">;
                        },
                        method2: function () {
                            </span><span style="color: #0000ff;">return</span> <span style="color: #800080;">100</span><span style="color: #000000;">;
                        }
                    }
                });
                </span><span style="color: #0000ff;">var</span> B =<span style="color: #000000;"> YYC.Class(A, {
                    Init: function () {
                        </span><span style="color: #0000ff;">this</span>.<span style="color: #0000ff;">base</span><span style="color: #000000;">();
                    },
                    Private: {
                        _a: </span><span style="color: #800080;">100</span><span style="color: #000000;">
                    },
                    Public: {
                        method1: function (t) {
                            </span><span style="color: #0000ff;">this</span>.<span style="color: #0000ff;">base</span><span style="color: #000000;">();
                            </span><span style="color: #0000ff;">return</span> <span style="color: #0000ff;">this</span>.baseClass.method2.call(<span style="color: #0000ff;">this</span>, <span style="color: #0000ff;">null</span>) + <span style="color: #0000ff;">this</span><span style="color: #000000;">._a;
                        }
                    }
                });
                </span><span style="color: #0000ff;">var</span> b = <span style="color: #0000ff;">new</span><span style="color: #000000;"> B();
                console.log(b.method1());  </span><span style="color: #008000;">//</span><span style="color: #008000;">200</span>
                console.log(b.p);  <span style="color: #008000;">//</span><span style="color: #008000;">100</span>
                console.log(b.m);  <span style="color: #008000;">//</span><span style="color: #008000;">300</span></pre>
</div>

<h2>父类调用子类</h2>
<div class="cnblogs_code" onclick="cnblogs_code_show('e3a2be67-7d0e-4470-83c8-ba38c13853f4')"><img id="code_img_closed_e3a2be67-7d0e-4470-83c8-ba38c13853f4" class="code_img_closed" src="http://images.cnblogs.com/OutliningIndicators/ContractedBlock.gif" alt="" /><img id="code_img_opened_e3a2be67-7d0e-4470-83c8-ba38c13853f4" class="code_img_opened" style="display: none;" onclick="cnblogs_code_hide('e3a2be67-7d0e-4470-83c8-ba38c13853f4',event)" src="http://images.cnblogs.com/OutliningIndicators/ExpandedBlockStart.gif" alt="" />
<div id="cnblogs_code_open_e3a2be67-7d0e-4470-83c8-ba38c13853f4" class="cnblogs_code_hide">
<pre><span style="color: #0000ff;">var</span> A =<span style="color: #000000;"> YYC.AClass({
    Public: {
        method: function () {
            console.log(</span><span style="color: #0000ff;">this</span><span style="color: #000000;">.value);
        }
    }
});
</span><span style="color: #0000ff;">var</span> B =<span style="color: #000000;"> YYC.Class(A, {
    Public: {
        value: </span><span style="color: #800080;">100</span><span style="color: #000000;">
    }
});
</span><span style="color: #0000ff;">var</span> b = <span style="color: #0000ff;">new</span><span style="color: #000000;"> B();
b.method(); </span><span style="color: #008000;">//</span><span style="color: #008000;">100</span></pre>
</div>

<h2>覆写父类方法，实现接口成员、抽象成员</h2>
<div class="cnblogs_code" onclick="cnblogs_code_show('97fdfde9-9bae-4c6a-9edf-8f0c0e468bbd')"><img id="code_img_closed_97fdfde9-9bae-4c6a-9edf-8f0c0e468bbd" class="code_img_closed" src="http://images.cnblogs.com/OutliningIndicators/ContractedBlock.gif" alt="" /><img id="code_img_opened_97fdfde9-9bae-4c6a-9edf-8f0c0e468bbd" class="code_img_opened" style="display: none;" onclick="cnblogs_code_hide('97fdfde9-9bae-4c6a-9edf-8f0c0e468bbd',event)" src="http://images.cnblogs.com/OutliningIndicators/ExpandedBlockStart.gif" alt="" />
<div id="cnblogs_code_open_97fdfde9-9bae-4c6a-9edf-8f0c0e468bbd" class="cnblogs_code_hide">
<pre><span style="color: #0000ff;">var</span> A = YYC.Interface(<span style="color: #800000;">"</span><span style="color: #800000;">m1</span><span style="color: #800000;">"</span><span style="color: #000000;">);
</span><span style="color: #0000ff;">var</span> B =<span style="color: #000000;"> YYC.AClass({ Interface: A }, {
    Protected: {
        Abstract: {
            P_method: function () { }
        }
    },
    Public: {
        method: function () { }
    }
});
</span><span style="color: #0000ff;">var</span> C =<span style="color: #000000;"> YYC.Class(B, {
    Protected: {
        P_method: function () {
            console.log(</span><span style="color: #800000;">"</span><span style="color: #800000;">实现抽象方法</span><span style="color: #800000;">"</span><span style="color: #000000;">);
        }
    },
    Public: {
        method: function () {
            console.log(</span><span style="color: #800000;">"</span><span style="color: #800000;">覆盖父类同名方法</span><span style="color: #800000;">"</span><span style="color: #000000;">);
        },
        m1: function () {
            console.log(</span><span style="color: #800000;">"</span><span style="color: #800000;">实现接口</span><span style="color: #800000;">"</span><span style="color: #000000;">);
        }
    }
});</span></pre>
</div>
<span class="cnblogs_code_collapse">View Code</span></div>
<div onclick="cnblogs_code_show('97fdfde9-9bae-4c6a-9edf-8f0c0e468bbd')">
<h2>其它API</h2>
<h3>stubParentMethod、stubParentMethodByAClass</h3>
<p>让父类（Class/AClass）指定方法不执行。</p>
<p>测试用例如下：</p>
<div class="cnblogs_code" onclick="cnblogs_code_show('15b404e0-607c-479a-ac33-644b97af531f')"><img id="code_img_closed_15b404e0-607c-479a-ac33-644b97af531f" class="code_img_closed" src="http://images.cnblogs.com/OutliningIndicators/ContractedBlock.gif" alt="" /><img id="code_img_opened_15b404e0-607c-479a-ac33-644b97af531f" class="code_img_opened" style="display: none;" onclick="cnblogs_code_hide('15b404e0-607c-479a-ac33-644b97af531f',event)" src="http://images.cnblogs.com/OutliningIndicators/ExpandedBlockStart.gif" alt="" />
<div id="cnblogs_code_open_15b404e0-607c-479a-ac33-644b97af531f" class="cnblogs_code_hide">
<pre>describe("stubParentMethod", <span style="color: #0000ff;">function</span><span style="color: #000000;"> () {
        </span><span style="color: #0000ff;">var</span> sandbox = <span style="color: #0000ff;">null</span><span style="color: #000000;">;
        </span><span style="color: #0000ff;">var</span> A = <span style="color: #0000ff;">null</span><span style="color: #000000;">,
            B </span>= <span style="color: #0000ff;">null</span><span style="color: #000000;">,
            C </span>= <span style="color: #0000ff;">null</span><span style="color: #000000;">,
            a </span>= <span style="color: #0000ff;">null</span><span style="color: #000000;">,
            b </span>= <span style="color: #0000ff;">null</span><span style="color: #000000;">,
            c </span>= <span style="color: #0000ff;">null</span><span style="color: #000000;">;

        beforeEach(</span><span style="color: #0000ff;">function</span><span style="color: #000000;"> () {
            A </span>=<span style="color: #000000;"> YYC.Class({
                Public: {
                    done: </span><span style="color: #0000ff;">function</span><span style="color: #000000;"> () {
                        </span><span style="color: #0000ff;">throw</span> <span style="color: #0000ff;">new</span> Error(""<span style="color: #000000;">);
                    }
                }
            });
            B </span>=<span style="color: #000000;"> YYC.Class(A, {
                Public: {
                    done: </span><span style="color: #0000ff;">function</span><span style="color: #000000;"> () {
                        </span><span style="color: #0000ff;">this</span>.baseClass.done.call(<span style="color: #0000ff;">this</span>, <span style="color: #0000ff;">null</span><span style="color: #000000;">);
                    }
                }
            });
            C </span>=<span style="color: #000000;"> YYC.Class(B, {
                Public: {
                    a: </span>0<span style="color: #000000;">,

                    done: </span><span style="color: #0000ff;">function</span><span style="color: #000000;"> () {
                        </span><span style="color: #0000ff;">this</span><span style="color: #000000;">.base();

                        </span><span style="color: #0000ff;">this</span>.a = 100<span style="color: #000000;">;
                    }
                }
            });
            a </span>= <span style="color: #0000ff;">new</span><span style="color: #000000;"> A();
            b </span>= <span style="color: #0000ff;">new</span><span style="color: #000000;"> B();
            c </span>= <span style="color: #0000ff;">new</span><span style="color: #000000;"> C();

            sandbox </span>=<span style="color: #000000;"> sinon.sandbox.create();
        });
        afterEach(</span><span style="color: #0000ff;">function</span><span style="color: #000000;"> () {
            sandbox.restore();
        });

        it(</span>"让父类指定方法不执行，用于Class的测试方法中调用了父类方法的情况", <span style="color: #0000ff;">function</span><span style="color: #000000;"> () {
            expect(</span><span style="color: #0000ff;">function</span><span style="color: #000000;"> () {
                b.done();
            }).toThrow();
            expect(</span><span style="color: #0000ff;">function</span><span style="color: #000000;"> () {
                c.done();
            }).toThrow();

            b.stubParentMethod(sandbox, </span>"done"<span style="color: #000000;">);
            c.stubParentMethod(sandbox, </span>"done"<span style="color: #000000;">);

            expect(</span><span style="color: #0000ff;">function</span><span style="color: #000000;"> () {
                b.done();
            }).not.toThrow();
            expect(</span><span style="color: #0000ff;">function</span><span style="color: #000000;"> () {
                c.done();
            }).not.toThrow();
        });
        it(</span>"可将父类指定方法替换为假方法", <span style="color: #0000ff;">function</span><span style="color: #000000;"> () {
            c.stubParentMethod(sandbox, </span>"done", <span style="color: #0000ff;">function</span><span style="color: #000000;"> () {
                </span><span style="color: #0000ff;">this</span>.val = 1<span style="color: #000000;">;
            });

            c.done();

            expect(c.val).toEqual(</span>1<span style="color: #000000;">);
        });
        it(</span>"可按照sinon-&gt;stub API测试父类指定方法的调用情况", <span style="color: #0000ff;">function</span><span style="color: #000000;"> () {
            c.stubParentMethod(sandbox, </span>"done"<span style="color: #000000;">);

            c.done();

            expect(c.lastBaseClassForTest.done.calledOnce).toBeTruthy();
        });
    });

    describe(</span>"stubParentMethodByAClass", <span style="color: #0000ff;">function</span><span style="color: #000000;"> () {
        </span><span style="color: #0000ff;">var</span> sandbox = <span style="color: #0000ff;">null</span><span style="color: #000000;">;
        </span><span style="color: #0000ff;">var</span> A = <span style="color: #0000ff;">null</span><span style="color: #000000;">,
            B </span>= <span style="color: #0000ff;">null</span><span style="color: #000000;">,
            t </span>= <span style="color: #0000ff;">null</span><span style="color: #000000;">;

        beforeEach(</span><span style="color: #0000ff;">function</span><span style="color: #000000;"> () {
            A </span>=<span style="color: #000000;"> YYC.AClass({
                Public: {
                    a: </span>0<span style="color: #000000;">,
                    done: </span><span style="color: #0000ff;">function</span><span style="color: #000000;"> () {
                        </span><span style="color: #0000ff;">throw</span> <span style="color: #0000ff;">new</span> Error(""<span style="color: #000000;">);
                    }
                }
            });
            B </span>=<span style="color: #000000;"> YYC.AClass(A, {
                Public: {
                    done: </span><span style="color: #0000ff;">function</span><span style="color: #000000;"> () {
                        </span><span style="color: #0000ff;">this</span><span style="color: #000000;">.base();
                    }
                }
            });

            </span><span style="color: #008000;">//</span><span style="color: #008000;">想要测试B的done方法，必须先建一个空子类继承B，然后测试空子类的done方法</span>
            <span style="color: #0000ff;">function</span><span style="color: #000000;"> getInstance() {
                </span><span style="color: #0000ff;">var</span> T =<span style="color: #000000;"> YYC.Class(B, {
                });

                </span><span style="color: #0000ff;">return</span> <span style="color: #0000ff;">new</span><span style="color: #000000;"> T();
            }

            t </span>=<span style="color: #000000;"> getInstance();

            sandbox </span>=<span style="color: #000000;"> sinon.sandbox.create();
        });
        afterEach(</span><span style="color: #0000ff;">function</span><span style="color: #000000;"> () {
            sandbox.restore();
        });

        it(</span>"让父类指定方法不执行，用于AClass的测试方法中调用了父类方法的情况", <span style="color: #0000ff;">function</span><span style="color: #000000;"> () {
            expect(t.done).toThrow();

            t.stubParentMethodByAClass(sandbox, </span>"done"<span style="color: #000000;">);

            expect(t.done).not.toThrow();
        });
        it(</span>"可将父类指定方法替换为假方法", <span style="color: #0000ff;">function</span><span style="color: #000000;"> () {
            t.stubParentMethodByAClass(sandbox, </span>"done", <span style="color: #0000ff;">function</span><span style="color: #000000;"> () {
                </span><span style="color: #0000ff;">this</span>.val = 1<span style="color: #000000;">;
            });

            t.done();

            expect(t.val).toEqual(</span>1<span style="color: #000000;">);
        });
        it(</span>"可按照sinon-&gt;stub API测试父类指定方法的调用情况", <span style="color: #0000ff;">function</span><span style="color: #000000;"> () {
            t.stubParentMethodByAClass(sandbox, </span>"done"<span style="color: #000000;">);

            t.done();

            expect(t.lastBaseClassForTest.done.calledOnce).toBeTruthy();
        });
    });</span></pre>
</div>
<span class="cnblogs_code_collapse">View Code</span></div>
<h3>isInstanceOf</h3>
<p>判断是否为类的实例。</p>
<p>测试用例如下：</p>
<div class="cnblogs_code" onclick="cnblogs_code_show('b1730895-ca72-43f4-80d7-919d8312d0c8')"><img id="code_img_closed_b1730895-ca72-43f4-80d7-919d8312d0c8" class="code_img_closed" src="http://images.cnblogs.com/OutliningIndicators/ContractedBlock.gif" alt="" /><img id="code_img_opened_b1730895-ca72-43f4-80d7-919d8312d0c8" class="code_img_opened" style="display: none;" onclick="cnblogs_code_hide('b1730895-ca72-43f4-80d7-919d8312d0c8',event)" src="http://images.cnblogs.com/OutliningIndicators/ExpandedBlockStart.gif" alt="" />
<div id="cnblogs_code_open_b1730895-ca72-43f4-80d7-919d8312d0c8" class="cnblogs_code_hide">
<pre>     describe("isInstanceOf", <span style="color: #0000ff;">function</span><span style="color: #000000;"> () {
        it(</span>"直接判断是否为Class的实例", <span style="color: #0000ff;">function</span><span style="color: #000000;"> () {
            </span><span style="color: #0000ff;">var</span> A =<span style="color: #000000;"> YYC.Class({});

            expect(</span><span style="color: #0000ff;">new</span><span style="color: #000000;"> A().isInstanceOf(A)).toBeTruthy();
        });
        describe(</span>"测试继承抽象类时的情况", <span style="color: #0000ff;">function</span><span style="color: #000000;"> () {
            it(</span>"测试1", <span style="color: #0000ff;">function</span><span style="color: #000000;"> () {
                </span><span style="color: #0000ff;">var</span> A =<span style="color: #000000;"> YYC.AClass({});
                </span><span style="color: #0000ff;">var</span> B =<span style="color: #000000;"> YYC.Class(A, {});

                expect(</span><span style="color: #0000ff;">new</span><span style="color: #000000;"> B().isInstanceOf(B)).toBeTruthy();
                expect(</span><span style="color: #0000ff;">new</span><span style="color: #000000;"> B().isInstanceOf(A)).toBeTruthy();
            });
            it(</span>"测试2", <span style="color: #0000ff;">function</span><span style="color: #000000;"> () {
                </span><span style="color: #0000ff;">var</span> A =<span style="color: #000000;"> YYC.AClass({});
                </span><span style="color: #0000ff;">var</span> B =<span style="color: #000000;"> YYC.AClass(A, {});
                </span><span style="color: #0000ff;">var</span> C =<span style="color: #000000;"> YYC.Class(B, {});
                </span><span style="color: #0000ff;">var</span> D =<span style="color: #000000;"> YYC.Class(A, {});

                expect(</span><span style="color: #0000ff;">new</span><span style="color: #000000;"> C().isInstanceOf(B)).toBeTruthy();
                expect(</span><span style="color: #0000ff;">new</span><span style="color: #000000;"> C().isInstanceOf(A)).toBeTruthy();
                expect(</span><span style="color: #0000ff;">new</span><span style="color: #000000;"> D().isInstanceOf(A)).toBeTruthy();
                expect(</span><span style="color: #0000ff;">new</span><span style="color: #000000;"> D().isInstanceOf(B)).toBeFalsy();
            });
        });

        describe(</span>"测试继承接口时的情况", <span style="color: #0000ff;">function</span><span style="color: #000000;"> () {
            it(</span>"测试1", <span style="color: #0000ff;">function</span><span style="color: #000000;"> () {
                </span><span style="color: #0000ff;">var</span> A = YYC.Interface("a"<span style="color: #000000;">);
                </span><span style="color: #0000ff;">var</span> B =<span style="color: #000000;"> YYC.Class({Interface: A}, {
                    Public: {
                        a: </span><span style="color: #0000ff;">function</span><span style="color: #000000;"> () {
                        }
                    }
                });

                expect(</span><span style="color: #0000ff;">new</span><span style="color: #000000;"> B().isInstanceOf(B)).toBeTruthy();
                expect(</span><span style="color: #0000ff;">new</span><span style="color: #000000;"> B().isInstanceOf(A)).toBeTruthy();
            });
            it(</span>"测试2", <span style="color: #0000ff;">function</span><span style="color: #000000;"> () {
                </span><span style="color: #0000ff;">var</span> A = YYC.Interface("a"<span style="color: #000000;">);
                </span><span style="color: #0000ff;">var</span> B = YYC.Interface("b"<span style="color: #000000;">);
                </span><span style="color: #0000ff;">var</span> C = YYC.Interface([A, B], "c"<span style="color: #000000;">);
                </span><span style="color: #0000ff;">var</span> D =<span style="color: #000000;"> YYC.Class({Interface: C}, {
                    Public: {
                        a: </span><span style="color: #0000ff;">function</span><span style="color: #000000;"> () {
                        },
                        b: </span><span style="color: #0000ff;">function</span><span style="color: #000000;"> () {
                        },
                        c: </span><span style="color: #0000ff;">function</span><span style="color: #000000;"> () {
                        }
                    }
                });

                expect(</span><span style="color: #0000ff;">new</span><span style="color: #000000;"> D().isInstanceOf(C)).toBeTruthy();
                expect(</span><span style="color: #0000ff;">new</span><span style="color: #000000;"> D().isInstanceOf(B)).toBeTruthy();
                expect(</span><span style="color: #0000ff;">new</span><span style="color: #000000;"> D().isInstanceOf(A)).toBeTruthy();
            });
        });

        it(</span>"综合测试", <span style="color: #0000ff;">function</span><span style="color: #000000;"> () {
            </span><span style="color: #0000ff;">var</span> A = YYC.Interface("a1"<span style="color: #000000;">);
            </span><span style="color: #0000ff;">var</span> B = YYC.Interface(A, "a2"<span style="color: #000000;">);
            </span><span style="color: #0000ff;">var</span> C =<span style="color: #000000;"> YYC.AClass({Interface: B}, {
                Public: {
                    a1: </span><span style="color: #0000ff;">function</span><span style="color: #000000;"> () {
                    },
                    a2: </span><span style="color: #0000ff;">function</span><span style="color: #000000;"> () {
                    }
                }
            });
            </span><span style="color: #0000ff;">var</span> D =<span style="color: #000000;"> YYC.AClass(C, {
                Public: {
                    a1: </span><span style="color: #0000ff;">function</span><span style="color: #000000;"> () {
                    },
                    a2: </span><span style="color: #0000ff;">function</span><span style="color: #000000;"> () {
                    }
                }
            });
            </span><span style="color: #0000ff;">var</span> E =<span style="color: #000000;"> YYC.Class(C, {
            });
            </span><span style="color: #0000ff;">var</span> F =<span style="color: #000000;"> YYC.Class(E, {
            });
            </span><span style="color: #0000ff;">var</span> G =<span style="color: #000000;"> YYC.Class({Interface: B, Class: D}, {
            });

            expect(</span><span style="color: #0000ff;">new</span><span style="color: #000000;"> E().isInstanceOf(C)).toBeTruthy();
            expect(</span><span style="color: #0000ff;">new</span><span style="color: #000000;"> E().isInstanceOf(B)).toBeTruthy();
            expect(</span><span style="color: #0000ff;">new</span><span style="color: #000000;"> E().isInstanceOf(A)).toBeTruthy();

            expect(</span><span style="color: #0000ff;">new</span><span style="color: #000000;"> F().isInstanceOf(E)).toBeTruthy();
            expect(</span><span style="color: #0000ff;">new</span><span style="color: #000000;"> F().isInstanceOf(C)).toBeTruthy();
            expect(</span><span style="color: #0000ff;">new</span><span style="color: #000000;"> F().isInstanceOf(B)).toBeTruthy();
            expect(</span><span style="color: #0000ff;">new</span><span style="color: #000000;"> F().isInstanceOf(A)).toBeTruthy();

            expect(</span><span style="color: #0000ff;">new</span><span style="color: #000000;"> G().isInstanceOf(B)).toBeTruthy();
            expect(</span><span style="color: #0000ff;">new</span><span style="color: #000000;"> G().isInstanceOf(D)).toBeTruthy();

            expect(</span><span style="color: #0000ff;">new</span><span style="color: #000000;"> G().isInstanceOf(E)).toBeFalsy();
        });
    }); </span></pre>
</div>
<span class="cnblogs_code_collapse">View Code</span></div>
<h3>YOOP.version</h3>
<p>返回当前版本号。</p>
<p>测试用例如下：</p>
<div class="cnblogs_code">
<pre><span style="color: #000000;">    it("获得当前版本号", function () {
       expect(YYC.YOOP.version).toBeString();
    });</span></pre>
</div>
</div>
<h1>约定</h1>
<p>在该框架的实现中，类的实例可以访问类的公有成员、保护成员、私有成员，所有成员都是添加到类的原型中（如果是继承，则将父类的成员添和子类的成员都添加到子类的原型中），框架只是从语义上区分了成员的访问权限，在机制上没有对成员的访问权限设任何限制！</p>
<p>因此，用户需要采用<span style="color: #ff0000;">命名约定</span>的方式来区分不同的成员，需要自觉遵守访问权限规则（如类的实例只能访问公有成员；不能访问其它类的私有成员；子类可以访问父类的保护成员等等）。</p>
<h2>私有成员和保护成员的建议命名约定</h2>
<p>建议的命名约定</p>
<p>基类的私有成员以&ldquo;_&rdquo;开头，保护成员以&ldquo;P_&rdquo;开头。</p>
<p>在继承中，第一层子类私有成员以&ldquo;__&rdquo;开头，第二层子类私有成员以&ldquo;___&rdquo;开头，以此类推。。。。。。（因为接口都是公有成员，故考虑该命名约定时忽略接口。）</p>
<p>每层类的保护成员前缀可以都为&ldquo;P_&rdquo;，不需要根据继承层级的不同，设置为&ldquo;P__&rdquo;、&ldquo;P___&rdquo;等。</p>
<p>因为一般而言，每层类的保护成员名字都不会一样，只有当子类需要专门重写父类的保护成员时，子类的保护成员才会与父类保护成员同名。</p>
<p>如：</p>
<p>不继承接口：</p>
<div class="cnblogs_code">
<pre><span style="color: #0000ff;">var</span> A = YYC.AClass({    <span style="color: #008000;">//</span><span style="color: #008000;">A为基类</span>
<span style="color: #000000;">    Private: {
        _value: </span><span style="color: #800080;">0</span><span style="color: #000000;">,
        _method: function () { }
    },
    Protected: {
        P_value: </span><span style="color: #800080;">0</span><span style="color: #000000;">,
        P_method: function () { }
    }
});
</span><span style="color: #0000ff;">var</span> B = YYC.Class(A, {  <span style="color: #008000;">//</span><span style="color: #008000;">B为第一层子类</span>
<span style="color: #000000;">    Private: {
        __value: </span><span style="color: #800080;">0</span><span style="color: #000000;">,
        __method: function () { }
    }</span><span style="color: #000000;">
});</span></pre>
</div>
<p>继承接口：</p>
<div class="cnblogs_code">
<pre><span style="color: #0000ff;">var</span> I = YYC.Interface(<span style="color: #800000;">"</span><span style="color: #800000;">method</span><span style="color: #800000;">"</span><span style="color: #000000;">);
</span><span style="color: #0000ff;">var</span> A = YYC.AClass({ Interface: I }, {
<span style="color: #000000;">    Private: {
        _value: </span><span style="color: #800080;">0</span><span style="color: #000000;">,
        _method: function () { }
    },
    Protected: {
        P_method: function () { }
    }
});
</span><span style="color: #0000ff;">var</span> B = YYC.Class(A, {  <span style="color: #008000;">//</span><span style="color: #008000;">B为第一层子类</span>
<span style="color: #000000;">    Private: {
        __value: </span><span style="color: #800080;">0</span><span style="color: #000000;">,
        __method: function () { }
    },
    Public: {
        method: function () { }
    }
});</span></pre>
</div>
<h3>为什么每层子类的私有成员前缀最好不一样？</h3>
<p>因为如果子类与父类有同名的私有成员时，当子类调用父类成员时，可能会出现以下情形的问题：</p>
<div class="cnblogs_code">
<pre><span style="color: #0000ff;">var</span> A =<span style="color: #000000;"> YYC.Class({
    Private: {
        _val: </span><span style="color: #800080;">100</span><span style="color: #000000;">
    },
    Public: {
        getVal: function () {
            </span><span style="color: #0000ff;">return</span> <span style="color: #0000ff;">this</span><span style="color: #000000;">._val;
        }
    }
});

</span><span style="color: #0000ff;">var</span> B =<span style="color: #000000;"> YYC.Class(A, {
    Private: {
        _val: </span><span style="color: #800080;">200</span><span style="color: #000000;">
    },
    Public: {
        getVal: function () {
            </span><span style="color: #0000ff;">return</span> <span style="color: #0000ff;">this</span>.<span style="color: #0000ff;">base</span><span style="color: #000000;">();
        }
    }
});

</span><span style="color: #008000;">//</span><span style="color: #008000;">无法通过测试！实际值为200
</span><span style="color: #008000;">//</span><span style="color: #008000;">这是因为通过&ldquo;this.base()&rdquo;调用父类A的getVal时，返回的是B覆写的_val！</span>
expect(<span style="color: #0000ff;">new</span> B().getVal()).toEqual(<span style="color: #800080;">100</span>);</pre>
</div>
<p>用户也可以将第一层子类的私有成员前缀设为&ldquo;_1_&rdquo;，第二层子类的私有成员设为&ldquo;_2_&rdquo;。。。。。。</p>
<p>前缀设置规则用户可自订，<span style="color: #ff0000;"><span style="color: #000000;">只要能</span>在继承中使不同层级的类的私有不同名即可</span>。</p>
<h2>baseClass</h2>
<p>为了防止子类的prototype.baseClass覆盖父类prototype.baseClass，在子类继承父类时，用户需要先判断父类prototype.baseClass是否存在。如果存在，则加上前缀&ldquo;_&rdquo;，如&ldquo;_baseClass&rdquo;。如果加上前缀后依然存在，则再加上前缀&ldquo;_&rdquo;，如&ldquo;__baseClass&rdquo;。以此类推。</p>
<p>如：</p>
<div class="cnblogs_code" onclick="cnblogs_code_show('cd98ce59-5a2e-4bc6-a6d7-f592a6c41ecb')"><img id="code_img_closed_cd98ce59-5a2e-4bc6-a6d7-f592a6c41ecb" class="code_img_closed" src="http://images.cnblogs.com/OutliningIndicators/ContractedBlock.gif" alt="" /><img id="code_img_opened_cd98ce59-5a2e-4bc6-a6d7-f592a6c41ecb" class="code_img_opened" style="display: none;" onclick="cnblogs_code_hide('cd98ce59-5a2e-4bc6-a6d7-f592a6c41ecb',event)" src="http://images.cnblogs.com/OutliningIndicators/ExpandedBlockStart.gif" alt="" />
<div id="cnblogs_code_open_cd98ce59-5a2e-4bc6-a6d7-f592a6c41ecb" class="cnblogs_code_hide">
<pre>                <span style="color: #0000ff;">var</span> A1 =<span style="color: #000000;"> YYC.AClass({
                    Public: {
                        arr: [],
                        a: function () {
                            </span><span style="color: #0000ff;">this</span>.arr.push(<span style="color: #800080;">1</span><span style="color: #000000;">);
                        }
                    }
                });
                </span><span style="color: #0000ff;">var</span> A2 =<span style="color: #000000;"> YYC.AClass(A1, {
                    Public: {
                        a: function () {
                            </span><span style="color: #0000ff;">this</span>.arr.push(<span style="color: #800080;">2</span><span style="color: #000000;">);
                            </span><span style="color: #0000ff;">this</span>.baseClass.a.call(<span style="color: #0000ff;">this</span>, <span style="color: #0000ff;">null</span>);  <span style="color: #008000;">//</span><span style="color: #008000;">调用A1.a</span>
<span style="color: #000000;">                        }
                    }
                });
                </span><span style="color: #0000ff;">var</span> B =<span style="color: #000000;"> YYC.Class(A2, {
                    Public: {
                        a: function () {
                            </span><span style="color: #0000ff;">this</span>.arr.push(<span style="color: #800080;">3</span><span style="color: #000000;">);
                            </span><span style="color: #0000ff;">this</span>._baseClass.a.call(<span style="color: #0000ff;">this</span>, <span style="color: #0000ff;">null</span>); <span style="color: #008000;">//</span><span style="color: #008000;">调用A2.a</span>
                            <span style="color: #0000ff;">this</span>.baseClass.a.call(<span style="color: #0000ff;">this</span>, <span style="color: #0000ff;">null</span>);  <span style="color: #008000;">//</span><span style="color: #008000;">调用A1.a</span>

                            <span style="color: #0000ff;">return</span> <span style="color: #0000ff;">this</span><span style="color: #000000;">.arr;
                        }
                    }
                });
                </span><span style="color: #0000ff;">var</span> b = <span style="color: #0000ff;">new</span><span style="color: #000000;"> B();

                expect(b.a()).toEqual([</span><span style="color: #800080;">3</span>, <span style="color: #800080;">2</span>, <span style="color: #800080;">1</span>, <span style="color: #800080;">1</span>]);</pre>
</div>
<span class="cnblogs_code_collapse">View Code</span></div>
<h1>注意事项</h1>
<p><strong><span style="font-size: 18px;">子类使用this.baseClass调用父类成员时，要将父类成员的this指向子类。</span></strong></p>
<p>错误的写法：</p>
<div class="cnblogs_code">
<pre><span style="color: #0000ff;">var</span> A =<span style="color: #000000;"> YYC.AClass({
    Public: {
        method: function () {
            </span><span style="color: #0000ff;">this</span>.p = <span style="color: #800080;">100</span><span style="color: #000000;">;
        }
    }
});
</span><span style="color: #0000ff;">var</span> B =<span style="color: #000000;"> YYC.Class(A, {
    Public: {
        method: function () {
            </span><span style="color: #0000ff;">this</span><span style="color: #000000;">.baseClass.method();
        }
    }
});
</span><span style="color: #0000ff;">var</span> b = <span style="color: #0000ff;">new</span><span style="color: #000000;"> B();
b.method();
console.log(b.p);   </span><span style="color: #008000;">//</span><span style="color: #008000;">此处为undefined，而不是100！</span></pre>
</div>
<p>正确的写法：</p>
<div class="cnblogs_code">
<pre><span style="color: #0000ff;">var</span> A =<span style="color: #000000;"> YYC.AClass({
    Public: {
        method: function () {
            </span><span style="color: #0000ff;">this</span>.p = <span style="color: #800080;">100</span><span style="color: #000000;">;
        }
    }
});
</span><span style="color: #0000ff;">var</span> B =<span style="color: #000000;"> YYC.Class(A, {
    Public: {
        method: function () {
            </span><span style="color: #0000ff;">this</span>.baseClass.method.call(<span style="color: #0000ff;">this</span>, <span style="color: #0000ff;">null</span><span style="color: #000000;">);
        }
    }
});
</span><span style="color: #0000ff;">var</span> b = <span style="color: #0000ff;">new</span><span style="color: #000000;"> B();
b.method();
console.log(b.p);   </span><span style="color: #008000;">//</span><span style="color: #008000;">100</span></pre>
</div>
<h1>已解决的问题</h1>
<p>1、同一个类的实例之间不应该共享属性。</p>
<p><strong>问题描述</strong></p>
<p>参考下面的代码：</p>
<div class="cnblogs_code">
<pre>            <span style="color: #0000ff;">var</span> A =<span style="color: #000000;"> YYC.Class({
                Init: function () {
                },
                Public: {
                    a:[]
                }
            });

            </span><span style="color: #0000ff;">var</span> t = <span style="color: #0000ff;">new</span><span style="color: #000000;"> A();
            t.a.push(</span><span style="color: #800000;">"</span><span style="color: #800000;">a</span><span style="color: #800000;">"</span><span style="color: #000000;">);
            </span><span style="color: #0000ff;">var</span> m = <span style="color: #0000ff;">new</span><span style="color: #000000;"> A();

            expect(t.a).toEqual([</span><span style="color: #800000;">"</span><span style="color: #800000;">a</span><span style="color: #800000;">"</span><span style="color: #000000;">]);
            expect(m.a).toEqual([]);    </span><span style="color: #008000;">//</span><span style="color: #008000;">失败！实际为["a"]！</span></pre>
</div>
<p><strong><span style="font-size: 1em; line-height: 1.5;">原因分析</span></strong></p>
<p>因为YOOP将类的成员都加入到类的原