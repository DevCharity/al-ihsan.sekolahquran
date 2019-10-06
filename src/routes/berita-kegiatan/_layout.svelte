<script>
    export let segment;
    
    function titleCase(str) {
		if (str != null) {
			var removeDash = str.replace(/-/g, ' ');
			var splitStr = removeDash.toLowerCase().split(' ');
			for (var i = 0; i < splitStr.length; i++) {
				splitStr[i] = splitStr[i].charAt(0).toUpperCase() + splitStr[i].substring(1);     
			}

			return splitStr.join(' '); 
		} else return 'Berita Kegiatan';
    }
</script>

<svelte:head>
	<title>{titleCase(segment)} - Sekolah Quran Al-Ihsan</title>
</svelte:head>

<!-- Breadcrumb area -->
<section class="cr-section breadcrumb-area" data-black-overlay="7">
	<div class="container">
		<div class="row">
			<div class="col-lg-12 text-center">
				<div class="cr-breadcrumb text-center">
					<h2 class="cr-breadcrumb__title">{titleCase(segment)}</h2>
					<div class="cr-breadcrumb__tree text-left text-md-left text-center">
						<ul>
							<li><a href=".">Beranda</a></li>
							{#if segment != null}
							<li><a href="berita-kegiatan">Berita Kegiatan</a></li>
							{/if}
							<li>{titleCase(segment)}</li>
						</ul>
					</div>
				</div>
			</div>
		</div>
	</div>
</section><!-- //Breadcrumb area -->


<!-- Page Conent -->
<main class="page-content">
	<slot></slot>
</main>