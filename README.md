# Problem

```svltestrap``` components don't want to play nicely with ```svelte-routing``` navigate function.

When implementating a scenario like:
```javascript 
on:click={() => navigate("/some-url")}
``` 
the script crashes with opaque message like:
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

Follow the instructions on the home page and click on the yellow button to see the problem occuring.

Then stop the dev server, checkout the ```plain-bs4``` branch and start the dev server again.

Follow the instructions on the home page and click on the GREEN button to see the NO problem occuring and the page navigation to the ```/hello``` url as expected.

NB1: This is because the button is a plain HTML button styled using BS4

NB2: Flip back to the master branch and uncomment the HTML button in the ```Home.svelte``` component and that too will fail. Smells like an event bubbling problem.