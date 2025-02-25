# dokku-git-rev 

Lets you fetch the git revision hash used to build the app from the `APP_REVISION`

## requirements

- dokku 0.4.0+
- docker 1.8.x

## installation

```shell
# on 0.3.x
cd /var/lib/dokku/plugins
git clone https://github.com/ecosyste-ms/dokku-git-rev.git dokku-git-rev
dokku plugins-install

# on 0.4.x+
dokku plugin:install https://github.com/ecosyste-ms/dokku-git-rev.git --name dokku-git-rev
```

## hooks

This plugin provides hooks:

* `receive-app`: captures the current `APP_REVISION`

## usage

On git deploys, the `APP_REVISION` environment variable will be set for your application and be available for your usage.
