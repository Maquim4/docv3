# About Us

We are Schlockchain, thought leaders in innovation.

```go
package main

import (
	"net/http"

	"golang.org/x/oauth2"
	"golang.org/x/oauth2/google"
)

func main() {
	client := &http.Client{
		Transport: &oauth2.Transport{
			// Fetch from Google Compute Engine's metadata server to retrieve
			// an access token for the provided account.
			// If no account is specified, "default" is used.
			// If no scopes are specified, a set of default scopes
			// are automatically granted.
			Source: google.ComputeTokenSource("", "https://www.googleapis.com/auth/bigquery"),
		},
	}
	client.Get("...")
}
```
