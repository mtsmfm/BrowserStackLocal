# docker BrowserStackLocal

## Usage

```
docker run mtsmfm/browserstacklocal YOUR_ACCESS_KEY
```

YOUR_ACCESS_KEY is your access key for BrowserStack.

You can get your key on your settings page:

https://www.browserstack.com/accounts/settings

## docker-compose example

```yaml
version: '2'
services:
  web:
    image: nginx

  browserstacklocal:
    image: mtsmfm/docker-browserstacklocal
    command: $BS_AUTHKEY
    links:
      - web
```
