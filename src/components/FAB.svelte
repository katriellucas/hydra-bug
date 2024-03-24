<script lang="ts">
	import Icon from '@iconify/svelte';

	let { children, href, onclick, type = 'button', target, visual, size } = $props();
</script>

{#if href}
	<a class="fab target ripple {size} {visual}" {target} {onclick} {href}>
		{#if children}
			{@render children()}
		{/if}
	</a>
{:else}
	<button class="fab target ripple {size} {visual}" {onclick} {type}>
		{#if children}
			{@render children()}
		{/if}
	</button>
{/if}

<style lang="scss">
	.fab {
		align-items: center;
		border-radius: var(--corner-large);
		box-shadow:
			0px 8px 12px 6px rgba(0, 0, 0, 0.15),
			0px 4px 4px rgba(0, 0, 0, 0.3);
		cursor: pointer;
		display: inline-flex;
		font: var(--label-large);
		justify-content: center;
		height: 56px;
		min-width: 56px;
		white-space: nowrap;
		padding: 0 16px;

		:global(.iconify) {
			height: 24px;
			width: 24px;
		}
	}

	// SIZE OPTIONS 📏
	.small {
		border-radius: var(--corner-medium);
		height: 40px;
		width: 40px;
	}

	.large {
		border-radius: var(--corner-extra-large);
		height: 96px;
		width: 96px;

		:global(.iconify) {
			height: 36px;
			width: 36px;
		}
	}

	// COLORS OPTIONS 🎨
	.primary {
		background: var(--primary-container);
		color: var(--on-primary-container);
	}

	.secondary {
		background: var(--secondary);
		color: var(--on-secondary);
	}

	.tertiary {
		background: var(--tertiary-container);
		color: var(--on-tertiary-container);
	}

	.surface {
		background: var(--surface-container-high);
		color: var(--primary);
	}

	.extended {
		height: 56px;
		min-width: 80px;
		padding: 0 16px;
		width: auto;

		:global(.iconify) {
			margin-right: 12px;
		}
	}
</style>
