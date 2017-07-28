
## validation


## 使用jquery-validation的好处

1. jquery-validation 是基于jquery的扩展插件，简单易用。

2. jquery-validation 易于实现自定义扩展。



## jquery-validation的使用

1. 引入相关依赖、类库

```html
    <script src="http://static.runoob.com/assets/jquery-validation-1.14.0/lib/jquery.js"></script>
    <script src="http://static.runoob.com/assets/jquery-validation-1.14.0/dist/jquery.validate.min.js"></script>
    <script src="http://static.runoob.com/assets/jquery-validation-1.14.0/dist/localization/messages_zh.js"></script>
```

2. 自定义表单

```html
    <form class="cmxform" id="commentForm" method="get" action="">
        <fieldset>
            <legend>输入您的名字，邮箱，URL，备注。</legend>
            <p>
                <label for="cname">Name (必需, 最小两个字母)</label>
                <input id="cname" name="name" minlength="2" type="text" required>
            </p>
            <p>
                <label for="cemail">E-Mail (必需)</label>
                <input id="cemail" type="email" name="email" required>
            </p>
            <p>
                <label for="curl">URL (可选)</label>
                <input id="curl" type="url" name="url">
            </p>
            <p>
                <label for="ccomment">备注 (必需)</label>
                <textarea id="ccomment" name="comment" required></textarea>
            </p>
            <p>
                <input class="submit" type="submit" value="Submit">
            </p>
        </fieldset>
    </form>

```

3. 自定义js

```js
    $.validator.setDefaults({
            submitHandler: function () {
                alert("提交事件!");
            }
        });
        $().ready(function () {
            $("#commentForm").validate();
        });

```

4. 自定义CSS样式


5. 根据文档进行相应的自定义扩展


[查看教程详细文档](http://www.runoob.com/jquery/jquery-plugin-validate.html)