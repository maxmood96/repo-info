## `debian:stable-backports`

```console
$ docker pull debian@sha256:f44091b91047cccc6f894fe802c481bb87ba44e830f362f56616374adef3d0e3
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
$ docker pull debian@sha256:dbd5a178bc174e9f70af98e5df98b35cf49285914e843fdce2b1a3fb0d94df6f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49556955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c71743fae6b23d4d64db229ed8195238d766ec5775d7616fc0365113b905ecb9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:31:57 GMT
ADD file:2c52b73c7ffcba2dddd245d8852699dc49eed34754c00e967efc063644b45be3 in / 
# Wed, 04 Sep 2024 22:31:58 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:32:01 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:666488449e265d667aeda2b2cef0bc12afed899335bffe44fd5bf7456f72e9a1`  
		Last Modified: Wed, 04 Sep 2024 22:36:07 GMT  
		Size: 49.6 MB (49556731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48ea3b6a4efa6d98921ab7252e921cdc836c41a21fdd2e6fc64e42ffd38f48a6`  
		Last Modified: Wed, 04 Sep 2024 22:36:14 GMT  
		Size: 224.0 B  
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
$ docker pull debian@sha256:f9a40a2b133255bee3de7ba6c7924d216df1ee96033ccd3c2aae7341d44d7cae
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49585815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9f9df31f9582b0582b4e791dbf2df41f7ba3501dd1587eae3b0012588438715`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:40:42 GMT
ADD file:aefd88d90b7065f1ebd802cd2ce02290bd918d612ccd1e72ed134583a85b87a1 in / 
# Wed, 04 Sep 2024 21:40:42 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 21:40:45 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:f8763adf53582aae4539130df0a79824468a12d27cb0f988a82aa6c3403901e7`  
		Last Modified: Wed, 04 Sep 2024 21:44:18 GMT  
		Size: 49.6 MB (49585594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d5a1b5652abee13ae1a7e9751fc89adeba1bc70d3542d1144691a4decf6f75d`  
		Last Modified: Wed, 04 Sep 2024 21:44:25 GMT  
		Size: 221.0 B  
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
