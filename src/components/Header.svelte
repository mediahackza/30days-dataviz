<div class="header">
	<div class="menu">
		<div class="menu-logo">
			<img src="/images/logo.png" alt="MHC Logo" />
		</div>
		<div class="menu-links">
			<div class="menu-item">
				<a href="https://mediahack.co.za/what-we-do/" target="_blank">What we do</a>
			</div>
			<div class="menu-item">
				<a href="https://mediahack.co.za/category/work/" target="_blank">Our Work</a>
			</div>
			<div class="menu-item">
				<a href="https://mediahack.co.za/category/tutorials/" target="_blank">Tutorials</a>
			</div>
		</div>
	</div>
</div>

<style>
	.header {
		padding-top: 5px;
		position: absolute;
		top: 0px;
		left: 0px;
		background: rgba(255, 255, 255, 0.95);
		width: 96%;
		padding-left: 2%;
		padding-right: 2%;
	}
	.header img {
		max-width: 100%;
	}
	.menu {
		display: grid;
		grid-template-columns: 1fr 1fr;
	}
	.menu a {
		color: inherit;
		text-decoration: none;
		border-bottom: none;
	}
	.menu a:hover {
		color: rgb(39, 180, 223);
	}
	.menu-links {
		text-align: right;
		padding: 9px;
		font-size: 1rem;
		text-transform: uppercase;
		font-weight: 700;
	}
	.menu-links * {
		display: inline-block;
	}
	.menu-item {
		margin-right: 15px;
	}

	@media only screen and (max-width: 800px) {
		.menu {
			display: grid;
			grid-template-columns: 1fr;
		}
		.menu-links {
			text-align: center;
			padding-top: 3px;
			padding-bottom: 15px;
		}
		.menu-logo {
			text-align: center;
		}
	}
</style>
