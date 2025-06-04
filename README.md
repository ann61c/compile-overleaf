# Compile-Overleaf

get latest version of compiled pdf download link from a overleaf read token

generated link can be directly download without cookie/token verification.

## Basic Usage

```js
const compileOverleaf = require('compile-overleaf');

try {
    // https://overleaf.com/read/bpzztvkfcqgy
    const token = 'bpzztvkfcqgy';
    const compiled = await compileOverleaf(token);

    /**
     * {
     *  name: 'projectName',
     *  link: {pdf: 'https://compiles.overleaf.com/....'}
     * }
     **/
    console.log(compiled);
} catch (e) {
    /**
     *     status: e.statusCode, <response from server>
     *     stage: e.message, <where error happens>
     **/
    console.log(e);
}
```

## Online Demo

`https://resume.lyc.sh/#{token}`

> e.g. <https://resume.lyc.sh/#bpzztvkfcqgy>

### API

`https://resume.lyc.sh/api/read?token={token}`

> e.g. <https://resume.lyc.sh/api/read?token=bpzztvkfcqgy>

Original project: <https://github.com/NeverBehave/compile-overleaf>
Original Author: [NeverBehave](https://github.com/NeverBehave)
