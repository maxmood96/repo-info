## `debian:stable-backports`

```console
$ docker pull debian@sha256:16525891470ce6d767ed7968fcdb2c42bd410bcadbe73bbcc1f02fd87c20e119
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
$ docker pull debian@sha256:87ee647ae2881679879d7e3976544c373e1d5a08c20a98fe3cd66444e146f9fd
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.1 MB (45148672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4227a2edeb112d651cb4dcab8e46296a2b305375012f5b30f09431f1bdd0b15`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:59:17 GMT
ADD file:6d69eee4be8d3dc69096ba6d0ae6083cd08d608e0f6d4bf4c63d87574dda52f6 in / 
# Wed, 04 Sep 2024 21:59:18 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 21:59:21 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:1aacfd79a22fc6f8b7d0a3e28ed5a6a60a17b6a06be91a14ecf3b0de0ba02bed`  
		Last Modified: Wed, 04 Sep 2024 22:03:46 GMT  
		Size: 45.1 MB (45148451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef6ee6d15dd758e70dfdd88d0913801e11eea7a8b8876367f658a8892b5b4522`  
		Last Modified: Wed, 04 Sep 2024 22:03:53 GMT  
		Size: 221.0 B  
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
$ docker pull debian@sha256:50b3fde9129f1a0d81ca4fb0cf396bdc71acf0ff8d7b595bf9a72ec4340b4835
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50574819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f7eec41a28078af006546ccde2f36b5674a4d03547f21b040968ac733980c1e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:45:46 GMT
ADD file:4559f9788c783aa5e9fb6e7fad945accc332ceec027dd9538d8311339c5257b1 in / 
# Wed, 04 Sep 2024 22:45:47 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:45:49 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:c00c751b531b3fe84c347b00345768dd683cfdcac65da2539cdd5efb5b79be42`  
		Last Modified: Wed, 04 Sep 2024 22:50:18 GMT  
		Size: 50.6 MB (50574598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51cdbff0aa9ddf76e885f58e34f342e2e76073c9d1825b071bb5c0b269347f33`  
		Last Modified: Wed, 04 Sep 2024 22:50:26 GMT  
		Size: 221.0 B  
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
$ docker pull debian@sha256:fff657eda805c7b84c8e7f4c72a4497e83e0f943862b128fe85fa10f9857c065
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.6 MB (53554137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35e992e5bf143e32614af1467812338d896bf7a94dbb8df95ca1a96861040003`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:27:20 GMT
ADD file:ae3bde839efc5a250f67ee7a4d92c9520f9afaff9ca2bbc2ccbde052ac860e59 in / 
# Wed, 04 Sep 2024 22:27:23 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:27:28 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:5550293488d0805582bdf4862318ba749cfc0db782025b3fcb0cc3f955682006`  
		Last Modified: Wed, 04 Sep 2024 22:32:24 GMT  
		Size: 53.6 MB (53553914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:530ef257ea4a66219a63a38855443159b912cf0be2897a5b74ecbe952155c825`  
		Last Modified: Wed, 04 Sep 2024 22:32:32 GMT  
		Size: 223.0 B  
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
