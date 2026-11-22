# adiskreader-testfiles

Test files of [adiskreader](https://github.com/skelsec/adiskreader) which are too large to be kept in its git repository.

The files are attached to the [releases](https://github.com/skelsec/adiskreader-testfiles/releases) of this repository.
The tests of adiskreader download the ones they need to `tests/testfiles` and check them against the SHA-256 values
pinned in `tests/config.py` (the same values are in `SHA256SUMS` here).

All of them hold generated test data only. They were made with the scripts in the `tests` folder of adiskreader:

| File | Contents | Made by |
|---|---|---|
| `adiskreader_diff_fixtures.zip` | differencing VHD / VHDX chains made by Windows | `make_diff_vhd.ps1` |
| `adiskreader_iso_fixtures.zip` | ISO9660, Joliet and UDF disc images made by Windows (IMAPI2) | `make_iso.ps1` |
| `adiskreader_qemu_fixtures.zip` | QCOW2 and VDI disks made by qemu and VirtualBox | `make_qemu_fixtures.py` |
| `adiskreader_wim_fixtures.zip` | WIM, split WIM and ESD files made by Windows (DISM) | `make_wim.ps1` |
| `vbk_fixtures.zip` | Veeam Backup & Replication 13 backup files (VBK, VIB, VBM) of a small test VM | `make_vbk.ps1` |
| `ntfs_test_*.vhdx.gz`, `ntfs_test_*.vmdk.gz` | the NTFS test image of adiskreader converted by qemu-img and VMware Workstation | |

The password in the manifest of `vbk_fixtures.zip` is a throwaway one generated for the encrypted test backup.
