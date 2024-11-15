brew install helmfile
helm plugin install https://github.com/databus23/helm-diff
helmfile apply -f helmfile.yml    or
helmfile apply