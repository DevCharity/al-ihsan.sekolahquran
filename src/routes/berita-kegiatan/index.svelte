<script context="module">
	export function preload({ params, query }) {
		return this.fetch(`berita-kegiatan.json`).then(r => r.json()).then(posts => {
			return { posts };
		});
	}
</script>

<script>
	export let posts;
</script>

<div class="events-grid ptb--150 bg--white">
	<div class="container">
		<div class="row">
			<div class="col-lg-12">
				<div class="events2">
					{#each posts as post}					
					<!-- Event Single -->
					<article class="event-single wow fadeInRight">
						<div class="event-single__thumb">
							<a rel='prefetch' href='berita-kegiatan/{post.slug}'>
								<img src="images/event/layout-2/2.jpg" alt="event thumb">
							</a>
							<div class="event-single__date">
								<h3>{post.published}</h3>
							</div>
						</div>
						<div class="event-single__content">
							<h3><a rel='prefetch' href='berita-kegiatan/{post.slug}'>{post.title}</a></h3>
							<p>{post.excerpt}</p>
							<div class="event-single__content__location">
								<p><i class="icofont icofont-location-pin"></i>{post.event_location}</p>
								<p><i class="icofont icofont-calendar"></i>{post.event_date}</p>
							</div>
						</div>
					</article><!-- //Event Single -->
					{/each}
				</div>
			</div>
		</div>
	</div>
</div>