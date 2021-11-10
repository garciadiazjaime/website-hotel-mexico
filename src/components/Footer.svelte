<style>
	.color-almendra {
		color: var(--color-almendra);
	}

	.color-blanco {
		color: white;
	}

	img {
		max-width: 100%;
		height: auto;
		display: block;
	}

	a {
		text-decoration: none;
	}

	p {
		margin: 0;
	}

	.content-menu {
		max-width: 1280px;
		margin: 0 auto;
		padding: 0 50px;
		box-sizing: border-box;
	}

	.smaller-text {
		font-size: 13px;
	}

	.row {
		display: flex;
		justify-content: space-between;
	}

	.padding-top-10 {
		padding-top: 10px;
	}

	.padding-top-20 {
		padding-top: 20px;
	}

	.padding-top-50 {
		padding-top: 50px;
	}

	p {
		color: var(--color-verde);
		font-family: gotham;
	}

	p.border-bottom {
		border-bottom: 1px solid;
	}
	
	.uppercase {
		text-transform: uppercase;
	}

	.green-background {
		background-color: var(--color-verde);
	}

	.text-right {
		text-align: right;
	}

	.signature {
		font-family: august;
		font-size: 80px;
		color: var(--color-almendra);
		position: relative;
		top: -20px;
	}

	.signature.color-blanco {
		color: white;
		font-size: 36px;
		position: relative;
		top: -16px;
	}

	.logo-r {
		width: 60px;
	}

	.link-map {
		display: inline-block;
		margin-right: 20px;
		position: relative;
		top: -7px;
		border-bottom: 1px solid;
	}

	.social-media {
		display: inline-flex;
	}

	.social-media img {
		width: 25px;
		margin-right: 6px;
	}

	@media (max-width: 480px) {
		.signature.color-blanco {
			font-size: 50px;
			top: -20px;
		}
		.row {
			display: block;
		}
		.content-menu {
			padding: 0 12px;
		}
	}
</style>

<footer class="green-background">
	<div class="content-menu">
		<div class="row padding-top-50">
			<div>
				<p class="color-almendra">El hotel de</p>
				<div class="signature color-blanco">México y el Vino</div>
				<p class="uppercase color-almendra border-bottom padding-top-20">HOTEL MÉXICO EN LA PIEL &#169;2021</p>
			</div>
			<div class="padding-top-10">
				<img src="/support/logo-r.svg" alt="" class="logo-r">
			</div>
			<div>
				<p class="color-almendra text-right">
					hola@hotelmexicoenlapiel.com
				</p>
				<p class="color-almendra uppercase smaller-text text-right">
					VALLE DE GUADALUPE, BC, MX.
				</p>
				<p class="color-almendra padding-top-50">
					<a class="link-map" href="https://goo.gl/maps/RTzByVDUc2jHMF178" target="_blank">Google Maps</a>
					<span class="social-media">
						<a href="https://www.airbnb.com/users/200220394/listings" target="_blank">
							<img src="/support/airbnb.svg" alt="">
						</a>
						<a href="https://www.booking.com/hotel/mx/mexico-en-la-piel.es.html?label=gen173nr-1BCAsooAFCEW1leGljby1lbi1sYS1waWVsSDNYBGigAYgBAZgBCrgBB8gBDNgBAegBAYgCAagCA7gC88KwjAbAAgHSAiQ5ZjdiMTA5OC1mMzA0LTQ1MTUtOWQ3My01ZTcxODczODRmMWLYAgXgAgE;sid=f79a7c6169d5313812f64748582de0c8;dist=0;keep_landing=1;sb_price_type=total;type=total;sig=v1C_O5gL6c&" target="_blank">
							<img src="/support/booking.svg" alt="">
						</a>
						<a href="https://www.facebook.com/hotelmexicoenlapiel" target="_blank">
							<img src="/support/facebook.svg" alt="">
						</a>
						<a href="https://www.instagram.com/hotelmexicoenlapiel/?hl=en" target="_blank">
							<img src="/support/instagram.svg" alt="">
						</a>
					</span>
				</p>
			</div>
		</div>
	</div>
	<div class="padding-top-50"></div>
</footer>
