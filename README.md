# Android 开发规范 V1.0

---

 1. 规范的规范
------------------------
 * **本规范的每一条目必须无二义性，并且可执行。否则作废**
 * **本规范的条目分为两个级别:**
  + **规则（加粗文字）**
  + 建议（普通文字）
 * **本规范所有的“规则”条目必须被遵守**
 2. 代码格式 
------------------------
*  **使用统一的代码格式**
 提交前格式化代码 (Ctrl + Shift +f)

3. 代码规范
------------------------
* 包
  + **包名必须全部小写，2个以内单词**
  + 最好为 1 个单数名词
  + **所有项目的包都要以“com.knet.eqxiu”为父包**
* 类
  + **类中每个单词的首字母必须大写**
  + 每个类都以功能性名词结尾，如xxxActivity,xxxFragment,xxxView,xxxAdapter
  + **每个类的都应该加上类注释，包括所有者、邮箱及日期**
* 接口
  + **如果接口表示一个事件，则应该取名为OnXxxListener**
  + 如果表示一种能力，应以"able"、"ible"结尾
* 方法
  + **大小写字母混合组成，第一个单词的首字母小写，其后单词的首字母大写(驼峰式命名)**
  + **继承的方法可以省略注释，但是被继承方法必须有注释。**
* 变量
  + **如果是集合或数组，用复数名词，如pets,houses**
  + **成员变量能private就不要default，能default就不要protected，最好不要public**
  + 不要在activity中使用静态成员变量
  + 不推荐使用下划线
  + 局域变量名要尽量短，推荐用缩写，比如 StringBuilder sb
  + 非公有，非静态成员变量以m开头
  + 静态成员变量以s开头
  + 其他变量以小写字母开头
* 常量
  + 只能包含字母和\_，字母全部大写，单词之间用\_隔开
* 注释
  + **注释必须和代码保持同步**

4. 资源规范
------------------------
* 使用tools命名空间:
  + 无默认text时使用tools:text 代替 andriod:text 进行效果预览
  + 无默认图片时使用tools:src 代替 andriod:src 进行效果预览
  + 无默认背景时使用tools:background 代替 andriod:background 进行效果预览
* 尽量以结构开头，业务结尾，中间用下划线区分:
  + layout: activity\_login,fragment\_login,view\_login,listitem\_login
  + drawable: selector\_login,shap\_login
* 控件id：尽量以对应控件的各单词英文首字母开头，如TextView就以tv开头(tv\_login)，ImageView就以iv开头(iv\_login)，CheckBox就以cb开头(cb\_login)，Button就以btn开头(btn\_login), LinearLayout(ll\_login), RelativeLayout(rl\_login), FrameLayout(fl\_login)等
* 菜单（menu）的id：建议以action开头,如action\_login
* 在主题和Style中定义Button，ImageButton等的点击效果，避免使用selector:
  + \<item name="colorButtonNormal"\>@color/red\</item\><!--正常状态下的颜色  -->
  + \<item name="colorControlHighlight"\>@color/bg_gray\</item\><!--覆盖色，按下的颜色  -->
5. 开发建议
------------------------
* 所有的非AtionBar的界面均采用Fragment（片段式）来实现，在Activity中只做Fragment对象的管理以及ActionBar的处理工作
* 按功能对Activity和Fragment进行分包（可以考虑将相同功能模块的Activity和Fragment放在同一个包下）
* 所有Activity继承BaseActivity，所有Fragment继承BaseFragment，公共部分应全部抽取到基类中
* 不要使用静态全局变量，如果确实需要，可以考虑将其作为Application的成员变量（慎用）
* 如果仅希望一段代码在UI线程执行，可以考虑使用activity.runOnUiThread方法
* 不要在Activity或者Fragment中写跟界面无关的代码
6. 其他开发建议
------------------------
https://github.com/cigk/AndroidBestPractice/blob/master/translations/Chinese/README.cn.md
