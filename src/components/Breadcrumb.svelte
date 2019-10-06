<script>
	export let segment;
</script>

<!-- Breadcrumb area -->
<section class="cr-section breadcrumb-area" data-black-overlay="7">
	<div class="container">
		<div class="row">
			<div class="col-lg-12 text-center">
				<div class="cr-breadcrumb text-center">
					<h2 class="cr-breadcrumb__title">{segment}</h2>
					<div class="cr-breadcrumb__tree text-left text-md-left text-center">
						<ul>
							<li><a href=".">Beranda</a></li>
							<li>{segment}</li>
						</ul>
					</div>
				</div>
			</div>
		</div>
	</div>
</section><!-- //Breadcrumb area -->