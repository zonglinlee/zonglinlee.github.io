- jQuery�����������飬����ÿ��Ԫ�ض���һ��������DOM�ڵ�Ķ���
- jQuery��ѡ�������᷵��undefined����null
- jQuery�����DOM����֮����Ի���ת��
```js
var div = $('#abc'); // jQuery����
var divDom = div.get(0); // �������div����ȡ��1��DOMԪ��
var another = $(divDom); // ���°�DOM��װΪjQuery����
```
- ���Բ���ͬʱ����red��green�Ľڵ�
```js
var a = $('.red.green');// ע��û�пո�
var email = $('[name=email]'); // �ҳ�<??? name="email">
var emailInput = $('input[name=email]');
����tag��class����ϲ���Ҳ�ܳ�����
var tr = $('tr.red'); 
```
- $('ancestor descendant')
-��ѡ����$('parent>child')
- ��������Filter��������һ�㲻����ʹ�ã���ͨ��������ѡ�����ϣ��������Ǹ���ȷ�ض�λԪ�ء�last-child/first-child/even/odd/nth-child
- ��Ա�Ԫ�أ�jQuery����һ�������ѡ����
:enabled/:disabled/:file/:radio/:focus

## ���Һ͹���
ͨ�������ѡ��������ֱ�Ӷ�λ��������Ҫ��Ԫ�أ����ǣ��������õ�һ��jQuery����󣬻��������������Ϊ��׼�����в��Һ͹��ˡ�

����Ĳ�������ĳ���ڵ�������ӽڵ��в��ң�ʹ��find()�������������ֽ���һ�������ѡ���������Ҫ�ӵ�ǰ�ڵ㿪ʼ���ϲ��ң�ʹ��parent()����parent() ����λ��ͬһ�㼶�Ľڵ㣬����ͨ��next()��prev()����

���˷�����filter()�������Թ��˵�������ѡ���������Ľڵ㣻map()������һ��jQuery�������������DOM�ڵ�ת��Ϊ�������󣻴��⣬һ��jQuery������������˲�ֹһ��DOM�ڵ㣬first()��last()��slice()�������Է���һ���µ�jQuery���󣬰Ѳ���Ҫ��DOM�ڵ�ȥ��
���˷����д���һ��������Ҫ�ر�ע�⺯���ڲ���this����ΪDOM���󣬲���jQuery����

## ����DOM
jQuery�����text()��html()�����ֱ��ȡ�ڵ���ı���ԭʼHTML�ı���jQuery��API��Ʒǳ�����޲�������text()�ǻ�ȡ�ı�����������ͱ�������ı���HTMLҲ�����Ʋ���

һ��jQuery������԰���0���������DOM�������ķ���ʵ���ϻ������ڶ�Ӧ��ÿ��DOM�ڵ���
## �޸�CSS
jQuery�����С��������������ص㣬�������޸�CSSʵ����̫������
$('#test-css li.dy>span').css('background-color', '#ffd351').css('color', 'red');
Ϊ�˺�JavaScript����һ�£�CSS���Կ�����'background-color'��'backgroundColor'���ָ�ʽ��
```js
var div = $('#test-div');
div.hasClass('highlight'); // false�� class�Ƿ����highlight
div.addClass('highlight'); // ���highlight���class
div.removeClass('highlight'); // ɾ��highlight���class
```
## ��ʾ������DOM
Ҫ����һ��DOM�����ǿ�������CSS��display����Ϊnone������css()�����Ϳ���ʵ�֡�������Ҫ��ʾ���DOM����Ҫ�ָ�ԭ�е�display���ԣ���͵��ȼ�����ԭ�е�display���Ե�����block����inline���Ǳ��ֵ��

���ǵ���ʾ������DOMԪ��ʹ�÷ǳ��ձ飬jQueryֱ���ṩshow()��hide()����
## ��ȡDOM��Ϣ
����jQuery��������ɷ���������ֱ�ӿ��Ի�ȡDOM�ĸ߿����Ϣ����������Բ�ͬ�������д�ض����룺

// ��������Ӵ��ڴ�С:
$(window).width(); // 800
$(window).height(); // 600

// HTML�ĵ���С:
$(document).width(); // 800
$(document).height(); // 3500

attr()��removeAttr()�������ڲ���DOM�ڵ������
prop()������attr()����
attr()��prop()��������checked����������ͬ��

var radio = $('#test-radio');
radio.attr('checked'); // 'checked'
radio.prop('checked'); // true
prop()����ֵ������һЩ����������is()�����жϸ��ã�

var radio = $('#test-radio');
radio.is(':checked'); // true
���Ƶ����Ի���selected������ʱ�����is(':selected')��
## ������
���ڱ�Ԫ�أ�jQuery����ͳһ�ṩval()������ȡ�����ö�Ӧ��value����,һ��val()��ͳһ�˸���������ȡֵ�͸�ֵ������
## �޸�DOM�ṹ
ֱ��ʹ��������ṩ��API��DOM�ṹ�����޸ģ��������븴�ӣ�����Ҫ��������д��ͬ�Ĵ��롣
- ����ͨ��jQuery��html()���ֱ��������⣬��������append()����
ul.append('<li><span>Haskell</span></li>');
���˽����ַ�����append()�����Դ���ԭʼ��DOM����jQuery����ͺ�������
���뺯��ʱ��Ҫ�󷵻�һ���ַ�����DOM�������jQuery������ΪjQuery��append()����������һ��DOM�ڵ㣬ֻ�д��뺯���������ÿ��DOM���ɲ�ͬ���ӽڵ㡣

append()��DOM��ӵ����prepend()���DOM��ӵ���ǰ��
����ע�⣬���Ҫ��ӵ�DOM�ڵ��Ѿ�������HTML�ĵ��У��������ȴ��ĵ��Ƴ���Ȼ������ӣ�Ҳ����˵����append()��������ƶ�һ��DOM�ڵ㡣

���Ҫ���½ڵ���뵽ָ��λ��after(),Ҳ����˵��ͬ���ڵ������after()����before()����

ɾ���ڵ�
Ҫɾ��DOM�ڵ㣬�õ�jQuery�����ֱ�ӵ���remove()�����Ϳ����ˡ����jQuery�����������DOM�ڵ㣬ʵ���Ͽ���һ��ɾ�����DOM�ڵ�

## �¼�
��������д���ȼۣ����߸�����
```js
var a = $('#test-link');
a.on('click', function () {
    alert('Hello!');
})
a.click(function () {
    alert('Hello!');
});
```
����¼���mousemove�������DOM�ڲ��ƶ�ʱ������ hover����������˳�ʱ���������������൱��mouseenter����mouseleave��
ready�¼���������document��������ready�¼���DOM��ɳ�ʼ���󴥷�����ֻ����һ�Σ����Էǳ��ʺ�����д�����ĳ�ʼ�����롣

$(function () {
    // init...
});
����д����Ϊ���������������$(function () {...})����ʽ���μ�����document�����ready�¼������������Է������¼������������ǻ�����ִ��
ȡ����
һ���ѱ��󶨵��¼����Խ���󶨣�ͨ��off('click', function)ʵ��
����ʹ��off('click')һ�����Ƴ��Ѱ󶨵�click�¼������д�������
ͬ���޲�������off()һ�����Ƴ��Ѱ󶨵��������͵��¼�������
�������ȫ����
��������У���ЩJavaScript����ֻ�����û������²���ִ�У����磬window.open()����

��дjQuery���
��jQuery�����һ���·�����ͨ����չ$.fn����ʵ�ֵ�
$.fn.highlight1 = function () {
    // this�Ѱ�Ϊ��ǰjQuery����:
    this.css('backgroundColor', '#fffceb').css('color', '#d85030');
    return this;
}
ע�⵽�����ڲ���this�ڵ���ʱ����ΪjQuery�������Ժ����ڲ��������������������jQuery����ķ�����

���գ����ǵó���дһ��jQuery�����ԭ��

��$.fn�󶨺�����ʵ�ֲ���Ĵ����߼���
����������Ҫreturn this;��֧����ʽ���ã�
�������Ҫ��Ĭ��ֵ������$.fn.<pluginName>.defaults�ϣ�
�û��ڵ���ʱ�ɴ����趨ֵ�Ա㸲��Ĭ��ֵ��