#Hack The Resume

## Development

1. Clone the repo
2. Clone gh-pages branch into dist directory

## Deployment

```bash
npm run build
cp -R public/* dist
cd dist
git add .
git commit -am "bump"
git push
```