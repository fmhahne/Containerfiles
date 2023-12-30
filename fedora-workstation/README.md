# Fedora Workstation container

This container exists primarily so that I can check what packages I need to `override remove` from Silverblue to get RPM Fusion codecs.
Basically, watch the output of the following command:

```sh
podman run --rm -it localhost/fedora-workstation dnf group update --allowerasing multimedia --setop="install_weak_deps=False" --exclude=PackageKit-gstreamer-plugin
```
