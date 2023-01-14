# Prerquisit:
`jq` install on mac using following command.

```
brew install jq
```

## For required packages:
```
composer require $(composer show -s --format=json | jq '.requires | keys | map(.+" ") | add' -r)
```


## For development packages:
```
composer require --dev $(composer show -s --format=json | jq '.devRequires | keys | map(.+" ") | add' -r)
```




Credits:
https://kau-boys.com/3152/web-development/update-all-composer-dependencies-to-their-latest-versions
