# Rakudist Teddy::Bear

Example of Raku module with RakuDist custom scenario

# Why?

* Your module installation need some external none Raku dependencies, not satisfied by `zef`
* Your module installation needs some custom configuration ( running database, installing configuration files, so on)

Here is RakuDist custom scenarios for the rescue!

# How?

## Set custom scenario


`mkdir .rakudist`

`nano .rakudist/sparrowfile`

```perl
package "sqlite-dev";
```

## Commit `.rakudist` folder

`git add .rakudist && git push`


# Run remote test

`curl -d os=alpine -d project=melezhik/rakudist-teddy-bear http://repo.westus.cloudapp.azure.com/rakudist/api/run/:github`

# Author 

Alexey Melezhik

