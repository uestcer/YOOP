<p>大家好！今天我正式发布我的OOP框架<strong>YOOP</strong>！该框架将帮助开发者更好地进行面向对象编程。</p>
<p>当前版本号：v1.1</p>
<h1>介绍</h1>
<p>该框架包含接口、抽象类、类。</p>
<p>接口Interface可以继承多个接口，可以定义方法、属性。</p>
<p>抽象类AClass可以继承多个接口、一个抽象类，可以定义构造函数、公有成员、私有成员、保护成员、静态成员、虚方法、抽象成员。</p>
<p>类Class可以继承多个接口、一个抽象类或类，可以定义构造函数、公有成员、私有成员、保护成员、静态成员、虚方法。&nbsp;</p>
<h2>子类调用父类成员</h2>
<p>在子类中，可以使用this.base()来调用父类同名方法。也可以使用this.baseClass来访问父类的原型。</p>
<h2>主要的语法规则</h2>
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
<h1>使用YOOP</h1>
<p>YOOP支持AMD、CMD、CommonJS规范，可在Sea.js、node.js中使用：</p>
```js
var yoop = require("./YOOP.js");

yoop.Class({});
```
<p>也可以<span style="font-size: 14px; line-height: 1.5;">通过script标签在页面上直接引用</span></p>
<p><span style="font-size: 14px; line-height: 1.5;">页面上引用script：</span></p>
```html
<script src="./YOOP.js"></script>
```
<p>然后通过命名空间YYC来使用：</p>
```js
YYC.Class({});
```
<h1>用法</h1>
<h2>接口</h2>
<h3>定义接口</h3>
<p>只有方法：</p>
```js
var A = YYC.Interface("method1", "method2");
```
<p>只有属性：</p>
```js
var A = YYC.Interface([], ["attribute1", "attribute2"]);
```
<p>既有方法又有属性：</p>
```js
var A = YYC.Interface(["method1", "method2"], ["attribute1", "attribute2"]);
```
<h3>继承接口</h3>
```js
var A = YYC.Interface(["method1", "method2"],["attribute1", "attribute2"]);
var B = YYC.Interface(A, "m1", "m2");
var C = YYC.Interface([A], ["m1", "m2"], ["a1", "a2"]);
var D = YYC.Interface([A, B], ["m1", "m2"], ["a1", "a2"]);
```
<h2>抽象类</h2>
<h3>定义抽象类</h3>
```js
var A = YYC.AClass({
    Init: function () { //构造函数
    },
    Protected: {    //保护成员
        Abstract: { //保护抽象成员
        },
        Virtual: {  //保护虚方法
        },
        P_proA: true,   //保护属性
       P_proM: function () { }    //保护方法
    },
    Public: {   //公有成员
        Abstract: { //公有抽象成员
        },
        Virtual: {  //公有虚方法
        },
        pubM: function () { },  //公有方法
      pubA: 0    //公有属性
    },
    Private: {  //私有成员
        _priA: "",   //私有属性
        _priM: function () { } //私有方法
    },
    Abstract: { //公有抽象成员
    },
    Virtual: {  //公有虚方法
    }
});
```

<h3>继承抽象类</h3>
```js
var A = YYC.AClass({});
var B = YYC.AClass(A, {});
var C = YYC.AClass({Class: A}, {}); 
```

<h3>继承接口</h3>
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
<h3>继承接口和抽象类</h3>
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
<h2>类</h2>
<h3>定义类</h3>
```js
var A = YYC.Class({
    Init: function () { //构造函数
    },
    Protected: {    //保护成员
        Virtual: {  //保护虚方法
        },
        P_proA: true,   //保护属性
        P_proM: function () { }    //保护方法
    },
    Public: {   //公有成员
        Virtual: {  //公有虚方法
        },
        pubM: function () { },  //公有方法
        pubA: 0    //公有属性
    },
    Private: {  //私有成员
        _priA: "",   //私有属性
        _priM: function () { } //私有方法
    },
    Virtual: {  //公有虚方法
    }
});
```
<h3>继承抽象类</h3>
```js
var A = YYC.AClass({});
var B = YYC.AClass(A, {});
var C = YYC.AClass({ Class: A }, {});
```
<h3>继承类</h3>
```js
var A = YYC.Class({});
var B = YYC.Class(A, {});
var C = YYC.Class({ Class: A }, {});
```
<h3>继承接口</h3>
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

<h3>继承接口和抽象类/类</h3>
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
<h2>构造函数</h2>
```js
var A = YYC.Class({
　　Init: function(t){
　　　　this.value = t;
　　}
});
var a = new A(100);
console.log(a.value);　　//100
```

<h2>静态成员</h2>
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
<h2>类的成员互相调用</h2>
<p>使用this来调用。</p>
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

<h2>子类调用父类</h2>
<p>使用this.base()可调用父类同名函数。</p>
<p>使用this.baseClass.xx.call(this, xx)可调用父类的成员。</p>
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

<h2>父类调用子类</h2>
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

<h2>覆写父类方法，实现接口成员、抽象成员</h2>
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
            console.log("实现抽象方法");
        }
    },
    Public: {
        method: function () {
            console.log("覆盖父类同名方法");
        },
        m1: function () {
            console.log("实现接口");
        }
    }
});
```
<h2>其它API</h2>
<h3>stubParentMethod、stubParentMethodByAClass</h3>
<p>让父类（Class/AClass）指定方法不执行。</p>
<p>测试用例如下：</p>
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

    it("让父类指定方法不执行，用于Class的测试方法中调用了父类方法的情况", function () {
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
    it("可将父类指定方法替换为假方法", function () {
        c.stubParentMethod(sandbox, "done", function () {
            this.val = 1;
        });

        c.done();

        expect(c.val).toEqual(1);
    });
    it("可按照sinon->stub API测试父类指定方法的调用情况", function () {
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

        //想要测试B的done方法，必须先建一个空子类继承B，然后测试空子类的done方法
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

    it("让父类指定方法不执行，用于AClass的测试方法中调用了父类方法的情况", function () {
        expect(t.done).toThrow();

        t.stubParentMethodByAClass(sandbox, "done");

        expect(t.done).not.toThrow();
    });
    it("可将父类指定方法替换为假方法", function () {
        t.stubParentMethodByAClass(sandbox, "done", function () {
            this.val = 1;
        });

        t.done();

        expect(t.val).toEqual(1);
    });
    it("可按照sinon->stub API测试父类指定方法的调用情况", function () {
        t.stubParentMethodByAClass(sandbox, "done");

        t.done();

        expect(t.lastBaseClassForTest.done.calledOnce).toBeTruthy();
    });
});
```
<h3>isInstanceOf</h3>
<p>判断是否为类的实例。</p>
<p>测试用例如下：</p>
```js
describe("isInstanceOf", function () {
    it("直接判断是否为Class的实例", function () {
        var A = YYC.Class({});

        expect(new A().isInstanceOf(A)).toBeTruthy();
    });
    describe("测试继承抽象类时的情况", function () {
        it("测试1", function () {
            var A = YYC.AClass({});
            var B = YYC.Class(A, {});

            expect(new B().isInstanceOf(B)).toBeTruthy();
            expect(new B().isInstanceOf(A)).toBeTruthy();
        });
        it("测试2", function () {
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

    describe("测试继承接口时的情况", function () {
        it("测试1", function () {
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
        it("测试2", function () {
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

    it("综合测试", function () {
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
<p>返回当前版本号。</p>
<p>测试用例如下：</p>
```js
it("获得当前版本号", function () {
    expect(YYC.YOOP.version).toBeString();
});
```
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
<```js
var A = YYC.AClass({    //A为基类
    Private: {
        _value: 0,
        _method: function () { }
    },
    Protected: {
        P_value: 0,
        P_method: function () { }
    }
});
var B = YYC.Class(A, {  //B为第一层子类
    Private: {
        __value: 0,
        __method: function () { }
    }
});
```
<p>继承接口：</p>
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
var B = YYC.Class(A, {  //B为第一层子类
    Private: {
        __value: 0,
        __method: function () { }
    },
    Public: {
        method: function () { }
    }
});
```
<h3>为什么每层子类的私有成员前缀最好不一样？</h3>
<p>因为如果子类与父类有同名的私有成员时，当子类调用父类成员时，可能会出现以下情形的问题：</p>
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

//无法通过测试！实际值为200
//这是因为通过“this.base()”调用父类A的getVal时，返回的是B覆写的_val！
expect(new B().getVal()).toEqual(100);
```
<p>用户也可以将第一层子类的私有成员前缀设为&ldquo;_1_&rdquo;，第二层子类的私有成员设为&ldquo;_2_&rdquo;。。。。。。</p>
<p>前缀设置规则用户可自订，<span style="color: #ff0000;"><span style="color: #000000;">只要能</span>在继承中使不同层级的类的私有不同名即可</span>。</p>
<h2>baseClass</h2>
<p>为了防止子类的prototype.baseClass覆盖父类prototype.baseClass，在子类继承父类时，用户需要先判断父类prototype.baseClass是否存在。如果存在，则加上前缀&ldquo;_&rdquo;，如&ldquo;_baseClass&rdquo;。如果加上前缀后依然存在，则再加上前缀&ldquo;_&rdquo;，如&ldquo;__baseClass&rdquo;。以此类推。</p>
<p>如：</p>
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
            this.baseClass.a.call(this, null);  //调用A1.a
        }
    }
});
var B = YYC.Class(A2, {
    Public: {
        a: function () {
            this.arr.push(3);
            this._baseClass.a.call(this, null); //调用A2.a
            this.baseClass.a.call(this, null);  //调用A1.a

            return this.arr;
        }
    }
});
var b = new B();

expect(b.a()).toEqual([3, 2, 1, 1]);
```
<h1>注意事项</h1>
<p><strong><span style="font-size: 18px;">子类使用this.baseClass调用父类成员时，要将父类成员的this指向子类。</span></strong></p>
<p>错误的写法：</p>
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
console.log(b.p);   //此处为undefined，而不是100！
```
<p>正确的写法：</p>
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
<h1>已解决的问题</h1>
<p>1、同一个类的实例之间不应该共享属性。</p>
<p><strong>问题描述</strong></p>
<p>参考下面的代码：</p>
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
expect(m.a).toEqual([]);    //失败！实际为["a"]！
```
<p><strong><span style="font-size: 1em; line-height: 1.5;">原因分析</span></strong></p>
<p>因为YOOP将类的成员都加入到类的原型对象中，而类实例的成员都是链接自类的原型对象，所以同一个类的实例之间成员共享。</p>
<p><strong>解决方案</strong></p>
<p>在Class的构造函数中深拷贝原型的属性到实例中，从而同一个类的实例之间共享同一原型对象的方法，但它们的属性相互独立。</p>
<p>2、继承于同一父类的子类实例之间不应该共享属性。</p>
<p><strong>问题描述</strong></p>
<p>参考下面的代码</p>
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
expect(k.a).toEqual([]);    //失败！实际为["a"]！
```
<p><strong><span style="font-size: 1em; line-height: 1.5;">原因分析</span></strong></p>
<p>目前是通过原型继承的方式来实现继承的。这样子类之间的成员都链接自父类的原型对象，从而会造成同一父类的子类实例之间成员共享。</p>
<p><strong>解决方案</strong></p>
<p>修改类继承方式，改为通过&ldquo;深拷贝父类原型所有成员到子类中&rdquo;的方式实现继承，从而同一父类的子类实例之间的成员相互独立。</p>
<h1>缺点</h1>
<p><strong><span style="font-size: 18px;">只是从语义上约定了访问权限，而没有从机制上限制访问权限。</span></strong></p>
<p>如可以根据命名约定区分类的公有成员、保护成员、私有成员，但是类的实例却可以访问类的所有成员。</p>
<h1>下载</h1>
<p><a href="https://github.com/yyc-git/YOOP" target="_blank">GitHub地址</a></p>
<h1>版本历史</h1>
<p><strong>2013-06-07 发布YOOP v1.0&nbsp;</strong></p>
<p><strong>2014-08-26 发布YOOP v1.1&nbsp;</strong></p>
<p>1、类实例增加isInstanceOf方法，用于判断是否为类的实例，适用于接口继承、类继承等情况</p>
<p>2、protected方法也可以使用this.base来访问父类同名方法了</p>
<p>3、解决了&ldquo;若一个方法中调用其它方法，则它们的this.base会互相干扰&rdquo;的问题</p>
<p>4、增加stubParentMethod和stubParentMethodByAClass方法，该方法让父类（Class/AClass）指定方法不执行，用于Class的测试方法中调用了父类方法的情况（如调用了this.base()或this.baseClass.xxx）</p>
<p><span style="font-size: 14px; line-height: 1.5;">5、现在支持AMD、CMD、CommonJS规范了</span></p>
<p>6、增加YYC.YOOP.version属性，用于获得当前版本号&nbsp;</p>
<p>7、Class的构造函数F中现在只拷贝原型的属性到实例中，从而同一个类的实例之间共享同一原型对象的方法，但它们的属性相互独立</p>