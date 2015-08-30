+++

Description = ""
title = "Accordion"

+++
 
# Accordion

{{%accordion test%}}

{{%accord title="accordion1" parent="test"%}}
{{%highlight java%}} 

private int age;
private String name;
 
{{%/highlight%}}
{{%/accord%}}

{{%accord title="accordion2" parent="test"%}}
 
 fdslfsdkfldkfdsf
 dsfsdf
 sdfsdfdsf

{{%/accord%}}


{{%accord title="accordion3" parent="test"%}}
 
 fdslfsdkfldkfdsf
 dsfsdf
 sdfsdfdsf

{{%/accord%}}

{{%/accordion%}}
 



{{%accordion test1%}}

{{%accord title="accordion11" parent="test1"%}}
{{%highlight java%}}

private int age;
private String name;

{{%/highlight%}}
{{%/accord%}}

{{%accord title="accordion21" parent="test1"%}}

 fdslfsdkfldkfdsf
 dsfsdf
 sdfsdfdsf

{{%/accord%}}



{{%accord title="accordion31" parent="test1"%}}

 fdslfsdkfldkfdsf
 dsfsdf
 sdfsdfdsf

{{%/accord%}}

{{%/accordion%}}


{{% accordion acc %}}
{{% accord title="Click to see the code example1:" parent="acc"%}}


Connection conn;
Statement stmt = conn.createStatement();
ResultSet rs = stmt.executeQuery("SELECT ID AS Identifier, NAME AS FullName FROM PERSON WHERE Identifier = 210");


{{% /accord %}}
{{% /accordion%}}
 

 