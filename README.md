<p>��Һã���������ʽ�����ҵ�OOP���<span style="color: #000000; font-size: 18px;">YOOP</span>���ÿ�ܽ����������߸��õؽ�����������̡�</p>
<p>��ǰ�汾�ţ�v1.1</p>
<h1>����</h1>
<p>�ÿ�ܰ����ӿڡ������ࡢ�ࡣ</p>
<p>�ӿ�Interface���Լ̳ж���ӿڣ����Զ��巽�������ԡ�</p>
<p>������AClass���Լ̳ж���ӿڡ�һ�������࣬���Զ��幹�캯�������г�Ա��˽�г�Ա��������Ա����̬��Ա���鷽���������Ա��</p>
<p>��Class���Լ̳ж���ӿڡ�һ����������࣬���Զ��幹�캯�������г�Ա��˽�г�Ա��������Ա����̬��Ա���鷽����&nbsp;</p>
<h2><span style="background-color: #ffffff; color: #000000;">������ø����Ա</span></h2>
<p>�������У�����ʹ��this.base()�����ø���ͬ��������Ҳ����ʹ��this.baseClass�����ʸ����ԭ�͡�</p>
<h2><span style="background-color: #ffffff; color: #000000;">��Ҫ���﷨����</span></h2>
<p>�����ͼ���������ԣ����׳��쳣��</p>
<h3>��Class��</h3>
<ol>
<li>����ʵ��ʱ���ù��캯����</li>
<li>��֤�Ƿ�ʵ���˽ӿڵķ��������ԣ����û��ʵ�ֻ��׳��쳣��</li>
<li>��֤�Ƿ�ʵ���˸���ĳ����Ա�����û��ʵ�ֻ��׳��쳣��</li>
<li>ֻ�ܼ̳�һ���ࣨAClass��Class���������׳��쳣.</li>
<li>���ܶ�������Ա�������׳��쳣��</li>
</ol>
<h3>������AClass��</h3>
<ol>
<li>�����������캯����������Class���á�</li>
<li>����������̳���Class�����׳��쳣��</li>
<li>����ʵ�ֽӿڣ����Խ�������Classʵ�֡�</li>
<li>����ʵ�ָ�������Ա�����Խ�������Classʵ�֡�</li>
<li>ֻ�ܼ̳�һ��������AClass�������׳��쳣��</li>
</ol>
<h3>�ӿ�Interface��</h3>
<ol>
<li>�ӿ�ֻ�ܼ̳нӿڣ������׳��쳣��&nbsp;</li>
</ol>
<p>ʹ��YOOP</p>
<p>YOOP֧��AMD��CMD��CommonJS�淶������Sea.js��node.js��ʹ�ã�</p>
<div class="cnblogs_code">
<pre><span style="color: #0000ff;">var</span> yoop = require(<span style="color: #800000;">"</span><span style="color: #800000;">./YOOP.js</span><span style="color: #800000;">"</span><span style="color: #000000;">);

yoop.Class({});</span></pre>
</div>
<p>Ҳ����<span style="font-size: 14px; line-height: 1.5;">ͨ��script��ǩ��ҳ����ֱ������</span></p>
<p><span style="font-size: 14px; line-height: 1.5;">ҳ��������script��</span></p>
<div class="cnblogs_code">
<pre><span style="color: #0000ff;">&lt;</span><span style="color: #800000;">script </span><span style="color: #ff0000;">src</span><span style="color: #0000ff;">="./YOOP.js"</span><span style="color: #0000ff;">&gt;&lt;/</span><span style="color: #800000;">script</span><span style="color: #0000ff;">&gt;</span></pre>
</div>
<p>Ȼ��ͨ�������ռ�YYC��ʹ�ã�</p>
<div class="cnblogs_code">
<pre>YYC.Class({});</pre>
</div>
<h1>�÷�</h1>
<h2>�ӿ�</h2>
<h3>����ӿ�</h3>
<p>ֻ�з�����</p>
<div class="cnblogs_code">
<pre><span style="color: #0000ff;">var</span> A = YYC.Interface(<span style="color: #800000;">"</span><span style="color: #800000;">method1</span><span style="color: #800000;">"</span>, <span style="color: #800000;">"</span><span style="color: #800000;">method2</span><span style="color: #800000;">"</span>);</pre>
</div>
<p>ֻ�����ԣ�</p>
<div class="cnblogs_code">
<pre><span style="color: #0000ff;">var</span> A = YYC.Interface([], [<span style="color: #800000;">"</span><span style="color: #800000;">attribute1</span><span style="color: #800000;">"</span>, <span style="color: #800000;">"</span><span style="color: #800000;">attribute2</span><span style="color: #800000;">"</span>]);</pre>
</div>
<p>���з����������ԣ�</p>
<div class="cnblogs_code">
<pre><span style="color: #0000ff;">var</span> A = YYC.Interface([<span style="color: #800000;">"</span><span style="color: #800000;">method1</span><span style="color: #800000;">"</span>, <span style="color: #800000;">"</span><span style="color: #800000;">method2</span><span style="color: #800000;">"</span>], [<span style="color: #800000;">"</span><span style="color: #800000;">attribute1</span><span style="color: #800000;">"</span>, <span style="color: #800000;">"</span><span style="color: #800000;">attribute2</span><span style="color: #800000;">"</span>]);</pre>
</div>
<h3>�̳нӿ�</h3>
<div class="cnblogs_code">
<pre><span style="color: #0000ff;">var</span> A = YYC.Interface([<span style="color: #800000;">"</span><span style="color: #800000;">method1</span><span style="color: #800000;">"</span>, <span style="color: #800000;">"</span><span style="color: #800000;">method2</span><span style="color: #800000;">"</span>],[<span style="color: #800000;">"</span><span style="color: #800000;">attribute1</span><span style="color: #800000;">"</span>, <span style="color: #800000;">"</span><span style="color: #800000;">attribute2</span><span style="color: #800000;">"</span><span style="color: #000000;">]);
</span><span style="color: #0000ff;">var</span> B = YYC.Interface(A, <span style="color: #800000;">"</span><span style="color: #800000;">m1</span><span style="color: #800000;">"</span>, <span style="color: #800000;">"</span><span style="color: #800000;">m2</span><span style="color: #800000;">"</span><span style="color: #000000;">);
</span><span style="color: #0000ff;">var</span> C = YYC.Interface([A], [<span style="color: #800000;">"</span><span style="color: #800000;">m1</span><span style="color: #800000;">"</span>, <span style="color: #800000;">"</span><span style="color: #800000;">m2</span><span style="color: #800000;">"</span>], [<span style="color: #800000;">"</span><span style="color: #800000;">a1</span><span style="color: #800000;">"</span>, <span style="color: #800000;">"</span><span style="color: #800000;">a2</span><span style="color: #800000;">"</span><span style="color: #000000;">]);
</span><span style="color: #0000ff;">var</span> D = YYC.Interface([A, B], [<span style="color: #800000;">"</span><span style="color: #800000;">m1</span><span style="color: #800000;">"</span>, <span style="color: #800000;">"</span><span style="color: #800000;">m2</span><span style="color: #800000;">"</span>], [<span style="color: #800000;">"</span><span style="color: #800000;">a1</span><span style="color: #800000;">"</span>, <span style="color: #800000;">"</span><span style="color: #800000;">a2</span><span style="color: #800000;">"</span>]);</pre>
</div>
<h2>������</h2>
<h3>���������</h3>
<div class="cnblogs_code" onclick="cnblogs_code_show('74d2895c-4a23-4e35-9396-13051e6c6202')"><img id="code_img_closed_74d2895c-4a23-4e35-9396-13051e6c6202" class="code_img_closed" src="http://images.cnblogs.com/OutliningIndicators/ContractedBlock.gif" alt="" /><img id="code_img_opened_74d2895c-4a23-4e35-9396-13051e6c6202" class="code_img_opened" style="display: none;" onclick="cnblogs_code_hide('74d2895c-4a23-4e35-9396-13051e6c6202',event)" src="http://images.cnblogs.com/OutliningIndicators/ExpandedBlockStart.gif" alt="" />
<div id="cnblogs_code_open_74d2895c-4a23-4e35-9396-13051e6c6202" class="cnblogs_code_hide">
<pre><span style="color: #0000ff;">var</span> A =<span style="color: #000000;"> YYC.AClass({
    Init: </span><span style="color: #0000ff;">function</span> () { <span style="color: #008000;">//</span><span style="color: #008000;">���캯��</span>
<span style="color: #000000;">    },
    Protected: {    </span><span style="color: #008000;">//</span><span style="color: #008000;">������Ա</span>
        Abstract: { <span style="color: #008000;">//</span><span style="color: #008000;">���������Ա</span>
<span style="color: #000000;">        },
        Virtual: {  </span><span style="color: #008000;">//</span><span style="color: #008000;">�����鷽��</span>
<span style="color: #000000;">        },
        P_proA: </span><span style="color: #0000ff;">true</span>,   <span style="color: #008000;">//</span><span style="color: #008000;">��������</span>
       P_proM: <span style="color: #0000ff;">function</span> () { }    <span style="color: #008000;">//</span><span style="color: #008000;">��������</span>
<span style="color: #000000;">    },
    Public: {   </span><span style="color: #008000;">//</span><span style="color: #008000;">���г�Ա</span>
        Abstract: { <span style="color: #008000;">//</span><span style="color: #008000;">���г����Ա</span>
<span style="color: #000000;">        },
        Virtual: {  </span><span style="color: #008000;">//</span><span style="color: #008000;">�����鷽��</span>
<span style="color: #000000;">        },
        pubM: </span><span style="color: #0000ff;">function</span> () { },  <span style="color: #008000;">//</span><span style="color: #008000;">���з���</span>
      pubA: 0    <span style="color: #008000;">//</span><span style="color: #008000;">��������</span>
<span style="color: #000000;">    },
    Private: {  </span><span style="color: #008000;">//</span><span style="color: #008000;">˽�г�Ա</span>
        _priA: "",   <span style="color: #008000;">//</span><span style="color: #008000;">˽������</span>
        _priM: <span style="color: #0000ff;">function</span> () { } <span style="color: #008000;">//</span><span style="color: #008000;">˽�з���</span>
<span style="color: #000000;">    },
    Abstract: { </span><span style="color: #008000;">//</span><span style="color: #008000;">���г����Ա</span>
<span style="color: #000000;">    },
    Virtual: {  </span><span style="color: #008000;">//</span><span style="color: #008000;">�����鷽��</span>
<span style="color: #000000;">    }
});</span></pre>
</div>

<h3>�̳г�����</h3>
<div class="cnblogs_code" onclick="cnblogs_code_show('86502fa7-140a-46a9-9ca3-cc15a69312c9')"><img id="code_img_closed_86502fa7-140a-46a9-9ca3-cc15a69312c9" class="code_img_closed" src="http://images.cnblogs.com/OutliningIndicators/ContractedBlock.gif" alt="" /><img id="code_img_opened_86502fa7-140a-46a9-9ca3-cc15a69312c9" class="code_img_opened" style="display: none;" onclick="cnblogs_code_hide('86502fa7-140a-46a9-9ca3-cc15a69312c9',event)" src="http://images.cnblogs.com/OutliningIndicators/ExpandedBlockStart.gif" alt="" />
<div id="cnblogs_code_open_86502fa7-140a-46a9-9ca3-cc15a69312c9" class="cnblogs_code_hide">
<pre><span style="color: #0000ff;">var</span> A =<span style="color: #000000;"> YYC.AClass({});
</span><span style="color: #0000ff;">var</span> B =<span style="color: #000000;"> YYC.AClass(A, {});
</span><span style="color: #0000ff;">var</span> C = YYC.AClass({Class: A}, {}); </pre>
</div>

<h3>�̳нӿ�</h3>
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

<h3>�̳нӿںͳ�����</h3>
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

<h2>��</h2>
<h3>������</h3>
<div class="cnblogs_code" onclick="cnblogs_code_show('9e441a77-56a3-4ab3-84c3-75f649488695')"><img id="code_img_closed_9e441a77-56a3-4ab3-84c3-75f649488695" class="code_img_closed" src="http://images.cnblogs.com/OutliningIndicators/ContractedBlock.gif" alt="" /><img id="code_img_opened_9e441a77-56a3-4ab3-84c3-75f649488695" class="code_img_opened" style="display: none;" onclick="cnblogs_code_hide('9e441a77-56a3-4ab3-84c3-75f649488695',event)" src="http://images.cnblogs.com/OutliningIndicators/ExpandedBlockStart.gif" alt="" />
<div id="cnblogs_code_open_9e441a77-56a3-4ab3-84c3-75f649488695" class="cnblogs_code_hide">
<pre><span style="color: #0000ff;">var</span> A =<span style="color: #000000;"> YYC.Class({
                Init: function () { </span><span style="color: #008000;">//</span><span style="color: #008000;">���캯��</span>
<span style="color: #000000;">                },
                Protected: {    </span><span style="color: #008000;">//</span><span style="color: #008000;">������Ա</span>
                    Virtual: {  <span style="color: #008000;">//</span><span style="color: #008000;">�����鷽��</span>
<span style="color: #000000;">                    },
                    P_proA: </span><span style="color: #0000ff;">true</span>,   <span style="color: #008000;">//</span><span style="color: #008000;">��������</span>
                    P_proM: function () { }    <span style="color: #008000;">//</span><span style="color: #008000;">��������</span>
<span style="color: #000000;">                },
                Public: {   </span><span style="color: #008000;">//</span><span style="color: #008000;">���г�Ա</span>
                    Virtual: {  <span style="color: #008000;">//</span><span style="color: #008000;">�����鷽��</span>
<span style="color: #000000;">                    },
                    pubM: function () { },  </span><span style="color: #008000;">//</span><span style="color: #008000;">���з���</span>
                    pubA: <span style="color: #800080;">0</span>    <span style="color: #008000;">//</span><span style="color: #008000;">��������</span>
<span style="color: #000000;">                },
                Private: {  </span><span style="color: #008000;">//</span><span style="color: #008000;">˽�г�Ա</span>
                    _priA: <span style="color: #800000;">""</span>,   <span style="color: #008000;">//</span><span style="color: #008000;">˽������</span>
                    _priM: function () { } <span style="color: #008000;">//</span><span style="color: #008000;">˽�з���</span>
<span style="color: #000000;">                },
                Virtual: {  </span><span style="color: #008000;">//</span><span style="color: #008000;">�����鷽��</span>
<span style="color: #000000;">                }
            });</span></pre>
</div>

<h3>�̳г�����</h3>
<div class="cnblogs_code" onclick="cnblogs_code_show('9384a505-35bc-44d2-aa46-b5e0deed39f9')"><img id="code_img_closed_9384a505-35bc-44d2-aa46-b5e0deed39f9" class="code_img_closed" src="http://images.cnblogs.com/OutliningIndicators/ContractedBlock.gif" alt="" /><img id="code_img_opened_9384a505-35bc-44d2-aa46-b5e0deed39f9" class="code_img_opened" style="display: none;" onclick="cnblogs_code_hide('9384a505-35bc-44d2-aa46-b5e0deed39f9',event)" src="http://images.cnblogs.com/OutliningIndicators/ExpandedBlockStart.gif" alt="" />
<div id="cnblogs_code_open_9384a505-35bc-44d2-aa46-b5e0deed39f9" class="cnblogs_code_hide">
<pre><span style="color: #0000ff;">var</span> A =<span style="color: #000000;"> YYC.AClass({});
</span><span style="color: #0000ff;">var</span> B =<span style="color: #000000;"> YYC.AClass(A, {});
</span><span style="color: #0000ff;">var</span> C = YYC.AClass({ Class: A }, {});</pre>
</div>

<h3>�̳���</h3>
<div class="cnblogs_code" onclick="cnblogs_code_show('976ac329-56ac-4f09-811f-66706040d12f')"><img id="code_img_closed_976ac329-56ac-4f09-811f-66706040d12f" class="code_img_closed" src="http://images.cnblogs.com/OutliningIndicators/ContractedBlock.gif" alt="" /><img id="code_img_opened_976ac329-56ac-4f09-811f-66706040d12f" class="code_img_opened" style="display: none;" onclick="cnblogs_code_hide('976ac329-56ac-4f09-811f-66706040d12f',event)" src="http://images.cnblogs.com/OutliningIndicators/ExpandedBlockStart.gif" alt="" />
<div id="cnblogs_code_open_976ac329-56ac-4f09-811f-66706040d12f" class="cnblogs_code_hide">
<pre><span style="color: #0000ff;">var</span> A =<span style="color: #000000;"> YYC.Class({});
</span><span style="color: #0000ff;">var</span> B =<span style="color: #000000;"> YYC.Class(A, {});
</span><span style="color: #0000ff;">var</span> C = YYC.Class({ Class: A }, {});</pre>
</div>

<h3>�̳нӿ�</h3>
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

<h3>�̳нӿںͳ�����/��</h3>
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

<h2>���캯��</h2>
<div class="cnblogs_code" onclick="cnblogs_code_show('1f31e68a-88be-4e95-85a9-35fcd59c1d1c')"><img id="code_img_closed_1f31e68a-88be-4e95-85a9-35fcd59c1d1c" class="code_img_closed" src="http://images.cnblogs.com/OutliningIndicators/ContractedBlock.gif" alt="" /><img id="code_img_opened_1f31e68a-88be-4e95-85a9-35fcd59c1d1c" class="code_img_opened" style="display: none;" onclick="cnblogs_code_hide('1f31e68a-88be-4e95-85a9-35fcd59c1d1c',event)" src="http://images.cnblogs.com/OutliningIndicators/ExpandedBlockStart.gif" alt="" />
<div id="cnblogs_code_open_1f31e68a-88be-4e95-85a9-35fcd59c1d1c" class="cnblogs_code_hide">
<pre><span style="color: #0000ff;">var</span> A =<span style="color: #000000;"> YYC.Class({
����Init: function(t){
��������</span><span style="color: #0000ff;">this</span>.value =<span style="color: #000000;"> t;
����}
});
</span><span style="color: #0000ff;">var</span> a = <span style="color: #0000ff;">new</span> A(<span style="color: #800080;">100</span><span style="color: #000000;">);
console.log(a.value);����</span><span style="color: #008000;">//</span><span style="color: #008000;">100</span></pre>
</div>

<h2>��̬��Ա</h2>
<p>ʹ��&ldquo;��.��̬��Ա&rdquo;����ʽ�����þ�̬��Ա�����ﾲ̬��Աʵ�����ࣨfunction��functionҲ�Ƕ��󣩵ĳ�Ա��</p>
<p>ע�⣡��̬�����е�thisָ���࣬����ָ�����ʵ����</p>
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

<h2>��ĳ�Ա�������</h2>
<p>ʹ��this�����á�</p>
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

<h2>������ø���</h2>
<p>ʹ��this.base()�ɵ��ø���ͬ��������</p>
<p>ʹ��this.baseClass.xx.call(this, xx)�ɵ��ø���ĳ�Ա��</p>
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

<h2>�����������</h2>
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

<h2>��д���෽����ʵ�ֽӿڳ�Ա�������Ա</h2>
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
            console.log(</span><span style="color: #800000;">"</span><span style="color: #800000;">ʵ�ֳ��󷽷�</span><span style="color: #800000;">"</span><span style="color: #000000;">);
        }
    },
    Public: {
        method: function () {
            console.log(</span><span style="color: #800000;">"</span><span style="color: #800000;">���Ǹ���ͬ������</span><span style="color: #800000;">"</span><span style="color: #000000;">);
        },
        m1: function () {
            console.log(</span><span style="color: #800000;">"</span><span style="color: #800000;">ʵ�ֽӿ�</span><span style="color: #800000;">"</span><span style="color: #000000;">);
        }
    }
});</span></pre>
</div>
<span class="cnblogs_code_collapse">View Code</span></div>
<div onclick="cnblogs_code_show('97fdfde9-9bae-4c6a-9edf-8f0c0e468bbd')">
<h2>����API</h2>
<h3>stubParentMethod��stubParentMethodByAClass</h3>
<p>�ø��ࣨClass/AClass��ָ��������ִ�С�</p>
<p>�����������£�</p>
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

        it(</span>"�ø���ָ��������ִ�У�����Class�Ĳ��Է����е����˸��෽�������", <span style="color: #0000ff;">function</span><span style="color: #000000;"> () {
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
        it(</span>"�ɽ�����ָ�������滻Ϊ�ٷ���", <span style="color: #0000ff;">function</span><span style="color: #000000;"> () {
            c.stubParentMethod(sandbox, </span>"done", <span style="color: #0000ff;">function</span><span style="color: #000000;"> () {
                </span><span style="color: #0000ff;">this</span>.val = 1<span style="color: #000000;">;
            });

            c.done();

            expect(c.val).toEqual(</span>1<span style="color: #000000;">);
        });
        it(</span>"�ɰ���sinon-&gt;stub API���Ը���ָ�������ĵ������", <span style="color: #0000ff;">function</span><span style="color: #000000;"> () {
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

            </span><span style="color: #008000;">//</span><span style="color: #008000;">��Ҫ����B��done�����������Ƚ�һ��������̳�B��Ȼ����Կ������done����</span>
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

        it(</span>"�ø���ָ��������ִ�У�����AClass�Ĳ��Է����е����˸��෽�������", <span style="color: #0000ff;">function</span><span style="color: #000000;"> () {
            expect(t.done).toThrow();

            t.stubParentMethodByAClass(sandbox, </span>"done"<span style="color: #000000;">);

            expect(t.done).not.toThrow();
        });
        it(</span>"�ɽ�����ָ�������滻Ϊ�ٷ���", <span style="color: #0000ff;">function</span><span style="color: #000000;"> () {
            t.stubParentMethodByAClass(sandbox, </span>"done", <span style="color: #0000ff;">function</span><span style="color: #000000;"> () {
                </span><span style="color: #0000ff;">this</span>.val = 1<span style="color: #000000;">;
            });

            t.done();

            expect(t.val).toEqual(</span>1<span style="color: #000000;">);
        });
        it(</span>"�ɰ���sinon-&gt;stub API���Ը���ָ�������ĵ������", <span style="color: #0000ff;">function</span><span style="color: #000000;"> () {
            t.stubParentMethodByAClass(sandbox, </span>"done"<span style="color: #000000;">);

            t.done();

            expect(t.lastBaseClassForTest.done.calledOnce).toBeTruthy();
        });
    });</span></pre>
</div>
<span class="cnblogs_code_collapse">View Code</span></div>
<h3>isInstanceOf</h3>
<p>�ж��Ƿ�Ϊ���ʵ����</p>
<p>�����������£�</p>
<div class="cnblogs_code" onclick="cnblogs_code_show('b1730895-ca72-43f4-80d7-919d8312d0c8')"><img id="code_img_closed_b1730895-ca72-43f4-80d7-919d8312d0c8" class="code_img_closed" src="http://images.cnblogs.com/OutliningIndicators/ContractedBlock.gif" alt="" /><img id="code_img_opened_b1730895-ca72-43f4-80d7-919d8312d0c8" class="code_img_opened" style="display: none;" onclick="cnblogs_code_hide('b1730895-ca72-43f4-80d7-919d8312d0c8',event)" src="http://images.cnblogs.com/OutliningIndicators/ExpandedBlockStart.gif" alt="" />
<div id="cnblogs_code_open_b1730895-ca72-43f4-80d7-919d8312d0c8" class="cnblogs_code_hide">
<pre>     describe("isInstanceOf", <span style="color: #0000ff;">function</span><span style="color: #000000;"> () {
        it(</span>"ֱ���ж��Ƿ�ΪClass��ʵ��", <span style="color: #0000ff;">function</span><span style="color: #000000;"> () {
            </span><span style="color: #0000ff;">var</span> A =<span style="color: #000000;"> YYC.Class({});

            expect(</span><span style="color: #0000ff;">new</span><span style="color: #000000;"> A().isInstanceOf(A)).toBeTruthy();
        });
        describe(</span>"���Լ̳г�����ʱ�����", <span style="color: #0000ff;">function</span><span style="color: #000000;"> () {
            it(</span>"����1", <span style="color: #0000ff;">function</span><span style="color: #000000;"> () {
                </span><span style="color: #0000ff;">var</span> A =<span style="color: #000000;"> YYC.AClass({});
                </span><span style="color: #0000ff;">var</span> B =<span style="color: #000000;"> YYC.Class(A, {});

                expect(</span><span style="color: #0000ff;">new</span><span style="color: #000000;"> B().isInstanceOf(B)).toBeTruthy();
                expect(</span><span style="color: #0000ff;">new</span><span style="color: #000000;"> B().isInstanceOf(A)).toBeTruthy();
            });
            it(</span>"����2", <span style="color: #0000ff;">function</span><span style="color: #000000;"> () {
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

        describe(</span>"���Լ̳нӿ�ʱ�����", <span style="color: #0000ff;">function</span><span style="color: #000000;"> () {
            it(</span>"����1", <span style="color: #0000ff;">function</span><span style="color: #000000;"> () {
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
            it(</span>"����2", <span style="color: #0000ff;">function</span><span style="color: #000000;"> () {
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

        it(</span>"�ۺϲ���", <span style="color: #0000ff;">function</span><span style="color: #000000;"> () {
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
<p>���ص�ǰ�汾�š�</p>
<p>�����������£�</p>
<div class="cnblogs_code">
<pre><span style="color: #000000;">    it("��õ�ǰ�汾��", function () {
       expect(YYC.YOOP.version).toBeString();
    });</span></pre>
</div>
</div>
<h1>Լ��</h1>
<p>�ڸÿ�ܵ�ʵ���У����ʵ�����Է�����Ĺ��г�Ա��������Ա��˽�г�Ա�����г�Ա������ӵ����ԭ���У�����Ǽ̳У��򽫸���ĳ�Ա�������ĳ�Ա����ӵ������ԭ���У������ֻ�Ǵ������������˳�Ա�ķ���Ȩ�ޣ��ڻ�����û�жԳ�Ա�ķ���Ȩ�����κ����ƣ�</p>
<p>��ˣ��û���Ҫ����<span style="color: #ff0000;">����Լ��</span>�ķ�ʽ�����ֲ�ͬ�ĳ�Ա����Ҫ�Ծ����ط���Ȩ�޹��������ʵ��ֻ�ܷ��ʹ��г�Ա�����ܷ����������˽�г�Ա��������Է��ʸ���ı�����Ա�ȵȣ���</p>
<h2>˽�г�Ա�ͱ�����Ա�Ľ�������Լ��</h2>
<p>���������Լ��</p>
<p>�����˽�г�Ա��&ldquo;_&rdquo;��ͷ��������Ա��&ldquo;P_&rdquo;��ͷ��</p>
<p>�ڼ̳��У���һ������˽�г�Ա��&ldquo;__&rdquo;��ͷ���ڶ�������˽�г�Ա��&ldquo;___&rdquo;��ͷ���Դ����ơ���������������Ϊ�ӿڶ��ǹ��г�Ա���ʿ��Ǹ�����Լ��ʱ���Խӿڡ���</p>
<p>ÿ����ı�����Աǰ׺���Զ�Ϊ&ldquo;P_&rdquo;������Ҫ���ݼ̳в㼶�Ĳ�ͬ������Ϊ&ldquo;P__&rdquo;��&ldquo;P___&rdquo;�ȡ�</p>
<p>��Ϊһ����ԣ�ÿ����ı�����Ա���ֶ�����һ����ֻ�е�������Ҫר����д����ı�����Աʱ������ı�����Ա�Ż��븸�ౣ����Աͬ����</p>
<p>�磺</p>
<p>���̳нӿڣ�</p>
<div class="cnblogs_code">
<pre><span style="color: #0000ff;">var</span> A = YYC.AClass({    <span style="color: #008000;">//</span><span style="color: #008000;">AΪ����</span>
<span style="color: #000000;">    Private: {
        _value: </span><span style="color: #800080;">0</span><span style="color: #000000;">,
        _method: function () { }
    },
    Protected: {
        P_value: </span><span style="color: #800080;">0</span><span style="color: #000000;">,
        P_method: function () { }
    }
});
</span><span style="color: #0000ff;">var</span> B = YYC.Class(A, {  <span style="color: #008000;">//</span><span style="color: #008000;">BΪ��һ������</span>
<span style="color: #000000;">    Private: {
        __value: </span><span style="color: #800080;">0</span><span style="color: #000000;">,
        __method: function () { }
    }</span><span style="color: #000000;">
});</span></pre>
</div>
<p>�̳нӿڣ�</p>
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
</span><span style="color: #0000ff;">var</span> B = YYC.Class(A, {  <span style="color: #008000;">//</span><span style="color: #008000;">BΪ��һ������</span>
<span style="color: #000000;">    Private: {
        __value: </span><span style="color: #800080;">0</span><span style="color: #000000;">,
        __method: function () { }
    },
    Public: {
        method: function () { }
    }
});</span></pre>
</div>
<h3>Ϊʲôÿ�������˽�г�Աǰ׺��ò�һ����</h3>
<p>��Ϊ��������븸����ͬ����˽�г�Աʱ����������ø����Աʱ�����ܻ�����������ε����⣺</p>
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

</span><span style="color: #008000;">//</span><span style="color: #008000;">�޷�ͨ�����ԣ�ʵ��ֵΪ200
</span><span style="color: #008000;">//</span><span style="color: #008000;">������Ϊͨ��&ldquo;this.base()&rdquo;���ø���A��getValʱ�����ص���B��д��_val��</span>
expect(<span style="color: #0000ff;">new</span> B().getVal()).toEqual(<span style="color: #800080;">100</span>);</pre>
</div>
<p>�û�Ҳ���Խ���һ�������˽�г�Աǰ׺��Ϊ&ldquo;_1_&rdquo;���ڶ��������˽�г�Ա��Ϊ&ldquo;_2_&rdquo;������������</p>
<p>ǰ׺���ù����û����Զ���<span style="color: #ff0000;"><span style="color: #000000;">ֻҪ��</span>�ڼ̳���ʹ��ͬ�㼶�����˽�в�ͬ������</span>��</p>
<h2>baseClass</h2>
<p>Ϊ�˷�ֹ�����prototype.baseClass���Ǹ���prototype.baseClass��������̳и���ʱ���û���Ҫ���жϸ���prototype.baseClass�Ƿ���ڡ�������ڣ������ǰ׺&ldquo;_&rdquo;����&ldquo;_baseClass&rdquo;���������ǰ׺����Ȼ���ڣ����ټ���ǰ׺&ldquo;_&rdquo;����&ldquo;__baseClass&rdquo;���Դ����ơ�</p>
<p>�磺</p>
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
                            </span><span style="color: #0000ff;">this</span>.baseClass.a.call(<span style="color: #0000ff;">this</span>, <span style="color: #0000ff;">null</span>);  <span style="color: #008000;">//</span><span style="color: #008000;">����A1.a</span>
<span style="color: #000000;">                        }
                    }
                });
                </span><span style="color: #0000ff;">var</span> B =<span style="color: #000000;"> YYC.Class(A2, {
                    Public: {
                        a: function () {
                            </span><span style="color: #0000ff;">this</span>.arr.push(<span style="color: #800080;">3</span><span style="color: #000000;">);
                            </span><span style="color: #0000ff;">this</span>._baseClass.a.call(<span style="color: #0000ff;">this</span>, <span style="color: #0000ff;">null</span>); <span style="color: #008000;">//</span><span style="color: #008000;">����A2.a</span>
                            <span style="color: #0000ff;">this</span>.baseClass.a.call(<span style="color: #0000ff;">this</span>, <span style="color: #0000ff;">null</span>);  <span style="color: #008000;">//</span><span style="color: #008000;">����A1.a</span>

                            <span style="color: #0000ff;">return</span> <span style="color: #0000ff;">this</span><span style="color: #000000;">.arr;
                        }
                    }
                });
                </span><span style="color: #0000ff;">var</span> b = <span style="color: #0000ff;">new</span><span style="color: #000000;"> B();

                expect(b.a()).toEqual([</span><span style="color: #800080;">3</span>, <span style="color: #800080;">2</span>, <span style="color: #800080;">1</span>, <span style="color: #800080;">1</span>]);</pre>
</div>
<span class="cnblogs_code_collapse">View Code</span></div>
<h1>ע������</h1>
<p><strong><span style="font-size: 18px;">����ʹ��this.baseClass���ø����Աʱ��Ҫ�������Ա��thisָ�����ࡣ</span></strong></p>
<p>�����д����</p>
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
console.log(b.p);   </span><span style="color: #008000;">//</span><span style="color: #008000;">�˴�Ϊundefined��������100��</span></pre>
</div>
<p>��ȷ��д����</p>
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
<h1>�ѽ��������</h1>
<p>1��ͬһ�����ʵ��֮�䲻Ӧ�ù������ԡ�</p>
<p><strong>��������</strong></p>
<p>�ο�����Ĵ��룺</p>
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
            expect(m.a).toEqual([]);    </span><span style="color: #008000;">//</span><span style="color: #008000;">ʧ�ܣ�ʵ��Ϊ["a"]��</span></pre>
</div>
<p><strong><span style="font-size: 1em; line-height: 1.5;">ԭ�����</span></strong></p>
<p>��ΪYOOP����ĳ�Ա�����뵽���ԭ