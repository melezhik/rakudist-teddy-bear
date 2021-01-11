# Rakudist Teddy::Bear

An example of Raku module installation customization using RakuDist

# Build status

![build status](http://161.35.142.50/badge/project/teddy-bear)

# Why?

* Your module installation/test needs some external none Raku dependencies, not satisfied by `zef`
* Your module installation/test needs some custom configuration ( running database, installing configuration files, so on)

Here is RakuDist custom scenarios for the rescue!

# How?

1. [Write](https://github.com/melezhik/Sparrow6/blob/master/documentation/dsl.md) custom scenario

`mkdir .rakudist`

`nano .rakudist/sparrowfile`

```
package-install "sqlite-dev";
```

2. Commit `.rakudist` folder

`git add .rakudist && git push`


3. Run module install test remotely

`curl -d os=alpine -d thing=https://github.com/melezhik/rakudist-teddy-bear http://rakudist.raku.org/`

# See also

[RakuDist](https://github.com/melezhik/RakuDist)

# Author 

Alexey Melezhik

