### Prebuilt Apps Repo
You can add this prebuilt apps to any custom ROM on any device .

Add the below line in your `device.mk` :
```
# Prebuilt Apps
$(call inherit-product, packages/apps/Prebuilts/config.mk)
```
Then add/delete the desired apps in the `config.mk` file in this repo.
