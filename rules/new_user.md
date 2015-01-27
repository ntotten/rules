---
gallery: true
categories:
- enrich profile
---
## Add Claim for New Users

This rule adds a claim to the profile indicating that this is the first time this user has logged in.

```js
function (user, context, callback) {
  if (context.stats.loginsCount === 1) {
    user.newuser = true;
  }
  callback(null, user, context);
}
```
