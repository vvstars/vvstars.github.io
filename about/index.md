---
permalink: "/about/"
layout: page
icon: heart
---

* content
{:toc}


<select class="btn" onchange= "onLanChange(this.options[this.options.selectedIndex].value)">
    <option class="btn" value="0" selected> 中文 Chinese </option>
    <option class="btn" value="1"> 英语 English </option>
</select>

<!-- Chinese Version -->
<div class="zh" style="padding-left:15px">
<h2>信息</h2>
<ul style="font-size:20px;">
<li>廖宇星，Luise Liao</li>
<li>南京大学环境学院本科四年级</li>
<li>中国江苏，南京</li>
<li>来自江西吉安</li>
<li><a href="mailto:{{site.email}}" title="email" style="color:#444;"><i class="fa fa-envelope-o" aria-hidden="true"></i>{{ site.email }}</a></li>
</ul>
<h2>标签</h2>
<ul style="font-size:20px;">
<li>咨询</li>
<li>摄影</li>
<li>轮滑</li>
<li>麦肯锡的朝圣者</li>
<li>环境，生命周期评价</li>
<li>Web前端开发，Jekyll</li>
</ul>
</div>

<!-- English Version -->
<div class="en" style="padding-left:15px">
<h2>Information</h2>
<ul style="font-size:20px;">
<li>廖宇星，Luise Liao</li>
<li>Senior student, School of Environment, Nanjing university</li>
<li>From Jian，Jiangxi</li>
<li>Nanjing, Jiangsu, China</li>
<li><a href="mailto:{{site.email}}" title="email" style="color:#444;"><i class="fa fa-envelope-o" aria-hidden="true"></i>{{ site.email }}</a></li>
</ul>
<h2>Features</h2>
<ul style="font-size:20px;">
<li>Consulting</li>
<li>McKinney Admirer</li>
<li>Photographer</li>
<li>Rollerskating</li>
<li>LCA, Environment</li>
<li>Jekyll, Html, Web</li>
</ul>
</div>

## Comments

{% include comments.html %}

<!-- Handle Language Change -->
<script type="text/javascript">
    var $zh = document.querySelector(".zh");
    var $en = document.querySelector(".en");
    function onLanChange(index){
        if(index == 0){
            $zh.style.display = "block";
            $en.style.display = "none";
        }else{
            $en.style.display = "block";
            $zh.style.display = "none";
        }
    }
    onLanChange(0);
</script>
