<script>
    export let type = 'default';
    export let disabled = false;
    export let classList = '';

    let styles =
        'px-4 py-2 rounded hover:-translate-y-1 hover:shadow active:translate-y-0 transform transition-all focus:ring ';

    switch (type) {
        case 'default':
            styles += 'bg-gray-100 hover:bg-gray-200 active:bg-gray-300 ';
            break;

        case 'primary':
            styles +=
                'bg-green-200 text-green-900 hover:bg-green-300 active:bg-green-400 ';
            break;
        case 'secondary':
            styles +=
                'text-green-800 border border-green-200 hover:bg-gray-100 active:bg-gray-200 ';
            break;
        case 'danger':
            styles +=
                'bg-red-200 text-red-900 hover:bg-red-300 active:bg-red-400 ';
            break;
        case 'dark':
            styles +=
                'bg-gray-800 text-gray-50 hover:bg-gray-900 active:bg-gray-700 ';
            break;
        default:
            break;
    }

    if (classList) styles += classList;
</script>

<button {disabled} on:click class={styles}>
    <slot />
</button>
