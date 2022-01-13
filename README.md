# Web Page for Mathematical Calculations

## AIM:

To design a static website with validation to perform mathematical calculations in client side.

## DESIGN STEPS:

### Step 1:

Requirement collection.

### Step 2:

Creating the layout using HTML and CSS.

### Step 3:

Write javascript to perform the calculations.

### Step 4:

Include regularexpression based input validation.

### Step 5:

Validate the layout in various browsers.

### Step 6:

Validate the HTML code.

### Step 6:

Publish the website in the given URL.

## PROGRAM :

### Index.html:
~~~
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mathematical Calculations</title>
    <link rel="stylesheet" href="./css/layout.css" />
</head>
<body>
  <h1>MATHEMATICAL CALCULATIONS</h1>
    <div class="container">
        <div class="content">
            <h1 class="text">VOLUME OF CONE</h1>
            <form>
                <div class="formelement"><label for="lenEdit">Length:</label>
                    <input type="text" id="lenEdit" value="0"/>
                    <lable for="lenEdit">Meter</lable>
                </div>
                <br>
                <div class="formelement">
                    <label for="bEdit">Radius:</label>
                    <input type="text" id="bEdit" value="0"/>
                    <lable for="bEdit">Meter</lable>
                </div>
                <br>
                <div class="formelement"><label for="hEdit">Height:</label>
                  <input type="text" id="hEdit" value="0"/>
                  <lable for="hEdit">Meter</lable>
              </div>
              <br>
                <div class="formelement">
                    <input type="button" value="Calculate" id="areaButton"/>
                </div>
                <br>
                <div class="formelement">
                    <label for="areaEdit">Volume:</label>
                    <input type="text" id="vEdit" value="0" readonly />
                    <label for="areaEdit">Meter<sup>3</sup></label>
                </div>
                <br><br>
                <hr size="20" color="greenyellow"> 
                <div class="body"></div>
                <div class="container">
                    <div class="content">
                        <h1>AREA OF CYLINDER</h1>
                        <form>
                            <div class=formelement>
                                <lable for="aedit">Height:</lable>
                                <input type="text" id="aedit" value="0"/>
                                <lable for="aedit">Meter</lable>
                            </div><br>
                            <div class=formelement>
                                <lable for="bedit">Radius:</lable>
                                <input type="text" id="bedit" value="0"/>
                                <lable for="bedit">Meter</lable>
                            </div><br>
                            <div class=formelement>
                                <input type="button" value="Calculate" id="addbutton"/>
                            </div><br>
                            <div class=formelement>
                                <lable for="vedit">Area:</lable>
                                <input type="text" id="vedit" value="0" readonly="0"/>
                                <lable for="vedit">Meter<sup>2</sup></lable>
                            </div>
                            
                        </form>
                    </div>
                </div>
            </form>
        </div>
    </div>
        </div>
    </div>
    <script type="text/javascript">
        var button;
        button = document.querySelector("#areaButton");
        button.addEventListener("click",function(){
            var len,b,h,v;
            var lenVal,bVal,hVal,vVal;
            var lenEdit,reg,res;
            len = document.querySelector("#lenEdit");
            b = document.querySelector("#bEdit");
            h= document.querySelector("#hEdit");
            v=document.querySelector("#vEdit");
            lenval = len.value;
            bval = b.value;
            hval = h.value;
            reg = new RegExp("^[.]?[0-9]+[.]?[0-9]*$");
            res1 = len.value.match(reg);
            res2 = b.value.match(reg);
            res3 = h.value.match(reg);
            if(res1==null)
            {
                alert("Please Enter a valid Value in 'Radius (R)' ");
            }else if(res2==null) {
              alert("Invalid Breadth value!")

            }else if(res3==null){
              alert("Invalid Height value!")
            }else{
              v.value = 1/3*22/7*bval*bval*hval;
            }
        });

        var button;
     
    button=document.querySelector("#addbutton");
    button.addEventListener("click",function(){
        
        var atext,btext,ctext;
        var aval,bval,cval
        var sum2
            var aedit,reg,res;
            sum2=document.querySelector("#aedit");
            aedit = sum2.value;
            reg = new RegExp("^[.]?[0-9]+[.]?[0-9]*$");
            res = aedit.match(reg);
            if(res==null)
            {
                alert("Please Enter a valid Value in 'Length (l)' ");
            }
            
            var sum3
            var bedit,reg,res;
            sum3=document.querySelector("#bedit");
            bedit = sum3.value;
            reg = new RegExp("^[1-9]+[0-9]*$");
            res = bedit.match(reg);
            if(res==null)
            {
                alert("Please Enter a valid Value in 'Width (w)' ");
            }
           
        atext=document.querySelector("#aedit");
        btext=document.querySelector("#bedit");
        ctext=document.querySelector("#cedit");

        aval=parseInt(atext.value);
        bval=parseInt(btext.value);
        cval=2*22/7*bval*(bval+aval);
        ctext.value=""+cval;

    });

    </script>
    <div class="footer">
      Developed by Deepika Ravikumar.
    </div>
</body>
</html>
~~~

### CSS:
~~~
* {
    box-sizing: border-box;
    font-family: Arial, Helvetica, sans-serif;
  }
  body {
    background-color: greenyellow;
  }
  .container {
    width: 1080px;
    padding-bottom: 100px;
    margin-left: auto;
    margin-right: auto;
  }
  .content {
    display: block;
    width: 100%;
    background-color: white;
    min-height: 300px;
    margin-top: 10px;
  }
  h1{
      text-align: center;
      padding-top: 50px;
      color: black;
  }
  .formelement{
      text-align: center;
      font-size:xx-large;
      margin-top: 5px;
      margin-bottom: 5px;
  }
    
    .footer {
        display: block;
        width: 100%;
        height: 40px;
        background-color: white;
        text-align: center;
        padding-top: 10px;
        margin: 0px 0px 0px 0px;
        color: black;
    }
~~~

## OUTPUT:

![Output](./output.png)

## Result:

Thus a website is designed to perform mathematical calculations in the client side.
