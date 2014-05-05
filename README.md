reference
=========

This is used to contain reference codes.


<html xmlns="http://www.w3.org/1999/xhtml">
<head runat="server">
    <title></title>
    <style type = "text/css">
        .selected
        {
            background-color:blue;
        }
    </style>
    <script type = "text/javascript">
        function Select(obj) {
            obj.className = 'selected';
            var tbl = document.getElementById("table1")
            var firstRow = tbl.getElementsByTagName("TR")[0];
            var oldRow = tbl.rows[firstRow.getElementsByTagName("input")[0].value];
            if (oldRow != null) {
                oldRow.className = '';
            }
            firstRow.getElementsByTagName("input")[0].value = obj.rowIndex;
        }
      	  
    </script>
</head>
<body>
    <form id="form1" runat="server">
    <div>
        <table id = "table1" border="1px">
        <tr style="cursor:pointer" onclick="Select(this);">
        <td>hello1
            <input type = "hidden" value = "false" />
        </td>
	<td>hello1
            <input type = "hidden" value = "false" />
        </td>
	<td>hello1
            <input type = "hidden" value = "false" />
        </td>
        </tr>
        <tr style="cursor:pointer" onclick="Select(this);">
        <td>hello2
        </td>
	
	<td>hello1
            <input type = "hidden" value = "false" />
        </td>
	<td>hello1
            <input type = "hidden" value = "false" />
        </td>
        </tr>
        </table>
    </div>
    </form>
</body>
</html>
