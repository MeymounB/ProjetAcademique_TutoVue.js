<template>
	<!-- <v-container fluid fill-height class="d-flex deep-purple lighten-1">
		<h1>Portfolio</h1>
	</v-container> -->
	<div>
		<h2>Mes projets</h2>
		<ul>
			<li class="div1 firstEffect">
				<p>Bee Driver</p>
			</li>
			<li class="div2">
				<p>Taxi Abdel</p>
			</li>
			<li class="div3">
				<p>Baby Quizz</p>
			</li>
			<li class="div4">
				<p>Portfolio</p>
			</li>

		</ul>
	</div>
</template>

<script>
</script>
      
<style scoped>
div {
	width: 100%;
	display: flex;
	flex-direction: column;
	justify-content: center;
	align-items: center;

}

ul {
	margin: 10px 0 0 0;
	padding: 0%;
	list-style: none;
	width: fit-content;

	/* display: flex;
	flex-wrap: wrap;
	flex-direction: row;
	justify-content: space-around; */

	display: grid;
	grid-template-columns: repeat(2, 1fr);
	grid-template-rows: repeat(2, 1fr);
	grid-column-gap: 200px;
	grid-row-gap: 100px;



}

.div1 {
	grid-area: 1 / 1 / 2 / 2;
}

.div2 {
	grid-area: 1 / 2 / 2 / 3;
}

.div3 {
	grid-area: 2 / 1 / 3 / 2;
}

.div4 {
	grid-area: 2 / 2 / 3 / 3;
}

li {
	width: 22vw;
	height: 27vh;

	display: flex;
	text-align: center;
	justify-content: center;
	align-items: center;
}

.firstEffect {

	--angle: 0deg;
	border: 1vmin solid;
	/* border-image: conic-gradient(from var(--angle), red, yellow, lime, aqua, blue, magenta, red) 1; */
	animation: 5s rotate linear infinite;
}

@keyframes rotate {
	to {
		--angle: 360deg;
	}
}

@property --angle {
	syntax: '<angle>';
	initial-value: 0deg;
	inherits: false;
}

li:first-child {
	background: radial-gradient(ellipse farthest-corner at right bottom, #FEDB37 0%, #FDB931 8%, #9f7928 30%, #8A6E2F 40%, transparent 80%), radial-gradient(ellipse farthest-corner at left top, #FFFFFF 0%, #FFFFAC 8%, #D1B464 25%, #5d4a1f 62.5%, #5d4a1f 100%);
	font: "Baskerville", "Garamond", "Georgia", "Palatino", "Times New Roman", "Arial", sans-serif;
	border-image: conic-gradient(from var(--angle), #FEDB37, #FDB931, #9f7928, #8A6E2F, #D1B464, #FFFFAC, #D1B464, #8A6E2F, #9f7928, #FDB931, #FEDB37) 1;

}

li:first-child:hover {
	animation: none;
}

li:nth-child(2) {
	--b: 5px;
	/* the border thickness */
	--d: 20px;
	/* the distance from the edge */
	--o: 15px;
	/* the offset on hover */
	--s: 1;
	/* the direction of the hover effect (+1 or -1)*/


	--_d: calc(var(--d) + var(--s)*1em);
	--_g: calc(100% - 2*(var(--_d) + var(--b)));
	--_m:
		conic-gradient(from 90deg at var(--_d) var(--_d), #0000 25%, #000 0) 0 0/calc(100% - var(--_d)) calc(100% - var(--_d)),
		linear-gradient(#000 0 0) 50%/var(--_g) var(--_g) no-repeat;
	-webkit-mask: var(--_m);
	mask: var(--_m);
	font-size: 0;
	cursor: pointer;
	transition: .35s;

	background: linear-gradient(90deg, rgba(0, 0, 0, 1) 0%, rgba(32, 32, 32, 1) 20%, rgba(134, 134, 134, 1) 40%, rgba(186, 186, 186, 1) 70%, rgba(255, 255, 255, 1) 100%);
}

li:nth-child(2):hover {
	font-size: var(--d);
}
</style>