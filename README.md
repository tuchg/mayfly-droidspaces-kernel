# mayfly Droidspaces kernel build

Private build repo for Xiaomi 12S (`mayfly`) on LineageOS 23.2 Android 16.

Goals:
- `baseline`: rebuild current Lineage kernel from the phone's `/proc/config.gz`.
- `droidspaces-min`: apply Droidspaces GKI 5.10 kABI patches and enable minimum configs for Droidspaces >= v5.9.5.

No automatic flashing. Artifacts are for manual inspection/testing only.

Current phone baseline:
- LineageOS: `23.2-20260605-NIGHTLY-mayfly`
- Kernel: `5.10.252-gki-gabcbe4b2bc10`
- Compiler from `/proc/config.gz`: Android clang `r563880c` / build `14054515`

Droidspaces-min changes:
```text
CONFIG_SYSVIPC=y
CONFIG_POSIX_MQUEUE=y
CONFIG_IPC_NS=y
CONFIG_PID_NS=y
CONFIG_DEVTMPFS=y
```

Patches from:
- https://github.com/Goldzxcbug/Droidspaces_Kernel_patch
