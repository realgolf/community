<script lang="ts">
	import ThemeToggler from './ThemeToggler.svelte';
</script>

<nav>
	<ul>
		<li><ThemeToggler></ThemeToggler></li>
	</ul>
</nav>

<style lang="scss">
	nav {
		padding-block: 1.25rem;
		background-color: var(--nav-color);

		@media (max-width: 38rem) {
			padding-block: 0.5rem;
		}

		ul {
			list-style-type: none;
			display: flex;
			flex-wrap: wrap;
			justify-content: right;
			gap: 1.25rem;
			margin-right: 20px;
			margin-left: 20px;
			a {
				position: relative;
				text-decoration: none;

				&::before {
					content: '';
					position: absolute;
					left: 0;
					bottom: -2px;
					width: 0;
					height: 2px;
					background-color: var(--highlight-color);
					transition: width 0.3s ease;
				}

				&:hover::before {
					width: 100%;
				}
			}

			li {
				span {
					margin-left: 15px;
					white-space: nowrap;
				}
			}
		}
	}
</style>
