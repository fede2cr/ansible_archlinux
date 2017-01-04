# Installs an Arch Linux Desktop

This is an ansible recipe I use to rebuild my Arch desktop, so it's quite personalized, but I hope you can use it to base off and build your own.

## TODO
- [x] The ansible pacman module seems to fail idempotency tests. I need to debug if this is a thing with one of my packages or in general with the module. Solution: It seem I needed to replace "libreoffice" for "libreoffice-fresh" to solve idempotency on the pacman module.
- [ ] Add automated testing. Partial. About half of the recipes are being tested.
