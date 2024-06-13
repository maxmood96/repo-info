## `debian:stable-backports`

```console
$ docker pull debian@sha256:afd2927a27c74ba2d5a3a839b59637ff752d9aa1e5250036c2a43a7915cc5470
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `debian:stable-backports` - linux; amd64

```console
$ docker pull debian@sha256:6ba50ad26f82c106f3daabbe00314dfaf0d0de2507a8d318677e67dd7f7015f8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49576867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4312ebf8ee6823fb3692d9958aec8ef8cae42e4dad6fcc7dcb99f68fc38c6026`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 01:22:48 GMT
ADD file:a97e929c314c6cd646d7ea12e7bf8ba9f6d14ebda7dbdedf866cbe4c4e8854aa in / 
# Thu, 13 Jun 2024 01:22:49 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:22:53 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:206929d2bade528278ec19d162f49bb6cb90d835addd10f7d4b8be7e68fbfbf0`  
		Last Modified: Thu, 13 Jun 2024 01:28:35 GMT  
		Size: 49.6 MB (49576647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a823c1643675343272dc85763c0859562e451fc76be0f16981df4b3c3bccbbe9`  
		Last Modified: Thu, 13 Jun 2024 01:28:43 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:8a386f741fd6e1386d03e4a7df966244b845aed3ab39630d1f693c49d0bc7cba
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47338685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80183a9093546d3d9679c978b9548da81fd093e4b51f5f04cb17ba3fd796bf1f`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:49:26 GMT
ADD file:4495608fd47098dd151f4f5bcfe5b2c3510bc9727ea774de59c8777d5b7b1812 in / 
# Thu, 13 Jun 2024 00:49:27 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 00:49:30 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:45e31bf94facab4d4040929ab83ff9180d2e383c16ce574a83b69e8cc92dceb9`  
		Last Modified: Thu, 13 Jun 2024 00:53:47 GMT  
		Size: 47.3 MB (47338463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:653c18ffe0a2ce9bbfcd5cd7e0a657724920e7afc810b434bb3229829407be73`  
		Last Modified: Thu, 13 Jun 2024 00:53:55 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:c633ed57779ed90953235eb7dbb1a5c7eaca79009b19fb0a9c1eb77e048e8a25
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45175294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fe593d4b1d8e19c1a721cb1ee081ad159878bc61b62b2f649f7cea228728e51`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:59:13 GMT
ADD file:d91c04beb7258cbeda73a92d52702ef1ce52bfd9b703f34f75b4f9dc116e8343 in / 
# Thu, 13 Jun 2024 00:59:14 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 00:59:16 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:df39248e2915accc98a43c4c3134a4faa4f170d5653dc893a2832fd057a9bf2c`  
		Last Modified: Thu, 13 Jun 2024 01:04:49 GMT  
		Size: 45.2 MB (45175071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66eadc393f57268d9042dd11df651010230a6ac2452eb88ce6b50e86aea8f1de`  
		Last Modified: Thu, 13 Jun 2024 01:04:57 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:f8b561c0fd0f4848f091d40e1d1cf7e91aa3a7617d033fda6dc42d28c6cebd88
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49613631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2ee6edd636099ab4fae03333868b8ab9ab25951206ddcb91f44178db4d8967d`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:41:05 GMT
ADD file:5b62f3039a87b1937cda1e5c97a7bf36461825c89832c832c078caf3bdbb2db7 in / 
# Thu, 13 Jun 2024 00:41:06 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 00:41:09 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:03457dbd69892698e00a797da22fe81fa1138e09da1460452eec507f5a36ca85`  
		Last Modified: Thu, 13 Jun 2024 00:46:05 GMT  
		Size: 49.6 MB (49613409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:519acf6599a603af4cab23dfd99bcf1df3680cd3a7306da6c276fedd1ecb7730`  
		Last Modified: Thu, 13 Jun 2024 00:46:13 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; 386

```console
$ docker pull debian@sha256:88fb7624bac4c5af86334e08aca60fff8f40546ce521fefabb64ea6073ee4105
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50602702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:626ea1ff87629261b2f6b41a1581834319dd7091af19cae5c9ead0f378a1e7a9`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:40:49 GMT
ADD file:c5d2f87fad57933dab55fe8a2afdb3356c6ca0819b886a9ec57a7e43699ff51f in / 
# Thu, 13 Jun 2024 00:40:49 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 00:40:52 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:5f757c13ac58ca20fa5b66862a2e124861be3549685bc4b380b7ef9a45b8a7c2`  
		Last Modified: Thu, 13 Jun 2024 00:46:43 GMT  
		Size: 50.6 MB (50602480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7128844e54e1c328d334fca7a3e5744e32f1458e8ef675b98499c5d51f18eea2`  
		Last Modified: Thu, 13 Jun 2024 00:46:51 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; mips64le

```console
$ docker pull debian@sha256:f265e0ad02a2c7c5d3312c15f0b1ab097815fbc0a9c770e9da60a8741d5385f9
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49582935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9722aa4a6824b850c7432e2b1a3b13a3789912095e54b2847e4fa49783646029`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 01:14:51 GMT
ADD file:80d218cef18aba8e0d2af99a9d9a92184c2edd106a58c972edba150b49a56b0a in / 
# Thu, 13 Jun 2024 01:14:57 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:15:12 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:356c630782ec3338f52aa63f535a94e3e3c208291194b75677b5424e3d70e9a6`  
		Last Modified: Thu, 13 Jun 2024 01:26:30 GMT  
		Size: 49.6 MB (49582710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6384e7e97f4f61d4ddf271f97a4d804d9c98e126b9db7cc3da6900ec3545254f`  
		Last Modified: Thu, 13 Jun 2024 01:26:41 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:c63815e0e1cf6cd49d05653e9dacc34b93e857ce0cfb4e45559f32cb3ca510ce
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.6 MB (53579892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2ecadc98365dbfb91debfadf9ea61e7b6c5b48fac94ea4b9b2f78b284e0a85c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 01:18:31 GMT
ADD file:315c86f5b83c1ee3bbbd211b9f454ce66e5902f84d0e702ea8ab3120a6a1f392 in / 
# Thu, 13 Jun 2024 01:18:34 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:18:39 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:eb6784fe578a67d0e186beaeb8a0172b2cca15a1734dab666bd58e3fdcc94ff4`  
		Last Modified: Thu, 13 Jun 2024 01:24:00 GMT  
		Size: 53.6 MB (53579667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46961ad51bcdf614e215214254cf2a9e2305fdf3e4b776529a79471a7dfd8f88`  
		Last Modified: Thu, 13 Jun 2024 01:24:09 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; s390x

```console
$ docker pull debian@sha256:bc66f5ef00e4c21d8e0165c41269e74a501d9bcb8d3b4c9630e87acc71c91a47
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.9 MB (47942658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9503d6b7d771750a552123ccdcb7244c1fe44b754d8775ddede1bf9b3fb5ec6e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:44:24 GMT
ADD file:f88f06b39d6c737a247de4dfad3590cf9bec53388b1f5430824faf715190a44b in / 
# Thu, 13 Jun 2024 00:44:26 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 00:44:33 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:f57b71f3fc0c90b322a6291423d2a6828b004a23ce04c403787ec3b1b904deea`  
		Last Modified: Thu, 13 Jun 2024 00:49:19 GMT  
		Size: 47.9 MB (47942435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38c9fae301a5a9a6fa91d13c27bda1d8b9501f77526e67e6cd8ffe7daad1543e`  
		Last Modified: Thu, 13 Jun 2024 00:49:25 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
