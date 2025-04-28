<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `clearlinux`

-	[`clearlinux:base`](#clearlinuxbase)
-	[`clearlinux:latest`](#clearlinuxlatest)

## `clearlinux:base`

```console
$ docker pull clearlinux@sha256:d3d36bfec72876f0e2b3a066ca472748f7c9ed73384ccf721d17193572b200e6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `clearlinux:base` - linux; amd64

```console
$ docker pull clearlinux@sha256:7dc6bdad92db1f0cdaf20e25661ee8ed939173bf87a483c8aae68377505028ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.7 MB (72737979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1ad7449fffbffd8f9b906a1a3be6b6a5c53db7f2cd77ac8ae6e9e759083a1d1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 24 Apr 2025 19:00:41 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Thu, 24 Apr 2025 19:00:41 GMT
ADD base.tar.xz / # buildkit
# Thu, 24 Apr 2025 19:00:41 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     echo 'root:!:::::::' > /etc/shadow # buildkit
# Thu, 24 Apr 2025 19:00:41 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:a8138b59d65c720a05d68d7171c89bea32b008f1ab895bcea9d3f8882767a634`  
		Last Modified: Mon, 28 Apr 2025 17:56:31 GMT  
		Size: 72.7 MB (72737766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:341301c720b99f411dce828d50ba43e13e3cb7f58c80a466b11eabe74da3a6c5`  
		Last Modified: Mon, 28 Apr 2025 17:56:30 GMT  
		Size: 213.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clearlinux:base` - unknown; unknown

```console
$ docker pull clearlinux@sha256:f3212f3e3951e4122b5bb14dc8cfa5919d9505b7c360608a338a480aa24ec649
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 KB (6274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d8693767a38d324c6f3ed421cf69b5f3cac96279ee2d572ff7c05890818fb7d`

```dockerfile
```

-	Layers:
	-	`sha256:386fe9226101ded6ca3f82559edf7e80ed5414fe287a39ddd7306bffb6a50493`  
		Last Modified: Mon, 28 Apr 2025 17:56:30 GMT  
		Size: 6.3 KB (6274 bytes)  
		MIME: application/vnd.in-toto+json

## `clearlinux:latest`

```console
$ docker pull clearlinux@sha256:d3d36bfec72876f0e2b3a066ca472748f7c9ed73384ccf721d17193572b200e6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `clearlinux:latest` - linux; amd64

```console
$ docker pull clearlinux@sha256:7dc6bdad92db1f0cdaf20e25661ee8ed939173bf87a483c8aae68377505028ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.7 MB (72737979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1ad7449fffbffd8f9b906a1a3be6b6a5c53db7f2cd77ac8ae6e9e759083a1d1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 24 Apr 2025 19:00:41 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Thu, 24 Apr 2025 19:00:41 GMT
ADD base.tar.xz / # buildkit
# Thu, 24 Apr 2025 19:00:41 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     echo 'root:!:::::::' > /etc/shadow # buildkit
# Thu, 24 Apr 2025 19:00:41 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:a8138b59d65c720a05d68d7171c89bea32b008f1ab895bcea9d3f8882767a634`  
		Last Modified: Mon, 28 Apr 2025 17:56:31 GMT  
		Size: 72.7 MB (72737766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:341301c720b99f411dce828d50ba43e13e3cb7f58c80a466b11eabe74da3a6c5`  
		Last Modified: Mon, 28 Apr 2025 17:56:30 GMT  
		Size: 213.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clearlinux:latest` - unknown; unknown

```console
$ docker pull clearlinux@sha256:f3212f3e3951e4122b5bb14dc8cfa5919d9505b7c360608a338a480aa24ec649
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 KB (6274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d8693767a38d324c6f3ed421cf69b5f3cac96279ee2d572ff7c05890818fb7d`

```dockerfile
```

-	Layers:
	-	`sha256:386fe9226101ded6ca3f82559edf7e80ed5414fe287a39ddd7306bffb6a50493`  
		Last Modified: Mon, 28 Apr 2025 17:56:30 GMT  
		Size: 6.3 KB (6274 bytes)  
		MIME: application/vnd.in-toto+json
