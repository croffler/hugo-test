+++

Description = ""
title = "Tab"

+++

<div class="container">

<!-------->
<div id="content">
    <ul id="tabs" class="nav nav-tabs" data-tabs="tabs">
        <li class="active"><a href="#red" data-toggle="tab">Red</a></li>
        <li><a href="#orange" data-toggle="tab">Orange</a></li>
        <li><a href="#yellow" data-toggle="tab">Yellow</a></li>
        <li><a href="#green" data-toggle="tab">Green</a></li>
        <li><a href="#blue" data-toggle="tab">Blue</a></li>
    </ul>
    <div id="my-tab-content" class="tab-content">
        <div class="tab-pane active" id="red">
            <h1>Red</h1>
            <p>red red red red red red</p>
        </div>
        <div class="tab-pane" id="orange">
            <h1>Orange</h1>
            <p>orange orange orange orange orange</p>
        </div>
        <div class="tab-pane" id="yellow">
            <h1>Yellow</h1>
            <p>yellow yellow yellow yellow yellow</p>
        </div>
        <div class="tab-pane" id="green">
            <h1>Green</h1>
            <p>green green green green green</p>
        </div>
        <div class="tab-pane" id="blue">
            <h1>Blue</h1>
            <p>blue blue blue blue blue</p>
        </div>
    </div>
</div>


# Hello

<h3 id="tabbed-pane">Tabbed Pane</h3>

<table border="1" cellpadding="10">
<colgroup><col span="1" style="width: 50%;" /><col span="1" style="width: 50%;" /></colgroup>
<tr><th> Example </th><th> Markdown </th></tr>
<tr><td>
<div class="tabsection"><ul class="nav nav-tabs"></ul><div class="tab-content">
<div class="tab-pane" id="foo" title="Foo"><p>This is tab Foo </p>
</div>
<div class="tab-pane" id="bar" title="Bar"><p>This is tab Bar </p>
</div>
</div></div>
</td>
<td><pre>
{% inittab %}
{% tabcontent Foo %} This is tab Foo {% endtabcontent %}
{% tabcontent Bar %} This is tab Bar {% endtabcontent %}
{% endinittab %}
</pre></td>
</tr>
</table>


 