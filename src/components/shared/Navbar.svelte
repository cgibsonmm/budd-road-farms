<script>
	import DropdownList from '../shared/DropdownList.svelte';
	import { clickOutside } from '../../assets/js/clickOutside.js';
	import { faBars } from '@fortawesome/free-solid-svg-icons';
	import { FontAwesomeIcon } from 'fontawesome-svelte';

	let toggle = false;

	function handleClickOutside(event) {
		if (
			event.targetSrc.nodeName === 'svg' ||
			event.targetSrc.nodeName == 'path' ||
			event.targetSrc.id === 'toggle-icon'
		) {
			toggle = !toggle;
		} else {
			toggle = false;
		}
	}
</script>

<div>
	<div class="bg-rose-600 h-20 flex items-center justify-between p-2 shadow-lg">
		<h1 class="text-2xl text-gray-100">Budd Road Family Farm</h1>
		<div id="icon-container" class="md:hidden">
			<FontAwesomeIcon id="toggle-icon" icon={faBars} class="text-gray-100" size="lg" />
		</div>
	</div>
	<!-- Dropdown Container -->
	<div
		use:clickOutside
		on:click_outside={handleClickOutside}
		class={toggle ? 'block md:hidden' : 'hidden'}
	>
		<DropdownList links={['hello']} />
	</div>
</div>
