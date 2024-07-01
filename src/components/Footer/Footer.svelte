<script>
	import { base } from '$app/paths';
	import logo from '$lib/images/logo.svg';
	import links from '$lib/utils/links';
</script>

<footer>
	<section>
		<div class="footer-top">
			<img class="footer-logo" src={logo} alt="Olymp Trade logotype" />
			<div class="footer-socials">
				<a href={links.facebook} target="_blank" class="facebook-link">
					<svg
						fill="#fff"
						width="25"
						height="25"
						viewBox="0 0 512 512"
						xmlns="http://www.w3.org/2000/svg"
					>
						<path
							d="M504 256C504 119 393 8 256 8S8 119 8 256c0 123.78 90.69 226.38 209.25 245V327.69h-63V256h63v-54.64c0-62.15 37-96.48 93.67-96.48 27.14 0 55.52 4.84 55.52 4.84v61h-31.28c-30.8 0-40.41 19.12-40.41 38.73V256h68.78l-11 71.69h-57.78V501C413.31 482.38 504 379.78 504 256z"
						>
						</path>
					</svg></a
				>
				<a href={links.tg} target="_blank" class="tg-link">
					<svg
						fill="#fff"
						width="25"
						height="25"
						viewBox="0 0 496 512"
						xmlns="http://www.w3.org/2000/svg"
						><path
							d="M248 8C111 8 0 119 0 256s111 248 248 248 248-111 248-248S385 8 248 8zm121.8 169.9l-40.7 191.8c-3 13.6-11.1 16.9-22.4 10.5l-62-45.7-29.9 28.8c-3.3 3.3-6.1 6.1-12.5 6.1l4.4-63.1 114.9-103.8c5-4.4-1.1-6.9-7.7-2.5l-142 89.4-61.2-19.1c-13.3-4.2-13.6-13.3 2.8-19.7l239.1-92.2c11.1-4 20.8 2.7 17.2 19.5z"
						></path></svg
					>
				</a>
				<a href={links.youtube} target="_blank" class="youtube-link">
					<svg
						fill="#fff"
						width="25"
						height="25"
						viewBox="0 0 576 512"
						xmlns="http://www.w3.org/2000/svg"
						><path
							d="M549.655 124.083c-6.281-23.65-24.787-42.276-48.284-48.597C458.781 64 288 64 288 64S117.22 64 74.629 75.486c-23.497 6.322-42.003 24.947-48.284 48.597-11.412 42.867-11.412 132.305-11.412 132.305s0 89.438 11.412 132.305c6.281 23.65 24.787 41.5 48.284 47.821C117.22 448 288 448 288 448s170.78 0 213.371-11.486c23.497-6.321 42.003-24.171 48.284-47.821 11.412-42.867 11.412-132.305 11.412-132.305s0-89.438-11.412-132.305zm-317.51 213.508V175.185l142.739 81.205-142.739 81.201z"
						></path></svg
					>
				</a>
			</div>
		</div>
		<div class="footer-license">
			<div class="text">
				Olymp Trade is a licensed and regulated broker by the Vanuatu Financial Services Commission
				(VFSC) with license number 40131. Olymp Trade is committed to providing the highest quality
				of service.
			</div>
			<div class="footer-license-img-wrap">
				<img src="{base}/images/license.webp" alt="" />
			</div>
		</div>
		<div class="footer-info">
			<div class="text">
				<div class="footer-info-title">RISK WARNING:</div>

				The trading products offered by the company listed on this website carry a high level of
				risk and can result in the loss of all your funds. You should consider whether you can
				afford to take the high risk of losing your money. Before deciding to trade, you need to
				ensure that you understand the risks involved and taking into account your investment
				objectives and level of experience.
			</div>

			<div class="text">
				<div class="footer-info-title">AFFILIATE DISCLOSURE:</div>

				This website utilizes affiliate links. Registering through an affiliate link means we may
				receive compensation for directing you. We only use affiliate links for products and
				services we would wholeheartedly recommend, whether we earn a commission or not.
			</div>

			<div class="text">
				<div class="footer-info-title">NOTE:</div>

				This is an unofficial website about “Olymp Trade”. We provide reviews of brokers and their
				offerings, including information about Olymp Trade. We endeavor to provide accurate and
				reliable material, but cannot guarantee the absolute accuracy or currency of the
				information.
			</div>

			<div class="text">
				<div class="footer-info-title">DISCLAIMER:</div>

				Our website does not provide personalized investment advice. We do not assume any
				responsibility for any potential losses incurred while using the information on this
				website.
			</div>
		</div>

		<div class="footer-bottom">
			<div class="text">© 2024 olymptrade.app</div>
			<div class="text">Privacy Policy</div>

			<div class="text">Terms and Conditions</div>

			<div class="text">Contact Olymp Trade</div>
		</div>
	</section>
</footer>

<style>
	.footer-logo {
		width: 180px;
	}
	.footer-info .text {
		margin-bottom: 40px;
	}
	.footer-info-title {
		font-weight: 600;
		padding-bottom: 15px;
	}
	.footer-bottom {
		display: flex;
		align-items: center;
		justify-content: space-between;
		gap: 40px;
	}
	footer {
		background-color: #021123;
		color: white;
	}

	.footer-bottom .text {
		margin-bottom: 0;
	}

	.footer-bottom {
		border-top: 1px solid white;
		padding-top: 30px;
		margin-top: 40px;
		padding-bottom: 30px;
	}
	.footer-socials a.facebook-link {
		background-color: #3b5998;
	}
	.footer-socials a.tg-link {
		background-color: #2ca5e0;
	}
	.footer-socials a.youtube-link {
		background-color: #cd201f;
	}
	.footer-socials a:hover {
		opacity: 0.9;
	}
	.footer-socials a {
		transition: opacity 0.2s ease-out;
		width: 50px;
		height: 50px;
		border-radius: 10px;
		display: flex;
		align-items: center;
		justify-content: center;
	}
	.footer-socials {
		display: flex;
		align-items: center;
		justify-content: flex-end;
		gap: 12px;
	}
	.footer-top {
		display: flex;
		align-items: center;
		justify-content: space-between;
		padding-top: 40px;
		padding-bottom: 60px;
	}

	.footer-license {
		display: flex;
		align-items: center;
		justify-content: space-between;
	}

	.footer-license .text {
		width: 55%;
	}

	.footer-license-img-wrap img {
		width: 135px;
		max-width: 80%;
	}

	.footer-license-img-wrap {
		width: 35%;
		text-align: center;
	}

	@media screen and (max-width: 960px) {
		.footer-license .text {
			width: 65%;
		}
		.footer-license-img-wrap {
			width: 30%;
			text-align: center;
		}
	}

	@media screen and (max-width: 768px) {
		footer {
			text-align: center;
			font-size: 14px;
		}
		.footer-license {
			width: 100%;
			display: block;
			margin-bottom: 40px;
		}
		.footer-license .text,
		.footer-license-img-wrap {
			width: 100%;
		}
		.footer-license-img-wrap img {
			width: 120px;
		}
		.footer-bottom {
			flex-wrap: wrap;
			justify-content: center;
		}
		.footer-bottom .text:first-child {
			width: 100%;
		}
	}

	@media screen and (max-width: 600px) {
		.footer-top {
			display: block;
		}
		.footer-socials {
			justify-content: center;
			margin-top: 40px;
		}
	}
</style>
