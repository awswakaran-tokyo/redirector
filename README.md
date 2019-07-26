# Redirector

Redirect from https://awswakaran.tokyo to https://www.awswakaran.tokyo

## How to customize

1. Click `Use this template` on GitHub and fork it.
2. Modify .firebaserc *1
3. Modify firebase.json *2
4. Run `yarn; yarn firebase deploy`

#### .firebaserc *1

```diff
{
  "projects": {
-    "default": "awswakaran-tokyo"
+    "default": "your-firebase-project-name"
  }
}
```

#### firebase.json *2

```diff
{
  "hosting": {
    "public": "public",
    "ignore": [
      "firebase.json",
      "**/.*",
      "**/node_modules/**"
    ],
    "redirects": [
      {
        "source": "/",
-        "destination": "https://www.awswakaran.tokyo/",
+        "destination": "https://your-redirect-domain.example.com/",
        "type": 301
      },
      {
        "source": "/:path*",
-        "destination": "https://www.awswakaran.tokyo/:path",
+        "destination": "https://your-redirect-domain.example.com/:path",
        "type": 301
      }
    ]
  }
}
```

## LICENCE

MIT
