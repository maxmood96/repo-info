<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `alt`

-	[`alt:latest`](#altlatest)
-	[`alt:p8`](#altp8)
-	[`alt:p9`](#altp9)
-	[`alt:sisyphus`](#altsisyphus)

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

## `alt:p8`

```console
$ docker pull alt@sha256:1bc52054d21c4163d2fa8c4608f2074dc6fb7b7cff7e3d4070fc21b9a7b465d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; 386

### `alt:p8` - linux; amd64

```console
$ docker pull alt@sha256:c9abe92b0cfb4db927be600f8418249a12713ad6146552d0345767e05a77245b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.8 MB (35783815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10f898227d4fe17e5abdc0353f47728e4f988bc255f934801e979a7285cc05d4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 26 Sep 2018 21:19:34 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Gleb Fotengauer-Malinovskiy <glebfm@altlinux.org>] [Mikhail Gordeev <obirvalger@altlinux.org]
# Fri, 17 Apr 2020 20:20:56 GMT
ADD file:f72c839d28157bfc5dff9fd80bbc88facdf6b16e8aa7e671e472032dfd2d9dbd in / 
# Fri, 17 Apr 2020 20:20:57 GMT
RUN true > /etc/security/limits.d/50-defaults.conf
# Fri, 17 Apr 2020 20:20:57 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:0b02a1fa02d3e924b7f7543dacf1159e7fbecc6c3b49910697751e5e884aa188`  
		Last Modified: Fri, 17 Apr 2020 20:21:43 GMT  
		Size: 35.8 MB (35783635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38fdf19384ef2e48550acc53d92ecbba1353f7521cb7c7ef07e21af235907cb3`  
		Last Modified: Fri, 17 Apr 2020 20:21:37 GMT  
		Size: 180.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `alt:p8` - linux; 386

```console
$ docker pull alt@sha256:00309a30a09de55b43b6cb09033a2409d57595eca9c399c9a77fac54a57735aa
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.9 MB (35940680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec492149008b874a3bc6e6661c45a9942043ce13f8405585a496646d6e62d4f1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 27 Sep 2018 10:38:37 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Gleb Fotengauer-Malinovskiy <glebfm@altlinux.org>] [Mikhail Gordeev <obirvalger@altlinux.org]
# Fri, 17 Apr 2020 20:39:13 GMT
ADD file:fbf04a50b6ecd44ec455383f64fc5cf4f089d7fc895caee88dc0dadfce000166 in / 
# Fri, 17 Apr 2020 20:39:13 GMT
RUN true > /etc/security/limits.d/50-defaults.conf
# Fri, 17 Apr 2020 20:39:14 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:68b9ef91f33e3125d2500957556b9e9fbd7dceabb7bd4ef2f85eb2173941a20e`  
		Last Modified: Fri, 17 Apr 2020 20:40:04 GMT  
		Size: 35.9 MB (35940499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee1ac4d1342ef06f596e5aca1e277825deaa7ce8dbb1bdcf835be64302a1f372`  
		Last Modified: Fri, 17 Apr 2020 20:39:56 GMT  
		Size: 181.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `alt:p9`

```console
$ docker pull alt@sha256:7ae29f8523f38dc958a1d288c9f024387a9b8dcff8842552bc05ec8919f2810e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `alt:p9` - linux; amd64

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

### `alt:p9` - linux; arm64 variant v8

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

### `alt:p9` - linux; 386

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

### `alt:p9` - linux; ppc64le

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
