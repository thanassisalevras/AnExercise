<html>
    <head>
        <title>Reservation</title>
       
    </head>
    <body style="text-align: center">
         <p>Number of kids:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<br />
         <input type="text" onclick="reset()"  id="NumberOfKids"/></p>
         <button type="button"  id="btConfirm" onclick="createFields(), selectAge()">Confirm</button>
         <button type="button" id="btnReset" onclick="reset()">Clear all</button>
         <div id="pane" >
             <p>Age:</p>
             <select id="ageSelect">
                 <option value="0">0</option>
                 <option value="1">1</option>
                 <option value="2">2</option>
                 <option value="3">3</option>
                 <option value="4">4</option>
                 <option value="5">5</option>
                 <option value="6">6</option>
             </select>
         </div>
        <script>
       document.getElementById("NumberOfKids").addEventListener('keyup', createFields);
       document.getElementById("btConfirm").addEventListener('click', createFields);
      
 
    function createFields(){
        
        var entry=parseInt(document.getElementById("NumberOfKids").value);
              if(entry.length===0 || isNaN(entry)){
                   alert("Put a number please");}
               else{
                       for (var i = 0; i < entry; i++) {
                          
             var firstname = document.createTextNode("First Name: ");
             document.getElementById("pane").appendChild(firstname);
             
             var boxFirstName = document.createElement("input");
             document.getElementById("pane").appendChild(boxFirstName);
             
             var lastname = document.createTextNode("Last Name: ");
             document.getElementById("pane").appendChild(lastname);
             
             var boxLastName = document.createElement("input");
             document.getElementById("pane").appendChild(boxLastName);
                               
             var age = document.createTextNode("Age: ");
             document.getElementById("pane").appendChild(age);
              
             var boxAge = document.createElement("select");
             boxAge.setAttribute("id", "ageSelect");
             document.body.appendChild(boxAge);
             

              var ageOption0=document.createElement("option");
              ageOption0.setAttribute("value", "0");
              var ageNum=document.createTextNode("0");
              ageOption0.appendChild(ageNum);
              document.getElementById("ageSelect").appendChild(ageOption0);  
                 
                  var ageOption1 = document.createElement("option");
             ageOption1.setAttribute("value", "1");
             var ageNum = document.createTextNode("1");
             ageOption1.appendChild(ageNum);
             document.getElementById("ageSelect").appendChild(ageOption1);
             
                var ageOption2 = document.createElement("option");
             ageOption2.setAttribute("value", "2");
             var ageNum = document.createTextNode("2");
             ageOption2.appendChild(ageNum);
             document.getElementById("ageSelect").appendChild(ageOption2);
             
                var ageOption3 = document.createElement("option");
             ageOption3.setAttribute("value", "3");
             var ageNum = document.createTextNode("3");
             ageOption3.appendChild(ageNum);
             document.getElementById("ageSelect").appendChild(ageOption3);
             
                var ageOption4 = document.createElement("option");
             ageOption4.setAttribute("value", "4");
             var ageNum = document.createTextNode("4");
             ageOption4.appendChild(ageNum);
             document.getElementById("ageSelect").appendChild(ageOption4);
             
                var ageOption5 = document.createElement("option");
             ageOption5.setAttribute("value", "5");
             var ageNum = document.createTextNode("5");
             ageOption5.appendChild(ageNum);
             document.getElementById("ageSelect").appendChild(ageOption5);
             
                var ageOption6 = document.createElement("option");
             ageOption6.setAttribute("value", "6");
             var ageNum = document.createTextNode("6");
             ageOption6.appendChild(ageNum);
             document.getElementById("ageSelect").appendChild(ageOption6);
             
                
             var br=document.createElement("br");
             document.getElementById("pane").appendChild(br);
          
                    } 
        }
    }
    
   function reset(){
       document.getElementById("NumberOfKids").value="";
       //document.getElementById("pane").innerHTML="";
       var pane = document.getElementById("pane");
       while(pane.firstChild){
           pane.removeChild(pane.firstChild);
       }
       
}      
        </script>
    </body>
</html>
