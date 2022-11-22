# Daart Android Advertisement SDK
## Shows Interstitial and Banner ads in Android platforms.

Add it in your root build.gradle at the end of repositories:
```sh
    allprojects {
        repositories {
          maven { url 'https://jitpack.io' }
        }
    }
```

Add the dependency and app/build.gradle
```sh
    dependencies {
        implementation 'com.github.soheilazimi2017:DaartAds:alpha'
    }
```
## How to implement

### initialize SDK
DaartAds.initialize("PLACE_YOUR_TOKEN");

### Show banner ad

   DaartAds banner = findViewById(R.id.testBanner);
   banner.setAdSize(AdSize.BANNER);

   banner.loadAd(new AdListener() {
      @Override
      public void onLoad(com.daartads.sdk.model.BannerAd ad) {
          Toast.makeText(MainActivity.this, "banner ad loaded success!", Toast.LENGTH_SHORT).show();
      }

   @Override
   public void onError(Exception e) {
       Toast.makeText(MainActivity.this, "failed to load banner ad!", Toast.LENGTH_SHORT).show();
   }
   });

