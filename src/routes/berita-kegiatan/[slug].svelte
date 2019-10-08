<script context="module">
	export async function preload({ params, query }) {
		// the `slug` parameter is available because
		// this file is called [slug].svelte
		const res = await this.fetch(`berita-kegiatan/${params.slug}.json`);
		const data = await res.json();

		if (res.status === 200) {
			return { post: data };
		} else {
			this.error(res.status, data.message);
		}
	}
</script>

<script>
	export let post;
</script>

<section class="cr-section about-area ptb--150 bg--white flower--left-top flower--right-bottom">
	<div class="container">
		<div class="row">
			<div class="col-lg-8 col-xl-9">
				<div class="event-details">
					<div class="event-details__thumb">
						<img src="images/event/single-event/1.jpg" alt="Single event Details">	
					</div>
					<h2 class="event-details__title">{post.title}</h2>
					<div class="event-details__meta">
						<ul>
							<li><span>Tanggal:</span> {post.event_date}</li>
							<li><span>Tempat :</span> {post.event_location}</li>
						</ul>
					</div>
					<div class="event-details__content">
						{@html post.html}
					</div>
				</div>
			</div>

			<!-- Sidebar Widgets Area -->
			<div class="col-lg-4 col-xl-3">
				<!-- Sidebar Widgets -->
				<div class="sidebar widgets">

					<!-- Single Widget (Searchbox) -->
					<div class="single-widget wgt-searchbox">
						<h4 class="widget-title">Cari Berita</h4>
						<form action=".">
							<input type="text" placeholder="Kata kunci...">
							<button type="submit"><i class="fa fa-paper-plane-o"></i></button>
						</form>
					</div><!-- //Single Widget (Searchbox) -->

					<!-- Single Widget (Categories) -->
					<div class="single-widget wgt-categories">
						<h4 class="widget-title">Kategory</h4>
						<ul>
							<li><a href="events.html">Ramadan <span>25</span></a></li>
							<li><a href="events.html">Sholat <span>20</span></a></li>
							<li><a href="events.html">Haji <span>15</span></a></li>
							<li><a href="events.html">Zakat <span>29</span></a></li>
						</ul>
					</div><!-- //Single Widget (Categories) -->

					<!-- Single Widget (Recentpost) -->
					<div class="single-widget wgt-recentpost">
						<h4 class="widget-title">Berita Lainnya</h4>
						<ul>
							<li>
								<div class="wgt-recentpost__thumb">
									<a href=".">
										<img src="images/event/sidebar-event/1.png" alt="event thumb">
									</a>
								</div>
								<div class="wgt-recentpost__content">
									<h5><a href=".">Al-Quran Learning</a></h5>
									<p><span>Central Mosque, NY city</span><span>12 October, 2017</span></p>
								</div>
							</li>
							<li>
								<div class="wgt-recentpost__thumb">
									<a href=".">
										<img src="images/event/sidebar-event/2.png" alt="event thumb">
									</a>
								</div>
								<div class="wgt-recentpost__content">
									<h5><a href=".">Sadaqah Collection</a></h5>
									<p><span>City Center hall, NY city</span><span>10 October, 2017</span></p>
								</div>
							</li>
							<li>
								<div class="wgt-recentpost__thumb">
									<a href=".">
										<img src="images/event/sidebar-event/3.png" alt="event thumb">
									</a>
								</div>
								<div class="wgt-recentpost__content">
									<h5><a href=".">History of Islam</a></h5>
									<p><span>Central Mosque, NY city</span><span>08 October, 2017</span></p>
								</div>
							</li>
						</ul>
					</div><!-- Single Widget (Recentpost) -->
				</div><!-- //Sidebar Widgets  -->
			</div><!-- //Sidebar Widgets Area -->
		</div>
	</div>
</section><!-- //Event Details Area -->
