back-to-top
===========
HTML

<div class="row">
  <div class="span3">
    <a href="#" class="go-top">Go back to top</a>
  </div>
</div>

CSS

.go-top{
  position: fixed;
	bottom: 2em;
	right: 2em;
	text-decoration: none;
	background-color: tomato;
	padding: 1em;
	font-size: 12px;
	color: black;
	font-weight: bold;
	display: none;
}

.go-top:hover{
	background-color: orange;
	text-decoration: none;
}

jQuery

$(document).ready(function(){
        // show or hide sticky button
        $(window).scroll(function(){
            if ($(this).scrollTop() > 200) {
                $('.go-top').fadeIn(200);
            }
            else
            {
                $('.go-top').fadeOut(200);
            }
        });

       $('.go-top').click(function(event){
        event.preventDefault();

        $('html, body').animate({scrollTop: 0}, 300);

       })
       });
