+++

Description = ""
title = "Cheat sheet"

+++

# Site variables

 
{{<latestxaprelease>}}



{{%inittab%}}

{{%tabcontent%}}
Tab 1 showing
{{%/tabcontent%}}

{{%tabcontent%}}
Tab 2 showing
{{%/tabcontent%}}

{{%/inittab%}}

# Section

{{%section%}}

{{%column%}}
column 1 dasdsajdjskajdkjskadjksjadkjskadjksjadkjsk
sdasdasdasdas
{{%/column%}}


{{%column%}}
column 2 dsajdsjadkjaskdjaskjdkasjdkjaskd
asdsadasdkjaskdjskajdkasjd
{{%/column%}}

{{%column%}}
column 3
asdhsahdjhsajdhjshdhsadhsahdashd
{{%/column%}}

{{%/section%}}


<br><br>

# Icons

{{<oksign>}} Ok Sign<br>
{{<infosign>}} Info Sign<br>
{{<exclamation>}} Exclamation Sign<br>
{{<question>}} Question Sign<br>
{{<plus>}} Plus Sign<br>
{{<remove>}} Remove Sign<br>
{{<star>}} Star sign<br>
{{<minus>}} Minus Sign<br>
{{<lampon>}} Lamp on<br>
{{<lampoff>}} Lamp off<br>


### Downloads

{{%externurl  "http://docs.gigaspaces.com"%}}<br>
{{%download  "http://docs.gigaspaces.com"%}}<br>
{{%pdf  "http://docs.gigaspaces.com"%}}<br>
{{%git  "http://docs.gigaspaces.com"%}}<br>
{{%zip  "http://docs.gigaspaces.com"%}}<br>
{{%word "http://docs.gigaspaces.com"%}}



# Code Highlight

{{%gshighlight java%}}
@SpaceClass
public class User {
  private Long id;
  private String name;
  private Double balance;
  private Double creditLimit;
 
  public User() {
  }

  @SpaceRouting
  @SpaceId(autoGenerate = false)
  public Long getId() {
	return id;
  }
}
{{%/gshighlight%}}

 


# Panels 


{{%fpanel%}}

This is a Front - Panel
ksjdjsdkjsjdsjdjsld
sadkjskjdkjskdjsjdjsld

dsadksajdkljklsjdl

sadklsjadjksjdsjdkla
{{%/fpanel%}}



{{%tip title="Tip"%}}
This is an info 
{{%/tip%}}


{{%warning title="Warning"%}}
This is a warning
{{%/warning%}}


{{%comment%}}

This should not show up 

{{%/comment%}}
 
 

# Youtube

{{%youtube kAe-ZxFnIYc%}}