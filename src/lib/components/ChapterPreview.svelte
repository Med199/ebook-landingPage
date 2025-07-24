<script>
	const chapters = [
		{
			number: 1,
			title: 'Navigating the Spanish Bureaucracy',
			strapline: 'Understanding Visas, Residency, and Legal Essentials',
			excerpt:
				'Moving to Spain is an incredible adventure! It’s a country full of life, with sunny weather, delicious food, and a culture that truly values enjoying the moment. Whether you’re strolling through historic cities, relaxing on the coast, or grabbing tapas with friends, there’s always something to love. The lifestyle is laid-back, the people are warm, and the beauty is everywhere—from art and architecture to the simple joy of a late-night meal under the stars. Moving to Spain isn’t just a change of place—it’s a whole new vibe. There’s a rhythm to life in Spain that’s both energizing and relaxing. Mornings start slow, afternoons are meant for connection, and nights are full of laughter and music.'
		},
		{
			number: 2,
			title: 'Finding Your Perfect Home',
			strapline: 'From Bustling Cities to Tranquil Villages',
			excerpt:
				'Spain offers a diverse range of living options, from vibrant urban centers like Madrid and Barcelona to charming villages nestled in the countryside. This chapter explores how to find the right home for your lifestyle and budget, understanding the rental market, buying property, and what to expect in different regions. Whether you want a seaside apartment, a rustic farmhouse, or a modern flat, you’ll learn how to navigate the housing landscape with confidence.'
		},
		{
			number: 3,
			title: 'Integrating into Spanish Culture',
			strapline: 'Language, Customs, and Making Connections',
			excerpt:
				'Adapting to a new culture can be one of the most rewarding parts of moving abroad. Here, we dive into the essentials of Spanish language basics, social etiquette, and the importance of family and community. Discover how to make friends, join local activities, and embrace the festivals and traditions that bring Spanish culture to life. Building meaningful relationships will help you feel at home faster.'
		},
		{
			number: 4,
			title: 'Building a Career in Spain',
			strapline: 'Job Markets, Freelancing, and Entrepreneurship',
			excerpt:
				'Whether you’re looking for a traditional job, planning to freelance, or interested in starting your own business, Spain’s work environment has a lot to offer. This chapter covers the key industries, how to navigate the job market, work permits, and the growing opportunities for entrepreneurs and digital nomads. Learn about the work-life balance in Spain and how to align your career goals with your new lifestyle.'
		},
		{
			number: 5,
			title: 'Enjoying Life and Exploring Spain',
			strapline: 'Travel, Food, and Everyday Joys',
			excerpt:
				'Once you’ve settled in, it’s time to enjoy everything Spain has to offer. From tapas tours and wine regions to beautiful hiking trails and historic sites, this chapter highlights the best ways to explore your new home. Discover how to make the most of festivals, local markets, and hidden gems. Life in Spain is about savoring the moment—this chapter will inspire you to dive deep into the Spanish experience.'
		}
	];
	let selectedChapterNumber = $state(1);
	let selectedChapter = $derived(
		chapters.find((chapter) => chapter.number === selectedChapterNumber)
	);
	function handleClickOnChapter(chapter) {
		selectedChapterNumber = chapter.number;
	}
</script>

<section class="landing-page-section">
	<h2 class="mb-l">What you're getting</h2>
	<div class="chapter-container">
		<ul>
			{#each chapters as chapter}
				<li>
					<button
						class="chapter-title {chapter.number === selectedChapterNumber
							? 'selected-chapter-title'
							: ''} "
						aria-controls={`chapter-info-${chapter.number}`}
						aria-expanded={selectedChapterNumber === chapter.number}
						onclick={() => handleClickOnChapter(chapter)}
					>
						<h3>chapter {chapter.number}: {chapter.title}</h3>
					</button>
				</li>
			{/each}
		</ul>

		<div class="chapter-info">
			<h3 class="chapter-strapline italic mb-s">
				{selectedChapter.title}
			</h3>
			<p>
				{selectedChapter.excerpt}
			</p>
		</div>
	</div>
</section>

<style>
	.chapter-container {
		display: flex;
		justify-content: space-between;
	}
	.chapter-container ul {
		width: 40%;
	}
	.chapter-info {
		width: 55%;
	}
	.chapter-title {
		border-bottom: 1px solid grey;
		width: 100%;
		display: block;
		padding: 12px;
		text-align: left;
	}
	.selected-chapter-title {
		background: black;
		border: none;
		color: white;
		box-shadow:
			0 4px 6px #02504a,
			0 1px 3px rgb(4, 101, 93);
	}
</style>
