# mip-taoge-form 表单

scaydk.com网表单提交组件。

标题|内容
----|----
类型|通用
支持布局|responsive,fixed-height,fill,container,fixed
所需脚本|https://c.mipcdn.com/extensions/platform/v1/mip-taoge-form/mip-taoge-form.js

## 示例

### 基本使用

```html
<mip-taoge-form method="get" url="https://www.mipengine.org?we=123">
    <input type="text" name="username" validatetarget="username" validatetype="must" placeholder="姓名">
    <div target="username">姓名不能为空</div>
    <input type="number" name="age" validatetarget="age" validatetype="must" placeholder="年龄">
    <div target="age">年龄不能为空</div>
    <input type="submit" value="提交">
</mip-taoge-form>
```
### 加清空按钮

```html
<mip-taoge-form method="get" url="https://www.mipengine.org" clear>
    <input type="text" name="username2" validatetarget="username2" validatetype="must" placeholder="姓名">
    <div target="username2">姓名不能为空</div>
    <input type="number" name="age2" validatetarget="age2" validatetype="must" placeholder="年龄">
    <div target="age2">年龄不能为空</div>
    <input type="submit" value="提交">
</mip-taoge-form>
```

### 自定义验证规则

```html
<mip-taoge-form method="get" url="https://www.mipengine.org">
     <input type="text" name="customnumber" validatetarget="custom" validatetype="custom" validatereg="^[0-9]*$" placeholder="我是自定义验证规则数字">
     <div class="mip-taoge-form-target" target="custom">请输入正确的数字</div>
     <input type="submit" value="提交">
 </mip-taoge-form>
```

## 属性

### method

说明：表单提交方法  
必选项：是  

### url

说明：表单提交url，建议填写https地址   
必选项: 是  

### validatetarget

说明:  验证提示对应tag,用于对应错误时的提示显示元素的查找    
必选项：否   

### validatetype

说明：验证类型, 用于支持简单的验证。目前提供email、phone、idcar、custom。当为custom时则需要填写validatereg    
必选项：否   

### validatereg

说明: 自定义验证，补充站长个性化的验证规则。如果validatetype为custom时需填写相应验证规则  
必选项：否

### clear

说明: 表单中input清空按钮开关 
必选项：否  

## 注意事项

1. 表单提交方法如果为post，应使用https地址。避免 MIP-Cache https环境提交到http，导致浏览器报错。
