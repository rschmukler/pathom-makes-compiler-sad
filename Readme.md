# Readme

This repo demonstrates an interesting issue that I ran into w/ pathom + clojure.

Namely, requiring `pathom` from `user.clj` causes really long start-times. To reporoduce, 
just run

```
clojure
```


What's especially interesting, however, is that this isn't the case if you instead require the same code
via an eval:

```
rm src/user.clj
clojure -e "(require '[com.wsscode.pathom.connect])"
```
