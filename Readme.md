## A responsive side menu for mobile devices

A simple responsive side drawer style menu for mobile devices. No additonal styles, you are free to customize it for your project.

### How to use

1. Set the meta tag

		<meta name="viewport" content="width=device-width, initial-scale=1.0">
		
2. Add your markup
		
		<!-- Container -->
  		<div class="container">
    
    		<!-- Open Menu Button -->
	    	<button class="js--open-menu">Open Menu</button>
	    	<!-- / Open Menu Button -->
    	 
		    <!-- Navigation -->    		
    		<nav class="menu">
		        <ul>
        		  <li><a href="#">Home</a></li>
		          <li><a href="#">Get started</a></li>
        		  <li><a href="#">Scaffolding</a></li>
		          <li><a href="#">Base CSS</a></li>
        		  <li><a href="#">Components</a></li>
		          <li><a href="#">JavaScript</a></li>
        		</ul>
		    </nav>
		    <!-- / Navigation -->
		    
		</div>
		<!-- / Container -->
		
3. Add Styles: Open up css/sidemenu.css
		
		/* Sidemenu Styles */

		.menu{
		  bottom: 0;
		  left: -70%;
		  position: absolute;
		  top: 0 ;
		  width: 70%;
		}

		/* Toggled Menu */

		.container{
			-webkit-transition: all 0.25s ease;
			-moz-transition: all 0.25s ease;
			-ms-transition: all 0.25s ease;
			transition: all 0.25s ease 0s;
		}

		.menu--opened .container{
			-webkit-transform: translate3d(70%, 0, 0);
			-moz-transform: translate3d(70%, 0, 0);
			-ms-transform: translate3d(70%, 0, 0);
			transform: translate3d(70%, 0, 0);
		}

		.menu--opened{
			overflow-x: hidden;
		}

4. Add 'click' Event Listener to the button

		<script>
	    
	    document.querySelector('.js--open-menu')
	      .addEventListener('click', function(e){
	        document.body.classList.toggle('menu--opened');
	        e.preventDefault();
	    });
	    
	  </script>
