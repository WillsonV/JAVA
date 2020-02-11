<!DOCTYPE html> 
<html> 

<head> 
	<title> 
		Appending new elements to document body .
	</title> 
	<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.4.1/jquery.min.js"></script>
	<script> 
	// Method 1 
	
	
	// Method 2 
	
var Elements = ["C", "C++", "Java","Python","R","Perl","C#","PHP"];
	
	function AddNewElementsByJquery() { 
									 for (var i=0;i<Elements.length; i++)
									 { 
									  $("#Languages").append('<li>'+Elements[i]+'</li>');  
								   }  
	                           } 
							   
							   
	
     function AddElementsByPureJs()
                         {
						     var fragment = document.createDocumentFragment();
                             for (var i=0;i<Elements.length; i++) 
							 {
							
							var e = document.createElement("li");
							e.innerHTML = Elements[i];
							fragment.appendChild(e);
                            }

                            var x= document.getElementById('Languages');
			                x.appendChild(fragment);


						 }	 
							   
	 function AddNewElementUsingString()
              {
			   var NodesString="";
			  
			   for (var i=0;i<Elements.length; i++) 
							 {
				
							 NodesString+="<li>"+Elements[i]+"</li>";

                            }
							
				 var UlElement= document.getElementById('Languages');
			             	
			    $("#Languages").append(NodesString);	
			   
						   
			  
			  
			  }	 
							   
							   
							   
							   
							   
							   
	</script> 
	
	
	
</head> 

<body> 
<button onclick="AddNewElementsByJquery()">AppendElements</button>
<button onclick="AddElementsByPureJs()">AppendElements By JS</button>
<button onclick="AddNewElementUsingString()">AppendElements Using String</button>
	<div id="LanguagesDiv">
       <ul id="Languages">
          <li>JavaScript</li>
       </ul>
    </div> 
</body> 

</html>				 
