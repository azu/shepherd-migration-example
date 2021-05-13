# shepherd-migration-example

Migration Scripts

- [NerdWalletOSS/shepherd: A utility for applying code changes across many repositories.](https://github.com/NerdWalletOSS/shepherd)

## Usage

````
export GITHUB_TOKEN=$GITHUB_TOKEN
export PROJECT="./2021-04-25-githook"
npm run checkout -- "$PROJECT"
npm run apply -- "$PROJECT"
npm run commit -- "$PROJECT"
npm run push -- "$PROJECT"
npm run pr -- "$PROJECT"
npm run pr-status -- "$PROJECT"
````

Get PRs

```
npm run list -- "$PROJECT" | grep -o -e "https://github.com/[^/]*/[^/]*/pull/[0-9]*" > "$PROJECT/result.txt"
```

Merge PRs

```
cat "$PROJECT/result.txt" | xargs -IXXX gh pr merge -m XXX
```

## Author

- azu: [GitHub](https://github.com/azu), [Twitter](https://twitter.com/azu_re)

## License

MIT © azu
