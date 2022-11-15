## `debian:bookworm-backports`

```console
$ docker pull debian@sha256:e777430d09f5438d3811278ede2edb51191b229314000496559c073f85ce6468
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

### `debian:bookworm-backports` - linux; amd64

```console
$ docker pull debian@sha256:abc75c72ef18773b067943a8a9673750fae98484c5b794e8475f3f93fad4995e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50297230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:072768c2a2e66a7bed0ea11c93ed04133e5f2ba0b800b8295cb63ed195e0e0a2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Nov 2022 04:04:23 GMT
ADD file:7d616c027c138495879d0578d333124a7a41f161d38339949eae9fc46a97bafc in / 
# Tue, 15 Nov 2022 04:04:23 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 04:04:26 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:6e44dba964a0f1646d06ab7f617603ef51c645dd641b4ce74411770449b003f3`  
		Last Modified: Tue, 15 Nov 2022 04:07:53 GMT  
		Size: 50.3 MB (50297005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c411151e4a916a2b6bed79336462dd83d5f39a4fd1ca2f1d9e4ce8bb83592390`  
		Last Modified: Tue, 15 Nov 2022 04:08:00 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:d19933b0abfe66cea4d8192e1cb52793959924e5ffc73ebd4fd8191b126c11ef
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49266067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab808975807d0291b34f6f1d2ee16f008a579ade0e758db9ea73773d8e849eea`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Nov 2022 01:48:32 GMT
ADD file:f5954c36a3601d3dcf67f8701fe7691c7a94bc36e88827c06ff7338a52d56c5f in / 
# Tue, 15 Nov 2022 01:48:34 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 01:48:41 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:34757784ba8ccecfd4a2f549aff99cd98b7b291a61176def51827463bc77aa00`  
		Last Modified: Tue, 15 Nov 2022 01:53:14 GMT  
		Size: 49.3 MB (49265841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea519cc0b59c9066fa22011a55ccba82a76d2c001b7a3197cb5075203b23ce7b`  
		Last Modified: Tue, 15 Nov 2022 01:53:24 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:704584caceb59292b7865aaf9d5232cac27294b63cd51918b1402a4e7679f526
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47088594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec1dc1669473bad667992c1f012e8e5a1bbf4555e4d849aeba38d1c46eab503c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Nov 2022 03:42:37 GMT
ADD file:7196c14a33cd1774b746a830598de6b6368174bf15faa83c36c244a6e27938fc in / 
# Tue, 15 Nov 2022 03:42:38 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 03:42:45 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:192a2a7ee5b2cd81557e51320bddd5cf2b318283cd7f7c0c0998525448fcf94a`  
		Last Modified: Tue, 15 Nov 2022 03:49:02 GMT  
		Size: 47.1 MB (47088370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f2e647e6d7a328f701242cb5061142a731d8ce938f6135c1dc5145952a6e697`  
		Last Modified: Tue, 15 Nov 2022 03:49:12 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:e951862d473047c48d017b0ae02f5eb35605eeb4a0def138f806da72db475593
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.4 MB (50353528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dbc8169cb56aca1a37d497c3c09d7da99279f169bdf0029b96500f48373cd68`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Nov 2022 01:40:57 GMT
ADD file:c622ea356e69bcfb00a0066c22b326eaa514f83ce688202c38b1cdf4e279f65f in / 
# Tue, 15 Nov 2022 01:40:58 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 01:41:01 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:d350c5c763d25fc284c82bdb22268efbb6376d35695fb6f09eef45b2f3dcbd9b`  
		Last Modified: Tue, 15 Nov 2022 01:43:42 GMT  
		Size: 50.4 MB (50353304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a388718881ba9fdb3ed61a5bc422ae96694aebd9c4fe52266f0b0d509a63953`  
		Last Modified: Tue, 15 Nov 2022 01:43:50 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; 386

```console
$ docker pull debian@sha256:6a90bd4ebbe191dca8388c2c114cc5cf413398f06884296bcbd189afcb0e6c79
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.3 MB (51345132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36c4231895aba98ce8b59552dd0dc7dd1699438dccba8d7726434e7e8113000a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Nov 2022 01:40:45 GMT
ADD file:dc52b19235f576e4601a85df40bbca1bd78982afc56d272746728294ee8a335a in / 
# Tue, 15 Nov 2022 01:40:46 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 01:40:52 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:eed5d6b8bc9dedab6a360f9b58991756d109919cc4cac0c030d7c94377a3a13d`  
		Last Modified: Tue, 15 Nov 2022 01:46:00 GMT  
		Size: 51.3 MB (51344908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4042ca96def17973d32b5e2b3a467cf6e688bb5f1d614258f9526919dc7cece1`  
		Last Modified: Tue, 15 Nov 2022 01:46:09 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; mips64le

```console
$ docker pull debian@sha256:7fcca122167406affb875a8e121e46b758a58d523fc4cd9fe8aba2466e298e1c
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50314418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ca2b797374b17a6ce039f24729828882fbe793c1321a9b2849615536da93e51`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Nov 2022 04:11:59 GMT
ADD file:0d439a2fdede63b0646f17fe0578b4ebab24012a35c93e6e63e5c511ccce8fe7 in / 
# Tue, 15 Nov 2022 04:12:04 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 04:12:16 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:52449a481885eb7aca2b2fbb088c8d233a6249a8aaaf65e32f8c268ad8340850`  
		Last Modified: Tue, 15 Nov 2022 04:19:19 GMT  
		Size: 50.3 MB (50314192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a83df67b53f6a81ed173410e1f2ce307db48458c0fb0dabbc9cbb599bb161d5`  
		Last Modified: Tue, 15 Nov 2022 04:19:28 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:1d124271323c8f0d72ab769cfe92bcb34347ae5c8269c5d878942c1356845741
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.3 MB (55339028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:701c3613a2606a64318e6c0a085a66d4ea79f1aff63ac13b836c68de9cb87f63`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 03:12:50 GMT
ADD file:1f55ca9aa64d69398e6bff99fdfd63dbf022ecefc46450a6fd32ae46e9718557 in / 
# Tue, 25 Oct 2022 03:12:53 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 03:12:59 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:264fa02db63011b604885c7feecaeb78fbee4ce4d8191fa5050f4fef88c74001`  
		Last Modified: Tue, 25 Oct 2022 03:18:00 GMT  
		Size: 55.3 MB (55338800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3855318dde18ac35b01a84f8fbb8667e7b4089ffd2ea81f973ab7c80f880b98`  
		Last Modified: Tue, 25 Oct 2022 03:18:12 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; s390x

```console
$ docker pull debian@sha256:0c3a1a5f833504dc9a0e6f4e56b738ab7d0c1f618d69a14cb3a5bd64ee7eee83
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48707625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8502835a8a992a5a6871006cad7480ba1206d6f8d158e0c902e2945609cb2274`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Nov 2022 01:41:40 GMT
ADD file:c4f7dc2db7bd88fefb0d92414f2efb03e7ea14cb79f11eb857199ab31069aaa7 in / 
# Tue, 15 Nov 2022 01:41:47 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 01:41:55 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:10619af8bae5734a158de8dfe5f8646bf40e3e004bd7a3c4ee4a89da0bbb688f`  
		Last Modified: Tue, 15 Nov 2022 01:46:45 GMT  
		Size: 48.7 MB (48707400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eccd150a00af4476d2960dafbf99256d4def4b1e6cecb1fccae644ca413197c`  
		Last Modified: Tue, 15 Nov 2022 01:46:51 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
