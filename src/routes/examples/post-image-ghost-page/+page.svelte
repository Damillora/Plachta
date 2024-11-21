<script>
	import PostHeader from '$lib/components/Post/PostHeader.svelte';

	import Post from '$lib/components/PageTypes/Post.svelte';
	import PostMain from '$lib/components/Post/PostMain.svelte';
	import PostNavigator from '$lib/components/Post/PostNavigator.svelte';
	import Container from '$lib/components/Container/Container.svelte';
	import PostRelated from '$lib/components/Post/PostRelated.svelte';
	import PostCard from '$lib/components/PostCard/PostCard.svelte';
	import GhostStyle from '$lib/components/Base/GhostStyle.svelte';
</script>

<Container>
	<Post>
		<PostHeader
			background="https://images.nanao.moe/r/7jETH3.png"
			authors={[
				{
					profile_image: 'https://images.nanao.moe/r/GDuirR.jpg',
					url: 'https://google.com',
					name: 'Sophie Neuenmuller'
				}
			]}
			date="2022 November 2020"
			primary_tag={{
				accent_color: '#3b7b9c',
				name: 'Sound Voltex',
				url: 'https://google.com'
			}}
			reading_time="3 min"
			title="Sophie!"
		/>
		<PostMain>
			<GhostStyle>
				<p>
					Welcome to another new Music Highlights post in a long time! Last time, I talked about
					dead franchises. This time, it's going to be a bit less coherent as I will post about a
					specific selections that I feel like choosing.
				</p>
				<p>
					The songs I've included in this post are quite diverse in nature, thought slightly slanted
					towards electronic music (as that's what I'm most familiar with). One common occurence
					though: they all are songs that I just. can't. stop. repeating.
				</p>
				<h2 id="drum-and-nanakura-rin">Drum and Nanakura Rin</h2>
				<figure class="kg-card kg-embed-card">
					<div class="fluid-width-video-wrapper" style="padding-top: 75%">
						<iframe
							src="https://www.youtube.com/embed/ib6xGN31BjE?feature=oembed"
							frameborder="0"
							allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
							referrerpolicy="strict-origin-when-cross-origin"
							allowfullscreen=""
							title="アドリブ"
						></iframe>
					</div>
				</figure>
				<p>
					An anisong inclusion in Music Highlights! Firstly, I cannot believe that <a
						href="https://anilist.co/anime/163623/Giji-Harem?ref=blog.nanao.moe"
						rel="noreferrer">Pseudo Harem</a
					>, of all things, is what brought me back to watching anime. Well, considering Pseudo
					Harem's simple and sweet premise is what works for me nowadays, it's not that surprising.
					However, what drove me to actually watch it, is because I found about its ending music,
					<strong>Ad-lib</strong>, sung by Nanakura Rin (voiced by Hayami Saori).
				</p>
				<p>
					Ad-lib very much sounds like anisong, but what piqued my interest is the drum and bass DNA
					it has. It is relatively light, but it is incredibly catchy. Furthermore, I did not know I
					like Hayami Saori's vocals this much, and sprinkled with a few Nanakura Rin noises to
					boot, too. Thanks to this banger of a song, Pseudo Harem becomes the first anime I managed
					to finish in a long time! She's way too adorable...
				</p>
				<h2 id="sound-so-crunchy-i-wanna-eat-it">Sound so crunchy I wanna eat it</h2>
				<figure class="kg-card kg-embed-card">
					<div class="fluid-width-video-wrapper" style="padding-top: 56.49999999999999%">
						<iframe
							src="https://www.youtube.com/embed/LN35zu145kI?feature=oembed"
							frameborder="0"
							allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
							referrerpolicy="strict-origin-when-cross-origin"
							allowfullscreen=""
							title="【Original Song】AposTASTY ✍︎ by Runie Ruse"
						></iframe>
					</div>
				</figure>
				<p>
					Next, we have <strong>AposTASTY</strong> from one of Phase Connect's talents, Runie Ruse! I
					was introduced to Phase Connect by a friend of mine, who thinks it is the best thing since
					sliced bread. While their main content is what a VTuber does nowadays, that is, streaming,
					I'm looking closely at their music output. Then, Runie Ruse just straight up delivered a punch
					with her new release.
				</p>
				<p>
					I've tried listening to a few of their talents' music, and the genres they chose are not
					usually what I would choose to listen... this is one of those exceptions. This is probably
					the first UK Hardcore song coming from a Phase Connect talent! (if there's an earlier one,
					hit me up about it, though). My favorite part, however, is around 2:25, where the sound
					design of composer Codly shines through.
				</p>
				<h2 id="the-math-isnt-mathing">The math isn't mathing</h2>
				<figure class="kg-card kg-embed-card">
					<div class="fluid-width-video-wrapper" style="padding-top: 75%">
						<iframe
							src="https://www.youtube.com/embed/4a6oeXjh8-E?feature=oembed"
							frameborder="0"
							allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
							referrerpolicy="strict-origin-when-cross-origin"
							allowfullscreen=""
							title="コントラスト"
						></iframe>
					</div>
				</figure>
				<p>
					Music wise, the Gakuen Idolm@ster series has been surprisingly forward thinking with its
					selection of musicians for the idol songs, and one idol stood out for their music:
					Shinosawa Hiro. Right from her first image song, <a
						href="https://www.youtube.com/watch?v=VJk2etK8I1w&amp;ref=blog.nanao.moe"
						rel="noreferrer">Koukei</a
					>, Hiro has cemented herself as an idol with <em>very</em> imaginative songs. I don't feel
					qualified to write about Koukei, and there's already
					<a
						href="https://rateyourmusic.com/music-review/ocsid/%E5%88%9D%E6%98%9F%E5%AD%A6%E5%9C%92-%E7%AF%A0%E6%BE%A4-%E5%BA%83/%E5%85%89%E6%99%AF-koukei/226538177?ref=blog.nanao.moe"
						rel="noreferrer">a review over at Rate Your Music</a
					>
					that serves that song justice, so I'll talk about her second image song,
					<strong>Contrast</strong>.
				</p>
				<p>
					Contrast's very notable feature is its irregular time signature, reminiscent of math rock
					songs. This kind of song doesn't usually appear in an idol series, let alone a idol <em
						>game</em
					>! Thanks to the irregular time signatures, I don't feel like I was listening to an idol
					song when listening to Contrast, Hiro feels more like an 'artist' rather than an 'idol'.
				</p>
				<h2 id="trinityaile-loves-uk-garage">TRINITYAiLE loves UK garage</h2>
				<figure class="kg-card kg-embed-card">
					<div class="fluid-width-video-wrapper" style="padding-top: 56.49999999999999%">
						<iframe
							src="https://www.youtube.com/embed/AlYxgEcJpxU?feature=oembed"
							frameborder="0"
							allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
							referrerpolicy="strict-origin-when-cross-origin"
							allowfullscreen=""
							title="【MV】Fantastique!  / TRINITYAiLE　作詞：稲葉エミ　作曲・編曲：Tomggg【IDOLY PRIDE/アイプラ】"
						></iframe>
					</div>
				</figure>
				<p>
					TRINITYAiLE has always been one of my favorite units in IDOLY PRIDE, because of their
					specifically electronic music direction (in contrast to TrySail's music!). While in the
					beginning, kz (livetune) handled the music of TRINTIYAiLE, today, that role is now held by
					Tomggg. I find that Tomggg's music for TRINITYAiLE are very stylish, fitting for the dance
					floor, and the latest release, titled <strong>Fantastique!</strong>, is no less stylish.
				</p>
				<p>
					Fantastique! adopts a structure that is pretty much UK Garage, with Tomggg's signature
					'future' sound design. Unlike TRINITYAiLE's previous songs, Fantastique! pretty much keeps
					being garage across the song, making it one of my favorite picks for the dance floor.
				</p>
				<h2 id="fighting-against-a-really-angry-cat">Fighting against a really angry cat</h2>
				<figure class="kg-card kg-embed-card">
					<div class="fluid-width-video-wrapper" style="padding-top: 75%">
						<iframe
							src="https://www.youtube.com/embed/Go-mH5MzThw?feature=oembed"
							frameborder="0"
							allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
							referrerpolicy="strict-origin-when-cross-origin"
							allowfullscreen=""
							title="Challenger"
						></iframe>
					</div>
				</figure>
				<p>
					Finally in the list... is an Arknights soundtrack. This is no usual soundtrack, however. <strong
						>Challenger</strong
					>, a song that serves as the boss battle soundtrack to the Vector Breakthrough event,
					marks the return of Akitaka Toyama (AJURIKA).
				</p>
				<p>
					AJURIKA has previously written the battle soundtrack of Contingency Contract#8 Operation
					Dawnseeker, <a
						href="https://www.youtube.com/watch?v=h_6Qxb0Iiuw&amp;ref=blog.nanao.moe"
						rel="noreferrer">Fading Sky</a
					>, which is a much more frantic drum and bass track. By comparison, Challenger is painted
					in AJURIKA's signature psytrance style. This makes the battle soundtrack feels quite a bit
					more analytical, and honestly this is my new favorite battle music.
				</p>
				<h2 id="closing-thoughts">Closing thoughts</h2>
				<p>
					In the end, the keyword I chose for this selection of music is <em>Sparkling Thoughts</em
					>. The reason is that those are all the songs that I've found out I constantly listen to
					lately! As for Sparkling... the songs are not really that somber to me. Well, the songs in
					this post are not really cohesively picked this time...
				</p>
				<h2>A image test</h2>
				<figure class="kg-card kg-image-card kg-card-hascaption">
					<img
						src="https://blog.nanao.moe/content/images/2021/06/Screenshot_20210624-200658.png"
						class="kg-image"
						alt="Introduction video"
						loading="lazy"
						width="2400"
						height="1080"
						srcset="https://blog.nanao.moe/content/images/size/w300/2021/06/Screenshot_20210624-200658.png 300w, https://blog.nanao.moe/content/images/size/w600/2021/06/Screenshot_20210624-200658.png 600w, https://blog.nanao.moe/content/images/size/w1000/2021/06/Screenshot_20210624-200658.png 1000w, https://blog.nanao.moe/content/images/size/w1500/2021/06/Screenshot_20210624-200658.png 1500w, https://blog.nanao.moe/content/images/size/w2000/2021/06/Screenshot_20210624-200658.png 2000w"
						sizes="(min-width: 768px) 640px, (min-width: 1024px) 768px, 100vw"
					/>
					<figcaption>The introduction is a video.</figcaption>
				</figure>
				<h2>A image text test</h2>
				<p>
					In the end, the keyword I chose for this selection of music is <em>Sparkling Thoughts</em
					>. The reason is that those are all the songs that I've found out I constantly listen to
					lately! As for Sparkling... the songs are not really that somber to me. Well, the songs in
					this post are not really cohesively picked this time...
				</p>
				<figure class="kg-card kg-image-card kg-card-hascaption">
					<img
						src="https://blog.nanao.moe/content/images/2021/06/Screenshot_20210624-200658.png"
						class="kg-image"
						alt="Introduction video"
						loading="lazy"
						width="2400"
						height="1080"
						srcset="https://blog.nanao.moe/content/images/size/w300/2021/06/Screenshot_20210624-200658.png 300w, https://blog.nanao.moe/content/images/size/w600/2021/06/Screenshot_20210624-200658.png 600w, https://blog.nanao.moe/content/images/size/w1000/2021/06/Screenshot_20210624-200658.png 1000w, https://blog.nanao.moe/content/images/size/w1500/2021/06/Screenshot_20210624-200658.png 1500w, https://blog.nanao.moe/content/images/size/w2000/2021/06/Screenshot_20210624-200658.png 2000w"
						sizes="(min-width: 768px) 640px, (min-width: 1024px) 768px, 100vw"
					/>
					<figcaption>The introduction is a video.</figcaption>
				</figure>
				<h2>A text image text test</h2>
				<p>
					In the end, the keyword I chose for this selection of music is <em>Sparkling Thoughts</em
					>. The reason is that those are all the songs that I've found out I constantly listen to
					lately! As for Sparkling... the songs are not really that somber to me. Well, the songs in
					this post are not really cohesively picked this time...
				</p>
				<figure class="kg-card kg-image-card kg-card-hascaption">
					<img
						src="https://blog.nanao.moe/content/images/2021/06/Screenshot_20210624-200658.png"
						class="kg-image"
						alt="Introduction video"
						loading="lazy"
						width="2400"
						height="1080"
						srcset="https://blog.nanao.moe/content/images/size/w300/2021/06/Screenshot_20210624-200658.png 300w, https://blog.nanao.moe/content/images/size/w600/2021/06/Screenshot_20210624-200658.png 600w, https://blog.nanao.moe/content/images/size/w1000/2021/06/Screenshot_20210624-200658.png 1000w, https://blog.nanao.moe/content/images/size/w1500/2021/06/Screenshot_20210624-200658.png 1500w, https://blog.nanao.moe/content/images/size/w2000/2021/06/Screenshot_20210624-200658.png 2000w"
						sizes="(min-width: 768px) 640px, (min-width: 1024px) 768px, 100vw"
					/>
					<figcaption>The introduction is a video.</figcaption>
				</figure>
				<p>
					In the end, the keyword I chose for this selection of music is <em>Sparkling Thoughts</em
					>. The reason is that those are all the songs that I've found out I constantly listen to
					lately! As for Sparkling... the songs are not really that somber to me. Well, the songs in
					this post are not really cohesively picked this time...
				</p>
			</GhostStyle>

			{#snippet comments()}
						<svelte:fragment  />
					{/snippet}
		</PostMain>
		<PostNavigator
			prev_post={{
				url: '/examples/post-page',
				title: 'Sophie!'
			}}
			next_post={{
				url: '/examples/post-page',
				title: 'Sophie!'
			}}
		/>
	</Post>

	<PostRelated name="Sophie" url="https://google.com" accent_color="#3b34dc">
		<PostCard
			authors={[
				{
					name: 'Damillora',
					profile_image: 'https://blog.nanao.moe/content/images/2021/09/special_01_01.jpg',
					url: 'https://blog.nanao.moe/author/damillora/'
				}
			]}
			date="2022 November 2020"
			excerpt="Sophie!"
			feature_image="https://images.nanao.moe/r/7jETH3.png"
			primary_tag={{
				accent_color: '#3b7b9c',
				name: 'Sound Voltex',
				url: '/examples/post-page'
			}}
			reading_time="3 min"
			title="Sophie!"
			url="/examples/post-page"
		/>
		<PostCard
			authors={[
				{
					profile_image: 'https://images.nanao.moe/r/GDuirR.jpg',
					url: '/examples/post-page',
					name: 'Sophie Neuenmuller'
				}
			]}
			date="2022 November 2020"
			excerpt="Sophie!"
			feature_image="https://images.nanao.moe/r/7jETH3.png"
			primary_tag={{
				accent_color: '#3b7b9c',
				name: 'Sound Voltex',
				url: '/examples/post-page'
			}}
			reading_time="3 min"
			title="Sophie!"
			url="/examples/post-page"
		/>
		<PostCard
			authors={[
				{
					profile_image: 'https://images.nanao.moe/r/GDuirR.jpg',
					url: '/examples/post-page',
					name: 'Sophie Neuenmuller'
				}
			]}
			date="2022 November 2020"
			excerpt="Sophie!"
			feature_image="https://images.nanao.moe/r/7jETH3.png"
			primary_tag={{
				accent_color: '#3b7b9c',
				name: 'Sound Voltex',
				url: '/examples/post-page'
			}}
			reading_time="3 min"
			title="Sophie!"
			url="/examples/post-page"
		/>
	</PostRelated>
</Container>
