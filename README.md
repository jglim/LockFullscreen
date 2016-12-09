# Locking a user in fullscreen mode

I chanced upon a malicious webpage (the *"Your PC has a virus pls call Microsoft sort"*) where the victim was forced into fullscreen to prevent closing the page. 

Entering (and keeping the page in) fullscreen while showing a fake *minimize/maximize/close* ensures that the user cannot exit via "clicking the red x". Normally it would be possible to press `ESC` to exit fullscreen, but apparently **it is possible to bind `ESC` to launch fullscreen** as that is after all, a user action.

## Demo

Open the page and click anywhere. (Chrome only as I wrote that with the `-webkit` prefix).
Try to get out of fullscreen. 
To exit, click the "Toggle Lock" link once, then press ESC to exit.


## Thoughts

An action started by pressing/releasing `ESC` should not be allowed to `requestFullScreen`

---

*works on my Chrome 55.0.2883.75, Windows7, 09/12/2016*