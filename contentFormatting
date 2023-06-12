function changeColor() {
    const doc = DocumentApp.openById("1-NPmx6YSjnpuXA3nMsQ4gcFLBoXYrnKMo2DGzbp_S7U"); //Provide the ID from the URL of your Google Doc.
    var body = doc.getBody();
    console.log(body.getAttributes())
    //------------------------ Change these variables --------------------------
    //Change the HEXCODE to the color you would like for the font color.
    var bgcolor = '#f9f2f4';

  var text = body.editAsText();
  var count = 0;
  for (var i = 0; i < text.getText().length; i++){
     //console.log(text.getBackgroundColor(i));
    if (text.getBackgroundColor(i) == bgcolor){
        if (count == 0){
        console.log(text.getText()[i]);
        text.insertText(i,"`");
        count++;
        i++;
        }
        
        //text.setBackgroundColor(i, i, "#000000");
    }
    else{
        //text.r;

        count = 0;
        if(i>0){
            if (text.getBackgroundColor(i-1) == bgcolor){
            text.insertText(i,"`");
            i++;
        }
        }
        
        
    }
   
    
}   
 
}



function changeBold (){
    const doc = DocumentApp.openById("1JBlJo1_vhZHE3q9VgAdYV_iNGgGBepOTAl78beRY7ik");
      var body = doc.getBody();
      console.log(body.getAttributes());
      var count = 0;
      var text = body.editAsText();
      const style = {}
      style[DocumentApp.Attribute.BOLD]=false
       for (var i = 0; i < text.getText().length; i++){
         if(text.isBold(i) && text.getText()[i] != "\n"){
            if (count == 0){
          console.log(text.getText()[i]);
          text.insertText(i,"**");
          count++;
          i = i+2;
         }
         }
         else{
          //text.r;
  
          count = 0;
          if(i>0){
              if (text.isBold(i-1)){
                if(text.getText()[i] == "\n"){
                    text.insertText(i,"**");
                    text.setAttributes(i+2,i+2,style)
                }
                else{
                    text.insertText(i,"**");
                }
                  
              i = i+2;
          }
          }
          
          
      } 
       }
  }
  



