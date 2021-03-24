<html>
<title> input</title>
<head>
<script
  src="https://code.jquery.com/jquery-3.4.1.js"
  integrity="sha256-WpOohJOqMqqyKL9FccASB9O0KwACQJpFTUBLTYOVvVU="
  crossorigin="anonymous"></script>
<script>
function SubForm (){
    $.ajax({
        url:'https://api.apispreadsheets.com/data/9998/',
        type:'post',
        data:$("#myForm").serializeArray(),
        success: function(){
          alert("Form Data Submitted :)")
		  alert("Form Data Submitted :)")
        },
        error: function(){
          alert("There was an error :(")
        }
    });
}
</script>
</head>
<body>
<form id="myForm">
    <label>Full Name</label>
    <br/>
    <input name="full_name" />
    <br/>
    <label>RollNum</label>
    <br/>
    <input name="RollNum" />
    <br/>
    <label>gender</label>
    <br/>
    <input type="radio" id="gender" name="gender" value="male" /> male<br/>
    <input type="radio" id="gender" name="gender" value="female" /> Female<br/>
    <br/>
  </form>
  <button onclick="SubForm()">Submit</button>
  </body>
</html>
