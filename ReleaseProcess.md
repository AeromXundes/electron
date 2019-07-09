Creating an electron release

```
python ./script/create-dist.py
npm run prepare-npm
npm run create-npm-package
```

zip file is in /dist
npm package is in the root.

create sha256 of zip file in this format:
```
<hash> *<filename>
```
Name it like so: `SHASUMS256.txt-<version>`

for example:
```
618788d5a1a8bb2eaee7a1f524afcb9a860a09199af0f2eb382a237bf28ebe55 *electron-v2.0.19-beta.1-win32-x64.zip
```
Name: `SHASUMS256.txt-2.0.19-beta.1`

The npm package needs to be uploaded to your favorite npm host.
The zip file also needs to be uploaded, but it also needs to have the sha file as a sibling file.
