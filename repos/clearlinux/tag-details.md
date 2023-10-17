<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `clearlinux`

-	[`clearlinux:base`](#clearlinuxbase)
-	[`clearlinux:latest`](#clearlinuxlatest)

## `clearlinux:base`

```console
$ docker pull clearlinux@sha256:818fb569e4f74a017089471084517ea8422f67bc9dfbf166d94d53051d55b196
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clearlinux:base` - linux; amd64

```console
$ docker pull clearlinux@sha256:cf9347a5cd051445f9f0ee92496f9cd4bfc70199028455658abd51445f6c65a5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.8 MB (67836051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:712b5c4227a8caf0ee01a90b4e4744d8fa6dca2e2de64ed544d454fa9adc7420`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 Mar 2021 00:22:54 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Tue, 17 Oct 2023 01:23:08 GMT
ADD file:6bf1fbd3bd6c288a993193ab0ce0eda6e68311a29bed93606c5458ae3f364495 in / 
# Tue, 17 Oct 2023 01:23:09 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     grep root /usr/share/defaults/etc/shadow > /etc/shadow
# Tue, 17 Oct 2023 01:23:10 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:dedd449878ea180264fda0a860e89126b1725ea19146146c018550a2475babc7`  
		Last Modified: Tue, 17 Oct 2023 01:23:28 GMT  
		Size: 67.8 MB (67835834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:138d715ae1965525a28ea653512c24a8a9711dfea6136b95573b0e8b4a159ab9`  
		Last Modified: Tue, 17 Oct 2023 01:23:20 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `clearlinux:latest`

```console
$ docker pull clearlinux@sha256:818fb569e4f74a017089471084517ea8422f67bc9dfbf166d94d53051d55b196
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clearlinux:latest` - linux; amd64

```console
$ docker pull clearlinux@sha256:cf9347a5cd051445f9f0ee92496f9cd4bfc70199028455658abd51445f6c65a5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.8 MB (67836051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:712b5c4227a8caf0ee01a90b4e4744d8fa6dca2e2de64ed544d454fa9adc7420`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 Mar 2021 00:22:54 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Tue, 17 Oct 2023 01:23:08 GMT
ADD file:6bf1fbd3bd6c288a993193ab0ce0eda6e68311a29bed93606c5458ae3f364495 in / 
# Tue, 17 Oct 2023 01:23:09 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     grep root /usr/share/defaults/etc/shadow > /etc/shadow
# Tue, 17 Oct 2023 01:23:10 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:dedd449878ea180264fda0a860e89126b1725ea19146146c018550a2475babc7`  
		Last Modified: Tue, 17 Oct 2023 01:23:28 GMT  
		Size: 67.8 MB (67835834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:138d715ae1965525a28ea653512c24a8a9711dfea6136b95573b0e8b4a159ab9`  
		Last Modified: Tue, 17 Oct 2023 01:23:20 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
