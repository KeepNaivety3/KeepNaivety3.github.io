---
layout: post
title: 博客自带功能
date: 2023-02-13 17:00:00
description: 整理一下blog自带的功能
tags: translate blogging
categories: blog
---

## 格式和链接

### 文本超链接

<a href="https://zh.wikipedia.org/wiki/Markdown">维基百科 Markdown 词条

### 列表

<ul>
    <li>後藤ひとり</li>
    <li>伊地知虹夏</li>
    <li>山田リョウ</li>
    <li>喜多郁代</li>
    <li>後藤ふたり</li>
</ul>

### 水平分割线

<hr>

### 块引用

<blockquote>
乐队……那是阴暗角色也能闪耀起来的唯一地方。
“波奇酱”，也就是后藤一里，是一个爱着吉他的孤独少女。每天在家中一个人寂寞的弹吉他就是她的日常，机缘巧合之下她加入了伊地知虹夏所组建的“结束乐队”。不习惯在观众面前演奏的后藤究竟能否成为一个优秀的乐队成员呢！？这是一份推送给孤独少年少女们的，最热血的音乐漫画！！
バンド活動に憧れているが人見知りがひどく、高校に入ってから1カ月経つも友達が1人もできない少女・後藤ひとりを主役に展開する音楽作品。
</blockquote>

## 图片画廊

### 图片并排显示

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/example_preview/Yagate_Kimi_ni_Naru_vol1_1.jpg" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/example_preview/Yagate_Kimi_ni_Naru_vol1_2.jpg" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    图像标题位
</div>

### 添加 data-zoomable 使图片可缩放

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/example_preview/101044191_p0.jpg" class="img-fluid rounded z-depth-1" zoomable=true %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/example_preview/Bocchi_the_Rock_all.jpg" class="img-fluid rounded z-depth-1" zoomable=true %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/example_preview/Lycoris_Recoil_vol01.jpg" class="img-fluid rounded z-depth-1" zoomable=true %}
    </div>
</div>
<div class="caption">
    添加 zoomable=true 使图片可缩放
</div>

## 代码块

### 输出原生 liquid 代码

{% raw  %}

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/example_preview/Yagate_Kimi_ni_Naru_vol1_1.jpg" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/example_preview/Yagate_Kimi_ni_Naru_vol1_2.jpg" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

{% endraw %}

### 显示一段 C++ 代码

关键词 `linenos` 触发行号的显示：

{% highlight c++ linenos %}

int main(int argc, char const \*argv[])
{
string myString;

    cout << "input a string: ";
    getline(cin, myString);
    int length = myString.length();

    char charArray = new char * [length];

    charArray = myString;
    for(int i = 0; i < length; ++i){
        cout << charArray[i] << " ";
    }

    return 0;

}

{% endhighlight %}

## 数学公式

支持使用 MathJax3 引擎显示数学公式

### 内联公式

$$ E = mc^2 $$（即质能守恒，亦称为质能转换公式、质能方程）是一种阐述能量（$$ E $$）与质量（$$ m $$）间相互关系的理论物理学公式，公式中的 $$ c $$ 是物理学中代表光速的常数。

### 行间公式

$$
\sum_{k=1}^\infty |\langle x, e_k \rangle|^2 \leq \|x\|^2
$$

### 使用 {equation} 显示数学公式

如果使用 `\begin{equation}...\end{equation}`，MathJax 会自动对等式进行编号：

\begin{equation}
\label{eq:cauchy-schwarz}
\left( \sum*{k=1}^n a_k b_k \right)^2 \leq \left( \sum*{k=1}^n a*k^2 \right) \left( \sum*{k=1}^n b_k^2 \right)
\end{equation}

通过 `\label{...}`，我们现在可以使用标签 `\eqref` 引用方程。

## Twitter 预览

显示一篇推文：

{% twitter https://twitter.com/_sa_220/status/1550686471366926336 %}

显示推主的时间线：

{% twitter https://twitter.com/_sa_220 maxwidth=800 limit=3 %}

更多内容请参考：[jekyll-twitter-plugin](https://github.com/rob-murray/jekyll-twitter-plugin)

