# Session 7.0 - Advanced SASS features

In this session we'll look at some more advanced features that will assist you greatly when making a responsive grid.



# Maths Operators 

- We can perform mathematical operations in sass 
- It is possible to use mathematical operators such as `+, -, *, /`
- Below is an example of how we'd work out the width of a grid column 

```
$grid_cols : 12;
$max_width : 100%; /* a var for max width */
$col_1_width : $max_width / $grid_cols;

.col-1 {
  width: $col_1_width;
}

.offset-1 {
  margin-left: $col_1_width;	
}

.col-2 {
  width: $col_1_width * 2;
}

.offset-2 {
  margin-left: $col_1_width * 2;	
}

```

# Media Queries 

- Below is an example of a media query that I used to set up a responsive grid

```
@media (min-width:650px){
    [class*='col-']{
        width: 100%;
   }
        
    [class*='offset-']  {
       margin-left: 0%;
   }
    
    .nav{
        display: none;   
    }
    
  h3 {
    
     text-align: center;
  }
}

```

- Sass gives you the choice of nesting a media query within the selector 

```
h3 {
	
	 {
	
		@media all and (min-width:650px) {
		
				 color:green;
	
	}

}

```

- We can tidy up media queries further by using variable


```
/*
  This variable would be in our _varibles.scc folder
*/
$sm: 'min-width: 460px';

h1 {
    
    @media ($sm) {
       color:green;
    }
    
}


```

# Loops (Advanced)


- You would of encountered loops before. The structures in programming that allow us to reuse blocks of code
- A loop can save us a lot of typing, especially when creating responsive grids 
- Here is how we could define our columns for a 16 col grid 

```

$max_width: 100%;
$max_cols: 16;
$single_col: $max_width / $max_cols;


@for $i from 1 through 16 {
    
    /** on the first loop i = 1 and iterates up to 16 
        on each loop 
    ***/
    .col-#{$i} { width: $single_col * $i }
}

```

# Practical

- [Implement your grid using SASS](task.md)
