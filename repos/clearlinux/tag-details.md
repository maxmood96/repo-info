<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `clearlinux`

-	[`clearlinux:base`](#clearlinuxbase)
-	[`clearlinux:latest`](#clearlinuxlatest)

## `clearlinux:base`

```console
$ docker pull clearlinux@sha256:c829b4eb00c46aab8a294f9cd3aa6d372acd3c4dc72a164c9d22758e26c142c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clearlinux:base` - linux; amd64

```console
$ docker pull clearlinux@sha256:df43130e0ed9e47d5485c804b32c7b1c19a3db4ffb0411232186e8645b00efe1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.1 MB (87147706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1356e8a4e1e24ce9d404627c30644609135d13665f2496254adf78a3dc44a0da`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 Mar 2021 00:22:54 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Mon, 21 Feb 2022 18:23:44 GMT
ADD file:370e8fadc567f5e2675f109570a67289133239d82caf10616fcdff0429521030 in / 
# Mon, 21 Feb 2022 18:23:46 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     grep root /usr/share/defaults/etc/shadow > /etc/shadow
# Mon, 21 Feb 2022 18:23:46 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:6939b6f5b04999dfa8b5db730960fbc5002309f8be609e98a01aa708e2cb98d0`  
		Last Modified: Mon, 21 Feb 2022 18:24:07 GMT  
		Size: 87.1 MB (87147489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41099a8d39bb74e6f2d1e39c3f2ad21c181c3a28ca78f858c00b7015fac47096`  
		Last Modified: Mon, 21 Feb 2022 18:23:55 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `clearlinux:latest`

```console
$ docker pull clearlinux@sha256:c829b4eb00c46aab8a294f9cd3aa6d372acd3c4dc72a164c9d22758e26c142c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clearlinux:latest` - linux; amd64

```console
$ docker pull clearlinux@sha256:df43130e0ed9e47d5485c804b32c7b1c19a3db4ffb0411232186e8645b00efe1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.1 MB (87147706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1356e8a4e1e24ce9d404627c30644609135d13665f2496254adf78a3dc44a0da`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 Mar 2021 00:22:54 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Mon, 21 Feb 2022 18:23:44 GMT
ADD file:370e8fadc567f5e2675f109570a67289133239d82caf10616fcdff0429521030 in / 
# Mon, 21 Feb 2022 18:23:46 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     grep root /usr/share/defaults/etc/shadow > /etc/shadow
# Mon, 21 Feb 2022 18:23:46 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:6939b6f5b04999dfa8b5db730960fbc5002309f8be609e98a01aa708e2cb98d0`  
		Last Modified: Mon, 21 Feb 2022 18:24:07 GMT  
		Size: 87.1 MB (87147489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41099a8d39bb74e6f2d1e39c3f2ad21c181c3a28ca78f858c00b7015fac47096`  
		Last Modified: Mon, 21 Feb 2022 18:23:55 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
