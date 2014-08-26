<p>��Һã���������ʽ�����ҵ�OOP���<strong>YOOP</strong>���ÿ�ܽ����������߸��õؽ�����������̡�</p>
<p>��ǰ�汾�ţ�v1.1</p>
<h1>����</h1>
<p>�ÿ�ܰ����ӿڡ������ࡢ�ࡣ</p>
<p>�ӿ�Interface���Լ̳ж���ӿڣ����Զ��巽�������ԡ�</p>
<p>������AClass���Լ̳ж���ӿڡ�һ�������࣬���Զ��幹�캯�������г�Ա��˽�г�Ա��������Ա����̬��Ա���鷽���������Ա��</p>
<p>��Class���Լ̳ж���ӿڡ�һ����������࣬���Զ��幹�캯�������г�Ա��˽�г�Ա��������Ա����̬��Ա���鷽����&nbsp;</p>
<h2>������ø����Ա</h2>
<p>�������У�����ʹ��this.base()�����ø���ͬ��������Ҳ����ʹ��this.baseClass�����ʸ����ԭ�͡�</p>
<h2>��Ҫ���﷨����</h2>
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
<h1>ʹ��YOOP</h1>
<p>YOOP֧��AMD��CMD��CommonJS�淶������Sea.js��node.js��ʹ�ã�</p>
```js
var yoop = require("./YOOP.js");

yoop.Class({});
```
<p>Ҳ����<span style="font-size: 14px; line-height: 1.5;">ͨ��script��ǩ��ҳ����ֱ������</span></p>
<p><span style="font-size: 14px; line-height: 1.5;">ҳ��������script��</span></p>
```html
<script src="./YOOP.js"></script>
```
<p>Ȼ��ͨ�������ռ�YYC��ʹ�ã�</p>
```js
YYC.Class({});
```
<h1>�÷�</h1>
<h2>�ӿ�</h2>
<h3>����ӿ�</h3>
<p>ֻ�з�����</p>
```js
var A = YYC.Interface("method1", "method2");
```
<p>ֻ�����ԣ�</p>
```js
var A = YYC.Interface([], ["attribute1", "attribute2"]);
```
<p>���з����������ԣ�</p>
```js
var A = YYC.Interface(["method1", "method2"], ["attribute1", "attribute2"]);
```
<h3>�̳нӿ�</h3>
```js
var A = YYC.Interface(["method1", "method2"],["attribute1", "attribute2"]);
var B = YYC.Interface(A, "m1", "m2");
var C = YYC.Interface([A], ["m1", "m2"], ["a1", "a2"]);
var D = YYC.Interface([A, B], ["m1", "m2"], ["a1", "a2"]);
```
<h2>������</h2>
<h3>���������</h3>
```js
var A = YYC.AClass({
    Init: function () { //���캯��
    },
    Protected: {    //������Ա
        Abstract: { //���������Ա
        },
        Virtual: {  //�����鷽��
        },
        P_proA: true,   //��������
       P_proM: function () { }    //��������
    },
    Public: {   //���г�Ա
        Abstract: { //���г����Ա
        },
        Virtual: {  //�����鷽��
        },
        pubM: function () { },  //���з���
      pubA: 0    //��������
    },
    Private: {  //˽�г�Ա
        _priA: "",   //˽������
        _priM: function () { } //˽�з���
    },
    Abstract: { //���г����Ա
    },
    Virtual: {  //�����鷽��
    }
});
```

<h3>�̳г�����</h3>
```js
var A = YYC.AClass({});
var B = YYC.AClass(A, {});
var C = YYC.AClass({Class: A}, {}); 
```

<h3>�̳нӿ�</h3>
```js
var A = YYC.Interface("m1");
var B = YYC.Interface("m2");
var C = YYC.AClass({ Interface: A }, {
    Public: {
        m1: function () { }
    }
});
var D = YYC.AClass({ Interface: [A, B] }, {
    Public: {
        m1: function () { },
        m2: function () { }
    }
});
```
<h3>�̳нӿںͳ�����</h3>
```js
var A = YYC.Interface("m1");
var B = YYC.Interface(["m2"], ["a"]);
var C = YYC.AClass({});
var D = YYC.AClass({ Interface: [A, B], Class: C }, {
    Public: {
        m1: function () { },
        a: 0
    }
});
```
<h2>��</h2>
<h3>������</h3>
```js
var A = YYC.Class({
    Init: function () { //���캯��
    },
    Protected: {    //������Ա
        Virtual: {  //�����鷽��
        },
        P_proA: true,   //��������
        P_proM: function () { }    //��������
    },
    Public: {   //���г�Ա
        Virtual: {  //�����鷽��
        },
        pubM: function () { },  //���з���
        pubA: 0    //��������
    },
    Private: {  //˽�г�Ա
        _priA: "",   //˽������
        _priM: function () { } //˽�з���
    },
    Virtual: {  //�����鷽��
    }
});
```
<h3>�̳г�����</h3>
```js
var A = YYC.AClass({});
var B = YYC.AClass(A, {});
var C = YYC.AClass({ Class: A }, {});
```
<h3>�̳���</h3>
```js
var A = YYC.Class({});
var B = YYC.Class(A, {});
var C = YYC.Class({ Class: A }, {});
```
<h3>�̳нӿ�</h3>
```js
var A = YYC.Interface("m1");
var B = YYC.Interface("m2");
var C = YYC.Class({ Interface: A }, {
    Public: {
        m1: function () { }
    }
});
var D = YYC.Class({ Interface: [A, B] }, {
    Public: {
        m1: function () { },
        m2: function () { }
    }
});
```

<h3>�̳нӿںͳ�����/��</h3>
```js
var A = YYC.Interface("m1");
var B = YYC.Interface(["m2"], ["a"]);
var C = YYC.AClass({});
var D = YYC.Class({});
var E = YYC.AClass({ Interface: [A, B], Class: C }, {
    Public: {
        m1: function () { },
        a: 0
    }
});
var F = YYC.AClass({ Interface: [A, B], Class: D }, {
    Public: {
        m1: function () { },
        a: 0
    }
});
```
<h2>���캯��</h2>
```js
var A = YYC.Class({
����Init: function(t){
��������this.value = t;
����}
});
var a = new A(100);
console.log(a.value);����//100
```

<h2>��̬��Ա</h2>
```js
var A = YYC.Class({
    Static: {
        a: 100,
        method1: function () {
            return 200;
        },
        method2: function () {
             this.k = 300;
        }
    }
});

A.method2();

console.log(A.a);   //100
console.log(A.method1());    //200
console.log(A.k);   //300
```
<h2>��ĳ�Ա�������</h2>
<p>ʹ��this�����á�</p>
```js
var A = YYC.Class({
    Private: {
        _a: 100
    },
    Public: {
        method: function (t) {
            return this._a;
        }
    }
});
var a = new A();
console.log(a.method);  //100
```

<h2>������ø���</h2>
<p>ʹ��this.base()�ɵ��ø���ͬ��������</p>
<p>ʹ��this.baseClass.xx.call(this, xx)�ɵ��ø���ĳ�Ա��</p>
<div class="cnblogs_code" onclick="cnblogs_code_show('1f442ed7-4339-49f7-abb1-7f1f1563cca6')">
```js
var A = YYC.AClass({
    Init: function () {
        this.p = 100;
    },
    Public: {
        method1: function () {
            this.m = 300;
        },
        method2: function () {
            return 100;
        }
    }
});
var B = YYC.Class(A, {
    Init: function () {
        this.base();
    },
    Private: {
        _a: 100
    },
    Public: {
        method1: function (t) {
            this.base();
            return this.baseClass.method2.call(this, null) + this._a;
        }
    }
});
var b = new B();
console.log(b.method1());  //200
console.log(b.p);  //100
console.log(b.m);  //300
```

<h2>�����������</h2>
```js
var A = YYC.AClass({
    Public: {
        method: function () {
            console.log(this.value);
        }
    }
});
var B = YYC.Class(A, {
    Public: {
        value: 100
    }
});
var b = new B();
b.method(); //100
```

<h2>��д���෽����ʵ�ֽӿڳ�Ա�������Ա</h2>
```js
var A = YYC.Interface("m1");
var B = YYC.AClass({ Interface: A }, {
    Protected: {
        Abstract: {
            P_method: function () { }
        }
    },
    Public: {
        method: function () { }
    }
});
var C = YYC.Class(B, {
    Protected: {
        P_method: function () {
            console.log("ʵ�ֳ��󷽷�");
        }
    },
    Public: {
        method: function () {
            console.log("���Ǹ���ͬ������");
        },
        m1: function () {
            console.log("ʵ�ֽӿ�");
        }
    }
});
```
<h2>����API</h2>
<h3>stubParentMethod��stubParentMethodByAClass</h3>
<p>�ø��ࣨClass/AClass��ָ��������ִ�С�</p>
<p>�����������£�</p>
```js
describe("stubParentMethod", function () {
    var sandbox = null;
    var A = null,
        B = null,
        C = null,
        a = null,
        b = null,
        c = null;

    beforeEach(function () {
        A = YYC.Class({
            Public: {
                done: function () {
                    throw new Error("");
                }
            }
        });
        B = YYC.Class(A, {
            Public: {
                done: function () {
                    this.baseClass.done.call(this, null);
                }
            }
        });
        C = YYC.Class(B, {
            Public: {
                a: 0,

                done: function () {
                    this.base();

                    this.a = 100;
                }
            }
        });
        a = new A();
        b = new B();
        c = new C();

        sandbox = sinon.sandbox.create();
    });
    afterEach(function () {
        sandbox.restore();
    });

    it("�ø���ָ��������ִ�У�����Class�Ĳ��Է����е����˸��෽�������", function () {
        expect(function () {
            b.done();
        }).toThrow();
        expect(function () {
            c.done();
        }).toThrow();

        b.stubParentMethod(sandbox, "done");
        c.stubParentMethod(sandbox, "done");

        expect(function () {
            b.done();
        }).not.toThrow();
        expect(function () {
            c.done();
        }).not.toThrow();
    });
    it("�ɽ�����ָ�������滻Ϊ�ٷ���", function () {
        c.stubParentMethod(sandbox, "done", function () {
            this.val = 1;
        });

        c.done();

        expect(c.val).toEqual(1);
    });
    it("�ɰ���sinon->stub API���Ը���ָ�������ĵ������", function () {
        c.stubParentMethod(sandbox, "done");

        c.done();

        expect(c.lastBaseClassForTest.done.calledOnce).toBeTruthy();
    });
});

describe("stubParentMethodByAClass", function () {
    var sandbox = null;
    var A = null,
        B = null,
        t = null;

    beforeEach(function () {
        A = YYC.AClass({
            Public: {
                a: 0,
                done: function () {
                    throw new Error("");
                }
            }
        });
        B = YYC.AClass(A, {
            Public: {
                done: function () {
                    this.base();
                }
            }
        });

        //��Ҫ����B��done�����������Ƚ�һ��������̳�B��Ȼ����Կ������done����
        function getInstance() {
            var T = YYC.Class(B, {
            });

            return new T();
        }

        t = getInstance();

        sandbox = sinon.sandbox.create();
    });
    afterEach(function () {
        sandbox.restore();
    });

    it("�ø���ָ��������ִ�У�����AClass�Ĳ��Է����е����˸��෽�������", function () {
        expect(t.done).toThrow();

        t.stubParentMethodByAClass(sandbox, "done");

        expect(t.done).not.toThrow();
    });
    it("�ɽ�����ָ�������滻Ϊ�ٷ���", function () {
        t.stubParentMethodByAClass(sandbox, "done", function () {
            this.val = 1;
        });

        t.done();

        expect(t.val).toEqual(1);
    });
    it("�ɰ���sinon->stub API���Ը���ָ�������ĵ������", function () {
        t.stubParentMethodByAClass(sandbox, "done");

        t.done();

        expect(t.lastBaseClassForTest.done.calledOnce).toBeTruthy();
    });
});
```
<h3>isInstanceOf</h3>
<p>�ж��Ƿ�Ϊ���ʵ����</p>
<p>�����������£�</p>
```js
describe("isInstanceOf", function () {
    it("ֱ���ж��Ƿ�ΪClass��ʵ��", function () {
        var A = YYC.Class({});

        expect(new A().isInstanceOf(A)).toBeTruthy();
    });
    describe("���Լ̳г�����ʱ�����", function () {
        it("����1", function () {
            var A = YYC.AClass({});
            var B = YYC.Class(A, {});

            expect(new B().isInstanceOf(B)).toBeTruthy();
            expect(new B().isInstanceOf(A)).toBeTruthy();
        });
        it("����2", function () {
            var A = YYC.AClass({});
            var B = YYC.AClass(A, {});
            var C = YYC.Class(B, {});
            var D = YYC.Class(A, {});

            expect(new C().isInstanceOf(B)).toBeTruthy();
            expect(new C().isInstanceOf(A)).toBeTruthy();
            expect(new D().isInstanceOf(A)).toBeTruthy();
            expect(new D().isInstanceOf(B)).toBeFalsy();
        });
    });

    describe("���Լ̳нӿ�ʱ�����", function () {
        it("����1", function () {
            var A = YYC.Interface("a");
            var B = YYC.Class({Interface: A}, {
                Public: {
                    a: function () {
                    }
                }
            });

            expect(new B().isInstanceOf(B)).toBeTruthy();
            expect(new B().isInstanceOf(A)).toBeTruthy();
        });
        it("����2", function () {
            var A = YYC.Interface("a");
            var B = YYC.Interface("b");
            var C = YYC.Interface([A, B], "c");
            var D = YYC.Class({Interface: C}, {
                Public: {
                    a: function () {
                    },
                    b: function () {
                    },
                    c: function () {
                    }
                }
            });

            expect(new D().isInstanceOf(C)).toBeTruthy();
            expect(new D().isInstanceOf(B)).toBeTruthy();
            expect(new D().isInstanceOf(A)).toBeTruthy();
        });
    });

    it("�ۺϲ���", function () {
        var A = YYC.Interface("a1");
        var B = YYC.Interface(A, "a2");
        var C = YYC.AClass({Interface: B}, {
            Public: {
                a1: function () {
                },
                a2: function () {
                }
            }
        });
        var D = YYC.AClass(C, {
            Public: {
                a1: function () {
                },
                a2: function () {
                }
            }
        });
        var E = YYC.Class(C, {
        });
        var F = YYC.Class(E, {
        });
        var G = YYC.Class({Interface: B, Class: D}, {
        });

        expect(new E().isInstanceOf(C)).toBeTruthy();
        expect(new E().isInstanceOf(B)).toBeTruthy();
        expect(new E().isInstanceOf(A)).toBeTruthy();

        expect(new F().isInstanceOf(E)).toBeTruthy();
        expect(new F().isInstanceOf(C)).toBeTruthy();
        expect(new F().isInstanceOf(B)).toBeTruthy();
        expect(new F().isInstanceOf(A)).toBeTruthy();

        expect(new G().isInstanceOf(B)).toBeTruthy();
        expect(new G().isInstanceOf(D)).toBeTruthy();

        expect(new G().isInstanceOf(E)).toBeFalsy();
    });
}); 
```
<h3>YOOP.version</h3>
<p>���ص�ǰ�汾�š�</p>
<p>�����������£�</p>
```js
it("��õ�ǰ�汾��", function () {
    expect(YYC.YOOP.version).toBeString();
});
```
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
<```js
var A = YYC.AClass({    //AΪ����
    Private: {
        _value: 0,
        _method: function () { }
    },
    Protected: {
        P_value: 0,
        P_method: function () { }
    }
});
var B = YYC.Class(A, {  //BΪ��һ������
    Private: {
        __value: 0,
        __method: function () { }
    }
});
```
<p>�̳нӿڣ�</p>
```js
var I = YYC.Interface("method");
var A = YYC.AClass({ Interface: I }, {
    Private: {
        _value: 0,
        _method: function () { }
    },
    Protected: {
        P_method: function () { }
    }
});
var B = YYC.Class(A, {  //BΪ��һ������
    Private: {
        __value: 0,
        __method: function () { }
    },
    Public: {
        method: function () { }
    }
});
```
<h3>Ϊʲôÿ�������˽�г�Աǰ׺��ò�һ����</h3>
<p>��Ϊ��������븸����ͬ����˽�г�Աʱ����������ø����Աʱ�����ܻ�����������ε����⣺</p>
```js
var A = YYC.Class({
    Private: {
        _val: 100
    },
    Public: {
        getVal: function () {
            return this._val;
        }
    }
});

var B = YYC.Class(A, {
    Private: {
        _val: 200
    },
    Public: {
        getVal: function () {
            return this.base();
        }
    }
});

//�޷�ͨ�����ԣ�ʵ��ֵΪ200
//������Ϊͨ����this.base()�����ø���A��getValʱ�����ص���B��д��_val��
expect(new B().getVal()).toEqual(100);
```
<p>�û�Ҳ���Խ���һ�������˽�г�Աǰ׺��Ϊ&ldquo;_1_&rdquo;���ڶ��������˽�г�Ա��Ϊ&ldquo;_2_&rdquo;������������</p>
<p>ǰ׺���ù����û����Զ���<span style="color: #ff0000;"><span style="color: #000000;">ֻҪ��</span>�ڼ̳���ʹ��ͬ�㼶�����˽�в�ͬ������</span>��</p>
<h2>baseClass</h2>
<p>Ϊ�˷�ֹ�����prototype.baseClass���Ǹ���prototype.baseClass��������̳и���ʱ���û���Ҫ���жϸ���prototype.baseClass�Ƿ���ڡ�������ڣ������ǰ׺&ldquo;_&rdquo;����&ldquo;_baseClass&rdquo;���������ǰ׺����Ȼ���ڣ����ټ���ǰ׺&ldquo;_&rdquo;����&ldquo;__baseClass&rdquo;���Դ����ơ�</p>
<p>�磺</p>
```js
var A1 = YYC.AClass({
    Public: {
        arr: [],
        a: function () {
            this.arr.push(1);
        }
    }
});
var A2 = YYC.AClass(A1, {
    Public: {
        a: function () {
            this.arr.push(2);
            this.baseClass.a.call(this, null);  //����A1.a
        }
    }
});
var B = YYC.Class(A2, {
    Public: {
        a: function () {
            this.arr.push(3);
            this._baseClass.a.call(this, null); //����A2.a
            this.baseClass.a.call(this, null);  //����A1.a

            return this.arr;
        }
    }
});
var b = new B();

expect(b.a()).toEqual([3, 2, 1, 1]);
```
<h1>ע������</h1>
<p><strong><span style="font-size: 18px;">����ʹ��this.baseClass���ø����Աʱ��Ҫ�������Ա��thisָ�����ࡣ</span></strong></p>
<p>�����д����</p>
```js
var A = YYC.AClass({
    Public: {
        method: function () {
            this.p = 100;
        }
    }
});
var B = YYC.Class(A, {
    Public: {
        method: function () {
            this.baseClass.method();
        }
    }
});
var b = new B();
b.method();
console.log(b.p);   //�˴�Ϊundefined��������100��
```
<p>��ȷ��д����</p>
```js
var A = YYC.AClass({
    Public: {
        method: function () {
            this.p = 100;
        }
    }
});
var B = YYC.Class(A, {
    Public: {
        method: function () {
            this.baseClass.method.call(this, null);
        }
    }
});
var b = new B();
b.method();
console.log(b.p);   //100
```
<h1>�ѽ��������</h1>
<p>1��ͬһ�����ʵ��֮�䲻Ӧ�ù������ԡ�</p>
<p><strong>��������</strong></p>
<p>�ο�����Ĵ��룺</p>
```js
var A = YYC.Class({
    Init: function () {
    },
    Public: {
        a:[]
    }
});

var t = new A();
t.a.push("a");
var m = new A();

expect(t.a).toEqual(["a"]);
expect(m.a).toEqual([]);    //ʧ�ܣ�ʵ��Ϊ["a"]��
```
<p><strong><span style="font-size: 1em; line-height: 1.5;">ԭ�����</span></strong></p>
<p>��ΪYOOP����ĳ�Ա�����뵽���ԭ�Ͷ����У�����ʵ���ĳ�Ա�������������ԭ�Ͷ�������ͬһ�����ʵ��֮���Ա����</p>
<p><strong>�������</strong></p>
<p>��Class�Ĺ��캯�������ԭ�͵����Ե�ʵ���У��Ӷ�ͬһ�����ʵ��֮�乲��ͬһԭ�Ͷ���ķ����������ǵ������໥������</p>
<p>2���̳���ͬһ���������ʵ��֮�䲻Ӧ�ù������ԡ�</p>
<p><strong>��������</strong></p>
<p>�ο�����Ĵ���</p>
```js
var Parent = YYC.AClass({
    Init: function () {
        console.log("Parent Init!");
    },
    Public: {
        a: []
    }
});
var Sub1 = YYC.Class(Parent, {
    Init: function () {
    },
    Public: {
    }
});
var Sub2 = YYC.Class(Parent, {
    Init: function () {
    }
});

var t = new Sub1();
t.a.push("a");
var k = new Sub2();

expect(t.a).toEqual(["a"]);
expect(k.a).toEqual([]);    //ʧ�ܣ�ʵ��Ϊ["a"]��
```
<p><strong><span style="font-size: 1em; line-height: 1.5;">ԭ�����</span></strong></p>
<p>Ŀǰ��ͨ��ԭ�ͼ̳еķ�ʽ��ʵ�ּ̳еġ���������֮��ĳ�Ա�������Ը����ԭ�Ͷ��󣬴Ӷ������ͬһ���������ʵ��֮���Ա����</p>
<p><strong>�������</strong></p>
<p>�޸���̳з�ʽ����Ϊͨ��&ldquo;�������ԭ�����г�Ա��������&rdquo;�ķ�ʽʵ�ּ̳У��Ӷ�ͬһ���������ʵ��֮��ĳ�Ա�໥������</p>
<h1>ȱ��</h1>
<p><strong><span style="font-size: 18px;">ֻ�Ǵ�������Լ���˷���Ȩ�ޣ���û�дӻ��������Ʒ���Ȩ�ޡ�</span></strong></p>
<p>����Ը�������Լ��������Ĺ��г�Ա��������Ա��˽�г�Ա���������ʵ��ȴ���Է���������г�Ա��</p>
<h1>����</h1>
<p><a href="https://github.com/yyc-git/YOOP" target="_blank">GitHub��ַ</a></p>
<h1>�汾��ʷ</h1>
<p><strong>2013-06-07 ����YOOP v1.0&nbsp;</strong></p>
<p><strong>2014-08-26 ����YOOP v1.1&nbsp;</strong></p>
<p>1����ʵ������isInstanceOf�����������ж��Ƿ�Ϊ���ʵ���������ڽӿڼ̳С���̳е����</p>
<p>2��protected����Ҳ����ʹ��this.base�����ʸ���ͬ��������</p>
<p>3�������&ldquo;��һ�������е������������������ǵ�this.base�ụ�����&rdquo;������</p>
<p>4������stubParentMethod��stubParentMethodByAClass�������÷����ø��ࣨClass/AClass��ָ��������ִ�У�����Class�Ĳ��Է����е����˸��෽����������������this.base()��this.baseClass.xxx��</p>
<p><span style="font-size: 14px; line-height: 1.5;">5������֧��AMD��CMD��CommonJS�淶��</span></p>
<p>6������YYC.YOOP.version���ԣ����ڻ�õ�ǰ�汾��&nbsp;</p>
<p>7��Class�Ĺ��캯��F������ֻ����ԭ�͵����Ե�ʵ���У��Ӷ�ͬһ�����ʵ��֮�乲��ͬһԭ�Ͷ���ķ����������ǵ������໥����</p>