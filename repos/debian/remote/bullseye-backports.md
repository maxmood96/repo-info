## `debian:bullseye-backports`

```console
$ docker pull debian@sha256:a8e65f4eaab25b1f87fe296a63332020868b00788758b6d4e781833c716ed621
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `debian:bullseye-backports` - linux; amd64

```console
$ docker pull debian@sha256:58daf891621718d69fefcc7a6722455943cc322abe404bbe5403ad4cf6869549
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.1 MB (54102701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d376d69edac96e9f51b95fef206fb96a0e3d8a369de3bdfcacdaa15757a4d982`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 02:02:39 GMT
ADD file:1fda4c82a4eaecf44b3fc4eb92bb0aac8d81c1c87822bd86f8b52b3620b70420 in / 
# Wed, 22 Jul 2020 02:02:40 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 02:02:46 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:c07b17c5753ba5920876a4091c37318cc0787c8027550cb13d9c1bd7ebfab87f`  
		Last Modified: Wed, 22 Jul 2020 02:09:11 GMT  
		Size: 54.1 MB (54102477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f14f34863765787204b24cdd456354f32e22dccb4c2a2c73db595ee7120496de`  
		Last Modified: Wed, 22 Jul 2020 02:09:15 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:cebc1cb184e5edc35796aeca8de9fda12ede3f99963eabcee61e753e0a231978
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.8 MB (49784753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:886d2ebb1422c1d859a688e1995378b870157ba8e93b6dc367445d3183f982cf`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Aug 2020 03:08:44 GMT
ADD file:2b581429c7fee51f5899cbb76a5d9c36cf7223edcbb473fbe2f8db3a53a82263 in / 
# Tue, 04 Aug 2020 03:08:52 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 03:09:55 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:7a2a8e3d684f3a7d5eba8b8ba267ffcbcf9d2089c1f803e105113f8b34f8991e`  
		Last Modified: Tue, 04 Aug 2020 03:32:48 GMT  
		Size: 49.8 MB (49784523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:831d934de5d70c69192f56bbaecfd663076c2eb056d5e00361bb1ffb0ae71e6b`  
		Last Modified: Tue, 04 Aug 2020 03:32:57 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:9e4062298b6d84b1ba86c0e2a27adfc75ed406147148bb68a77029c9e9a03d9c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49461983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dab0069a6c1b43a7620c8154a360e6a9777d09302ab46c6d88065a4b9df127ec`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 01:16:07 GMT
ADD file:b12e6ee23a8c36af2c020959d86c9277008b6b54ceff80954502340dee6e145e in / 
# Wed, 22 Jul 2020 01:16:12 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 01:16:56 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:9142e33629754cf85d79355e893c9c07e344f32f4fbe710c344514aada5f1b92`  
		Last Modified: Wed, 22 Jul 2020 01:39:35 GMT  
		Size: 49.5 MB (49461754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e5edc559d25763b800fb9f86591f141175fe3e25a703aadc5ebadab88086efd`  
		Last Modified: Wed, 22 Jul 2020 01:39:42 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:0d81694f076d34b144449c967ecba346f233e555ea512c461fc2cb06f7d2f1fd
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.9 MB (52886595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa660f1d2afcb01554f4b916f55fa4596c8edcae71ec61ceb9f3eb42cc588a4e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 00:39:52 GMT
ADD file:19b87dac8088f103e1a9992c229b17344439af0da8af45bc6d678f69471077d4 in / 
# Wed, 22 Jul 2020 00:39:54 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 00:40:02 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:508fd3fb95b7fcde22f3f927caabf293cc04dcbdb4c45b85a5130d5122e12a0c`  
		Last Modified: Wed, 22 Jul 2020 00:46:40 GMT  
		Size: 52.9 MB (52886369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48668216798dff110651d7b84042a26b05ac952d75a75a61ca6c27a304d66d56`  
		Last Modified: Wed, 22 Jul 2020 00:46:47 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; 386

```console
$ docker pull debian@sha256:5867c1a8b460ce4ef42f32f0c784efdb52f02efdbfe5a6545ee054d37126fdb5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.9 MB (52909953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a141a59ae1a168798203dcc92c531dc8f5b224771e97ea537ed215e07c845c5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Aug 2020 03:36:50 GMT
ADD file:e3f476fccb15ccc08c3c8c26ac23f1909e7c0f79bc060289f35fc37bb4483f80 in / 
# Tue, 04 Aug 2020 03:36:50 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 03:36:58 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:308ce7c38ffec8ca43e219653810c298ee87abfaaa068ff112f1e8003b108546`  
		Last Modified: Tue, 04 Aug 2020 03:41:50 GMT  
		Size: 52.9 MB (52909727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58b101b50eeb421812ccbd78cd6c00c3df6905a8492e05062e4d7c9fce4e7041`  
		Last Modified: Tue, 04 Aug 2020 03:41:54 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; mips64le

```console
$ docker pull debian@sha256:31b56dbdaae0b8ac8d1dd33a4e8cd97c715d08642004f55d5042300eceaec349
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.4 MB (52358459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f16b89bdce0d9c639b1b54b1fe331a1685d754fc0c132d0c84f4c011f68f05ef`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 01:08:31 GMT
ADD file:7401625ebd06dafb2256bbcc5a70246e5e6282bcc356478f05fd7ddcaa55003c in / 
# Wed, 22 Jul 2020 01:08:32 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 01:08:37 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:c240b05d7ff10891b36c505769b275684894e6a8ed8b5d40f20220a3da221e14`  
		Last Modified: Wed, 22 Jul 2020 01:14:40 GMT  
		Size: 52.4 MB (52358232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e192af6848a96478f6d0857d48bb1c0f5cef1664d19e48dc91322a7b6faa2268`  
		Last Modified: Wed, 22 Jul 2020 01:14:51 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:bd0e2431c98e6801a2d8a64d4ea452f9fbbf09108e76eee7124f91b8d870b5aa
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.0 MB (57953621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cab757a0913d0d1ffb718751d37c0520bc7afd28b33d5f3657fd50b6e99e717d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 02:13:38 GMT
ADD file:92efdcf349a6f1580ab27a2612939d75fc0e449e05e20e6385f5f7e409cd6684 in / 
# Wed, 22 Jul 2020 02:13:52 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 02:14:27 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:1eb910fa0fdd2afbde1007491a0fe3461e3029a0c5950e2a5ea3a69d15cab80c`  
		Last Modified: Wed, 22 Jul 2020 02:22:28 GMT  
		Size: 58.0 MB (57953394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d0e5c2d693a0ca8abb31f92f082a046389c016063b8ece0a9d8bb6013a151de`  
		Last Modified: Wed, 22 Jul 2020 02:22:39 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; s390x

```console
$ docker pull debian@sha256:896b058494659b31b83ceab0fe82ae2b0806d86aba23ac91a9bb5507c6350948
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.4 MB (50417048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f9d3263326efd2d2cb393ba7616609dd6ea5b3188932f1fee9e2595f566b6a4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Aug 2020 01:16:37 GMT
ADD file:be061a89b8959a241d8303ec83a6494b37d71fe20736b073046173371101421e in / 
# Tue, 04 Aug 2020 01:16:40 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 01:16:45 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:67f968df5fed9ab1993b2cba53f4810f984f47936fce947baf7ef2e7d8a5a20c`  
		Last Modified: Tue, 04 Aug 2020 01:19:19 GMT  
		Size: 50.4 MB (50416822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5df00006419f0cb5444ed52da3b2569020d7972369677378b0c66b469982c2f`  
		Last Modified: Tue, 04 Aug 2020 01:19:26 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
