## `alt:sisyphus`

```console
$ docker pull alt@sha256:703f5815c64ec607b83853c876a74d7223c192a232355b55fc07b9675be063ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `alt:sisyphus` - linux; amd64

```console
$ docker pull alt@sha256:b38012f5a92bbe2bd1ce9d9a652cead4415dd9b95dea8360b1f52e72664c466f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.5 MB (42516711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0255885cb0fa2b6c8c9ebe19455053f5cd1047ad1aa164ce730b17f529fc3aa9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 26 Sep 2018 21:19:34 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Gleb Fotengauer-Malinovskiy <glebfm@altlinux.org>] [Mikhail Gordeev <obirvalger@altlinux.org]
# Fri, 17 Apr 2020 20:21:15 GMT
ADD file:bdc95de4a2134b26633b0cf33f5ea909da0ec8c98d5450ee3d16996b2dc91968 in / 
# Fri, 17 Apr 2020 20:21:16 GMT
RUN true > /etc/security/limits.d/50-defaults.conf
# Fri, 17 Apr 2020 20:21:16 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:a486e48e06c564fc25aea11e4075c481d81cfefac16ca8154834d8f788da5fe3`  
		Last Modified: Fri, 17 Apr 2020 20:22:30 GMT  
		Size: 42.5 MB (42516529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f854ecf46147bf3123f7664e92b805a3f98c0a02fd0a4d89c326842aab345aa`  
		Last Modified: Fri, 17 Apr 2020 20:21:47 GMT  
		Size: 182.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `alt:sisyphus` - linux; arm64 variant v8

```console
$ docker pull alt@sha256:87f7d21699475e321a001066e06b5be08b4d2e032edf2223baa52cfa74d415d1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.5 MB (41450509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d50d2c032633af162388d7f2b0d9c6e973b4f4c17bc4d4c20f8d17d38795f901`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 28 May 2019 22:39:34 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Gleb Fotengauer-Malinovskiy <glebfm@altlinux.org>] [Mikhail Gordeev <obirvalger@altlinux.org]
# Fri, 17 Apr 2020 20:53:09 GMT
ADD file:f6ed3d9bba90a1e88e3f18bf780263eb99e8832d4f55be40a217b2742dca5e69 in / 
# Fri, 17 Apr 2020 20:53:13 GMT
RUN true > /etc/security/limits.d/50-defaults.conf
# Fri, 17 Apr 2020 20:53:14 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:fb95dca6947e373b5fa76230a7fbd765112dcd69cb8b68725c25f57a89ca6569`  
		Last Modified: Fri, 17 Apr 2020 20:53:52 GMT  
		Size: 41.5 MB (41450326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c1a64449e3977f1a6ae25332e0350bd729b16d84690697d0a6212d1e995b9da`  
		Last Modified: Fri, 17 Apr 2020 20:53:41 GMT  
		Size: 183.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `alt:sisyphus` - linux; 386

```console
$ docker pull alt@sha256:3d580a5c9fda073d808a5cec6b5eb70d4b8c5568ec541fa678ec9e10bcc0e582
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.0 MB (42983776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bf66fd79e0268d31b1e3a2dbc228e38a66bf4623db248a0dd744b065b9f4712`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 27 Sep 2018 10:38:37 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Gleb Fotengauer-Malinovskiy <glebfm@altlinux.org>] [Mikhail Gordeev <obirvalger@altlinux.org]
# Fri, 17 Apr 2020 20:39:32 GMT
ADD file:7e9203f8033407ce397c14c2cf32e0cd3e453e17f1dc5237945a3f771c21eca0 in / 
# Fri, 17 Apr 2020 20:39:33 GMT
RUN true > /etc/security/limits.d/50-defaults.conf
# Fri, 17 Apr 2020 20:39:33 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:71721a1bdd8f1dae99dcd35ef8fbaeccf05fb70a020f31529f397affbccad29f`  
		Last Modified: Fri, 17 Apr 2020 20:40:35 GMT  
		Size: 43.0 MB (42983595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa3b229641aed5df96ba41d6074fffb4c1ce979a6607aa7bcbb34c305d598e48`  
		Last Modified: Fri, 17 Apr 2020 20:40:09 GMT  
		Size: 181.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `alt:sisyphus` - linux; ppc64le

```console
$ docker pull alt@sha256:f79ac87c2fb8ec0b6fbce05da934e8ae92737c8ae06f64c817d48a9c492700f7
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.2 MB (46218110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c079aa9069bdabb48c4f67017631e03c0ca573dedd95f251f6d87ff5d20f18b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 03 Jul 2019 23:03:07 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Gleb Fotengauer-Malinovskiy <glebfm@altlinux.org>] [Mikhail Gordeev <obirvalger@altlinux.org]
# Sat, 18 Apr 2020 04:35:27 GMT
ADD file:d1d20ef0f73f210f21613bb585286ab37fcc3e326b39322992af933ef0f6d8b8 in / 
# Sat, 18 Apr 2020 04:35:35 GMT
RUN true > /etc/security/limits.d/50-defaults.conf
# Sat, 18 Apr 2020 04:35:37 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:6599e71ba4e11556113f9ca691216692499612e53216e0145377c93683a669db`  
		Last Modified: Sat, 18 Apr 2020 04:36:22 GMT  
		Size: 46.2 MB (46217926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6bfe6ac85c48dfcb99ce47fd4e691f610d7cc8bfb4e88af2d793b9aeed61c99`  
		Last Modified: Sat, 18 Apr 2020 04:36:11 GMT  
		Size: 184.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
