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

The placeholder repo is deployed on Vercel, with the new project assigned to the FROM domain.

The project then uses Vercel's redirect tool.
