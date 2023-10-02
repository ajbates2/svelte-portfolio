<script>
	import IconDocument from "~icons/ion/document-text";
</script>

<p class="container">
	<button class="link_button">
		<a href="/contact">Let's talk!</a>
	</button>
	<a
		href="/AJ_Bates_Resume.pdf"
		type="resume/pdf"
		title="resume"
		target="_blank"
		class="resume_link"
	>
		<IconDocument width="46px" height="46px" />
	</a>
</p>

<style>
	.container {
		height: 46px;
		display: flex;
		flex-direction: row;
		justify-content: flex-start;
		align-items: start;
	}

	button {
		background-size: 220%;
		border: none;
		box-shadow: 0 0.2em 0.3em rgba(0, 0, 0, 0.15);
		color: var(--red);
		background-position: 100%;
		text-transform: uppercase;
		padding: 15px 20px;
		border-radius: 3px;
		transition: all 0.2s ease-out;
		font-weight: 400;
		cursor: pointer;
		letter-spacing: 2px;
		background-image: linear-gradient(
			110deg,
			var(--red) 0%,
			var(--pink) 50%,
			transparent 50%,
			transparent 100%
		);
		font-size: 14px;
		background-color: var(--charcoal);
	}

	button:hover {
		transform: translateY(-2px);
		box-shadow: 0 0 0.3em rgba(0, 0, 0, 0.25);
		background-position: 0;
		color: var(--foreground);
	}

	.resume_link {
		margin-left: 10px;
		transition: all 0.2s ease-out;
		color: var(--foreground);
	}

	.resume_link:hover {
		transform: translateY(-2px);
		color: var(--red);
	}

	@media only screen and (max-width: 600px) {
		.container {
			justify-content: center;
		}
	}
</style>
