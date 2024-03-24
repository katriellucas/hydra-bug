<script lang="ts">
	import FAB from "../components/FAB.svelte";
	import Icon from "@iconify/svelte";
</script>

<FAB visual="tertiary" >
	<Icon icon="mdi:whatsapp" color="green" width="24px" height="24px"/>
</FAB>
<Icon icon="mdi:google" color="green" width="24px" height="24px"/>
<br><br><br>
Try change this text when your local/dev server is active, when you are using<br>
adapter 4.2.0 no icons or changes should appear, roll back to 4.1.0 on package<br>
and it should render normally. 11111111111