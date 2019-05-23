<html>
<head>
	<title>Lab</title>
  <meta charset="utf-8">
  <link rel="stylesheet" href="css/bootstrap.min.css">
  <script src="js/jquery.min.js"></script>
  <script src="js/bootstrap.min.js"></script>
</head>

<style type="text/css">
td{
	border: 1px solid black;
	padding-right: 80px;
}
body{
  margin-top: 40px;
}
button{
  float: left;
  margin-left: 10px;
}
h1{
  margin-left: 450px;
  float: left;
}
table{
  float: left;
  margin-left: 350px;
}
</style>

<body>
	<button type="button" class="btn btn-info btn-md" data-toggle="modal" data-target="#myModal">Add Student</button>

<!-- Modal -->
<div id="myModal" class="modal fade" role="dialog">
  <div class="modal-dialog">

    <!-- Modal content-->
    <div class="modal-content">
      <div class="modal-header">
        <button type="button" class="close" data-dismiss="modal">&times;</button>
        <h4 class="modal-title">Add Student Information</h4>
      </div>
      <div class="modal-body">
        <form name = "form1">
        <h5>ID Number</h5>
        <input type = "text" class = "form-control" value = "2019000" id = "ID" disabled>
        <h5>Last Name</h5>
        <input type = "text" class = "form-control" name = "" id = "lname">
        <h5>First Name</h5>
        <input type = "text" class = "form-control" name = "" id ="fname">
        <h5>Middle Name</h5>
        <input type = "text" class = "form-control" name = "" id = "mname">
        <h5>Course</h5>
        <input type = "text" class = "form-control" name = "" id = "course">
        <h5>Year</h5>
        <input type = "text" class = "form-control" name = "" id = "year">
        
      </div>
      <div class="modal-footer">
        <button type="button" class="btn btn-primary" onclick="add()" data-dismiss = "modal">Add Student</button>
        <button type="button" class="btn btn-default" data-dismiss="modal">Close</button>
       </form>
      </div>
    </div>

  </div>
</div>
    <button type="button" class="btn btn-danger" onclick="del()">Delete</button>	
<center>

	<h1>Student Information</h1>
<div class="col-md-9">       
        <table class="table table-bordered">
      <thead>
<tr>
<td>Id Number</td>
<td>Last Name</td>
<td>First Name</td>
<td>Middle Name</td>
<td>Course</td>
<td>Year</td>
</tr>
</thead>
<tbody id = "tbody" ></tbody>
</table>
</center>

<script type="text/javascript">
    var ID=2019001;

  function add(){
    
      var a = document.getElementById("lname").value;
      var b = document.getElementById("fname").value;
      var c = document.getElementById("mname").value;
      var d = document.getElementById("course").value;
      var e = document.getElementById("year").value;

      var x = document.createElement("tr");
      x.innerHTML="<td>"+ID+"</td><td>"+a+"</td>"+"<td>"+b+"</td>"+"<td>"+c+"</td>"+"<td>"+d+"</td>"+"<td>"+e+"</td>";
      document.getElementById("tbody").appendChild(x);
      ++ID;
      var count = document.getElementById("ID");
      count.value = ID;
      
      document.getElementById("lname").value = "";
      document.getElementById("fname").value  = "";
      document.getElementById("mname").value  = "";
      document.getElementById("course").value  = "";
      document.getElementById("year").value = "";  
    }
    function del(){
      var y = document.getElementById("tbody");
        y.removeChild(tbody.lastChild);
    }
</script>
</body>
</html>
