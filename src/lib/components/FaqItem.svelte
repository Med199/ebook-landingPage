<script>
	import chevronDown from '$assets/icons/chevron-down.svg';
	let { faq, isExpanded, onclick } = $props();
	$inspect(isExpanded);
</script>

<button class="container {isExpanded === true ? 'container-expanded' : ''}" {onclick}>
	<div class="question-and-answer">
		<p class="question mb-s">{faq.question}</p>
		<p class="answer">
			{faq.answer}
		</p>
	</div>
	<img src={chevronDown} alt="" />
</button>

<style>
	.container {
		display: flex;
		justify-content: space-between;
		padding: 12px 0;
		align-items: flex-start;
		border-bottom: 1px solid grey;
		text-align: left;
	}
	.question-and-answer {
		flex-grow: 1;
		padding-right: 150px;
	}
	.answer {
		max-height: 0px;
		overflow: hidden;
		opacity: 0;
		transition:
			max-height 0.3s ease-out,
			opacity 0.3s ease-out;
	}
	.container img {
		width: 24px;
		height: 24px;
		transition: transform 0.3s linear;
	}
	.question {
		font-weight: 600;
	}
	.container-expanded img {
		transform: rotate(180deg);
	}
	.container-expanded .answer {
		max-height: unset;
		opacity: 1;
	}
</style>
