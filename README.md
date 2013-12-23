# Heroku buildpack: Meteorite (DEBUG MODE)

This buildpack is forked from [https://github.com/oortcloud/heroku-buildpack-meteorite.git](https://github.com/oortcloud/heroku-buildpack-meteorite.git)

Due to some reasons, sometimes the minified codes cannot work. This build use the debug mode, in which codes won't be minified.

## Usage

```bash
heroku create --stack cedar --buildpack https://github.com/waitingkuo/heroku-buildpack-meteorite-debug-mode.git
```

Then `git push` to heroku as usual.

## NOTES

You need to set the `ROOT_URL` environment variable:

```bash
heroku config:add ROOT_URL=your.domain.com
```

You can specify meteor settings by setting the `METEOR_SETTINGS` environment variable:

```bash
heroku config:add METEOR_SETTINGS='{"herp":"derp"}'
```


You need to have a verified account so the buildpack can add a `mongohq:sandbox` addon.
