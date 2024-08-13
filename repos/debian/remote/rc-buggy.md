## `debian:rc-buggy`

```console
$ docker pull debian@sha256:c424f9b1b112e8acecae8bdea59120e9e000874c0978411f4158465a15326f5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 9
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `debian:rc-buggy` - linux; amd64

```console
$ docker pull debian@sha256:24cd399744447d167aa414122b56d5ef60c2f5e8814d7dbfa4173ff29f6cecde
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.8 MB (52836414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2813a7c9f4157654a72714c43d12e636a03cbe22c88c88691dec74ad1db2c14c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:21:13 GMT
ADD file:ec9b256ad5af9d6c88b912d94fd4e58256e2b29a1c5ff616fe47488c72c1256c in / 
# Tue, 13 Aug 2024 00:21:13 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 00:22:46 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:0ee0708ec9247cb19ad61d1bba3a89642d7eb4cfcd5031f23018c732b0ce201c`  
		Last Modified: Tue, 13 Aug 2024 00:25:12 GMT  
		Size: 52.8 MB (52836188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a5d240b1f8d1b62baf9c896a43918795a5abba65bee50ea231bfb42650cacef`  
		Last Modified: Tue, 13 Aug 2024 00:27:38 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; arm variant v5

```console
$ docker pull debian@sha256:d921670176f46877072c8e5bd7a7e94a5cafd995e538cf2ac99a2d92e237826b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.8 MB (49825988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0884a8f0ce8efb63037d8d3a6ead3b5733c9d3b298c366f402b71d0243e64763`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:56:10 GMT
ADD file:cf690ebeafabc8d93fcaa85c06bf4be7451eca6abfcd3d67e6a0b14ecae9eed6 in / 
# Tue, 13 Aug 2024 00:56:11 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 00:57:26 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:bf57c73982c97d1f73ecf70b56ea68e85c073b81e6abeed2594a6b283cfa2910`  
		Last Modified: Tue, 13 Aug 2024 01:00:06 GMT  
		Size: 49.8 MB (49825762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b35d7ae7467b4abec618ee2bc1632a38181a781d5bf8a7772c2a374d0f63595d`  
		Last Modified: Tue, 13 Aug 2024 01:02:43 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; arm variant v7

```console
$ docker pull debian@sha256:a4bf7f005ded97e9de279452fc523e81af3ce6d5daef49a36c6b54a5241833e6
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47328503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e16b2049957dde2b7a9fa9aedee59af6ea5f344caa914e0f883d56b4ea4d485d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:58:22 GMT
ADD file:e72a0297e96519fce159ae96a576801ad216aaabe4ba4c18342172c3277d4f63 in / 
# Tue, 13 Aug 2024 00:58:23 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 00:59:46 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:5985c1abf8d738f84db0f982b117de5f003cae7137cf3fbeccf69d06419b0eb0`  
		Last Modified: Tue, 13 Aug 2024 01:02:30 GMT  
		Size: 47.3 MB (47328276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:327e134c30a4bcbc840dbcd18531eb908bf3065d0bdee41bbdb5d3e72672d352`  
		Last Modified: Tue, 13 Aug 2024 01:04:54 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:7b9580a9f098d17cd2ad85900a1a030c127167a6739039e0f935dc3319c40b26
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53155474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5232c37025a96d28edf00ed004e0f2d95b2d08f714b0235b75941a52ede18c5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:40:28 GMT
ADD file:5d3aa31e5e33290bb28cfd74e2b2a88ce7e4415dc0d995c3c39d36c332bdbfcf in / 
# Tue, 13 Aug 2024 00:40:29 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 00:41:38 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:543c0d8816b61b146fc103b18d6ec335253cba7bad9fa7f1cb3e794a6b9e450c`  
		Last Modified: Tue, 13 Aug 2024 00:44:13 GMT  
		Size: 53.2 MB (53155250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96c3e07cc45ac4394c3063514ee3bbb3256c0bb5bdbac9685b8d3672c13ddc2e`  
		Last Modified: Tue, 13 Aug 2024 00:46:32 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; 386

```console
$ docker pull debian@sha256:eca6a7a8531952f24a01679d6e90cec5754e269943f665ce335d11a8f8fe08e9
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.7 MB (53738701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e4bdb189ed3db91030e911fb989d1a3b71c337b7dad62cd3d4974991b971d0f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:39:51 GMT
ADD file:79c443f9d7d3c4ead1afa700b0409049a5e5def4db762097116c9f15a44a29ca in / 
# Tue, 13 Aug 2024 00:39:52 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 00:41:33 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:47aa20e0d3978e830fbdc52fb1b018e2dc37ff9f122461c55040f23300208844`  
		Last Modified: Tue, 13 Aug 2024 00:44:14 GMT  
		Size: 53.7 MB (53738474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34f009963566851fae53863d9a42678800092b94d5dd95ed84bf2fdbcbe636f8`  
		Last Modified: Tue, 13 Aug 2024 00:47:01 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; mips64le

```console
$ docker pull debian@sha256:ab9c82b10e31c7171bdf2f9949ca68d93260ac62a635d326fe926f79535f3029
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51721009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5dcecbb2418dfb619505435bc2859604518ca69c6b23389ae05a5baf361c151`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:14:27 GMT
ADD file:c2b8305463bd9ec2de5e34b309a574fda4d3201acf2be1eeaf77b17be497d769 in / 
# Tue, 13 Aug 2024 00:14:35 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 00:20:32 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:96d1cb60a321cb9bcad04942005c2d893de36bfa358a946f876b980ee7696e7a`  
		Last Modified: Tue, 13 Aug 2024 00:25:52 GMT  
		Size: 51.7 MB (51720781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09cb4994ee91a187cd120d3adb7183d9a74b19c0a8abcf11f012a6fae83bb790`  
		Last Modified: Tue, 13 Aug 2024 00:31:38 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; ppc64le

```console
$ docker pull debian@sha256:4a7b5b09e38af7f9d2d0b5cc071a6a42646c427b3c08ab79f1e91114c23bdd40
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.7 MB (56730050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16f054369e5c93fc4d0dab3a2c26b5c35e79aec4e63ba069c7df04c88c0aa5de`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:23:11 GMT
ADD file:e6eea681cf56e20007639454c01cfebeefac45036637c0c5aa781f32e61086f3 in / 
# Tue, 13 Aug 2024 00:23:13 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 00:25:13 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:f94a26791ad674a64a864ec5ea20fbd30c5f7f3fa34d6b6d03306d943685df53`  
		Last Modified: Tue, 13 Aug 2024 00:28:16 GMT  
		Size: 56.7 MB (56729826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f55e3f746eade185f364d05ad9bba14695d4a71f9a09b259be9a57f12e6e494c`  
		Last Modified: Tue, 13 Aug 2024 00:31:17 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; riscv64

```console
$ docker pull debian@sha256:f43a584110e42c4d2189e9270de6a9db8f7a5a2a2a60300c5b93a227bddfd688
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.1 MB (51106386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:503a337ab462fc38e736405c337eaacd33e4619ef5a4793ea6d571ab5d646010`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:11:01 GMT
ADD file:97cc40f71485a0c47367bf7de8cb1715072dce719d216195de9b049516a29e45 in / 
# Tue, 13 Aug 2024 00:11:03 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 00:15:13 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:e7e6753663bf71667278434bd9ec3bfbf244788b1855805c384ac83204bc13ef`  
		Last Modified: Tue, 13 Aug 2024 00:16:18 GMT  
		Size: 51.1 MB (51106160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:225cc588450bd0812cd66a46abadbecf609e2f72517f2edea59aa46a321c9a64`  
		Last Modified: Tue, 13 Aug 2024 00:21:06 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; s390x

```console
$ docker pull debian@sha256:3be5415d6e6165c5ec998542b2a566050128fead1dc002038f2be3e27f8c5fd5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.5 MB (52451502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c975ebd7e62dc6decd0c6d377940081e5a248c4ad7ed5a75914de2c265e9d36`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:43:57 GMT
ADD file:b1f8fb7433720897f885f62e5bb1f6d60cfbf4392c753cd6772799dbe4712db3 in / 
# Tue, 13 Aug 2024 00:44:00 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 00:46:24 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:99d54a6f148f09f9af6f5923c0f9be21666ce72118617d82a7147f9b44fb20bd`  
		Last Modified: Tue, 13 Aug 2024 00:48:34 GMT  
		Size: 52.5 MB (52451278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0297081c3c9f03154f1e618078528a7e069eaa260e005a9bad44ea4edd4e8120`  
		Last Modified: Tue, 13 Aug 2024 00:50:25 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
