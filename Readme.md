# picidae-transformer-exec

Execute command and Replace the placeholder by stdout.

- Input
```md
<<EXEC echo abc>>
```

- Output
```md
abc
```

## Options

- cache {boolean} (default: `true`)  
  cache the latest stdout. If you don't edit the markdown with `<<EXEC ...>>`, the content is from cache.

- env: {Object} (default: `{}`)  
  The additional env, like `process.env`

- paths: {array} (default: `[]`)  
  same as `$PATH`, and it would appends the `node_modules/.bin` to `$PATH` automatically.
  
- cwd: {string} (default: `'curr'`)  
  - `curr`: `process.cwd()`  
  - `file`: the markdown file's dirname  
  - `path/to/cwd`: The exact cwd  
