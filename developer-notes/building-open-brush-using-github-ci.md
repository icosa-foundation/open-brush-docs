# Setting up CI for Open Brush using Github Actions

This file will explain the various secrets used in creating formal builds. All of this is currently enabled on the icosa-foundation/open-brush repo, but in case a new repo ever needs to be created, this file explains what needs to be done to configure the repo.

By default, builds can be created with no secrets required, and this in fact what happens for builds from pull requests, where secrets are not exposed for security reasons.

## Unity Professional License

If you have a Unity Pro license, three secrets should be created: `UNITY_EMAIL`, `UNITY_PASSWORD`, and `UNITY_SERIAL`. If defined, these will be used instead of the default `UNITY_LICENSE` embedded in the github actions workflow, which is a free license. Using a professional license will suppress the splash screen, but otherwise, there is no functional difference.

## Google & Sketchfab Integration

As described in the main README, a `Secrets.asset` file should be used to store credentials for authenticating with Google and Sketchfab. For CI builds, create this file using the instructions in the README, and the add two Github secrets named `SECRETS_ASSET` and `SECRETS_ASSET_META` with the contents of `Assets/Secrets.asset` and `Assets/Secrets.asset.meta` respectively.

The CI build will automatically enable the use of this file instead of the default `SecretsExample.asset` in the repo. Do not attempt to commit your `Secrets.asset` file to source control!

## Signed Android Builds

When building Oculus Android builds, you can use your own keystore instead of the default "Debug" signing keys. This will allow you to upgrade your application, instead of needing to uninstall and reinstall it each time to avoid Signature Mismatch errors. To do this, create a keystore, and a key, and define the following secrets: `ANDROID_KEYSTORE_PASS`, `ANDROID_KEYALIAS_NAME`, and `ANDROID_KEYALIAS_PASS`. The keystore itself should be converted to base64 and stored in a secret named `ANDROID_KEYSTORE_BASE64`; you can get the value to store in the secret by using `base64 -i YOUR_KEYSTORE_NAME.keystore`.

## Oculus Publish

Pre-release builds and release builds will automatically be uploaded to Oculus for both Rift and Quest. This requires the following values to be defined (you can get the values from the Admin page in Oculus profile, or from the command line provided in the "Upload a build" button on a release channel. `OCULUS_QUEST_APP_ID`, `OCULUS_QUEST_APP_SECRET`, `OCULUS_RIFT_APP_ID`, `OCULUS_RIFT_APP_SECRET`

## Steam Publish

All pre-release builds are pushed to Steam, although Steam does not support updating the main release channel automatically upon formal builds. When a formal build is released, it will also be pushed as a pre-release; it should be promoted manually at https://partner.steamgames.com/apps/builds/1634870

To set up builds, first, create a new user for Steam with limited permissions. See https://partner.steamgames.com/doc/sdk/uploading#Build_Account for details. Note that multiple users can be created with the same email address. Do NOT connect this user to the mobile steam guard; it should only use email based OTPs.

After the user is created, create two github secrets: `STEAM_USERNAME` and `STEAM_PASSWORD`.

Then, download steamcmd locally, and run:

```
steamcmd +login $STEAM_USERNAME $STEAM_PASSWORD +quit
```

It will prompt you for a code; check the email associated with the account and enter the one time password.

After that, three more secrets need to be created. Check the steam directory (\~/Library/Application Support/Steam on Mac, I don't know for other platforms), and run `base64 -i config/config.vdf` and store the output as `STEAM_CONFIG_VDK`

If, at any point, Steam starts rejecting logins and sending a new OTP by email, simply use it locally, which will regenerate config.vdk. Upload the new version as a secret, and future build jobs will work again.

## Itch Publish

Both pre-release and release builds are pushed to Itch. The channel names are `<os>-beta` and `<os>-beta-experimental` for pre-release builds, and `<os>-release` and `<os>-release-experimental`.

To enable this, create a secret named `BUTLER_CREDENTIALS` with a valid API key from Itch.

