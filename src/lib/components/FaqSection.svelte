<script>
	import { FaqItem, Button } from '$components';
	import twitterIcon from '$assets/icons/twitter.webp';
	const faqs = [
		{
			question: 'What will I learn from this ebook?',
			answer: `This ebook offers a captivating journey through the vibrant culture, rich history, and
        breathtaking landscapes of Spain. You’ll learn about the unique customs and traditions that
        define each region—from the flamenco rhythms of Andalusia to the architectural wonders of
        Catalonia. Discover the best local dishes and culinary experiences, from tapas bars in Madrid
        to fresh seafood along the Galician coast.`
		},
		{
			question: 'Who is this ebook for?',
			answer: `This ebook is perfect for anyone interested in discovering the beauty, culture, and travel experiences Spain has to offer. Whether you're planning a future trip, considering a move, or simply curious about Spanish life, this guide is designed for travelers, expats, and culture lovers alike.`
		},
		{
			question: 'How much does the ebook cost?',
			answer: `The ebook is completely free! It’s our way of sharing valuable insights and helping you get the most out of your Spanish adventure—no strings attached.`
		},
		{
			question: 'What format is the ebook available in?',
			answer: `The ebook is available as a downloadable PDF, making it easy to read on any device—whether you're using a phone, tablet, or laptop. It’s also printable if you prefer a hard copy for your travels.`
		},
		{
			question: 'Do I need to know Spanish to enjoy the ebook?',
			answer: `Not at all. The ebook is written in clear, easy-to-understand English. While we include useful Spanish phrases and tips for communication, no prior language skills are required to enjoy the content.`
		},
		{
			question: 'Can I share this ebook with friends or family?',
			answer: `Absolutely! Feel free to share the ebook with anyone who might enjoy or benefit from it. We believe in making travel knowledge accessible, and we’d love for more people to discover the magic of Spain.`
		}
	];
	let questionCurrentlyExpanded = $state(-1);
	function onclick(index) {
		if (questionCurrentlyExpanded === index) {
			questionCurrentlyExpanded = -1;
		} else {
			questionCurrentlyExpanded = index;
		}
	}
</script>

<section class="landing-page-section">
	<h2 class="mb-l">Frequently asked questions</h2>
	<div class="faq-container">
		{#each faqs as faq, index}
			<FaqItem
				{faq}
				isExpanded={index === questionCurrentlyExpanded}
				onclick={() => onclick(index)}
			/>
		{/each}
	</div>

	<div class="additional-info mt-m">
		<Button class="mt-s">BUY NOW</Button>
		<p class="mt-m">Any other questions?</p>
		<a href="https://x.com/KIZO_ES">
			<p>
				Hit me up on Twitter <img src={twitterIcon} class="twitterIcon" alt="" />
			</p>
		</a>
	</div>
</section>

<style>
	.additional-info {
		display: flex;
		flex-direction: column;
		align-items: center;
	}
	.twitterIcon {
		width: 16px;
		height: 16px;
	}
	a {
		text-decoration: underline;
	}
</style>
