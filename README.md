# Problem

```svltestrap``` components don't want to play nicely with ```svelte-routing``` navigate function.

When implementating a ```javascript on:click={() => navigate("/some-url")}``` scenario, the script crashes with opaque message like:
```bash
19:55:56.734 TypeError: os is undefined sveltestrap.es.js:1:392
```

## Replicating the problem

Clone the repo, install the deps and start the dev server ...

```bash
git clone https://github.com/LaughingBubba/sveltestrap-problem.git
cd sveltestrap-problem
npm install
npm run dev
```

Follow the instructions on the home page and click on the yellow to see the problem occuring.

Then stop the dev server, checkout the ```plain-bs4``` branch and start the dev server again.

This time 