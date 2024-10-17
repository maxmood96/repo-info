## `debian:stable-backports`

```console
$ docker pull debian@sha256:852dc755ece273d57b6f4dfd1930c25808485d6409285ed48bcdec5058486f69
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
$ docker pull debian@sha256:f9fc17e5c33b0a983f3ee841e840d06664fca3040ad3c45560f04baa0d229a87
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49555216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43103c79b9305d63c3bd1c7699426f157ff34c6f9c4c94c8f6df6415191aaebd`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 00:21:40 GMT
ADD file:5b0b330a1744d2fc462db73ca1ede3057676f55ba9ba4fbd0c8f1dc7f35e4fa5 in / 
# Thu, 17 Oct 2024 00:21:41 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 00:21:44 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:5f399c0ccf91e64b5bd6c7483b37ef860d40c3b621e2543638d6f73be6022ba5`  
		Last Modified: Thu, 17 Oct 2024 00:25:48 GMT  
		Size: 49.6 MB (49554995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e65e296a38f44013ee9025314a88ced58804c4dd1f7ff5dd1633ee7089e333b9`  
		Last Modified: Thu, 17 Oct 2024 00:25:55 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:c08e9ff443a5dc49af27457811995bb4c42980da3bbeabf465de62b8f0d70d8d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47330715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cddcc408b27a2d00c6d4822da4645f528ab415ddce6dbb2b9fffce15798588e5`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 00:55:06 GMT
ADD file:5a6ca6c398caf783271e97f0e110e9cf53955304db967e78094aa5d4bd1caa04 in / 
# Thu, 17 Oct 2024 00:55:07 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 00:55:11 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:1f19ba83087ea5a419d7d26a8b21cefed9a0e836845908d9c67cf4c0c5cf5ac1`  
		Last Modified: Thu, 17 Oct 2024 00:58:13 GMT  
		Size: 47.3 MB (47330491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a1d2e26c5a2b143961c836d642efeeff656ffa40f36daff31ae0c02574cc9f7`  
		Last Modified: Thu, 17 Oct 2024 00:58:22 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:3c23bc4e5a42d6eed200aacc04f71700a15d1770d5838965fcd0ea6c916e504b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.1 MB (45148146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1a9cd4f8ba10a944aa9d5a41b586b8c8f37202eb6d8a4e6aa4fada84496bd9f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 05:14:56 GMT
ADD file:372c663cd46ff5eef36f3a802b3a97ad7a1c9e6e6d9fba01d5768cf0cfc6a4f3 in / 
# Fri, 27 Sep 2024 05:14:58 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:15:02 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:1c38f5fbe6c9aec03cce965911e2a0b50e9de8ff99188631d3881d0ad54c1019`  
		Last Modified: Fri, 27 Sep 2024 05:19:04 GMT  
		Size: 45.1 MB (45147924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c02700594728b4acf212db5b5440adc9b993597bdc924dac65706f1bbffdf389`  
		Last Modified: Fri, 27 Sep 2024 05:19:13 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:03e8350e3b5fa6c6c5a37bd90889366ccaad064f37cdbbd1781136ef394ec1f9
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49585136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b849de541a0146b0ecc1658351a2126e5ab5a901f0491e667d8b42ff815bec4`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 04:39:06 GMT
ADD file:467ac5787e38284ef2d5c5a94a9cf5fffb15c33e414ef2241905bcfe2c8b1e8a in / 
# Fri, 27 Sep 2024 04:39:07 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 04:39:09 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:2432e489a182835bc1d7c8bcdd3360c8ba575422e6348c42db9ff72e6be02b49`  
		Last Modified: Fri, 27 Sep 2024 04:42:35 GMT  
		Size: 49.6 MB (49584917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2e75d5e630e44ff4c17abb9fbaa5d03ba6899bf7ee28fad121da331d6ea392a`  
		Last Modified: Fri, 27 Sep 2024 04:42:42 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; 386

```console
$ docker pull debian@sha256:98c0800788b92edfed4c8e4f434d428f5706f1056ab45d76ce2c3fb93e73b785
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50577041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a04b218cda7840aabf69a06f9f19793921acb6025c9b2da4ac3f9dbcc023ea7`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 00:40:11 GMT
ADD file:77a67911f7516e842633ee4e2e8cd8e96a98bdd6df5c6b0a68794aa2e3f0cf7d in / 
# Thu, 17 Oct 2024 00:40:11 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 00:40:15 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:0d4f01c14d037e59aeee1b97d0b72f4595f4f68cb8af1dc8909656eed2e4ae16`  
		Last Modified: Thu, 17 Oct 2024 00:44:42 GMT  
		Size: 50.6 MB (50576821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e640e2fade7d18df4dfcc5fe4ea4264a4f25574d8eb6cb157ee76083ef3fa803`  
		Last Modified: Thu, 17 Oct 2024 00:44:50 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; mips64le

```console
$ docker pull debian@sha256:52b04db0f65ecfdb93b829283a4b30a68eb1debdf21577d739ad6cbf321ad64d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49561869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34be17385dad9cdb0b880c719df87155b654a9c98cba041964e1f1a0e67e8025`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 09:04:49 GMT
ADD file:f0244c6bdbb50b2376fe255f8387f412242f4a50412522be702909c1fc17a5ad in / 
# Fri, 27 Sep 2024 09:04:55 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 09:05:09 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:7b341ffa4a71d4ca3809a7e676b67045a8008088f9e4ef96edcd44fdfca121d6`  
		Last Modified: Fri, 27 Sep 2024 09:13:25 GMT  
		Size: 49.6 MB (49561644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4a1829b559a4a8d46eda6e8da3447661b77d90e2c9338143050fde99da4f86c`  
		Last Modified: Fri, 27 Sep 2024 09:13:34 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:265f2c01281da414aac061ef2f3d36e97270f6d6d0175530de7a661caeeac41b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.6 MB (53555386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e99c2b22b5aee1cd42a6afb9e89dfb47ccba44f8fe6e113afd86d436d909e00`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 05:33:42 GMT
ADD file:107fce0e2935d8dd2436177b74b172f737ecd19df6449805ed6215fbc89e2682 in / 
# Fri, 27 Sep 2024 05:33:44 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:33:48 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:69239a6be9c2075005cb211b21c4d3e30e9991707bf374745de76b883517a184`  
		Last Modified: Fri, 27 Sep 2024 05:37:08 GMT  
		Size: 53.6 MB (53555165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec537e2945b2fa199c102a0a4fddeeeedc5d45c5479864d5d4f3416a532aede1`  
		Last Modified: Fri, 27 Sep 2024 05:37:16 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; s390x

```console
$ docker pull debian@sha256:0a6f54ebd5ca78cecc551da614c13deb13bffe91b6d7491b3672daf3deb8b1b0
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.9 MB (47938871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:517f16db5246078c580ca712a036d4e8964c085f3f24d458c0d663d532f60e5e`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 02:44:20 GMT
ADD file:7bc52cfc79ac6522699b9f40506294e674da790ee5da0e32a1d301c1b27384b6 in / 
# Fri, 27 Sep 2024 02:44:21 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 02:44:29 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:349cd307f1a7373fd38f6f6929dcb3ef5a2de93bcc4018c8240d1b79c86974b0`  
		Last Modified: Fri, 27 Sep 2024 02:47:58 GMT  
		Size: 47.9 MB (47938650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6714b4c9b180960c6b48e10aa49c13735b7eb8e4aba963885582f205ec215eea`  
		Last Modified: Fri, 27 Sep 2024 02:48:05 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
