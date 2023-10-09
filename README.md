# extract_android_ota_payload.py

Extract an Android payload.bin file.

With the introduction of the A/B system update, the OTA file format changed.
This tool allows to extract and decompress the firmware images packed using the 'brillo' toolset.
Incremental firmware images are not supported (source_copy, source_bsdiff operations).


## Example (directory/sourcefile >> new directory)

```
python3 extract_android_ota_payload.py miui_CAMELLIANEEAGlobal_V14.0.3.0.TKSEUXM_3029e0954c_13.0.zip poco
```

```
Example output:
Extracting 'payload.bin' from OTA file...
Extracting 'boot.img'
Extracting 'dpm.img'
Extracting 'dtbo.img'
Extracting 'gz.img'
Extracting 'lk.img'
Extracting 'mcupm.img'
Extracting 'md1img.img'
Extracting 'pi_img.img'
Extracting 'preloader_raw.img'
Extracting 'product.img'
Extracting 'scp.img'
Extracting 'spmfw.img'
Extracting 'sspm.img'
Extracting 'system.img'
Extracting 'system_ext.img'
Extracting 'tee.img'
Extracting 'vbmeta.img'
Extracting 'vbmeta_system.img'
Extracting 'vbmeta_vendor.img'
Extracting 'vendor.img'
Extracting 'mi_ext.img'
```

## Dependencies

```
python-protobuf,bzcat,xzcat
```

## Fix this error

```
TypeError: Descriptors cannot not be created directly.
If this call came from a _pb2.py file, your generated code is out of date and must be regenerated with protoc >= 3.19.0.
If you cannot immediately regenerate your protos, some other possible workarounds are:
 1. Downgrade the protobuf package to 3.20.x or lower.
 2. Set PROTOCOL_BUFFERS_PYTHON_IMPLEMENTATION=python (but this will use pure-Python parsing and will be much slower).

```

## Apply fix

```
pip3 install 'protobuf<=3.20.1' --force-reinstall
```
