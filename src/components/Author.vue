<template>
	<div class="author">

		<h1 v-if="showTitle" class="author__site-title" style="margin-bottom: 20px;">
			<i class="fas fa-sun fa-3x"></i>
			&nbsp; {{ $static.metaData.siteName }}
		</h1>

		<p class="author__intro" style="margin-bottom: 47px; text-align: right;">
			Νε vελ ομνεσ φαβθλασ. Cορπορα cοπιοσαε ρεφορμιδανσ ναμ θτ. Vισ ιν μανδαμθσ ινcορρθπτε. Vιμ ωισι οφφενδιτ ρεφορμιδανσ τε, ατqθι νονθμυ πθτεντ νο qθι, vελ αδ ενιμ vερι φαλλι. Περ πορρο ελειφενδ cθ, δενιqθε μολεστιαε ιδ προ.
		</p>

		<p class="author__links">
			<i class="fab fa-twitter fa-2x"></i>&nbsp;&nbsp;
			<i class="fab fa-github fa-2x"></i>
		</p>

	</div>
</template>

<static-query>
query {
  metaData {
    siteName
  }
}
</static-query>

<script>
export default {
	props: ['showTitle']
}
</script>

<style lang="scss">
.author {
	margin: 0 auto;
	max-width: 500px;
	text-align: center;
	padding-bottom: calc(var(--space) / 2);

	&__image {
		border-radius: 100%;
		width: 90px;
		height: 90px;
		margin-bottom: 1em;
	}

	&__intro {
		opacity: .8;
	}

	&__site-title {
		margin: 0 auto;
		font-size: 1.5em;
		max-width: 400px;
	}

	&__links {
		margin-top: -.5em;
		a {
			margin: 0 .5em;
		}
	}
}
</style>
