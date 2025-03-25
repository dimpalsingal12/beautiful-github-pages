<!DOCTYPE html>
<html>
<head>
	<title>Sunset Gallery</title>
    <link rel="stylesheet" type="text/css" href="styles.css">

	<style>
		.page {
			display: none;
		}
		.page.active {
			display: block;
		}
	</style>
</head>
<body>
	<h1>Sunset Gallery</h1>
	
	<!-- Page 1 -->
	<div class="page active">
		<h2>SUNSET</h2>
		<img src="c:\Users\Dimpal Singal\AppData\Local\Packages\5319275A.WhatsAppDesktop_cv1g1gvanyjgm\TempState\AF8D9C4E238C63FB074B44EB6AED80AE\WhatsApp Image 2025-03-25 at 07.31.36_8b0d647b.jpg" alt="Sunset over the ocean">
		<p>Sunset over the ocean, captured in Hawaii.</p>
		<img src="https://www.holidify.com/images/cmsuploads/compressed/hgcgc_20181120142913.jpg" alt="Sunset in dwarka">
		<p>Sunset over ocean, taken in dwarka.</p>
		<a href="#" class="next-page">Next Page &raquo;</a>
	</div>
	
	<!-- Page 2 -->
	<div class="page">
		<h2></h2>
		<img src="c:\Users\Dimpal Singal\AppData\Local\Packages\5319275A.WhatsAppDesktop_cv1g1gvanyjgm\TempState\7F278AD602C7F47AA76D1BFC90F20263\WhatsApp Image 2025-03-25 at 07.31.35_6b2fa0f3.jpg" alt="Sunset over the city">
		<p>Sunset over the city, captured in New York.</p>
		<img src="c:\Users\Dimpal Singal\AppData\Local\Packages\5319275A.WhatsAppDesktop_cv1g1gvanyjgm\TempState\6E2D5D50A943A0E0D738377F51011685\WhatsApp Image 2025-03-25 at 07.31.37_2b3e63e2.jpg" alt="Sunset on the beach">
		<p>Sunset on the beach, taken in California.</p>
		<a href="#" class="prev-page">&laquo; Previous Page</a>
		<a href="#" class="next-page">Next Page &raquo;</a>
	</div>
	
	<!-- Page 3 -->
	<div class="page">
		<h2></h2>
		<img src="c:\Users\Dimpal Singal\AppData\Local\Packages\5319275A.WhatsAppDesktop_cv1g1gvanyjgm\TempState\B928FEC5932BF2FDDD2CC88C038B8CCB\WhatsApp Image 2025-03-25 at 07.31.36_570f9cb2.jpg" alt="Sunset in the desert">
		<p>Sunset in the desert, captured in Arizona.</p>
		<a href="#" class="prev-page">&laquo; Previous Page</a>
	</div>
	
	<script>
		const pages = document.querySelectorAll('.page');
		const nextPageLinks = document.querySelectorAll('.next-page'); 
		const prevPageLinks = document.querySelectorAll('.prev-page');
		
		let currentPageIndex = 0;
		
		nextPageLinks.forEach(link => {
			link.addEventListener('click', () => {
				currentPageIndex++;
				updatePage();
			});
		});
		
		prevPageLinks.forEach(link => {
			link.addEventListener('click', () => {
				currentPageIndex--;
				updatePage();
			});
		});
		
		function updatePage() {
			pages.forEach(page => page.classList.remove('active'));
			pages[currentPageIndex].classList.add('active');
		}
	</script>
</body>
</html>

