# crDroid OTA repo
OTA configuration for crDroidOTA (push OTA info when new build is ready for device users)

## Introduction ##
In order for a device to be OTA compliant, there are a few things to know. 

## XML structure ##
```
      <manufacturer id="Manufacturer">
            <DeviceCode>
                  <maintainer>MaintainerName</maintainer>
                  <devicename>DeviceName</devicename>
                  <filename>FileName</filename>
                  <buildtype>BuildType</buildtype>
                  <download>DownloadLink</download>
                  <changelog>ChangelogLink</changelog>
                  <gapps>GappsLink</gapps>
                  <forum>ForumLink</forum>
                  <paypal>PaypalLink</paypal>
                  <telegram>TelegramLink</telegram>
            </DeviceCode>
      </manufacturer>
```

### Mandatory XML tags ###
* **Manufacturer** - Add under existing manufacturer; Create manufacturer if required
* **DeviceCode** - Device code name
* **MaintainerName** - Maintainer name followed by prefered name in parenthesis
* **DeviceName** - Device name (not code name)
* **FileName** - Latest crdroid build name; OTA code parses date to check for new version
* **BuildType** - Nightly/Weekly/Final
* **DownloadLink** - Official download folder url (afh); Masked with goo.gl
* **ChangelogLink** - Changelog url (github)
* **GappsLink** - Google apps url (preferred: opengapps url)
* **ForumLink** - Forum url for discussions and support (preferred: xda url)
* All mandatory XML tags need to be there. Please leave blank in case some do not apply to you.

### Optional XML tags ###
* **PaypalLink** - paypal url (for donations)
* **TelegramLink** - telegram url (if you offer support via telegram - can be a group link or telegram.me link)

## Guidelines ##
* Check if manufacturer is already existing
* Check if published link is official
* Check if XML is intact
* Check if no extra / missing spaces

