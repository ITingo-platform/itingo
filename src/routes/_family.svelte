<script>
	import FaqSection from '../layout/FaqSection.svelte';
	import ContactSection from '../layout/landing/ContactSection.svelte';

	import OurFamily from '../layout/ngo/OurFamily.svelte';
	import partnersList from '../data/ngo/partnersList';
	import faqList from '../data/faq/ngoFaqList';
	import SupportSection from '../layout/SupportSection.svelte';
	
</script>

<svelte:head>
	<title>ITingo dla NGO</title>
</svelte:head>

<!-- 
    1. sponsors
    2. bussines partnewrs
    3. ngp partners
    4. volonteers
    5. startups
 -->
{#each partnersList as member}
	<OurFamily {member} anchor='partners'/>
{/each}

<SupportSection />

<a id="faq" ></a>
<FaqSection {faqList}/>

<ContactSection />