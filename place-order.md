---
layout: page
title: Place Order Request
show_tile: false
nav-menu: false
---

<!-- Main -->
<div id="main" class="alt">

<!-- Intro -->
<section>
	<div class="inner">
		<section style="margin-top: 6em" >
			<h2>Place Order</h2>
			<!-- Success! -->
			<div id="showme" style="display:none;" class="box order-success">
				<div class="loader" id="loader"></div>
				<div id="order-success-message" class="order-success-message">
					<h3>Order Placed - Deposit Required</h3>
					<p>Your order request has been placed and I will be in touch soon about the details of your build.</p>
					<p>A deposit is required before your name can be added to our waitlist.</p>
					<ul class="actions">
						<li><input type="button" value="Pay Deposit Now" class="special" onclick="window.location.assign('/checkout/' + guitarmodel.value,'newtab')"/></li>
					</ul>
				</div>
			</div>
			<p>So you’ve gone through my site and have come to the excellent decision that you want to order a guitar. First off thanks! That’s brilliant news, welcome to the family! To commit you and I to the build, and to get onto my waiting list - <strong>once you place this request, you will be asked to pay for your deposit via PayPal</strong>. The waiting list is currently about 4 months from me receiving the deposit to you receiving your guitar.</p> 
			<p>I am also still very much a custom shop, and love taking on one of a kind, custom orders. Want a hollow flying V, a fretless baritone RD, a headless, midi connected bass, I am fresh! Just <a href="{{ 'contact' | relative_url }}">send me a mail</a> and we can chat.</p>
			<!-- Form -->
			<form id="order-request" method="post" action="https://formspree.io/xdowqbno">
				<div class="field">
					<label for="customer">Email</label>
					<input type="email" id="email" placeholder="team@moarguitars.com" name="email" required/>
				</div>
				<div class="field half first" style="margin-bottom: 0.4em">
					<label for="name">Name</label>
					<input type="text" id="yourname" placeholder="Morty Moar" name="customer" required/>
				</div>
				<div class="field half">
					<label for="guitarmodel">Choose Guitar Model</label>
					<div class="select-wrapper">
						<select name="model" id="guitarmodel" required>
							<option value="solid-t">Solid Morty (500USD)</option>
							<option value="hollow-t">Hollow Morty (600USD)</option>
							<option value="offset">Moar Offset (700USD)</option>
							<option value="solid-bass">Solid Bass (700USD)</option>
							<option value="hollow-bass">Hollow Bass (800USD)</option>
							<option value="wayfair">Wayfair (1000USD)</option>
						</select>
					</div>
				</div>
				<!-- <div class="field">
					<label for="name">Serial Number</label>
					<input type="text" id="yourname" placeholder="If you have created a Moar serial number, please add it here" name="customer"/>
				</div> -->
				<div class="row uniform" style="display:none;">
					<div class="4u 12u$(xsmall)">
						<div class="field">
							<label for="wood">Body Wood</label>
							<div class="select-wrapper">
								<select name="wood" id="wood">
									<option value="test">Wood 1</option>
								</select>
							</div>
						</div>
					</div>
					<div class="4u 12u$(xsmall)">
						<div class="field">
							<label for="neck">Neck Radius</label>
							<div class="select-wrapper">
								<select name="neck" id="neck">
									<option value="test">Option 1</option>
								</select>
							</div>
						</div>
					</div>
					<div class="4u 12u$(xsmall)">
						<div class="field">
							<label for="scale">Scale Length</label>
							<div class="select-wrapper">
								<select name="scale" id="scale">
									<option value="test">Option 1</option>
								</select>
							</div>
						</div>
					</div>
				</div>
				<ul class="actions">
					<li><input id="submit" type="submit" value="Continue to Pay" class="special" onclick="showme();"/></li>
					<li><input id="reset" type="reset" value="Clear" /></li>
				</ul>
				<p style="font-size:0.6em">Prices listed are the total deposit required to process your order - after submitting this form you will be redirected to a page where you can make a payment.</p>	
			</form>	
		</section>
	</div>
</section>

<!-- URL Parameters -->
<script type="text/javascript">
    var hashParams = window.location.hash.substr(1).split('&'); // substr(1) to remove the `#`
    for(var i = 0; i < hashParams.length; i++){
        var p = hashParams[i].split('=');
        document.getElementById(p[0]).value = decodeURIComponent(p[1]).replace('+', ' ').replace('+', ' ');;
    }
</script>

