<script>
	import { base } from '$app/paths';
	import LazyImage from '$comps/LazyImage/LazyImage.svelte';
</script>

<section class="desktop-apps-wrap">
	<h2>Access Olymp Trade on Your Windows and Mac PCs</h2>
	<div class="flex-text flex-text-left">
		<div class="img-wrap-left">
			<LazyImage src="{base}/images/desktop_apps_1.webp" alt="Laptop" className="img1" />
		</div>
		<div>
			<div class="text">
				On top of a web app, Olymp Trade offers custom desktop apps for Windows and Mac featuring:
			</div>

			<ul>
				<li><span>Better performance</span></li>
				<li><span>More tools</span></li>
				<li><span>Multi-screen support</span></li>
				<li><span>Keyboard shortcuts</span></li>
				<li><span>Price alerts</span></li>
			</ul>

			<div class="text">Below are the minimum system requirements:</div>

			<table class="info info-light">
				<thead
					><tr>
						<th>Windows</th>
						<th>MacOS</th>
					</tr>
				</thead>
				<tbody>
					<tr>
						<td>Windows 7 and up</td>
						<td>macOS 10+</td>
					</tr>
					<tr>
						<td>Intel/AMD processor</td>
						<td>Intel chip</td>
					</tr>
					<tr>
						<td>4GB RAM</td>
						<td>4GB RAM</td>
					</tr>
					<tr>
						<td>5GB disk space</td>
						<td>5GB disk space</td>
					</tr>
				</tbody>
			</table>
			<div class="text">
				Please note that the actual performance depends on your hardware configuration. Make sure
				you keep your OS and drivers up to date!
			</div>
		</div>
	</div>
</section>

<style>
	:global(.img-wrap-left img) {
		max-width: 100%;
	}
	@media screen and (max-width: 768px) {
		table {
			margin-left: auto;
			margin-right: auto;
		}
		.flex-text-left {
			display: flex;
			flex-direction: column-reverse;
		}
		:global(.desktop-apps-wrap .img-wrap-left .img1) {
			max-width: 80%;
		}
	}
</style>
