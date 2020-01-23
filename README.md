# Rakudist Teddy::Bear

Example of Raku module installation customization using RakuDist

# Why?

* Your module installation need some external none Raku dependencies, not satisfied by `zef`
* Your module installation needs some custom configuration ( running database, installing configuration files, so on)

Here is RakuDist custom scenarios for the rescue!

# How?

1. [Write](https://github.com/melezhik/Sparrow6/blob/master/documentation/dsl.md) custom scenario

`mkdir .rakudist`

`nano .rakudist/sparrowfile`

```perl
package-install "sqlite-dev";
```

2. Commit `.rakudist` folder

`git add .rakudist && git push`


3. Run module install test remotely

`curl -d os=alpine -d project=melezhik/rakudist-teddy-bear http://repo.westus.cloudapp.azure.com/rakudist/api/run/:github`

# See also

[RakuDist](https://github.com/melezhik/RakuDist)

# Author 

Alexey Melezhik

