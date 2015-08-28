+++

Description = ""
title = "Table"

+++

 

 # Simple markdown table


Keyname       | Required | Type          | Description
-----------   | -------- | ----          | -----------
type          | yes      | string        | The [node type](dsl-spec-node-types.html) of this node template.
properties    | no       | dict          | The properties of the node template matching its node type properties schema.
instances     | no       | dict          | Instances configuration.
interfaces    | no       | interfaces    | Used for mapping plugins to [interfaces](dsl-spec-interfaces.html) operation or for specifying inputs for already mapped node type operations.
relationships | no       | relationships | Used for specifying the [relationships](dsl-spec-relationships.html) this node template has with other node templates.

 
<br>


# Short Code 

{{%table%}}

{{%row "skdsjdsdsdsjkd"   "dkjsdjksjdksjdkskd"%}}
{{%row "skdsjdsdsdsjkd"   "dkjsdjksjdksjdkskd"%}}
{{%row "skdsjdsdsdsjkd"   "dkjsdjksjdksjdkskd"%}}
{{%row "skdsjdsdsdsjkd"   "dkjsdjksjdksjdkskd"%}}
{{%row "skdsjdsdsdsjkd"   "dkjsdjksjdksjdkskdsasahsghagshgas"%}}

{{%/table%}}


## Option

[bootstrap-table](https://github.com/wenzhixin/bootstrap-table)

<table data-toggle="table">
    <thead>
    <tr>
        <th>Name</th>
        <th>Stars</th>
        <th>Forks</th>
        <th>Description</th>
    </tr>
    </thead>
    <tbody>
    <tr id="tr-id-1" class="tr-class-1">
        <td id="td-id-1" class="td-class-1">
            <a href="https://github.com/wenzhixin/bootstrap-table">bootstrap-table</a>
        </td>
        <td>526</td>
        <td>122</td>
        <td>An extended Bootstrap table with radio, checkbox, sort, pagination, and other added features. (supports twitter bootstrap v2 and v3) 
        </td>
    </tr>
    <tr id="tr-id-2" class="tr-class-2">
        <td id="td-id-2" class="td-class-2">
            <a href="https://github.com/wenzhixin/multiple-select">multiple-select</a>
        </td>
        <td>288</td>
        <td>150</td>
        <td>A jQuery plugin to select multiple elements with checkboxes :)
        </td>
    </tr>
    <tr id="tr-id-3" class="tr-class-3">
        <td id="td-id-3" class="td-class-3">
            <a href="https://github.com/wenzhixin/bootstrap-show-password">bootstrap-show-password</a>
        </td>
        <td>32</td>
        <td>11</td>
        <td>Show/hide password plugin for twitter bootstrap.
        </td>
    </tr>
    <tr id="tr-id-4" class="tr-class-4">
        <td id="td-id-4" class="td-class-4">
            <a href="https://github.com/wenzhixin/blog">blog</a>
        </td>
        <td>13</td>
        <td>4</td>
        <td>my blog</td>
    </tr>
    <tr id="tr-id-5" class="tr-class-5">
        <td id="td-id-5" class="td-class-5">
            <a href="https://github.com/wenzhixin/scutech-redmine">scutech-redmine</a>
        <td>6</td>
        <td>3</td>
        <td>Redmine notification tools for chrome extension.</td>
    </tr>
    </tbody>
</table>

 
 

 