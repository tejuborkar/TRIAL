# TRIAL
TRIAL REPOSITORY
<html>
<head>
   <meta name="viewport" content="width=device-width, initial-scale=1">
  <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.4.1/css/bootstrap.min.css">
  <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.6.0/jquery.min.js"></script>
  <script src="https://maxcdn.bootstrapcdn.com/bootstrap/3.4.1/js/bootstrap.min.js"></script>
</head>
<body>

<form method="post">
  <div class="container">
  	<h1>Registration form</h1>
	<div class="row" method="" id=""> 
<div class ="col-md-12" >

<div class="col-md-6">
    <label for="name"><b>Name :</b></label>
    <input type="text" class="form-group" style="margin:left:20px" placeholder="Enter full name" name="Name" id="Name" >

    <label for="address"><b>Address :</b></label>
    <input type="text"  class="form-group" placeholder="Enter Address" name="Address" id="Address">
	

    <label for="email"><b>Email :</b></label>
    <input type="text"  class="form-group" placeholder="Enter Email" name="Email" id="Email">
	</div>
<div class="col-md-6">
    <label for="MONO"><b>Mobile number :</b></label>
    <input type="text"  class="form-group" placeholder="Enter Number" name="Mobile" id="Mobile">
	<br>
    <label for="pin"><b>Pincode : </b></label>
    <input type="pin"  class="form-group" placeholder="Pincode" name="Pincode" id="Pincode">
	
    <label for="City"><b>City :</b></label>
    <input type="CITY"  class="form-controls " placeholder="City name" name="City" id="City">
	<br>
    <button type="submit" name="submit" class="registerbtn">Submit</button>
  </div>
  </div>
  </div>
  </div>
</form>
</body>
</html>
<?php

include'connection.php';
if(isset($_POST['submit'])){
   echo("Data Submited");
 
   $Name=$_POST['Name'];
   $Address=$_POST['Address'];
   $Mobile=$_POST['Mobile'];
   $Email=$_POST['Email'];
   $Pincode=$_POST['Pincode'];
   $City=$_POST['City'];
 

//$sql= "INSERT INTO `registration form` (`Name`, `Address`, `Mobile number`, `Email`, `Pincode`,'City') VALUES ('$Name', '$Address', '$Mobile number', '$Email', '$Pincode','$City')";

$sql= "INSERT INTO `login` (`Name`, `Address`, `Email`, `Mobile`, `Pincode`, `City`) VALUES ('$Name', '$Address', '$Email', '$Mobile', '$Pincode', '$City')";

 //echo "$sql";

 if (mysqli_query($conn,$sql))
{
  echo "Sucessfully Inserted";
}
 else
  {
  echo "Insertion Failed".$sql;
 }
 
  mysqli_close($conn);
 }
 ?>
