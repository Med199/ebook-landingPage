<script>
	import authorPic from '$assets/profile_pic.jpg';
</script>

<section class="landing-page-section">
	<h2 class="mb-l">About the Author</h2>
	<div class="author-container">
		<div class="author-text">
			<p class="mb-s">
				Maria González is a passionate traveler, writer, and long-time resident of Spain. With over
				a decade of experience living in various Spanish cities and regions, she has developed a
				deep understanding of Spanish culture, lifestyle, and the practical aspects of relocating
				abroad. Maria combines her love for storytelling with practical advice, helping newcomers
				navigate everything from visas and housing to integrating into local communities. Through
				Moving to Spain, she hopes to inspire and empower readers to embrace the vibrant life that
				Spain offers, making their transition smooth, exciting, and full of discovery.
			</p>
			<p>
				Before moving to Spain, Maria worked in international education and cultural exchange
				programs, which sparked her fascination with cross-cultural experiences. She holds a degree
				in International Relations and is fluent in Spanish and English. When she’s not writing or
				exploring new towns, Maria enjoys cooking traditional Spanish dishes, hiking in the
				countryside, and sharing her experiences through workshops and seminars aimed at helping
				expats feel at home.
			</p>
		</div>
		<img src={authorPic} alt="Author Alex Müller" />
	</div>
</section>

<style>
	.author-container {
		display: flex;
		justify-content: space-between;
	}
	.author-container img {
		width: 40%;
		border: 6px solid black;
		box-shadow: 0 4px 24px rgba(0, 0, 0, 0.5);
	}
	.author-container .author-text {
		width: 55%;
	}
</style>
