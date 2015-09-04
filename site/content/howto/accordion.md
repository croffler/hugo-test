+++

Description = ""
title = "Accordion"

+++

<div class="container">
   <h2>Basic Accordion</h2>
    <p>Click on panel header to show its content.</p>
    <div style="margin:20px 0 10px 0;"></div>
    <div class="easyui-accordion" plain="true" style="width:500px;height:auto;border:true">
        <div title="About"   style="overflow:auto;padding:10px;">
            <p>Accordion is a part of easyui framework for jQuery. It lets you define your accordion component on web page more easily.</p>
        </div>
        <div title="Help"   style="padding:10px;">
            <p>The accordion allows you to provide multiple panels and display one or more at a time. Each panel has built-in support for expanding and collapsing. Clicking on a panel header to expand or collapse that panel body. The panel content can be loaded via ajax by specifying a 'href' property. Users can define a panel to be selected. If it is not specified, then the first panel is taken by default.</p>
        </div>
         <div title="Help"   style="padding:10px;">
                    <p>The accordion allows you to provide multiple panels and display one or more at a time. Each panel has built-in support for expanding and collapsing. Clicking on a panel header to expand or collapse that panel body. The panel content can be loaded via ajax by specifying a 'href' property. Users can define a panel to be selected. If it is not specified, then the first panel is taken by default.</p>
                </div>


    </div>
</div>
<br>


# Accordion

{{%accordion test%}}

{{%accord title="accordion1" parent="test" id="test110"%}}
{{%highlight java%}} 

private int age;
private String name;
 
{{%/highlight%}}
{{%/accord%}}

{{%accord title="accordion2" parent="test" id="test2"%}}
 
 fdslfsdkfldkfdsf
 dsfsdf
 sdfsdfdsf

{{%/accord%}}


{{%accord title="accordion3" parent="test" id="test3"%}}
 
 fdslfsdkfldkfdsf
 dsfsdf
 sdfsdfdsf

{{%/accord%}}

{{%/accordion%}}


# Accordion 2
 
{{%accordion test1%}}

{{%accord title="accordion1" parent="test1" id="test11"%}}
{{%highlight java%}}

private int age;
private String name;

{{%/highlight%}}
{{%/accord%}}

{{%accord title="accordion2" parent="test1" id="test21"%}}

 fdslfsdkfldkfdsf
 dsfsdf
 sdfsdfdsf

{{%/accord%}}


{{%accord title="accordion3" parent="test1" id="test31"%}}

 fdslfsdkfldkfdsf
 dsfsdf
 sdfsdfdsf

{{%/accord%}}

{{%/accordion%}}


 