## `debian:testing-backports`

```console
$ docker pull debian@sha256:72b02041e1cdfd047398165ec112fc78cdee01aa74b20fcfef28613fe3f4916e
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

### `debian:testing-backports` - linux; amd64

```console
$ docker pull debian@sha256:15d1ad0b202e3302bf30217df612bac4b6d9991851f98dcbc3299a2c40bcd580
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53238944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25a2f961482705e8a75f4398d7926311688ff2a0d11a29de6b2b797ca1ae4ebf`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 00:22:01 GMT
ADD file:7cd25c47cea2c8bd0960e59bbb70e07523a0cf45c77c330ba29dd0040fd2ae3a in / 
# Thu, 17 Oct 2024 00:22:01 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 00:22:06 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:bfa02bb5331e16713de983c8b0601bfcd284f32c36808d948bf38003dcc2a65a`  
		Last Modified: Thu, 17 Oct 2024 00:26:18 GMT  
		Size: 53.2 MB (53238722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46b4b2345b023d4da3abd49e93a8beb6e7029b7e4515a80dde33c1697defce13`  
		Last Modified: Thu, 17 Oct 2024 00:26:25 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:edf42196519a3509cc5125753d4f40d2db6af8ccb63c5f27e9c9753d59322c97
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50146320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc53ac3c947c4a197c3a1a91fe0db961a4afa79c37d8640c235fbbc79a5c4a50`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 00:55:26 GMT
ADD file:8ca508f4aa10fbbd4763585ad66153e001d58d356c8d78804db912ec3b2c26cf in / 
# Thu, 17 Oct 2024 00:55:27 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 00:55:29 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:92fc55f27ee43568f631f9e9bf8b96fc9cc011f9dd8f77d49e2f8f720ac28722`  
		Last Modified: Thu, 17 Oct 2024 00:58:45 GMT  
		Size: 50.1 MB (50146097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a68dc5efe0609cceb5e9cca62079f87a7412d1880e78c3c03b3557c61a6e4bb0`  
		Last Modified: Thu, 17 Oct 2024 00:58:58 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:4367cd61a4aa95495d76b0fc72308e8621e04ad606bf5c45cad981c00627b813
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 MB (47659874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bc2f9b09333f178018b1d86439a738b9f1543ee07d3f7585398bea6c6a5ac47`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 03:05:01 GMT
ADD file:445312fa78b709be6c28d6d5508c2657f3834595879ee37cd682577916fd2e22 in / 
# Thu, 17 Oct 2024 03:05:01 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 03:05:05 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:8a32718205f28682a37c9402dea50cd26fa77ce85fae02e2da7f571e3fd30faf`  
		Last Modified: Thu, 17 Oct 2024 03:09:55 GMT  
		Size: 47.7 MB (47659653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bfa4914db999ca9910e3e9d8a6bac4345f603fa0d829937abe51de11e62cb07`  
		Last Modified: Thu, 17 Oct 2024 03:10:03 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:d4b611e0013377ec08f6aaff7371a31d774e142e89c8c25f0064d8b91e173e24
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.6 MB (53599979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4e82c0627458164f3170b352a265911cf47ddf912461806aee6c05c9d88e3ca`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:13:03 GMT
ADD file:e3e9f477c791fc688010cc87eaedfcd80ede2cdd070c953518b515ed1b668a55 in / 
# Thu, 17 Oct 2024 01:13:04 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 01:13:07 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:a6d8e57ff3309f685dd823e43fca05a8da4dba501d2eae9451a046edaeaca8d2`  
		Last Modified: Thu, 17 Oct 2024 01:16:49 GMT  
		Size: 53.6 MB (53599758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f4f52d342344bee65eb460d57b8a152d4bd4dcafdd2ae96843013f8184de9dc`  
		Last Modified: Thu, 17 Oct 2024 01:16:57 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; 386

```console
$ docker pull debian@sha256:148648a084ee2265b4bf01dbdfad9f628bc680867fa696c9633d18a544874b2c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.1 MB (54077656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:259c9f7f76997f3f10c84928b146844d4acf2e89fb066aac1c96d8508a0ba1e6`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 00:40:33 GMT
ADD file:a7ecd48c19b46d7a871710ed2d610975d1c54151fa41fbce20c1568c6aa36e82 in / 
# Thu, 17 Oct 2024 00:40:34 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 00:40:38 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:ef528d0513269e1e9a57e7933e2f31b93816b991227b43f1d3e56d437c4f3370`  
		Last Modified: Thu, 17 Oct 2024 00:45:18 GMT  
		Size: 54.1 MB (54077433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7f9fe0bfda6feba64e4b1c72beb28f9d75b8d633bd0c1f7ea3949a2dbc4c19a`  
		Last Modified: Thu, 17 Oct 2024 00:45:26 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; mips64le

```console
$ docker pull debian@sha256:b226ef2fdd6594982434568129027181c119e85ac19ca162b25bb9679fe849fd
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.1 MB (52128691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0454d3c8e82d53f38991a13bdb7277ef97e59e0fd59c754bcb55c51fb434d99`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:12:39 GMT
ADD file:0b3096a7990b518ac87fbbde3a9fdb21311fd2379ff418127666988a0cef4ce9 in / 
# Thu, 17 Oct 2024 01:12:45 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 01:12:58 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:a975ead2645831f25c1c869d441f073d183882a28ac8f4deb27c446f0f189418`  
		Last Modified: Thu, 17 Oct 2024 01:21:06 GMT  
		Size: 52.1 MB (52128467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31721227d3356ef82d418375131a2b7f19be4cffda98ea1db5c06dbdda9bda36`  
		Last Modified: Thu, 17 Oct 2024 01:21:15 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:9013bab7d94d6deb8958284aee06c6f7f8165037ccc461412306d0145b9ef5b8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.1 MB (57126881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbaaef9f7af19f2599fab9befab835d7979eb8daa7e6ce90172b773132b8dc63`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:19:50 GMT
ADD file:5c4544ac0d27b357afba9feb379224b111f7149e7b3f21fe35317eef03b8bcea in / 
# Thu, 17 Oct 2024 01:19:53 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 01:19:58 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:311042d460227ad120f24056ab56c7fe2202f03f09ec22ed4f93b2ffc0adb201`  
		Last Modified: Thu, 17 Oct 2024 01:23:20 GMT  
		Size: 57.1 MB (57126660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bfc1b701c9dc531fb4cfdb34e0b054888beb3c9d3728e0eab55cb2c223ab0a7`  
		Last Modified: Thu, 17 Oct 2024 01:23:28 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; riscv64

```console
$ docker pull debian@sha256:ca671cece153cf95bcbece5463c8dc36de0b43cfcef9ae3ae1ebe56960946dec
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.5 MB (51529389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:010479cb1dcb98b3c1e2a226572cd131489f62a33c7b80049b324b76f1ca82d5`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:10:18 GMT
ADD file:b0ab5ac595ad741930a2f60e224b42189315492e0837eac491f53a9eb60e7d7b in / 
# Thu, 17 Oct 2024 01:10:21 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 01:10:34 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:569b3ccb4a7ed8765dde5567b672e7b833f45410878496943c01617ebc4331c5`  
		Last Modified: Thu, 17 Oct 2024 01:16:02 GMT  
		Size: 51.5 MB (51529165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dac8715e6fc41c5276bfe2efba4f023d469d28e565b7e878f08d01810bba9d5`  
		Last Modified: Thu, 17 Oct 2024 01:16:12 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; s390x

```console
$ docker pull debian@sha256:272f2cf3e2393b6dd7533938ab3fe3a03513451f75a421ef04daa617381fec3a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.8 MB (52809077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b631620c07954277615955f64455209eb1a202fcb05c03d56fb1b435c562208a`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:47:36 GMT
ADD file:61f096f81ed7cfc876be4edad4438e9e9e439382507d192f09f51c428e99a482 in / 
# Thu, 17 Oct 2024 01:47:38 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 01:47:49 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:f66a11769d6242f4b78b255eed3607d4c3b4b3fa3e8fb47724dd3586e9a6da4f`  
		Last Modified: Thu, 17 Oct 2024 01:51:31 GMT  
		Size: 52.8 MB (52808853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08eef8d8b96ac33278304a92bc0a66da423eae15a1b7ffa01055b42eea358542`  
		Last Modified: Thu, 17 Oct 2024 01:51:36 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
