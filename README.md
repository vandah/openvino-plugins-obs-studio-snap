# Snap for Intel OpenVINO™ AI plugins for OBS Studio

This snap delivers [OpenVINO™ AI
plugins](https://github.com/intel/openvino-plugins-for-obs-studio) to the [OBS
Studio snap](https://snapcraft.io/obs-studio).

## Installation

### Get OBS Studio

Right now, this snap only works with a not yet released version of OBS Studio
that you can find
[here](https://github.com/vandah/obs-studio/tree/core24-content-snaps).

### Optional: Intel GPU and NPU support

These plugins can also take advantage of Intel GPUs and NPUs if one or both are
available on your machine. To enable either, first ensure you are in the
`render` Unix group and re-login to your session:

```shell
sudo usermod -a -G render $USER
```

For Intel NPU support, you also need to install the `intel-npu-driver` snap:

```shell
sudo snap install intel-npu-driver
```

### Install from the Store

```shell
sudo snap install openvino-plugins-obs-studio
```

### Connect to the OBS Studio snap

```shell
sudo snap connect obs-studio:obs-plugins openvino-plugins-obs-studio:obs-plugins
```
