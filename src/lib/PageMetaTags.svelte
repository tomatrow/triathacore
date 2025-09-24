<script lang="ts">
	import { MetaTags } from "svelte-meta-tags"
	import seoData from "$lib/cms_data/seo.json"

	const {
		siteName,
		siteDescription,
		pageTitle,
		pageDescription,
		pageCanonicalUrl,
		ogImage,
		ogImageAlt,
		ogImageWidth,
		ogImageHeight
	} = seoData

	const ogImageUrl = `https://www.triathacore.com${ogImage}`
</script>

<MetaTags
	title={pageTitle}
	description={pageDescription}
	canonical={pageCanonicalUrl}
	openGraph={{
		url: pageCanonicalUrl,
		title: pageTitle,
		description: pageDescription,
		siteName,
		images: [{ url: ogImageUrl, alt: ogImageAlt, width: ogImageWidth, height: ogImageHeight }]
	}}
	twitter={{
		cardType: "summary_large_image",
		title: siteName,
		description: siteDescription,
		image: ogImage,
		imageAlt: ogImageAlt
	}}
/>
