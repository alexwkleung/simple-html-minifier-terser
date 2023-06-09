# simple-html-minifier-terser

A utility to minify HTML using [html-minifier-terser](https://github.com/terser/html-minifier-terser) with predefined options.

Minifying HTML using html-minifier-terser requires setup by default. While some may prefer to manually setup html-minifier-terser, some just want a simple zero-config HTML minifier that just works. Therefore, those who are in the latter, including myself, will prefer using simple-html-minifier-terser for their needs. 

This is ESM-only.

# Installation

Install via npm, directly from the repository.

```bash
npm install https://github.com/alexwkleung/simple-html-minifier-terser
```

# Example Usage

`minifyHtml` function returns a promise, therefore you need to resolve it. 

Here is a basic example:

```typescript
async function f(): Promise<void> {
    let template: string = `
    <!DOCTYPE html>
    <html lang="en">
    <head>
        <meta charset="UTF-8">
        <meta http-equiv="X-UA-Compatible" content="IE=edge">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>foo</title>
    </head>
    <body>
        <p>foo</p>
    </body>
    </html>`;

    return Promise.resolve(minifyHtml(template)).then((minifiedCallbackData) => {
        console.log(minifiedCallbackData);
    });
}
```

# License 

[MIT License.](https://github.com/alexwkleung/simple-html-minifier-terser/blob/main/LICENSE)