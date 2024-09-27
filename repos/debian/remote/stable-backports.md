## `debian:stable-backports`

```console
$ docker pull debian@sha256:5303501d36d5a4c40c28083e7d90a5ffb6df3aee17c20d58d632ebbe5bb59fcb
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
$ docker pull debian@sha256:74f58af799b8d850d31817fd9c82e162f267771fc80cf0f64e0e7dd3a99475a4
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49555259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5b624461946f7a9a5ce4dd7044b47dc2dce6d0be833850b29a9c326a840dad7`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 04:30:47 GMT
ADD file:8180c97be22a2926cf796b83caf1405a2d65a0faabb05375c064b0ebd34622df in / 
# Fri, 27 Sep 2024 04:30:48 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 04:30:53 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:0e1b4dc9987e1b9c33773bd60df3344e52af12b3854c1845ddcd6d0eb0f2d05c`  
		Last Modified: Fri, 27 Sep 2024 04:35:02 GMT  
		Size: 49.6 MB (49555037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f3e193c5498762509faa9c3787710dc5edebfcb83038fc58a3bb7140f425f81`  
		Last Modified: Fri, 27 Sep 2024 04:35:10 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:cd55ed13934302dd1363f2db813bed1406dac3dad92c7baa7bcb0abfdcb6ef54
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47330941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f1b6b9b2a5ec0575cc9128427d0682cbd97c9288e94148909d145ee210a6e35`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 03:19:45 GMT
ADD file:d006460fcd550f9258fd8849b77aefb3b61a36731cb1ab6f046d9209510d304b in / 
# Fri, 27 Sep 2024 03:19:46 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 03:19:48 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:b4adef03fc680ffd29451cb61b1c77311335f7b166ecab28f0bc1d94bf5551f0`  
		Last Modified: Fri, 27 Sep 2024 03:22:28 GMT  
		Size: 47.3 MB (47330717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43dc524a538eeaa3b2dba4db9dd8e07e81bf2c0021995395c6b6171f1ac48909`  
		Last Modified: Fri, 27 Sep 2024 03:22:36 GMT  
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
$ docker pull debian@sha256:37796e5e3b33cc53d2205b36aee4bf343127ed3485014945423ef884541ebc19
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50576899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6cd7c01f0cd3ac00abf333c35428ef7658957266c7abdecd654c7b2d1b12df5`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 07:24:20 GMT
ADD file:210168087f8ed83d6c703e12c83e67426921eceec028d8e54116734d7130b4e8 in / 
# Fri, 27 Sep 2024 07:24:20 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 07:24:24 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:e912cc1557f63d252f988720f732cecfe943f7f0d4174c45f1e252383ebc0822`  
		Last Modified: Fri, 27 Sep 2024 07:29:18 GMT  
		Size: 50.6 MB (50576677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a936bcf2d6ad2987d2725ed3ca144ec5da8c38f5cca4b3d056aa4924b9884716`  
		Last Modified: Fri, 27 Sep 2024 07:29:25 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; mips64le

```console
$ docker pull debian@sha256:451433e834b5d11060eec46c049b03433e31a382f8573213f726edaa5748fc6b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49562226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:209a840b19d8630d302316bc50ddcc8f8452d7566d4407e454edaf14c9616506`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:17:28 GMT
ADD file:cabec016e206ad553b5e022429ce54d85540ce329e716375f22e226573c3580e in / 
# Wed, 04 Sep 2024 22:17:33 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:17:49 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:b141cd4b325e0a7013a84c4ab5346ecabc6277e04fac652b2a3c8839c82b17b0`  
		Last Modified: Wed, 04 Sep 2024 22:26:03 GMT  
		Size: 49.6 MB (49562004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c9a61806c2aa9d676834f49ed6c1ac0b6df7dfb16bbda074f322db3794a343c`  
		Last Modified: Wed, 04 Sep 2024 22:26:13 GMT  
		Size: 222.0 B  
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
