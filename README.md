## Next.js Partial Prerendering Demo

This is a demo of React and Next.js using Partial Prerendering).

This sample uses the new Next.js App Router and the experimental Partial Prerendering feature available in Next.js 14. Partial Prerendering combines ultra-quick static edge delivery with fully dynamic capabilities, bringing together the best of static site generation and dynamic delivery.

Here is a full breakdown of its core features

![image](https://vercel.com/_next/image?url=https%3A%2F%2Fimages.ctfassets.net%2Fe5382hct74si%2F5VDyzuymkOUuQVo1ECuayK%2F051b687701d68d1590068323eeb0be30%2FGraphic_1_-_Dark.png&w=1080&q=75&dpl=dpl_7BsSCkzUxGRMVFVmKbSPAgMRzoUt)

> ⚠️ PPR is an experimental technology and is not recommended for production.

## How it works

The index route `/` uses Partial Prerendering through:

1. Enabling the experimental flag in `next.config.js`.

```js
experimental: {
    ppr: true,
},
```

2. Using `<Suspense />` to wrap Dynamic content.

The below image distinguishes between the static and dynamic parts of the page, showing the true potential of PPR

![image](https://vercel.com/_next/image?url=https%3A%2F%2Fimages.ctfassets.net%2Fe5382hct74si%2F19oHbnORNyZdAYAxuzQHbP%2F4e7196649e205805d8ef419da4e25d6d%2Fthinking-in-server-components.png&w=828&q=75&dpl=dpl_7BsSCkzUxGRMVFVmKbSPAgMRzoUt)

### The final build output should look as follows:

> ![screenshot](./public/Screenshot%202024-02-12%20155253.png)

## Further Reading

[Announcement: Partial Prerendering (NEXT.js CONF 2023)](https://vercel.com/blog/partial-prerendering-with-next-js-creating-a-new-default-rendering-model)

[Docs: Partial Prerendering (experimental)](https://nextjs.org/docs/app/api-reference/next-config-js/partial-prerendering)

[Learn: Partial Prerendering](https://nextjs.org/learn/dashboard-app/partial-prerendering)
