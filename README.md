# renovate_bugreport1

https://github.com/renovatebot/renovate/discussions/26761

Dart packages are getting update info from `pub.dev` instead of the `hosted:` repository version that should be used.

https://docs.renovatebot.com/modules/datasource/dart/ <-- here I've read that it does support custom registry so it should work.

https://git.mrcyjanek.net/mrcyjanek/anonero/pulls/2 <-- here is PR that renovate created 
as you can see in the PR made by renovate:

```diff
   mobile_scanner:
     hosted: https://git.mrcyjanek.net/api/packages/mrcyjanek/pub/
-    version: 3.5.5
+    version: 3.5.6
```

There is [no version 3.5.6 in the hosted version](https://git.mrcyjanek.net/mrcyjanek/-/packages/pub/mobile_scanner/3.5.5) (I've forked and edited only version 3.5.5.


- minimal repo: https://git.mrcyjanek.net/mrcyjanek/renovate-bugreport1 (or https://github.com/mrcyjanek/renovate-bugreport1)
- commit causing problem: https://git.mrcyjanek.net/mrcyjanek/renovate-bugreport1/commit/22fc52d49d261b215c760cd55da1bb9d898e6769
- PR: https://git.mrcyjanek.net/mrcyjanek/renovate-bugreport1/pulls/1 (initial one, you can see the version of mobile_scanner getting bumped.
