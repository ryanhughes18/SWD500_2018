#Session 4 Notes 


##Lesson plan 


####0-5 mins chrome web developer tools tools

Introduce the chrome web developer tool kit, in particular the inspect element feature. It also allows us to look at other websites and get style ideas. The ability tweak our own styles in realtime is probably the most utilised feature. 

###5-10 mins css review (slide 1-6)
Cover: 
   
* External style sheets and how to link them    
* Styling elements directly   e.g. `h { text-align : center; }`
* Styling classes 
* Styling id's


###10-15 Mins Pseudo-elements  DEMO1 (slide 7, 8 and 9)

* Can be used for general elements `p:first-line`, `p:first-letter`, `h1:after`, `h1:before`
* Most commonly used for links, really helps with usability of the site.
		
		a:link {
		    color: #FF0000;
		}
		
		/* visited link */
		a:visited {
		    color: #00FF00;
		}
		
		/* mouse over link */
		a:hover {
		    color: #FF00FF;
		}
		
		/* selected link */
		a:active {
		    color: #0000FF;
		    
		}`
	
###15-20 mins Inline to block DEMO2  (slide 12) 

**Key points**

* Inline elements can be changed to block elements, this is common with images.  Saves putting them in a needless block tag. 
* Show `float:left` , `float:right` but no centre!!!!   
* How to align a block element to the centre using `margin: 0 auto`.  
	


####25-35 mins Box model DEMO3  (slide 13, 14, 15, 16, 17) 

Introduce the idea of the box model using DEMO1. 
**Key points**

* State that we'll mostly use `px` and `%` to assign sizes, however there are other units. 
* Use `px` for the demo and measure the box using a rule tool or google developer tools. **I need them to understand that padding is added to the width/height of the element**. 
	 
**Demo css**

    .box {
    /* STEP1 set up a basic box  discuss about setting width and height as per the slides*/
    /* Note, the box is not flush against the side - the browser default assign styles*/ 
    /* box is 500px x 500px */
    
    width: 500px;
    height: 500px;
    background-color: black;
    color: red;
    
    /* STEP2 add some padding */
    /* box is now (500px + 50px + 50px) x (500px + 50px +50px) = 600px x 600px
    
    padding-left: 50px;
    padding-right: 50px;
    padding-bottom: 50px;
    padding-top: 50px; 
    
    Transition to shorthand 
    
    padding : 50px 50px 50px 50px;    
    */
    
    padding: 50px;
    
    /* STEP3 add a border */
    /* box is now  (600px + 50px +50px) x  (600px + 50px +50px)  = 700px
    border: 50px solid green;
    
	

###35-40 mins simple 2 col layout using floats DEMO4
Use the below skeleton and style it up for the students. Demo how the site resizes based on window/devices.    
 
    <body>    
        <div id="wrapper">    
               <div id="left-nav">
                   <!-- we use # as placeholders, we'll make the other pages later -->
                   <ul>
                        <li> <a href="#">Home</a> </li>
                        <li> <a href="#">About</a> </li>
                        <li> <a href="#">Contact</a></li>	ontact</a></li>
                   
                   </ul>
                   
               </div> <!--[END]#left-nav -->
               <div class="section">
                        <p> 
                            Here's our content for the page, Notice that section is a class.
                            A page can have multiple sections's
                        </p>
               </div> <!--[END].section -->
        </div> <!--[END]#wrapper -->        
    </body>
    
</html> 

**css**
   			
	#wrapper{ 
	    /** just so we can see the elements */
	    border: 1px solid green;
	    
	}
	
	#left-nav{
	    border: 1px solid red;  
	}
	
	.section {  
	  border: 1px solid orange;        
	}

 **after**   
 
	#wrapper{ 
	background: b
	border: 1px solid #00ff00;
	width: 80%;
	margin: 0 auto;
	}
		
	#left-nav{
	border: 1px solid  #ff0000;
	float: left;
	width: 18%;
	min-height: 100%;
	}
		
	.section {  
	  border: 1px solid #ffa500;    
	  float: right; /* also try using float left, it has a similar effect */   
	  width: 80%;   /* however the div will be flush with #left-nav 
	                /* it will go as far left as possible. */    
	}
	
###40  MIN +++ Task

Get the students to kick of the task on myCourse. Ensure that everyones learning log is now in HTML if you get a chance. 

		   
	
	
	










