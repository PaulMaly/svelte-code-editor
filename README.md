# svelte-code-editor

Code editor action and component with highting for [Svelte 3](https://svelte.dev). [demo](https://svelte.dev/repl/2a569b9090b8454980917041f3250ebc?version=3.29.4)

## Usage

Install with npm or yarn:

```bash
npm install --save-dev svelte-code-editor
```

## Parameters

Based on [codejar](https://www.npmjs.com/package/codejar) and [prismjs](https://www.npmjs.com/package/prismjs). Any options of `codejar` can be passed to action params or CodeEditor props. 

```svelte
<CodeEditor bind:code loc={true} autofocus={true} tab="\t" on:change={change} />

<script>
  import CodeEditor from 'svelte-code-editor';

  let code = `
    { foo: 1, bar: true, baz: 'quux' }
  `;
</script>
```

OR import `codedit` action to get more control.

```html
<div 
  use:codedit={{ code, loc: true, autofocus: true, tab: '\t' }} 
  on:change={change}
/>
 
<script>
  import { codedit } from 'svelte-code-editor';

  let code = `
    { foo: 1, bar: true, baz: 'quux' }
  `;

  function change({ detail: code }) {
    console.log('code changed', code);
  }
</script>
```

## TODO...

Readme is still a work-in-progress.

## License

MIT &copy; [PaulMaly](https://github.com/PaulMaly)
