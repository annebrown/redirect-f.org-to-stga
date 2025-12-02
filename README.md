# redirect-f.org-to-stga

## Description

Dummy GH repo configured with redirect rule to catch all requests from https://friendsofthegrove.org and redirect them to https://savethegroveagain.com.  This rule will be used by Vercel's built-in redirect tool for use with Vercel's Edge Network.

## Workflow

Create GH repo with `vercel.json`:

```json
{
  "redirects": [
    {
      "source": "/:path*",
      "destination": "https://savethegroveagain.com/:path*",
      "permanent": true
    }
  ]
}
```

Deploy repo on Vercel, then assign the new project to the FROM domain.

Next, open the project settings and open 'Domains'.  Edit the domain to be directed from.

Select `Redirect...` and `308 Permanent..` to ensure the SEO value (link equity) from the old domain is transferred to the new one.


