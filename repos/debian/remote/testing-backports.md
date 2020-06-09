## `debian:testing-backports`

```console
$ docker pull debian@sha256:53a1521252ff7ae54f61732a61cfaa24107d8bf62333368886eadd2fe436ad6b
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

### `debian:testing-backports` - linux; amd64

```console
$ docker pull debian@sha256:921cbb6fb00221315ea6bce6c4bd5e008923bc1fb2f4330fbaec20143e38d29d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.4 MB (51413718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0328f899d14430aa3b16d00123c1a262b8c06d0d22e9e84ce3d369d44c4892f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:23:49 GMT
ADD file:63ef8f38bb25d9c0e944d04e91b6d6c6eb32289709829d3bb80998e94ff2a506 in / 
# Tue, 09 Jun 2020 01:23:49 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 01:23:54 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:0ab9185ddfe50c951de582032c5e29e21a851a328056e6bee6299e0ff55ec807`  
		Last Modified: Tue, 09 Jun 2020 01:28:27 GMT  
		Size: 51.4 MB (51413498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a31facb95bb98719772a36de029b60bfc0befc171931a1ab21a0dfca3214f6a`  
		Last Modified: Tue, 09 Jun 2020 01:28:31 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:43e4e7a442b68c217d25c441960269a800170351887b2743a3e06e30f1a5a9bf
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49386902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8c603b16cb582b9cafb2b8bfe963316e8f054bb2dec818810282ebfbe5f7ad9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 00:56:08 GMT
ADD file:ec4e832a8c722e5ba63ff829e9e2965e61d34e7fa552a45f9250af61100b99f3 in / 
# Tue, 09 Jun 2020 00:56:12 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 00:56:20 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:edb0509d8d0a3427a82b93ff4a3cdb09f3c6b29dbdf9bae8afa9d3c9804fa804`  
		Last Modified: Tue, 09 Jun 2020 01:03:31 GMT  
		Size: 49.4 MB (49386679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9db63d04da02ad174f9b79bf2a3ab99adc621ec3105a0ee342696c3682bf5ca1`  
		Last Modified: Tue, 09 Jun 2020 01:03:37 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:b70d2e0be9be880f3fc6d4c309b2e2c188176ec31fad53d8a8f356077c0a7712
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47198055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09bc2fdbd4ded2aeb1d3f4496a42b27d8d2a1c52c97502f344336d8d5f52093e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:06:57 GMT
ADD file:a92bebba26bf70b6cc36cec474ca64ec08f9191f03a453491c4eff5565784990 in / 
# Tue, 09 Jun 2020 01:06:59 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 01:07:10 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:e0373ff65f424cecbb68f974a2205ed5bf26e67688deae59bcc85995d6dddca6`  
		Last Modified: Tue, 09 Jun 2020 01:14:12 GMT  
		Size: 47.2 MB (47197832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93d1ff11b03660655580b61b4db99aaab0c5bfa4ccf85d105bde273b678c38fa`  
		Last Modified: Tue, 09 Jun 2020 01:14:19 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:bb07a7b4038e303960939c6d202b8e4300ae2e32371b7248eead43593d938d16
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.4 MB (50354045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9cb9970535faad61da62c42354e00c46e628ecb97ce23552f4f0f92ab626804`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:55:08 GMT
ADD file:3705d77b7f9ddcac964099514289de1ff74f3618435e1c0846d112f5075abfae in / 
# Tue, 09 Jun 2020 01:55:11 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 01:55:21 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:a2b4880979f186e2b0fb3aceb4435b72654989a46906ae64e190d06c969f2926`  
		Last Modified: Tue, 09 Jun 2020 02:00:48 GMT  
		Size: 50.4 MB (50353822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bb906b351f22604c9274767825732228f023d0c2e473a5c3770af28415f730d`  
		Last Modified: Tue, 09 Jun 2020 02:00:54 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; 386

```console
$ docker pull debian@sha256:b2da89d3075cd93c8487f2342c3adceee23abf0dcd834466def564a13290ac7c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.5 MB (52523026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34c4645116b822699634a0fff7ebd9edda2ff3aeb68a2b366dc00d504a09de03`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:42:48 GMT
ADD file:c0c632031fb28fd966af219c01671ab3f2a28056bd8d9c5f603b69418bfa1992 in / 
# Tue, 09 Jun 2020 01:42:48 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 01:42:53 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:5df710d3ecf23d12964ebb23f2eba3207f5333c27c0c906da0842ce86a443de8`  
		Last Modified: Tue, 09 Jun 2020 01:48:49 GMT  
		Size: 52.5 MB (52522805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02a29f4e0fcd463c6e88295c2626f75648b9fbaa0626afa5e4a56c1f3245105f`  
		Last Modified: Tue, 09 Jun 2020 01:48:55 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; mips64le

```console
$ docker pull debian@sha256:b2749ae0e70ed820579365c41d5b100a7877dfd71ff1db4b87aca16eb1c75bec
```

-	Docker Version: 19.03.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.2 MB (50162275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37b058c5c4ab36f3f5d60dfa70a82896aab1b843580f872796112104ea224c06`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:13:36 GMT
ADD file:b1c981ebeb4e09d412b3437ef7fb0e52b702959d0e06a7046aa6964978f9518c in / 
# Tue, 09 Jun 2020 01:13:37 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 01:13:46 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:8b3ff1428667ab0f3d48d4b4642b04e41efc68dbc7b6b95371c90eb0e60ac4f1`  
		Last Modified: Tue, 09 Jun 2020 01:24:21 GMT  
		Size: 50.2 MB (50162052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dede7e43a5db9946e3acfdab1dbbd0c5d2bb86afa729185a62d53f0e5d172245`  
		Last Modified: Tue, 09 Jun 2020 01:24:31 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:9f8326ac44f3b4b7752b72c30b7dcebab397251d07e6a5840131001db3c2f076
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.1 MB (55148225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c373533d52677fd080889073e02ac7e6b68c290b55db8a9f30b0dfa0cd18dd4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:25:56 GMT
ADD file:72fcd44a3cd61718c43b8fd4856b710ec66a4c58ddc118863a85dfa8016f5c8c in / 
# Tue, 09 Jun 2020 01:26:00 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 01:26:14 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:9ff154698924dfd0c8d74f3ad2e91d17dd68ef0c5b54849d3f7241b9df7886b5`  
		Last Modified: Tue, 09 Jun 2020 01:38:19 GMT  
		Size: 55.1 MB (55148002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:785ea13e8fbe40b418e3c7399599ea434d641e57442e16c2a12e599cbce90b7f`  
		Last Modified: Tue, 09 Jun 2020 01:38:32 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; s390x

```console
$ docker pull debian@sha256:006983cdc2be30cf2f04d3d2fe67c754158b427b307fda8126bd4408cd0d916f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (50017862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f9b754ddb1884d018a24d3057d3b7b3e234c65a20c840ddef9263b6668a142f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:44:32 GMT
ADD file:896c8fdee5ac4956de95b560e2a554657f15dbc99efc06afb2f0214200806d27 in / 
# Tue, 09 Jun 2020 01:44:35 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 01:44:40 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:a975764cea82ba35daffff6181552a130f94c9e9f6362f6d4b825304a753b83f`  
		Last Modified: Tue, 09 Jun 2020 01:48:16 GMT  
		Size: 50.0 MB (50017640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:870776e00989cff507b16b1d9fe18788dcdd12a6721c3f4714180b0b121be1b5`  
		Last Modified: Tue, 09 Jun 2020 01:48:22 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
