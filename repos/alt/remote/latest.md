## `alt:latest`

```console
$ docker pull alt@sha256:7ae29f8523f38dc958a1d288c9f024387a9b8dcff8842552bc05ec8919f2810e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `alt:latest` - linux; amd64

```console
$ docker pull alt@sha256:f0f4c74168b712cc7f1953cb106cb99d1ff94a9a3ba63e5f3aa730823637ef9d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.4 MB (42402845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fa7a4e7b43b8c39804edcc28d3c9054b6946d73cce1ff7f70df62a64a2faec8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 26 Sep 2018 21:19:34 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Gleb Fotengauer-Malinovskiy <glebfm@altlinux.org>] [Mikhail Gordeev <obirvalger@altlinux.org]
# Fri, 17 Apr 2020 20:20:30 GMT
ADD file:2d06afea910d9968616d800ef8051c9a310341a5ebf7d6e2d0e8dcc35dacb369 in / 
# Fri, 17 Apr 2020 20:20:31 GMT
RUN true > /etc/security/limits.d/50-defaults.conf
# Fri, 17 Apr 2020 20:20:31 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:a7f990b672518341cc3ab2b0ca77d33a1e5241443f33558b19b6dce765b8787d`  
		Last Modified: Fri, 17 Apr 2020 20:21:32 GMT  
		Size: 42.4 MB (42402665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8d15b4d031b574e5e8a9e108544c242a42b4317b3fd2b07a00c0ec81c91beda`  
		Last Modified: Fri, 17 Apr 2020 20:21:23 GMT  
		Size: 180.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `alt:latest` - linux; arm64 variant v8

```console
$ docker pull alt@sha256:3048ec6af4886a3a96f2347f154e54706e24f5e92008eb16b41b3674ac3030ff
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.2 MB (41196983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cc17b1cc026b8a31b396a884b75cd3487eb0940538184d41d790cf2febe6224`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 28 May 2019 22:39:34 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Gleb Fotengauer-Malinovskiy <glebfm@altlinux.org>] [Mikhail Gordeev <obirvalger@altlinux.org]
# Fri, 17 Apr 2020 20:52:40 GMT
ADD file:610dad395b67002fb5c133f808e9f29a836033d66440ce1d52258b39e46077d6 in / 
# Fri, 17 Apr 2020 20:52:45 GMT
RUN true > /etc/security/limits.d/50-defaults.conf
# Fri, 17 Apr 2020 20:52:46 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:989db8cdbac34d0dcdffe069780f9fd0b9e681bf6645164168e6ed5fc7a7e789`  
		Last Modified: Fri, 17 Apr 2020 20:53:35 GMT  
		Size: 41.2 MB (41196800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88e5b93c0c1d774cce81cb8b2eda896d36078e9937265045912c3ed2bd411472`  
		Last Modified: Fri, 17 Apr 2020 20:53:25 GMT  
		Size: 183.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `alt:latest` - linux; 386

```console
$ docker pull alt@sha256:bcd8de279ee81103614114c64f9201bde7210c1e5cd1b297742ce55073bbc686
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.6 MB (42594068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88f07dc7c31927bcd60847ca77541db74722d89a276229db5267ec7216420503`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 27 Sep 2018 10:38:37 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Gleb Fotengauer-Malinovskiy <glebfm@altlinux.org>] [Mikhail Gordeev <obirvalger@altlinux.org]
# Fri, 17 Apr 2020 20:38:55 GMT
ADD file:6b64bdf711a63686f6ed2662d9a257fb7229f8b2a94edf0744e3d9bf6b1d046a in / 
# Fri, 17 Apr 2020 20:38:56 GMT
RUN true > /etc/security/limits.d/50-defaults.conf
# Fri, 17 Apr 2020 20:38:56 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:3e67baf00d718ba790dde80ef3b86d68fec111df67c570a0fe26054ae56052e1`  
		Last Modified: Fri, 17 Apr 2020 20:39:51 GMT  
		Size: 42.6 MB (42593886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:139b377770205804800b11d89a62f3eaa537e26ea26340db484a81a4f41490e7`  
		Last Modified: Fri, 17 Apr 2020 20:39:41 GMT  
		Size: 182.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `alt:latest` - linux; ppc64le

```console
$ docker pull alt@sha256:27a3ed9ed4f2944e0ac36619826451999059528a1a9f211f6f8ad9023aa30250
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.1 MB (46108660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad3095ccfb7a2fc8ec47eabd81074d710dc935615ade5ba7a4924206c276d0c6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 03 Jul 2019 23:03:07 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Gleb Fotengauer-Malinovskiy <glebfm@altlinux.org>] [Mikhail Gordeev <obirvalger@altlinux.org]
# Sat, 18 Apr 2020 04:34:10 GMT
ADD file:42020f00b647b672042891c4a1a40cb904303e7363b9bcb8e0c0d792be41be22 in / 
# Sat, 18 Apr 2020 04:34:18 GMT
RUN true > /etc/security/limits.d/50-defaults.conf
# Sat, 18 Apr 2020 04:34:22 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:780e6e08ed6a41ad1924f35f6227aaabeca9d5681650126dfc1d9625d3ccec39`  
		Last Modified: Sat, 18 Apr 2020 04:36:01 GMT  
		Size: 46.1 MB (46108477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbf2adab93193d1318901fca1d8278c73e8055f92f122fe6356b7762b017b255`  
		Last Modified: Sat, 18 Apr 2020 04:35:51 GMT  
		Size: 183.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
