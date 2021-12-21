## `debian:stable-backports`

```console
$ docker pull debian@sha256:b78b6d56f572a1c13bf9c093e472dd051a1e20022bb791988d003346d5fd9490
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
$ docker pull debian@sha256:07b27106f4ed7fd54350a1d95a5832f4087c1636f4dd41bc7473d78d4f42ae06
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54919274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63e2ea0cbd8c26fadb1300997c960a70c7acbc453e96b98698ab2bcfae1ca11a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 01:24:11 GMT
ADD file:9378b685ba5d4d29919e2c751e51e9a375e8f77e04325cc6c39e530f59b41609 in / 
# Tue, 21 Dec 2021 01:24:12 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 01:24:14 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:8bb8ae9b0185f5d889dc74832bccc98639959d52f66fa45c7afd30917bb4e60a`  
		Last Modified: Tue, 21 Dec 2021 01:30:38 GMT  
		Size: 54.9 MB (54919051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13d48b6a0e9c67d9fe549f3d4acc3953ff9f0ba63bd9d07b53372dab0682feb9`  
		Last Modified: Tue, 21 Dec 2021 01:30:47 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:4acc44d907bb3547c6143aa11f9d4fad4b6dcf51ac4deff7ca2af12adb928bc2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.5 MB (52453721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2b2b40911fde04a64cd859144b5ec8e4b1847727b564c7ad90b3049b143cd47`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 01:54:37 GMT
ADD file:4f3f22afdfdaa22f59d1efc385d16b52868d60756e17fd6b26394e1d5be7f850 in / 
# Tue, 21 Dec 2021 01:54:38 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 01:54:50 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:956145b992cc940fbe651aec596803c4a6aa0af6d3d091062d0fcb3cdf18264a`  
		Last Modified: Tue, 21 Dec 2021 02:11:48 GMT  
		Size: 52.5 MB (52453498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bf3a27f9a8c7a80d308db7996f715e085712416a78714b101913090e3568346`  
		Last Modified: Tue, 21 Dec 2021 02:11:59 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:c9014b4d8846553336063fe9a477cab329c63561b5a783cc493037cc83d3b0a0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50121678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63cdc09fd3824d19ce22517333ccce33686729309cc93d5bd6e5eb71a8f82e4a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 02:04:08 GMT
ADD file:0856a8b478f73785b5fca42e3113f09ef718a70c031cc5f1856e64644c4494a1 in / 
# Tue, 21 Dec 2021 02:04:09 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 02:04:21 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:0e26b403ba001a083a3e55132d1773c77008d0f16eade63efddafbf2177d15b3`  
		Last Modified: Tue, 21 Dec 2021 02:20:57 GMT  
		Size: 50.1 MB (50121455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09227fa898311e76bcd5cf1c5ee117de818f45bac59c2a0e1cedaaeb5206aa2c`  
		Last Modified: Tue, 21 Dec 2021 02:21:09 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:b01ad767b5b4003c5dbe8620b866ad897d72facce39ff0c7dc1de0378477a8fb
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.6 MB (53604804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:beb29c18e2752562335590c8135636f0624c9b4ce6d97a00cd1fa3e0cede7bdd`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 01:44:03 GMT
ADD file:7f6adb94fd06bbaa06d615f8d997a5dea3eea2bfe451ea6af5a85010bbf6ce56 in / 
# Tue, 21 Dec 2021 01:44:03 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 01:44:09 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:d39780c72a13b02b33aaeb60c4d3e849378d96e0a6e0578b855a5f5becb8cd14`  
		Last Modified: Tue, 21 Dec 2021 01:51:57 GMT  
		Size: 53.6 MB (53604583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4fee78b69a0ae5354c82366cdaaed9ab501288c646a2a3cd65e322a40c68f1f`  
		Last Modified: Tue, 21 Dec 2021 01:52:08 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; 386

```console
$ docker pull debian@sha256:9a0a0cff9ae70e80fadcfb1283d4ea22de85272d2145c91a90e62a44cf4380f5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.9 MB (55925573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60a0299c560d7055ee1b385597b66e9f30fa5cd0d660b07864645af5d323edd5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 01:42:38 GMT
ADD file:efe6538a62fd559c8b5b161326aa8d88a559e80bbcac8326bc2797b4a8755112 in / 
# Tue, 21 Dec 2021 01:42:39 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 01:42:46 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:eeb955a987714dea410926ad2c657ba42f543f9c87f31c3c6da72ac6f8da3459`  
		Last Modified: Tue, 21 Dec 2021 01:52:34 GMT  
		Size: 55.9 MB (55925350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:696dd31ea2a8b6b036f64799f4773ab88add8a3cbb58a2d08c8d6efffd8e76fc`  
		Last Modified: Tue, 21 Dec 2021 01:52:44 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; mips64le

```console
$ docker pull debian@sha256:f02cf0bd7671c65ddbb4863a4bcdf4fbe623f0c3bc0f5d5b891ffdeb481b0782
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53171328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b67eb71815973e5c733629abad30fc5430fdcf37bda4e49cc6571b33995d8e2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 02:12:14 GMT
ADD file:7c9a4bb4ed0b21fea9779041f874df015e94f7a681760e0a6f7deb38884f7ac0 in / 
# Tue, 21 Dec 2021 02:12:15 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 02:12:22 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:2bd0bd25439c4488473f55670346e81173f530293350d0cb3130b957b1d29e2b`  
		Last Modified: Tue, 21 Dec 2021 02:23:11 GMT  
		Size: 53.2 MB (53171102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1adaa5b10a3efe58fe2acc18927d3a8477f2bdd24293be2a20994367d1fe28c8`  
		Last Modified: Tue, 21 Dec 2021 02:23:20 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:988a5208f66e8fe874e983780adb2ce9598707b1c0458a70e08e6b74648ea8ef
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.8 MB (58809268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:455f17e1e9b6727174455fe21b194668ca835247a4b599e90d53105efc995b56`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 02:22:55 GMT
ADD file:f13d55a9aeb53630894059cab3d743f024be466bc039c61ce6b1ebdd30394eaa in / 
# Tue, 21 Dec 2021 02:23:01 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 02:23:14 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:06d052b8414cd2a418a84e2386b7d928cadd09af9d9ed602c969a6db9e02ac8e`  
		Last Modified: Tue, 21 Dec 2021 02:32:16 GMT  
		Size: 58.8 MB (58809042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70159028adf854eb98243dd74bdeb1fb40c335d4f0c553412341f7eabb1bd038`  
		Last Modified: Tue, 21 Dec 2021 02:32:35 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; s390x

```console
$ docker pull debian@sha256:9cd507b82d2040e0aa5b257e8706538619dedcd351ae6261582b7e8abd24722f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53194893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a794a8359e5f59e7a15c7400f55afb17e05bc73072cf13205bec7476d143a53b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 01:44:00 GMT
ADD file:16e8e0f2c31bbb1175dba1423169ce15b023b8d964ab8aa7d94b78431a2fa60f in / 
# Tue, 21 Dec 2021 01:44:02 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 01:44:09 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:8aac6c6e3d3fd37ea4df120da2a600b462626de6fb0d0beadf30fc203e5c093f`  
		Last Modified: Tue, 21 Dec 2021 01:50:05 GMT  
		Size: 53.2 MB (53194668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:319c559de6e487e673ed78305a67fbed5fdeae75ad913d7de453f1cd5fd4b0ab`  
		Last Modified: Tue, 21 Dec 2021 01:50:12 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
