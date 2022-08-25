*Information sources* 

1. Company subdomains 
2. Websites 
3. Public IP addresses (including the one on the cloud AWS/Azure) 
4. Leaked internal IP addresses Public DNS records (MX mail records, etc.)
5.  Leaked credentials (mainly on GitHub or Pastebin) 
6. Previous breaches 
7. Significant business change (e.g., acquisitions) 
8. Business financial information (this can reveal a secret partner) 
9. Business phone numbers (for social engineering) 
10. Employee public information (for social engineering) 
11. A company presence on social media (e.g., LinkedIn)


*Internet Search Engines*

Shodan is a great online tool that will scan the internet for you. There are limitless options that you can use on this monster. Here's a quick example: let's say you want to find Docker engines that are visible on the internet and listening on port 2375 (the default port number for a Docker daemon).  I used the following query: port:2375 product: "Docker"
<div class="rich-link-card-container"><a class="rich-link-card" href="https://www.shodan.io/" target="_blank">
	<div class="rich-link-image-container">
		<div class="rich-link-image" style="background-image: url('https://www.shodan.io/static/img/opengraph.png')">
	</div>
	</div>
	<div class="rich-link-card-text">
		<h1 class="rich-link-card-title">Shodan</h1>
		<p class="rich-link-card-description">
		Search engine of Internet-connected devices. Create a free account to get started.
		</p>
		<p class="rich-link-href">
		https://www.shodan.io/
		</p>
	</div>
</a></div>


<div class="rich-link-card-container"><a class="rich-link-card" href="https://duckduckgo.com/" target="_blank">
	<div class="rich-link-image-container">
		<div class="rich-link-image" style="background-image: url('https://duckduckgo.com/assets/logo_social-media.png')">
	</div>
	</div>
	<div class="rich-link-card-text">
		<h1 class="rich-link-card-title">DuckDuckGo — Privacy, simplified.</h1>
		<p class="rich-link-card-description">
		The Internet privacy company that empowers you to seamlessly take control of your personal information online, without any tradeoffs.
		</p>
		<p class="rich-link-href">
		https://duckduckgo.com/
		</p>
	</div>
</a></div>


<div class="rich-link-card-container"><a class="rich-link-card" href="https://www.google.com" target="_blank">
	<div class="rich-link-image-container">
		<div class="rich-link-image" style="background-image: url('https://www.google.com/favicon.ico')">
	</div>
	</div>
	<div class="rich-link-card-text">
		<h1 class="rich-link-card-title">Google</h1>
		<p class="rich-link-card-description">
		
		</p>
		<p class="rich-link-href">
		https://www.google.com
		</p>
	</div>
</a></div>

google dorking cheet sheet

<div class="rich-link-card-container"><a class="rich-link-card" href="https://gist.github.com/sundowndev/283efaddbcf896ab405488330d1bbc06" target="_blank">
	<div class="rich-link-image-container">
		<div class="rich-link-image" style="background-image: url('/render?uri=https%3A%2F%2Fgist.github.com%2Fsundowndev%2F283efaddbcf896ab405488330d1bbc06')">
	</div>
	</div>
	<div class="rich-link-card-text">
		<h1 class="rich-link-card-title">Google dork cheatsheet</h1>
		<p class="rich-link-card-description">
		Google dork cheatsheet · GitHub
		</p>
		<p class="rich-link-href">
		https://gist.github.com/sundowndev/283efaddbcf896ab405488330d1bbc06
		</p>
	</div>
</a></div>

<div class="rich-link-card-container"><a class="rich-link-card" href="https://hackr.io/blog/google-dorks-cheat-sheet" target="_blank">
	<div class="rich-link-image-container">
		<div class="rich-link-image" style="background-image: url('https://hackr.io/blog/google-dorks-cheat-sheet/thumbnail/large')">
	</div>
	</div>
	<div class="rich-link-card-text">
		<h1 class="rich-link-card-title">Google Dorks Cheat Sheet 2022 [Free PDF]</h1>
		<p class="rich-link-card-description">
		This Google Dorks cheat sheet covers everything you need to know about how to use the Google hacking technique to reach hidden search results and data.
		</p>
		<p class="rich-link-href">
		https://hackr.io/blog/google-dorks-cheat-sheet
		</p>
	</div>
</a></div>
exploit db google hacking database
https://www.exploit-db.com/google-hacking-database


<div class="rich-link-card-container"><a class="rich-link-card" href="https://pimeyes.com/en " target="_blank">
	<div class="rich-link-image-container">
		<div class="rich-link-image" style="background-image: url('https://pimeyes.com/files/images/for_individuals_white.png')">
	</div>
	</div>
	<div class="rich-link-card-text">
		<h1 class="rich-link-card-title">PimEyes: Face Recognition Search Engine and Reverse Image Search |</h1>
		<p class="rich-link-card-description">
		PimEyes is an advanced face recognition search engine, a reverse image search tool, and a photo search mechanism used to find out where your face appears online.
		</p>
		<p class="rich-link-href">
		https://pimeyes.com/en 
		</p>
	</div>
</a></div>



*Information gathering on kali*
tools:
1. whois - domain name info
2. theHarvester -> email and account finding ->theHarvester -d ethicalhackingblog.com -b all -s
3. ![[Pasted image 20220715133709.png]]
4. DMitry
5. ![[Pasted image 20220715133736.png]]
6. Maltego- all in one tool
7. 