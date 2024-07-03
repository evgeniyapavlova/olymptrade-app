<script>
	import links from '$lib/utils/links';
	import DepositMethods from '$comps/DepositMethods/DepositMethods.svelte';
</script>

<section>
	<h3>Why Go for the Mobile and Desktop Apps?</h3>
	<div class="text">
		In short, Olymp Trade's mobile and desktop apps beat out the web browser platform in terms of
		reliability, speed, and security. Namely, the apps give you a steady, uninterrupted trading
		environment and enable faster trade execution and updates, ensuring your data protection by
		cutting-edge security features.
	</div>
	<h3>How You Can Deposit Funds</h3>
	<div class="text">
		When depositing trading funds to your Olymp Trade account, you've got flexible options:
	</div>
	<ul>
		<li>
			<span><b>Bank cards:</b> Link credit/debit cards for fast and seamless transactions</span>
		</li>
		<li><span><b>E-wallets:</b> Use popular digital wallets to easily manage capital</span></li>
		<li><span><b>Bank transfers:</b> Reliable, direct channel for funding</span></li>
		<li><span><b>Cryptocurrencies:</b> Extra funding choice for crypto enthusiasts</span></li>
	</ul>

	<DepositMethods />
	<a href={links.deposit} class="button" target="_blank">Deposit now</a>
</section>

<style>
	section {
		text-align: center;
		padding-top: 60px;
		padding-bottom: 60px;
	}

	ul li {
		text-align: center;
	}

	@media screen and (max-width: 768px) {
		section {
			padding-top: 20px;
		}
	}
</style>
