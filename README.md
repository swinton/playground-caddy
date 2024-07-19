# `reverse-proxy-github-dotcom`
> A reverse proxy for GitHub.com using Caddy

## Purpose

Acts as a reverse proxy for API and Git traffic to GitHub.com, so you can analyze the traffic, e.g. to validate you are sending conditional API requests to GitHub, or to dig into API rate-limiting issues for a running GitHub integration.

## Usage

```shell
ngrok http 8080

caddy run --config ./Caddyfile --watch
```

## Analyze the logs

The logs can be analyzed via `jq`, which can handle a stream of JSON, e.g.

```shell
cat access.log | jq ".request,.status"
```

## Resources

https://chatgpt.com/share/62253048-df26-47c2-922f-a79b32959c51
