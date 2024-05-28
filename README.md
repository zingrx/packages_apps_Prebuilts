### Prebuilt Apps Repo
You can add this prebuilt apps to any custom ROM on any device.

Start by cloning this repo to your directory by either one of the two methods below:
1. Direct clone (this requires manual fetching of updates by `git pull` in the cloned folder)
   ```
   git clone https://github.com/zingrx/packages_apps_Prebuilts packages/apps/Prebuilts
   ```
   
2. Add it to `.repo/local_manifest.xml` file (this method provides auto updates with `repo sync`). Create the file if it's found.
   ```
   <remote name="zingrx" fetch="https://github.com/zingrx" />
   <project path="packages/apps/Prebuilts" name="packages_apps_Prebuilts" remote="zingrx" revision="main" />
   ```
   Then run `repo sync --force-sync packages/apps/Prebuilts`.

Add the below line in your `device.mk` :
```
# Prebuilt Apps
$(call inherit-product, packages/apps/Prebuilts/config.mk)
```
Then add/delete the desired apps in the `config.mk` file in this repo.
