MicroG and FDroid for Custom ROMs
=================================

Download FDroid and MicroG prebuilt APKs for inclusion in a custom ROM. This
also downloads the GPG armor files of the packages to verify them.

Getting the packages
--------------------

* Add it to your local manifest:

      <?xml version="1.0" encoding="UTF-8"?>
      <manifest>
          <!-- MicroG -->
          <project name="cryptomilk/android_vendor_microg"
                   path="vendor/microg"
                   remote="github"
                   revision="master" />
      </manifest>

* After downloading to to the vendor dir and get the packages:

      cd vendor/microg
      ./get_packages.sh

* Add it to your device.mk

      $(call inherit-product, vendor/microg/microg-vendor.mk)
