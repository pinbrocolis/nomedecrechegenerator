# nomedecrechegenerator
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.1//EN" 
        "http://www.w3.org/TR/xhtml11/DTD/xhtml11.dtd">	
<html xmlns="http://www.w3.org/1999/xhtml" xml:lang="en" lang="en">
<head>
	<meta http-equiv="Content-Type" content="text/html; charset=utf-8" />
	<title>Name Generator Script Demo</title>
	<meta name="description" content="A do it yourself name generator from online-generators.com" />
	
	
	
	<!-- The Generator script. You can move the script to an external file for better overview -->
	<script type="text/javascript">	
	/*  Online Name Generators v.1.0 script is  made by Niels Gamborg webmaster at online-generator.com.  
	*    The script is  free (as in "free speech" and also as in "free beer") in anyway. Use it after you own likings.
	*    Peace and love. :)
	*/	
		function generator(){
			// Add your own words to the wordlist. Be carefull to obey the showed syntax
			
			var wordlist1 = ["pedacinho","cantinho","Reino","reininho","casinha","cheirinho","circo","pingo","moleque","molequinho","pinguinho"];
			
			var wordlist2 = ["de gente","do céu","dos baixinho","do pitoco","doce mel","pequeno mundo","de flor","da folia","seis moranguinho","chameguinho","do puff","dengoso"]
			
			// Random numbers are made 
			var randomNumber1 = parseInt(Math.random() * wordlist1.length);
			var randomNumber2 = parseInt(Math.random() * wordlist2.length);
			var name = wordlist1[randomNumber1] + " " + wordlist2[randomNumber2];			
			
			//alert(name); //Remove first to slashes to alert the name
			
			//If there's already a name it is removed  
			if(document.getElementById("result")){
				document.getElementById("placeholder").removeChild(document.getElementById("result"));
			}
			// A div element is created to show the generated name. The Name is added as a textnode. Textnode is added to the placeholder.
			var element = document.createElement("div");
			element.setAttribute("id", "result");
			element.appendChild(document.createTextNode(name));
			document.getElementById("placeholder").appendChild(element);
		}		
	</script>
	
	
	
	<!-- Stylesheet. Change styles here. You can move the stylesheet to a extern file for better overview -->
	<style type="text/css">
		body{font-family: arial, serif;}
		#wrapper{border-left:1px solid #cccccc;border-right:1px solid #cccccc;margin:0 auto;padding: 0 20px;width: 700px}
		#generator{background:#e9f3f6;border:1px solid #cccccc;margin:30px 0;font-size:28px;font-weight:bold;padding:50px 0 20px;text-align:center;-moz-border-radius: 5px;-webkit-border-radius: 5px;}
		#generator input{font-size:16px;font-weight:normal;margin-top: 30px}
		#footer{font-size: 10px; color: #999; margin: 30px 0 0 0;}
		#footer a{color:#999}
	</style>
	
	
</head>
<body onload="generator()">
	<div id="wrapper">
		
		<!-- Change the text to your needs -->
		<h1>Name generator script demo</h1>
		<p>This is a do-it-yourself name generator. You just need to adjust the name lists and the text.
		</p>
		<p>		
		And voila! You have got your own brand new and personal name generator.</p>
		<p>Good luck with your project. :)</p>
		
		<!-- The generator result and button. Change text on the button by changing button value. Be carefull changing ID's in this part -->
		<div id="generator" >
			<div id="placeholder"></div>
			<input type="button" value="Make name" onclick="generator()" />		
		</div>
		
		<!--  Change the text to your needs -->
		<p>Download the <a href="http://name-generators.com/download/name-generator-script.zip">name-generator-script.zip</a> 
		or: Right click this page. Select view source.  Copy the source to a text-editor.
		Save is at generator.html.</p>
		
		<p>To edit this page open it with a text editor with syntax highlighting. I'll recommend 
		<a href="http://notepad-plus.sourceforge.net/">notepadd++</a> a free, fast and flexible text editor.</p>
		
		<p>Need help? You can ask questions to the script at my blog: 
		<a href="http://www.name-generators.com/name-generators/name-generator-script.htm">Name generator script</a>. 
		I'll try my best to help you.</p>
		
		<p>If you make a cool name generator, write me a line, and I might make a review of it for you. </p> 
		
		<p>If all this has been any help to you, please leave a link back to my site. :)</p>
		
		<!-- The footer. Place any contact info ect here.-->
		<div id="footer">
		<p>This generator is developed with help from the <a href="http://online-generator.com">online name generators</a>.
		</p>
		</div>
	</div>
</body>
</html>
