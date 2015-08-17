+++

Description = ""
title = "Table"

+++




{{%table%}}

{{%row "skdsjdsdsdsjkd"   "dkjsdjksjdksjdkskd"%}}
{{%row "skdsjdsdsdsjkd"   "dkjsdjksjdksjdkskd"%}}
{{%row "skdsjdsdsdsjkd"   "dkjsdjksjdksjdkskd"%}}
{{%row "skdsjdsdsdsjkd"   "dkjsdjksjdksjdkskd"%}}
{{%row "skdsjdsdsdsjkd"   "dkjsdjksjdksjdkskdsasahsghagshgasgasasgagsacxzcxcxcxcxcxcxcxcxcxcxgccbxcxzbcbmxnzbcnxncbxnbcnxbcnbxncbxncbxncnxcxzcxcxncbxnbcxnbcnbxncbxbcnxbcnbxncbxncbnxzncxsgas"%}}




{{%/table%}}


<div class="container">
  <h2>Hover Rows</h2>
  <p>The .table-hover class enables a hover state on table rows:</p>      
  <table class="table-hover table-bordered table-striped table-condensed table-scrollable">     
    <thead>
      <tr>
        <th>Firstname</th>
        <th>Lastname</th>
        <th>Email</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>John</td>
        <td>Doe</td>
        <td>john@example.com bhjhhjkjhjhjhjhjhjhjhkhkhjhjhjhjkhjjkhjhjhjhjhjhjhjkhjhjhjhjhjhjhjhkhjkhjhjkhjkhjhhjkhkhhjhjhjkhjhjkhjkhjhjhjhjhjhjkhk111111111111111111
            hjhjhjhjhjhjhjkhkhk</td>
      </tr>
      <tr>
        <td>Mary</td>
        <td>Moe</td>
        <td>mary@example.com</td>
      </tr>
      <tr>
        <td>July</td>
        <td>Dooley</td>
        <td>july@example.com</td>
      </tr>
    </tbody>
  </table>
</div>




<div>
    <label><input id="hover" type="checkbox" checked=""> hover</label>
    <label><input id="striped" type="checkbox"> striped</label>
    <label><input id="condensed" type="checkbox"> condensed</label>
</div>
<table id="table-style" data-url="data1.json" data-height="400" data-row-style="rowStyle">
    <thead>
    <tr>
        <th data-field="id" class="col-md-2">Item ID</th>
        <th data-field="name" class="col-md-6">
            <i class="glyphicon glyphicon-star"></i>
            Item Name
        </th>
        <th data-field="price" class="col-md-4">
            <i class="glyphicon glyphicon-heart"></i>
            Item Price
        </th>
    </tr>
    </thead>
</table>
<script>
    $(function () {
        $('#hover, #striped, #condensed').click(function () {
            var classes = 'table';

            if ($('#hover').prop('checked')) {
                classes += ' table-hover';
            }
            if ($('#condensed').prop('checked')) {
                classes += ' table-condensed';
            }
            $('#table-style').bootstrapTable('destroy')
                .bootstrapTable({
                    classes: classes,
                    striped: $('#striped').prop('checked')
                });
        });
    });

    function rowStyle(row, index) {
        var classes = ['active', 'success', 'info', 'warning', 'danger'];

        if (index % 2 === 0 && index / 2 < classes.length) {
            return {
                classes: classes[index / 2]
            };
        }
        return {};
    }
</script>

 