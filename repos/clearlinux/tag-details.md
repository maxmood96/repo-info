<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `clearlinux`

-	[`clearlinux:base`](#clearlinuxbase)
-	[`clearlinux:latest`](#clearlinuxlatest)

## `clearlinux:base`

```console
$ docker pull clearlinux@sha256:a9bd36416228e71d16ae045e734ff1e82b54092e03c559b427e44d9dfac7b1f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clearlinux:base` - linux; amd64

```console
$ docker pull clearlinux@sha256:2c925954d454c68a298f3cd2f7387f4ab45ce15ce7389d17ba460980029f04b6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.2 MB (88217844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a89c37c194dcd4c623565c5b8bc8961ccb441ec0bc24636939e2f57114ef71e0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 Mar 2021 00:22:54 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Mon, 27 Jun 2022 17:23:08 GMT
ADD file:fc8b49709d53f894e6653f01ef5d972cc6fa237cf56cb5bc8305a6d1c313374d in / 
# Mon, 27 Jun 2022 17:23:09 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     grep root /usr/share/defaults/etc/shadow > /etc/shadow
# Mon, 27 Jun 2022 17:23:09 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:fcde559ee63b2f6e257ec99b58f002ee2c4cf864adb53a9e80b70d56e25a303e`  
		Last Modified: Mon, 27 Jun 2022 17:23:30 GMT  
		Size: 88.2 MB (88217627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f135ecea2b6a3ff1d645a73572bbdf770a6a0b5d9b67aa8ac79485d509f732a3`  
		Last Modified: Mon, 27 Jun 2022 17:23:18 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `clearlinux:latest`

```console
$ docker pull clearlinux@sha256:a9bd36416228e71d16ae045e734ff1e82b54092e03c559b427e44d9dfac7b1f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clearlinux:latest` - linux; amd64

```console
$ docker pull clearlinux@sha256:2c925954d454c68a298f3cd2f7387f4ab45ce15ce7389d17ba460980029f04b6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.2 MB (88217844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a89c37c194dcd4c623565c5b8bc8961ccb441ec0bc24636939e2f57114ef71e0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 Mar 2021 00:22:54 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Mon, 27 Jun 2022 17:23:08 GMT
ADD file:fc8b49709d53f894e6653f01ef5d972cc6fa237cf56cb5bc8305a6d1c313374d in / 
# Mon, 27 Jun 2022 17:23:09 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     grep root /usr/share/defaults/etc/shadow > /etc/shadow
# Mon, 27 Jun 2022 17:23:09 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:fcde559ee63b2f6e257ec99b58f002ee2c4cf864adb53a9e80b70d56e25a303e`  
		Last Modified: Mon, 27 Jun 2022 17:23:30 GMT  
		Size: 88.2 MB (88217627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f135ecea2b6a3ff1d645a73572bbdf770a6a0b5d9b67aa8ac79485d509f732a3`  
		Last Modified: Mon, 27 Jun 2022 17:23:18 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
