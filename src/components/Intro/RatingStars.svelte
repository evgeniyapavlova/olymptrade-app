<script>
	export let percent;
</script>

<div role="img" class="stars">
	<span aria-hidden="true" class="span-wrapper" data-number="1"
		><span class="span-inner" aria-hidden="true"
			><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24"
				><path d="M0 0h24v24H0z" fill="none"></path><path d="M0 0h24v24H0z" fill="none"></path><path
					d="M12 17.27L18.18 21l-1.64-7.03L22 9.24l-7.19-.61L12 2 9.19 8.63 2 9.24l5.46 4.73L5.82 21z"
				></path></svg
			></span
		></span
	><span aria-hidden="true" class="span-wrapper" data-number="2"
		><span class="span-inner" aria-hidden="true"
			><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24"
				><path d="M0 0h24v24H0z" fill="none"></path><path d="M0 0h24v24H0z" fill="none"></path><path
					d="M12 17.27L18.18 21l-1.64-7.03L22 9.24l-7.19-.61L12 2 9.19 8.63 2 9.24l5.46 4.73L5.82 21z"
				></path></svg
			></span
		></span
	><span aria-hidden="true" class="span-wrapper" data-number="3"
		><span class="span-inner" aria-hidden="true"
			><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24"
				><path d="M0 0h24v24H0z" fill="none"></path><path d="M0 0h24v24H0z" fill="none"></path><path
					d="M12 17.27L18.18 21l-1.64-7.03L22 9.24l-7.19-.61L12 2 9.19 8.63 2 9.24l5.46 4.73L5.82 21z"
				></path></svg
			></span
		></span
	><span aria-hidden="true" class="span-wrapper" data-number="4"
		><span class="span-inner" aria-hidden="true"
			><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24"
				><path d="M0 0h24v24H0z" fill="none"></path><path d="M0 0h24v24H0z" fill="none"></path><path
					d="M12 17.27L18.18 21l-1.64-7.03L22 9.24l-7.19-.61L12 2 9.19 8.63 2 9.24l5.46 4.73L5.82 21z"
				></path></svg
			></span
		></span
	><span aria-hidden="true" class="span-wrapper" data-number="5"
		><span class="span-inner" aria-hidden="true"
			><svg
				class="xdPrrd"
				xmlns="http://www.w3.org/2000/svg"
				viewBox="0 0 24 24"
				fill="url(#perc-{percent})"
				><defs
					><linearGradient id="perc-{percent}"
						><stop stop-opacity="1" offset="{percent}%" class="span-inner"></stop><stop
							stop-opacity="1"
							offset="{percent}%"
							class="star-bgr"
						></stop></linearGradient
					></defs
				><path d="M0 0h24v24H0z" fill="none"></path><path d="M0 0h24v24H0z" fill="none"></path><path
					d="M12 17.27L18.18 21l-1.64-7.03L22 9.24l-7.19-.61L12 2 9.19 8.63 2 9.24l5.46 4.73L5.82 21z"
				></path></svg
			></span
		></span
	>
</div>

<style>
	.star-bgr {
		fill: #d9d9d9;
		stop-color: #d9d9d9;
	}
	.stars {
		display: inline-block;
	}
	.span-wrapper {
		width: 16px;
		height: 16px;
		display: inline-block;
		text-align: left;
	}
	.span-inner {
		color: var(--stars-bgr);
		fill: var(--stars-bgr);
		stop-color: var(--stars-bgr);
	}
</style>
