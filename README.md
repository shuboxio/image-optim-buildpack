# Heroku Image-Optim Buildpack

Add binaries for image-optim on Heroku, can be used with heroku-buildpack-multi.

Built-in support for [image-optim](https://github.com/toy/image_optim) gem, creation of `.image-optim.yml` config file.

Binaries in this buildpacks :

- `cwebp`
- `dwebp`
- `advpng`
- `gifsicle`
- `jpegoptim`
- `jpegtran`
- `optipng`
- `pngcrush`

Binaries are in this git repo in `vendor/image-optim`

On compilation :

- Binaries are copied into vendor/image-optim
- Symlink to binaries is added to ensure next buildpacks will have binaries available
- vendor/image-optim is added to PATH through a .profile.d script
- Add config file .image-optim.yml if Gemfile present
- Version of each binaries is displayed


