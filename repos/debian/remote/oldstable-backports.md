## `debian:oldstable-backports`

```console
$ docker pull debian@sha256:fd4f5eb687e4765d71230032eeeb9ac7d682d70bb790372d5e8944544b0ba11c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `debian:oldstable-backports` - linux; amd64

```console
$ docker pull debian@sha256:c4d674cb60812aa997f2e2c9fd9d55b53279fad0cd592fd163357d4a975db82d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45369889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83d506d082d18acfa894da73c072d6c40dacec18ba302a421d026cddab168542`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 02:05:05 GMT
ADD file:d82d5477ad39cb7abe24ce64e83337baf085a09223487876e34f8902d7e959b4 in / 
# Wed, 22 Jul 2020 02:05:06 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 02:05:11 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:2c72f8e54c0498da77a3186087ede3cd0f8c19f98d2f0391c1af097906d684c8`  
		Last Modified: Wed, 22 Jul 2020 02:11:03 GMT  
		Size: 45.4 MB (45369662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6efaac8181bd2a0d274a90fec1a03fddb99d6e2a6112a8444e71dd15f7f5bf0c`  
		Last Modified: Wed, 22 Jul 2020 02:11:07 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:165eef8acf85a4e27ebf56aca5dc5acf863fbacf59816c52429ca280ea919d15
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.1 MB (44081376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca2143fde75006c25b60dc62bf8fd4389b61d410d12c6121526b85f44ef9f44a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Aug 2020 03:17:19 GMT
ADD file:9849c3d9bfc94351af6af8b09ae67ac5c436d2adf5dc6a4466c17343f41b46be in / 
# Tue, 04 Aug 2020 03:17:26 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 03:18:08 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:6ee45b7007ef9a3afb582a3b04f9b23dff044c2db3229e4d6c134638079530b2`  
		Last Modified: Tue, 04 Aug 2020 03:36:11 GMT  
		Size: 44.1 MB (44081147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f44d3d05692d40f95a122965f424c46f68109d188a09b4979b559cd4fbefe37d`  
		Last Modified: Tue, 04 Aug 2020 03:36:22 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:80f66628d0313a840455fe89b4b4dddb481af3276a53d37dc5412b535e17a8a3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.1 MB (42107653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:770c22caf102d9da7000549117594aac3ee5ea0f51dd614b07b25949f07cc555`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 01:25:24 GMT
ADD file:14cc58e8ae9b03746c983cb41d0fd43f0d339cadb578d2e02090071a87edb324 in / 
# Wed, 22 Jul 2020 01:25:31 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 01:26:26 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:eb4312b69f0e4d6f13fab3412235cb22326cfa3fb057f0a62e9d8cb585c19063`  
		Last Modified: Wed, 22 Jul 2020 01:42:16 GMT  
		Size: 42.1 MB (42107427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df40ed1914e4748d0cc00aff8d12b1edf61321176e08106f0f72ec8832d4a982`  
		Last Modified: Wed, 22 Jul 2020 01:42:23 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:1ab9860741ab88aacf1a758a8e40d1d212884528c068569cfe35346d1666edb9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.2 MB (43169596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b021dc29389068a2ad632474e12385d98a931916b0ba3e7f92fd45b2b9b5a793`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 00:41:27 GMT
ADD file:c3e784b1a0fcf338c9ea2e4941098e5301a514012f3a924750f3b0db08153603 in / 
# Wed, 22 Jul 2020 00:41:30 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 00:41:39 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:41ea194606dcb7fcac3404e4f40fe7ed4b8a22ab9c27f1ad4ebe3b3fb4c9998f`  
		Last Modified: Wed, 22 Jul 2020 00:48:00 GMT  
		Size: 43.2 MB (43169371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27aa998deb60e54bca64139bd92f84b5d72a06f89480fce7cb7350bf17a2f1d8`  
		Last Modified: Wed, 22 Jul 2020 00:48:13 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; 386

```console
$ docker pull debian@sha256:6728c991710bb4a5694fdd298986312bf076bdd63b4efdceac84098794b2f5e6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.1 MB (46086969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab71c8ad02da7f5ec981d5e89696ffd86c32df1cc1db876651783d23e0225184`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Aug 2020 03:38:37 GMT
ADD file:87fb04cc1d57075d6bb55169ae9a73688c99a88e3b176d4a0d329cb0e0bc678a in / 
# Tue, 04 Aug 2020 03:38:38 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 03:38:42 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:d70c3df3aa8d2a0cfe6590fa8261e03e8344be0b3d98c50a961f639b3305fc66`  
		Last Modified: Tue, 04 Aug 2020 03:43:45 GMT  
		Size: 46.1 MB (46086744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1da598e44326b4ce9ca098c87586feede376484d15abaa109dad6cdebd1943f3`  
		Last Modified: Tue, 04 Aug 2020 03:43:50 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
