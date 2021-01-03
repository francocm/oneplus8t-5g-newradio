# oneplus8t-5g-newradio

> **Disclaimer**: Use the content in this repo at your own risk. The content shared is all based on personal experiments on personal devices, and not affiliated with OnePlus, Qualcomm, or any mobile operator.

> Hopefully this repository becomes redundant **soon**, by having OnePlus handle 5G properly in some future software OTA update.

## About
Qualcomm `carrier_policy` XML files for NR 5G fixes on OnePlus 8T.

This repository is inspired by the work described in the [OnePlus forums](https://forums.oneplus.com/threads/enable-5g-for-android-11-on-oneplus-8-series-and-oneplus-7-5g.1345340/).

Whilst the steps (not files) presented there are compatible with the OnePlus 8T, there were 2 main issues with the provided carrier policy files:

* The provided files had no effect on the OnePlus 8T, at least in the UK
* The provided files are severely outdated in terms of base
    * Based on OnePlus 7 / early 8 series
    * Based on XML version `16.11.21`, whereas this is based on the one provided in the EU stable OP8T firmware (`Oxygen OS 11.0.6.8.KB05BA` - 29 December 2020): `16.23.6` / `16.29.8`

## Usage

Follow the same instructions as indicated in [the original thread](https://forums.oneplus.com/threads/enable-5g-for-android-11-on-oneplus-8-series-and-oneplus-7-5g.1345340/), however use the following two files from this repository, under `qualcomm-modem-fs`:

* [/policyman/carrier_policy.xml](qualcomm-modem-fs/policyman/carrier_policy.xml)
* [/policyman/carrier_policy.xml_Subscription01](qualcomm-modem-fs/policyman/carrier_policy.xml_Subscription01)

### Extra steps

* Unfortunately the OP8T UI does not automatically update to show the 5G option. Therefore, the `*#*#4636#*#*` procedure as documented in the [original post](https://forums.oneplus.com/threads/enable-5g-for-android-11-on-oneplus-8-series-and-oneplus-7-5g.1345340/) has to be done upon every device reboot, by setting the value to `NR/LTE/TDSCDMA/GSM/WCDMA`. Failure to do so will not cause problems, but 5G will not work.

## Implementation

This change solves the problem by enabling NR 5G **always** in the EU/UK region. The rationale  here is that:
* NR band 78 is allowed throughout the EU/UK space
* The lack of support should be dependant on the operator offering it and not the phone deciding it - if there is no operator on a particular band, the phone will simply just not connect to it and fallback to other radios (LTE, WCDMA, etc), making it transparent to the user anyway
* The EU/UK region definition is as pre-defined already in the original policy files, under `europe_mccs`.

The philosophy here is: *a phone should not wait until its manufacturer puts the respective operator on the allow list for 5G to work. Instead, it should dynamically work based on available implementations in the user's context*.

## Additional Info

### Tested on
* OnePlus 8T KB2003 (EU Model - 8GB RAM / 128GB ROM)

### Tested regions / operators
* UK
    * O2

### Enabled NR bands

> **Note**: The `carrier_policy.xml*` files start the band count from 0 not 1. As an example, band 78 is listed as 77 in the XML files.

* n78

### Additional points

* The initial commit contains the files as provided in the original firmware, without any modifications. Refer to [CHANGELOG.md](CHANGELOG.md) for changes that were applied onto it.
* The related file [.version.json](.version.json) describes the files at that particular commit, and the revision number within it is aligned with [CHANGELOG.md](CHANGELOG.md). The possible values for `type` are:
    * `OP8T_ORIGINAL` - As extracted from the stock OnePlus 8T modem partition
    * `MOD` - Modified version
* Improvements or suggestions welcome. Please do so either via the issue tracker or via pull requests.

***EOF***   
