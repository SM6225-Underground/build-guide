## Add this line to your manifest ROM before ```repo sync```:

Sepolicy line:
```
    <project path="device/qcom/sepolicy_vndr/sm6225" name="SM6225-Underground/device_qcom_sepolicy_vndr" remote="github" revision="lineage-21" />
```
hardware/qcom-caf/common line:
```
    <linkfile src="os_pickup_audio-ar.mk" dest="hardware/qcom-caf/sm6225/audio/Android.mk" />
    <linkfile src="os_pickup_qssi.bp" dest="hardware/qcom-caf/sm6225/Android.bp" />
    <linkfile src="os_pickup.mk" dest="hardware/qcom-caf/sm6225/Android.mk" />
```

HALs line:
```
  <project path="hardware/qcom-caf/sm6225/audio/agm" name="SM6225-Underground/vendor_qcom_opensource_agm" remote="github" revision="lineage-21" />
  <project path="hardware/qcom-caf/sm6225/audio/pal" name="SM6225-Underground/vendor_qcom_opensource_arpal-lx" remote="github" revision="lineage-21" />
  <project path="hardware/qcom-caf/sm6225/audio/primary-hal" name="SM6225-Underground/hardware_qcom_audio-ar" remote="github" revision="lineage-21" />
  <project path="hardware/qcom-caf/sm6225/data-ipa-cfg-mgr" name="SM6225-Underground/vendor_qcom_opensource_data-ipa-cfg-mgr" remote="github" revision="lineage-21" />
  <project path="hardware/qcom-caf/sm6225/dataipa" name="SM6225-Underground/vendor_qcom_opensource_dataipa" remote="github" revision="lineage-21" />
  <project path="hardware/qcom-caf/sm6225/display" name="SM6225-Underground/hardware_qcom_display" remote="github" revision="lineage-21" />
  <project path="hardware/qcom-caf/sm6225/media" name="SM6225-Underground/hardware_qcom_media" remote="github" revision="lineage-21" />
```

Adapt new platform to your BoardConfigQcom.mk ROM:
- https://github.com/SM6225-Underground/hardware_qcom-caf_common/commit/b682c8d6a2a1794ba74ac4529f5dc61aba1f7ced

- https://github.com/SM6225-Underground/hardware_qcom-caf_common/commit/215ad7ce3c07b0138158a4478b178115c4a9583e

- https://github.com/SM6225-Underground/hardware_qcom-caf_common/commit/7bfeadc6911b4422e66b889cb487ee0efd2f61a7

- https://github.com/SM6225-Underground/hardware_qcom-caf_common/commit/1d7c1ed0985ae4d815de67762d3ec505f8ac07a9

- https://github.com/SM6225-Underground/hardware_qcom-caf_common/commit/94efc0911bd439ae0a70a5a93a18e71ced285141

- https://github.com/SM6225-Underground/hardware_qcom-caf_common/commit/d88b407057a85135bc236d7222dcc143d830fd9d

Clone device tree to your initialize repo, done!!

Compile Now!!