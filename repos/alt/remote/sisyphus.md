## `alt:sisyphus`

```console
$ docker pull alt@sha256:9f81bd7c4628ce002bbb6f7fa5e9bf9d33e2ef8e6ade1312273fcfb589c7b2fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `alt:sisyphus` - linux; amd64

```console
$ docker pull alt@sha256:c52ff94a4e137c3ed2defb8723b2dd4dbc14e177cf8898c929d9e2401c36db56
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.0 MB (40956570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04643c8d43c5f4e2303416ed29925cb6737606367a5a6bb26ff265ba1b77f8bb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 11 Aug 2020 20:19:59 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Mikhail Gordeev <obirvalger@altlinux.org]
# Mon, 01 Feb 2021 20:20:13 GMT
ADD file:945eee9ef7da82ce6c4cb7b1a5593a9dbc158b890b7c5c374ffc5f843d42da83 in / 
# Mon, 01 Feb 2021 20:20:14 GMT
RUN true > /etc/security/limits.d/50-defaults.conf
# Mon, 01 Feb 2021 20:20:14 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:aeab78fcd50dbef8be4ed043471f76dc8eb4ff42a22b56c426af3d54a69a9f6c`  
		Last Modified: Mon, 01 Feb 2021 20:20:56 GMT  
		Size: 41.0 MB (40956382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76836a64da353d147fc64b259d5195722fa3b60f30fa46c6da24762b02c183ac`  
		Last Modified: Mon, 01 Feb 2021 20:20:49 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `alt:sisyphus` - linux; arm64 variant v8

```console
$ docker pull alt@sha256:f2dc2f3c427496e4727dd091960300952657d2520fa7c758f193966b05568b05
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.9 MB (39896257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f08c7724a76e61795d2f4b3a766aeeff616d725087727e3363339d72d9b1776`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 11 Aug 2020 19:40:59 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Mikhail Gordeev <obirvalger@altlinux.org]
# Mon, 01 Feb 2021 20:53:10 GMT
ADD file:edfe676f051f130b01931d226f8241ef506a84c37dc5f5dedd7861f7c6cb91a4 in / 
# Mon, 01 Feb 2021 20:53:14 GMT
RUN true > /etc/security/limits.d/50-defaults.conf
# Mon, 01 Feb 2021 20:53:14 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:c1321b7cb80b8ced4b876f8f7585cf5597481f56ea71517968230abaa02ee130`  
		Last Modified: Mon, 01 Feb 2021 20:53:51 GMT  
		Size: 39.9 MB (39896065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:432752a61467df95d80e892037ec61b723ec953ff5582abd7be91d9e389eefdf`  
		Last Modified: Mon, 01 Feb 2021 20:53:41 GMT  
		Size: 192.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `alt:sisyphus` - linux; 386

```console
$ docker pull alt@sha256:cbaf8b48d554090acae7d90efd8e49000920b1f0b546d0df8db32aff406cfe6a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.5 MB (41511545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c96335827dd148e1aa06b61fed271d1af274d7453ee5d307410ee9c373caa919`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 11 Aug 2020 19:38:56 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Mikhail Gordeev <obirvalger@altlinux.org]
# Mon, 01 Feb 2021 20:39:03 GMT
ADD file:19b5aef2295cd03c37e87287ec0ee374bd35ea074418e6471ab7415b63f21c6a in / 
# Mon, 01 Feb 2021 20:39:04 GMT
RUN true > /etc/security/limits.d/50-defaults.conf
# Mon, 01 Feb 2021 20:39:04 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:00e3f5568fae73d4c50247ef0f1bee2bb72ee0b0fac8b7775c09a96d633074ea`  
		Last Modified: Mon, 01 Feb 2021 20:40:03 GMT  
		Size: 41.5 MB (41511354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:924870bd27fa41c2f8961c5d5351c02d126fc8e47197677b5a7d5b268a95b588`  
		Last Modified: Mon, 01 Feb 2021 20:39:50 GMT  
		Size: 191.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `alt:sisyphus` - linux; ppc64le

```console
$ docker pull alt@sha256:32e180ccf08ac30b57dc2709fc4768bf1bb08832e9c02ec5ac2cbc9595b7875e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.4 MB (44433398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5760169c929340863d25defc6b7c0fa23d5362a9ca5684800248994a7b2fea51`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 11 Aug 2020 20:29:27 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Mikhail Gordeev <obirvalger@altlinux.org]
# Mon, 01 Feb 2021 20:22:54 GMT
ADD file:4368d541839f946a7ffbfac2f3ed62d3398609e6110c0fefde0441d2960793d3 in / 
# Mon, 01 Feb 2021 20:23:09 GMT
RUN true > /etc/security/limits.d/50-defaults.conf
# Mon, 01 Feb 2021 20:23:16 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:3602ce16123324a6e598c2e5b487ff7a196a09a063b9cbd0f1a21a0f25b136d1`  
		Last Modified: Mon, 01 Feb 2021 20:24:07 GMT  
		Size: 44.4 MB (44433207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06f21b597c57144e9314a9544801da71dfcada81af4743d5ad03a93733013b5c`  
		Last Modified: Mon, 01 Feb 2021 20:23:58 GMT  
		Size: 191.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
