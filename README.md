# Markdown - Dokumentation - LB3 - ALP - MATAY
## Modul300
**Modul 300:** Plattformübergreifende Dienste in ein Netzwerk integrieren - Docker

**Autor:** Alp Matay

**Datum:** 07.05.2020

## Allgemeines
In meinem Docker-compose file ist ein nginx Webserver ""installiert"".

### LB3-WEB-NGINX
#### Wichtig
>- **Name:** LB3-ALP-M300
>- **Installierte Dienste:** NGINX
>- **Portweitetleitung:** Port 5556

#### Weiteres
> Ich habe eine Startseite selber mit HTML selber geschrieben.   
Es ist etwas einfaches, da man ja auch sehen soll ob der Dienst funktioniert oder nicht. 
#### Vorgehen
> Um die Seite anzeigen zu lassen, habe ich einen Ordner Sync erstellt und im docker-compose file ebenfalls den pfad angepasst.  
Dann hab ich im Sync folder die index.html datei erstellt. 

#### Docker-compose code  
    web:
      image: nginx # Hier wird das File angegben das installiert wird   
      ports: # Hier wird die Portweiterleitung konfiguraiert 
        - 5556:80
      volumes:
        - "./share:/usr/share/nginx/ht  #./Share ist der Ordner wo das index.html file reinkommt.

#### Bild
![ ](./indexseite.jpg "Index Seite")

#### Code
##### HTML
<!DOCTYPE HTML>
<html>
	<head>
		<title>M300-ALP-MATAY</title>
		<meta charset="utf-8" />
		<meta name="viewport" content="width=device-width, initial-scale=1" />
		<link rel="stylesheet" href="assets/css/main.css" />
	</head>
	<body>

		<!-- Header -->
			<header id="header">
				<div class="inner">
					<a href="index.html" class="logo"><strong>M300-ALP-MATAY</strong></a>
					<nav id="nav">
						<a href="index.html">Home</a>
						<a href="generic.html">Allgemein</a>
					</nav>
					<a href="#navPanel" class="navPanelToggle"><span class="fa fa-bars"></span></a>
				</div>
			</header>

		<!-- Banner -->
			<section id="banner">
				<div class="inner">
					<header>
						<h1>Willkommen bei meiner Webseite für das Modul-M300</h1>
					</header>

					

					<div class="flex ">

						<div>
							<span class="icon fa-car"></span>
							<h3>DOCKER</h3>
							<p></p>
						</div>

			

						<div>
							<span class="icon fa-bug"></span>
							<h3>LB3</h3>
							<p></p>
						</div>
					</div>

					<footer>
						<a href="#" class="button">Zur Startseite</a>
					</footer>
				</div>
			</section>


		<!-- Three -->
			<section id="three" class="wrapper align-center">
				<div class="inner">
					<div class="flex flex-2">
						<article>
							<div class="image round">
								<img src="images/pic01.jpg" alt="Pic 01" />
							</div>
							<header>
								<h3>Lorem ipsum<br /> dolor amet nullam</h3>
							</header>
							<p>Morbi in sem quis dui placerat ornare. Pellentesquenisi<br />euismod in, pharetra a, ultricies in diam sed arcu. Cras<br />consequat  egestas augue vulputate.</p>
							<footer>
								<a href="#" class="button">Mehr</a>
							</footer>
						</article>
						<article>
							<div class="image round">
								<img src="images/pic02.jpg" alt="Pic 02" />
							</div>
							<header>
								<h3>Sed feugiat<br /> tempus adipicsing</h3>
							</header>
							<p>Pellentesque fermentum dolor. Aliquam quam lectus<br />facilisis auctor, ultrices ut, elementum vulputate, nunc<br /> blandit ellenste egestagus commodo.</p>
							<footer>
								<a href="#" class="button">Mehr</a>
							</footer>
						</article>
					</div>
				</div>
			</section>

		<!-- Footer -->
			<footer id="footer">
				<div class="inner">

					<h3>Informieren Sie mich</h3>

					<form action="#" method="post">

						<div class="field half first">
							<label for="name">Name</label>
							<input name="name" id="name" type="text" placeholder="Name">
						</div>
						<div class="field half">
							<label for="email">Email</label>
							<input name="email" id="email" type="email" placeholder="Email">
						</div>
						<div class="field">
							<label for="message">Message</label>
							<textarea name="message" id="Nachricht" rows="6" placeholder="Nachricht"></textarea>
						</div>
						<ul class="actions">
							<li><input value="Senden Sie mir eine Nachricht" class="button alt" type="submit"></li>
						</ul>
					</form>

				</div>
			</footer>

		<!-- Scripts -->
			<script src="assets/js/jquery.min.js"></script>
			<script src="assets/js/skel.min.js"></script>
			<script src="assets/js/util.js"></script>
			<script src="assets/js/main.js"></script>

	</body>
</html>
```
