# oneplus8t-5g-newradio | Changelog

## Note

Make sure you are on the latest commit on the `main` branch to see the most up to date version of this file.

## Changes

* **rev_0014** - `2021-08-25` - `MOD` - Reapplied mod to enable 5G NR NSA/SA on band n78 in EU/UK region. Moreover, included NSA and SA NR bands 1, 3, 28 and 40 over and above 78. These extra bands or now included based on information online of these bands being used throughout the EU/UK in addition to n78. However, these extra bands are untested / unverified, but should not cause any trouble by enabling them anyway. These changes / mod are applied on top of the latest changes by OnePlus provided in **rev_0013** so any latest changes by OnePlus are inherited here as well.
* **rev_0013** - `2021-08-25` - `OP8T_ORIGINAL` - Resynced original carrier policy files as originated from the `Oxygen OS 11.0.10.10.KB05BA` OTA released in August 2021. The main difference between this version and the previous original change in **rev_0011** is that OnePlus have corrected the PLMN list for H3G Ireland.
* **rev_0012** - `2021-08-18` - `MOD` - Reapplied mod to enable 5G NR on band n78 in EU/UK region. These changes / mod is applied on top of the latest changes by OnePlus provided in **rev_0011** so any latest changes by OnePlus are inherited here as well.
* **rev_0011** - `2021-08-18` - `OP8T_ORIGINAL` - Resynced original carrier policy files as originated from the `Oxygen OS 11.0.9.9.KB05BA` OTA released in August 2021. The main difference between this version and the previous original change in **rev_0009** is that OnePlus have added official support for 5G for the Italian operator `Iliad` (`222-50`) on bands n28 and n78 NSA.
* **rev_0010** - `2021-05-30` - `MOD` - Reapplied mod to enable 5G NR on band n78 in EU/UK region. Since **rev_0009** did not introduce changes from OnePlus, and since no additional mods were required compared to the previous mod, this revision is identical to **rev_0008**.
* **rev_0009** - `2021-05-30` - `OP8T_ORIGINAL` - Resynced original carrier policy files as originated from the `Oxygen OS 11.0.8.13.KB05BA` OTA released in May 2021. It is worth noting that these are identical to **rev_0007**, meaning OnePlus has not made any changes since the latest stable build. This revision is created for versioning reasons only.
* **rev_0008** - `2021-04-15` - `MOD` - Reapplied mod to enable 5G NR on band n78 in EU/UK region. These changes / mod is applied on top of the latest changes by OnePlus provided in **rev_0007** so any latest changes by OnePlus are inherited here as well.
* **rev_0007** - `2021-04-15` - `OP8T_ORIGINAL` - Resynced original carrier policy files as originated from the `Oxygen OS 11.0.8.12.KB05BA` OTA released in April 2021. It seems that OnePlus has enabled 5G in the Vietnamese region for PLMNs `452-01` (MobiFone), `452-02` (Vinaphone) and `452-04` (Viettel Mobile) on NSA bands 41 and 78. Since this puts back OnePlus' original file, this commit reverses the 5G mode for EU/UK region.
* **rev_0006** - `2021-02-23` - `MOD` - Reapplied mod to enable 5G NR on band n78 in EU/UK region. Since **rev_0005** did not introduce changes from OnePlus, and since no additional mods were required compared to the previous mod, this revision is identical to **rev_0002** and **rev_0004**.
* **rev_0005** - `2021-02-23` - `OP8T_ORIGINAL` - Resynced original carrier policy files as originated from the `Oxygen OS 11.0.7.10.KB05BA` OTA released in February 2021. It is worth noting that these are identical to **rev_0001** and **rev_0003**, meaning OnePlus has not made any changes. This revision is created for versioning reasons only.
* **rev_0004** - `2021-02-06` - `MOD` - Reapplied mod to enable 5G NR on band n78 in EU/UK region. Since **rev_0003** did not introduce changes from OnePlus, and since no additional mods were required compared to the previous mod, this revision is identical to **rev_0002**.
* **rev_0003** - `2021-02-06` - `OP8T_ORIGINAL` - Resynced original carrier policy files as originated from the `Oxygen OS 11.0.6.9.KB05BA` OTA released in January 2021. It is worth noting that these are identical to **rev_0001**, meaning OnePlus has not made any changes. This revision is created for versioning reasons only.
* **rev_0002** - `2021-01-03` - `MOD` - Enabled 5G NR on band n78 in EU/UK region.
* **rev_0001** - `2021-01-03` - `OP8T_ORIGINAL` - Initial commit - OnePlus 8T original files as extracted from stock OP8T device running `Oxygen OS 11.0.6.8.KB05BA` released on 29 December 2020.

***EOF***   
