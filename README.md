# harf-auth

Return page for Harf's Slack sign-in. Slack requires an https redirect for
distributed apps; this page forwards Slack's `?code=…&state=…` to the Harf
app listening on `http://localhost:8471/harf/slack` on the user's own Mac.
It stores and sends nothing anywhere else. PKCE keeps the code useless to
anyone without the verifier held by the app.
