<script>
	export let segment;
</script>

<!-- <nav>
	<ul>
		<li><a class='{segment === undefined ? "selected" : ""}' href='.'>Beranda</a></li>
		<li><a class='{segment === "about" ? "selected" : ""}' href='about'>Profil</a></li>

		<!-- for the blog link, we're using rel=prefetch so that Sapper prefetches
		     the blog data when we hover over the link or tap it on a touchscreen -->
		<!-- <li><a rel=prefetch class='{segment === "information" ? "selected" : ""}' href='information'>Informasi</a></li> -->
	<!-- </ul> -->
<!-- </nav> -->

<!-- Header -->
<header id="header-area" class="header-area sticky--header">
	<div class="header header--style-2">
		<!-- Header Top Area <-->
		<div class="header__top bg--white">
			<div class="container">
				<div class="header__top__inner">
					<div class="logo image--logo hidden-md hidden-sm hidden-xs">
						<a href="."><img src="images/logo/logo-theme.png" alt="header logo"></a>
					</div>
					<div class="header__right">
						<div class="header__right__top d-flex justify-content-end align-items-center flex-wrap flex-sm-nowrap">
							<ul class="header__right__times d-flex justify-content-end" >
								<li><p><i class="icofont icofont-full-sunny"></i>SUNRISE : [04:30]</p></li>
								<li><p><i class="icofont icofont-full-night"></i>SUNSET : [17:51]</p></li>
							</ul>
							<ul class="header__right__icons d-flex justify-content-end">
								<li class="minicart-trigger"><a href="#"><i class="fa fa-opencart"></i><span class="cart-counter">2</span></a></li>
								<li class="accountbox-trigger"><a href="#"><i class="fa fa-user-o"></i></a></li>
							</ul>
						</div>
					</div>
				</div>
			</div>
		</div><!-- //Header Top Area -->
		
		<!-- Header Bottom Area -->
		<div class="header__bottom bg--theme">
			<div class="container">
				<div class="row">
					<div class="col-lg-12">
						<!-- Main naviagtion -->
						<nav class="menu">
							<ul class="justify-content-center">
								<li><a href=".">Beranda</a></li>
								<li><a href="profil">Profil</a></li>
								<li class="cr-dropdown"><a href="informasi/pendaftaran">Informasi</a>
									<ul class="cr-dropdown-menu">
										<li><a href="informasi/pendaftaran">Pendaftaran</a></li>
										<li><a href="informasi/rincian-biaya">Rincian Biaya</a></li>
										<li><a href="informasi/kurikulum">Kurikulum</a></li>
										<li><a href="informasi/jadwal-sekolah">Jadwal Sekolah</a></li>
										<li><a href="informasi/berita-kegiatan">Berita Kegiatan</a></li>
										<li><a href="informasi/galeri">Galeri</a></li>
										<li><a href="informasi/afiliasi">Afiliasi</a></li>
										<li><a href="informasi/infaq">Infaq</a></li>
									</ul>
								</li>
								<li><a href="kontak-kami">Kontak Kami</a></li>
							</ul>
						</nav><!-- //Main naviagtion -->

						<!-- Mobile Menu -->
						<div class="mobile-menu hidden-lg hidden-xlg hidden-xx hidden-sp">
							<a class="mobile-logo" href="."><img src="images/logo/logo-theme.png" alt="logo"></a>
						</div><!-- //Mobile Menu -->
					</div>
				</div>
			</div>
		</div>
		<!-- //Header Bottom Area -->
	</div>
</header><!-- //Header -->