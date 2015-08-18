+++

Description = ""
title = "Cheat sheet"

+++
 


# Site variables

 
The latest XAP release is : {{<latestxaprelease>}}


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


# Downloads

{{%externurl  "http://docs.gigaspaces.com"%}}<br>
{{%download  "http://docs.gigaspaces.com"%}}<br>
{{%pdf  "http://docs.gigaspaces.com"%}}<br>
{{%git  "http://docs.gigaspaces.com"%}}<br>
{{%zip  "http://docs.gigaspaces.com"%}}<br>
{{%word "http://docs.gigaspaces.com"%}}



# Navigation

{{%tryit "http://docs.gigaspaces.com"%}}

{{%learn "http://docs.gigaspaces.com"%}}



# Code Highlight

{{<highlight java>}}
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
{{</highlight>}}


 


# Color


## Text Color

This is a color {{%color blue%}} test {{%/color%}}

This is a color {{%color red%}} test {{%/color%}}


## Background color

This is a color {{%bcolor yellow%}} test {{%/bcolor%}}

This is a color {{%bcolor green%}} test {{%/bcolor%}}

### Text stuff 


This is a text {{%sub%}} small text should be here {{%/sub%}}


# Text Alignment

{{%align center%}} This text should be aligned in the center{{%/align%}}

{{%align right%}} This text should be aligned to the right{{%/align%}}

{{%align left%}} This text should be aligned to the left{{%/align%}}


 