## `debian:oldstable-backports`

```console
$ docker pull debian@sha256:6f561a8994b3e23a63491c20505833fb97366c633ed64ed52612c522a650b3a8
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

### `debian:oldstable-backports` - linux; amd64

```console
$ docker pull debian@sha256:8dd5996ecafbe1ac97610193235331ae1110190cfbc5dc4d66d01467ad8bd029
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.1 MB (55055811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9946fb52acca3fe295df9109f415b473bd1e9bd0fdf991c9fe05e6e5e6b1478c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Jul 2023 23:26:02 GMT
ADD file:d3d35fb8232fe43e10dc766c041fa6d6435ac21d31451258d21f040405ae5563 in / 
# Thu, 27 Jul 2023 23:26:03 GMT
CMD ["bash"]
# Thu, 27 Jul 2023 23:26:06 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:784493098d3cfa412835581409baba2f10667893e59b83360d4e8a525cadc867`  
		Last Modified: Thu, 27 Jul 2023 23:31:42 GMT  
		Size: 55.1 MB (55055587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d9e14c83f55be936fb81758830ae4d6befc9bd610fe62b24cc023f3cd840512`  
		Last Modified: Thu, 27 Jul 2023 23:31:50 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:7067369ed7b364cc564add1ec7804ec8592ca8f6b43c1f0dd49a70faff23007b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.6 MB (52557339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caef8f678b641371c522003d51c17f7cbf2d2e419fb62f5d7ef4d1c35e12fe9c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Jul 2023 23:48:53 GMT
ADD file:3baf05fb6ee586b94828532bde6fdc5417c7a8007e317b8a78ac7611b3bacd05 in / 
# Thu, 27 Jul 2023 23:48:53 GMT
CMD ["bash"]
# Thu, 27 Jul 2023 23:48:55 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:897f30a77ffc14a367809e2e776e53600c91e915a38c8674d72770cfbb74535c`  
		Last Modified: Thu, 27 Jul 2023 23:52:30 GMT  
		Size: 52.6 MB (52557114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbd897223efefacdd80b6fc1f1da9c7d19b8f55118963c8d45f569d544ae86dd`  
		Last Modified: Thu, 27 Jul 2023 23:52:40 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:e1cb2217ec12128a2bf0d8f043e6a7bc2ec09c8d95ebf423e1777c0cfbd623a5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.2 MB (50218774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c1a1ef97e3723bb3f6aebd783f2f70e3cc5fa46117ff57d9d25489afaaf8943`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Jul 2023 23:59:26 GMT
ADD file:d7a24eba8d49f00c4088435934f4be16ef020d2c559a54f859d05bdd5b0a4b8f in / 
# Thu, 27 Jul 2023 23:59:29 GMT
CMD ["bash"]
# Thu, 27 Jul 2023 23:59:33 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:f801e05ad008c87aedbfa56a853a8d47fdf7b5dc2680b742cc77606e7eb55664`  
		Last Modified: Fri, 28 Jul 2023 00:05:31 GMT  
		Size: 50.2 MB (50218549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90c1c6f919b8bbb0eafaa8a8049774cfd0ef5a3711acbd4809de44b335f23b38`  
		Last Modified: Fri, 28 Jul 2023 00:05:41 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:cf3be5717fb0fbe27234f20372a9ed9f720546fc147c486e4085318b198cadf5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.7 MB (53705013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c50fd1eab2bb4c4123c21c43325cdc8a5b2c933ce357150d3afb2a424607b39f`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Jul 2023 23:43:50 GMT
ADD file:bc7cc494d1bf8080669b09f776d8d081dcf7d615460c7ed663132ce34a5c4e00 in / 
# Thu, 27 Jul 2023 23:43:50 GMT
CMD ["bash"]
# Thu, 27 Jul 2023 23:43:52 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:d71ae21f0cd49d2c1051e89fc3817f6e955cf2488ed07a25e39c65f859b425f0`  
		Last Modified: Thu, 27 Jul 2023 23:48:38 GMT  
		Size: 53.7 MB (53704788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:129e6458757acc131b536062638660a0b695f448a2a8acffce8120eb9712a6bb`  
		Last Modified: Thu, 27 Jul 2023 23:48:46 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; 386

```console
$ docker pull debian@sha256:199d9065e12f16bd157314ff6aef6733935ff5da712cea39ed44340208a01f23
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.0 MB (56041205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b45962ce0dc9087609d837842afa46da22a1d71ed69c4db068f6ac33557ef7e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Jul 2023 23:40:08 GMT
ADD file:56ae544ce7cd8aeaebf43546c849f8eea86ff527535d9290f5fbfc88c30fa587 in / 
# Thu, 27 Jul 2023 23:40:09 GMT
CMD ["bash"]
# Thu, 27 Jul 2023 23:40:13 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:71f90141aa13246d9ba53f56fb4c82fc82540f3bebb5913be045846abe879de1`  
		Last Modified: Thu, 27 Jul 2023 23:45:58 GMT  
		Size: 56.0 MB (56040980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b330797e2c82e13e1f4dd478b78bce7f1b9c104271c2ac73568008f2576975ff`  
		Last Modified: Thu, 27 Jul 2023 23:46:07 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; mips64le

```console
$ docker pull debian@sha256:46622afab5aebbf9f375bebb8458464771e1f7f9b8e55b4a646c47e98cdd1fbe
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53271167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaa12f6858dea5af3a64763025df7ca44d812855ccce56ad480013cb2680ada1`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Jul 2023 23:13:12 GMT
ADD file:71a75d283ef59ae2efbfd71e5f85e3666fbccd01ba9e283c10da754e25f58079 in / 
# Thu, 27 Jul 2023 23:13:20 GMT
CMD ["bash"]
# Thu, 27 Jul 2023 23:13:32 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:331241b14a925146f04f0b145afd991bdbec8cf1f6d09fdce38db830eea2dd62`  
		Last Modified: Thu, 27 Jul 2023 23:24:35 GMT  
		Size: 53.3 MB (53270939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92076d43a4ca638bd0040e11da426929fad4d8d72f78aacfa62e0bde9b59647f`  
		Last Modified: Thu, 27 Jul 2023 23:24:46 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:682b713a57c8cef351b24ce4db01693dfa50d4d3c52d463a4bb39b371f0d66ba
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.9 MB (58927716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e8486b924ddbd22fb5b31dbe25bf2fb8751da4871e7a5e1b10859159403ac77`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Jul 2023 23:23:58 GMT
ADD file:ec924dbdcd458a572b817c41d54fa01ec94c123408db29504d74b0611a32ac0e in / 
# Thu, 27 Jul 2023 23:24:01 GMT
CMD ["bash"]
# Thu, 27 Jul 2023 23:24:05 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:ffc8d5ed9189fcc970c2f6120db280ccede96fb66fb23bf47ec8c1f64880ef0f`  
		Last Modified: Thu, 27 Jul 2023 23:31:05 GMT  
		Size: 58.9 MB (58927491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7d6b8f92ba07230fecbcf93709e08d6e874b3374ea54b52e3f82d4162a9d098`  
		Last Modified: Thu, 27 Jul 2023 23:31:17 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; s390x

```console
$ docker pull debian@sha256:be71d4990135e2e94d3c7e3a6e501134da4a6d5ae84fef86c691aec64a85cb35
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53289290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:389e931b0277b677ae8cfbb5c40777ffd786ea847a8edab25944d088bebb1d41`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Jul 2023 23:47:53 GMT
ADD file:233c9f803364f50edd88167775328c5d1bb65ea21af7dc6bd482a01f1e675bf8 in / 
# Thu, 27 Jul 2023 23:47:56 GMT
CMD ["bash"]
# Thu, 27 Jul 2023 23:48:02 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:11b0e9cb1f4b5da52d2937d7f6d1c9a3cc7e8b750df464882931973769a28853`  
		Last Modified: Thu, 27 Jul 2023 23:53:01 GMT  
		Size: 53.3 MB (53289062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5eb6367690a9adfc14a9cdd83c67e00f760616128bf21fcc22c3927fbee9e99`  
		Last Modified: Thu, 27 Jul 2023 23:53:07 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
