<script>
	import Nav from '../components/Nav.svelte';

	export let segment;
</script>

<!-- Main wrapper -->
<div class="wrapper" id="wrapper">
	<Nav {segment}/>

	<main>
		<slot></slot>
	</main>

	<footer id="footer" class="footer-area fixed--footer">

		<!-- Footer Widgets -->
		<div class="footer__widgets ptb--100 bg--dark--light">
			<div class="container">
				<div class="row">
					<div class="col-md-12">
						<div class="widgets footer--widgets d-flex justify-content-between flex-md-wrap flex-wrap flex-lg-nowrap">

							<!-- Single Widgets -->
							<div class="single-widget widget--details">
								<div class="logo">
									<a href=".">
										<img src="images/logo/logo-dark.png" alt="footer logo">
									</a>
								</div>
								<p>Pendidikan setingkat SD yang berfokus pada Al Qur’an dan Agama Islam</p>
								<div class="social-icons social-icons--rounded">
									<ul>
										<li class="facebook"><a href="https://www.facebook.com/"><i class="fa fa-facebook"></i></a></li>
										<li class="twitter"><a href="https://twitter.com/"><i class="fa fa-twitter"></i></a></li>
										<li class="instagram"><a href="https://www.instagram.com/"><i class="fa fa-instagram"></i></a></li>
										<li class="google-plus"><a href="https://plus.google.com/"><i class="fa fa-google-plus"></i></a></li>
									</ul>
								</div>
							</div><!-- //Single Widgets -->

							<!-- Single Widgets -->
							<div class="single-widget widget--support">
								<h4 class="widget-title">Navigasi</h4>
								<ul>
									<li><a href=".">Beranda</a></li>
									<li><a href="profile">Profil</a></li>
									<li><a href="informasi/pendaftaran">Informasi</a></li>
									<li><a href="berita-kegiatan">Berita Kegiatan</a></li>
									<li><a href="kontak-kami">Kontak Kami</a></li>
								</ul>
							</div><!-- //Single Widgets -->

							<!-- Single Widgets -->
							<div class="single-widget widget--contact">
								<h4 class="widget-title">Kontak</h4>
								<ul>
									<li>
										Komplek Astek, Jl. Jamsostek No. 76 RT 001/Rw 05, Kel. Lengkong Gudang Timur, Serpong, Tangerang Selatan, Banten 15321
									</li>
									<li>
										<a href="callto://+6285960041425">0859 6004 1425 (Ust. Ari)</a>
									</li>
									<li>
										<a href="mailto://kontak@sekolahquranalihsan.com">kontak@sekolahquranalihsan.com</a>
									</li>
								</ul>
							</div><!-- //Single Widgets -->

							<div class="widget-row">

								<!-- Single Widget -->
								<div class="single-widget widget--newsletter">
									<h4 class="widget-title">Info Terbaru</h4>
									<form action="#">
										<input type="text" placeholder="Masukan email Anda">
										<button type="submit"><i class="fa fa-paper-plane-o"></i></button>
									</form>
								</div><!-- //Single Widget -->

							</div>
						</div>
					</div>
				</div>
			</div>
		</div><!-- //Footer Widgets -->

		<!-- Footer Copyright -->
		<div class="footer__copyright bg--dark ptb--20">
			<div class="container">
				<div class="row">
					<div class="col-lg-12 col-md-12">
						<p>Copyright© Sekolah Quran Al-Ihsan, All rights Reserved, 2019. Created with ♥ by <a href="https://github.com/DevCharity">DevCharity</a></p>
					</div>
				</div>
			</div>
		</div><!-- //Footer Copyright -->

	</footer><!-- //Footer -->
</div>