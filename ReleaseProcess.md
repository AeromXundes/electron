Creating an electron release

```
python ./script/create-dist.py -v
npm run create-hash
npm run prepare-npm
npm run create-npm-package
```

zip file and hash file are in /dist
npm package is in the root.

The npm package needs to be uploaded to your favorite npm host.
The zip file also needs to be uploaded, but it also needs to have the sha file as a sibling file.
