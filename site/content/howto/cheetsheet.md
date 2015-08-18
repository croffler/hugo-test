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

{{%refer%}} Please refer to this section if you need more info [docs](http://docs.gigaspaces.com) {{%/refer%}}


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

 
 {{< highlight  yaml >}}
tosca_definitions_version: cloudify_dsl_1_0

imports:
  - http://www.getcloudify.org/spec/cloudify/3.2/types.yaml
  - http://www.getcloudify.org/spec/openstack-plugin/1.2/plugin.yaml

inputs:
  image_name:
    description: The server's image name
    type: string
    default: "Ubuntu 12.04"

node_templates:
  vm:
    type: cloudify.openstack.nodes.Server
    properties:
      server:
        image_name: { get_input: image_name }
{{< /highlight >}}





 


 
 
 

 


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


 