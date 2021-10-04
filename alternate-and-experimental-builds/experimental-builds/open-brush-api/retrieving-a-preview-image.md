# Retrieving a preview image

[http://localhost:40074/cameraview](http://localhost:40074/cameraview) is a convenient endpoint you can call to get the current desktop view as a png. It will either be the headset or monoscopic user view - or the spectator camera if that is active.

Image size is based on the current desktop window size. Combined with API commands to move the spectator camera around, this can be used to automate complex renders or your own custom camera paths.

In a web page you can use this for a simple \(nearly\) realtime preview:

```text
function refreshCameraPreview() {
    var image = document.getElementById("cameraPreview");
    image.src = "http://localhost:40074/cameraview?t=" + new Date().getTime();
}
setInterval(refreshCameraPreview, 1000);
```

Be careful calling it too often as it's not terribly efficient and will slow down Open Brush. The above example refreshes once per second. We plan to implement a much more efficient WebRTC streaming endpoint at some stage but that will be more complex for client scripts to implement so this simple endpoint will still remain useful.

If you want to access the preview image from a different device to the one running Open Brush, you'll need to allow external connections to the API: [https://docs.openbrush.app/alternate-and-experimental-builds/experimental-builds/open-brush-api\#how-do-i-configure-it](https://docs.openbrush.app/alternate-and-experimental-builds/experimental-builds/open-brush-api#how-do-i-configure-it)



