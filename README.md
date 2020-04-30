<!DOCTYPE html> 
<html> 
 
<head> 
 <meta name="viewport" content="width=device-width, initial-scale=1"> 
</head> 
 
<body> 
 
 <h1>Simple Conditions</h1> 
 
 <button onclick="smplechk();">Simple Validate</button> 
 <button onclick="difichk();">Dificult Validate</button> 
 
 <script> 
  //Simple Way 
  function smplechk() 
  { 
   var num = 4; 
 
   if ([1, 2, 3, 4, 5, 6, 7, 8, 9].indexOf(num) != -1) 
   { 
    alert("Hola te invito a registrarte en newsletter:"); 
   } 
  } 
 
  //Bad Way 
  function difichk() 
  { 
   var num = 4; 
 
   if (num == 1 || num == 2 || num == 3 || num == 4 || num == 5 || num == 6 || num == 7 || num == 8 || num == 9) 
   { 
    alert("This is the number"); 
   } 
  } 
 </script> 
 
</body> 
 
</html>
