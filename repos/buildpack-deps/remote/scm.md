## `buildpack-deps:scm`

```console
$ docker pull buildpack-deps@sha256:b1465fbe338256ae5979c4f31f7601f69867ac3d762f25a2c514d04b2af59335
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:8fa75851d950e798bf713fc586f9b8b2c81867e896cc158d65f6bb945b70033b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.7 MB (142700003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6475fa5515c86efb1a506dfdcd396422c7f2a13c3e93f8270322ea374ad817af`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:38:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Mon, 16 Mar 2026 23:25:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:8f6ad858d0a46fa8ee628532c70b8dc82d06179d543b0b09ec19fc03d4c5b373`  
		Last Modified: Mon, 16 Mar 2026 21:53:17 GMT  
		Size: 49.3 MB (49297530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b012eb15dff0bce418c03ec940325aee6aa4300d771c325728855697e620c63a`  
		Last Modified: Mon, 16 Mar 2026 22:38:25 GMT  
		Size: 25.6 MB (25621715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee3a0e7d77f0c84203cab438fcf345647c8121bbd80506a3c692f8608a14c4f4`  
		Last Modified: Mon, 16 Mar 2026 23:25:57 GMT  
		Size: 67.8 MB (67780758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8f100349c860d9e43c43477b657a8bbd2118dadde8cce6ea7b7dd0d464943ead
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7775788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7a43e52bc30aeff029e5ab8171529537f206bb3ca7421688784b025cd6915b8`

```dockerfile
```

-	Layers:
	-	`sha256:216d2bb16d3264697ab5c799ab4baa77adf62dfe6ba34315084fd8ade48707e8`  
		Last Modified: Mon, 16 Mar 2026 23:25:56 GMT  
		Size: 7.8 MB (7768211 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81298b5cf03750a07deb482d2f2fe3937413ea3964825274332f3e3fe3c3f50a`  
		Last Modified: Mon, 16 Mar 2026 23:25:55 GMT  
		Size: 7.6 KB (7577 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:f1105d568d4f508f1f434c4a637d156ea423d75c3cf1249b9011847deaae1ff8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.1 MB (137140874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b79c83b4750b69074067c33157adf70dad0f0308b9873d44f69501a8d63b1c8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 23:16:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 17 Mar 2026 01:08:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:8524aea9c07f7c3a1779bfcb961bdcea323ac7abd571c794a134ffeb31a825be`  
		Last Modified: Mon, 16 Mar 2026 21:52:54 GMT  
		Size: 47.5 MB (47460612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4a10acd8de7c2ea5feeb4bbe7b5147fdee10ce64d8ad5f6db26957ab6ab82a0`  
		Last Modified: Mon, 16 Mar 2026 23:17:07 GMT  
		Size: 24.4 MB (24364203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:043762e26fc507e51d741404184de0ffa48c048233f8091ab9a9f0a36a848703`  
		Last Modified: Tue, 17 Mar 2026 01:08:51 GMT  
		Size: 65.3 MB (65316059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:53524971a04ce4896c2708c345f7e1d7b13192825fd86a12c49809d27a5a6e41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7776898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fa89be7c1e7134daf99f835692636833229c4d0a78b77eb418f3cada1540cc5`

```dockerfile
```

-	Layers:
	-	`sha256:dc2b643e9e92425cb38c93b1f5c619275f1ea8f726857e8d098f32e7af045f9f`  
		Last Modified: Tue, 17 Mar 2026 01:08:50 GMT  
		Size: 7.8 MB (7769249 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fbc21b4a22f664b564d3615b461a6c307109b8e4b50b63ebda4120bfbc7325f9`  
		Last Modified: Tue, 17 Mar 2026 01:08:49 GMT  
		Size: 7.6 KB (7649 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:813f86de3244193339097384713be71b807f2b8b25cfc73fbd21aaef23683098
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.1 MB (132072332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d9dde28078454df3240600507577a47966fa9950cb7a1dbefaab5e948ea3e8f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 20:04:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 21:34:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e7e4c87ce6959403c140ef3f01bab08f94d7dd517c0acf6ae810804957e70b9d`  
		Last Modified: Tue, 24 Feb 2026 18:42:48 GMT  
		Size: 45.7 MB (45725086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77120a84626d4a7f2d6bdca75bb942d16ac419ff1bc25fc6e9d95035fe35f65e`  
		Last Modified: Tue, 24 Feb 2026 20:04:48 GMT  
		Size: 23.6 MB (23633662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c27016c2923c40df4d7f8b1909d8aac2050fedaaac6d29c1a4942dcab0ae038b`  
		Last Modified: Tue, 24 Feb 2026 21:35:13 GMT  
		Size: 62.7 MB (62713584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8694f6ea48a3a14bf630c8f8c222854ce2837043112f09cda10c84bb05d5615d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7776291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b5896fa3c918c76860caba45c8a86af9aae08fbfcffc343658a3130423f2d81`

```dockerfile
```

-	Layers:
	-	`sha256:1a9014e315d1d45295f3a64f82465ca48f6d514a944478b9c445ee2e09241750`  
		Last Modified: Tue, 24 Feb 2026 21:35:12 GMT  
		Size: 7.8 MB (7768644 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25f61f228e2a2bf29b1e2bc072586dc83a1799b057467ac18529473418bad788`  
		Last Modified: Tue, 24 Feb 2026 21:35:11 GMT  
		Size: 7.6 KB (7647 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:aa5d3b513466c24c78df06a736821ec25a5420925f55e08dc583fe8c237f495e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.3 MB (142273249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe0cc0e2bb642e883b44319887dcb1a0903cf817f93a76c56f570c0b0d08e059`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:40:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Mon, 16 Mar 2026 23:30:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:deab8db42772fcfeb45003461fe0eb7bf63bdb29199a4fb76242b9493437c28b`  
		Last Modified: Mon, 16 Mar 2026 21:53:03 GMT  
		Size: 49.7 MB (49664953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6778b62bd97b31237948877e89abc29ad2b2c003f3b965027457c8c90d4f44e0`  
		Last Modified: Mon, 16 Mar 2026 22:40:45 GMT  
		Size: 25.0 MB (25023728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d16813bdedcf0a1acbd78336c5bed6fbfaee2674574408140ba7e896cd49cb95`  
		Last Modified: Mon, 16 Mar 2026 23:31:00 GMT  
		Size: 67.6 MB (67584568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:cacc4315e9ede49677902ea5112bb65cbdc40246d7e0d5e4c701ca9b455485f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7783555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f9a4aed8143c4c4058c3f9c6e92e4c8a1767dd93b43f75325cb9158013a6b88`

```dockerfile
```

-	Layers:
	-	`sha256:6fc033ca8e2bf15c99648317b8554fe2d73cc951e7caac2f87129cd8dee10cf3`  
		Last Modified: Mon, 16 Mar 2026 23:30:58 GMT  
		Size: 7.8 MB (7775886 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10ec307835ba5ef67efb7a12422d99d916cfb90918a3920d7e752b6a05c1e182`  
		Last Modified: Mon, 16 Mar 2026 23:30:58 GMT  
		Size: 7.7 KB (7669 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:d138ad8b4b3ff8b1b75c8a069e79031c3f6020e9f32badb8da6296005daef5cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.4 MB (147397647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee5e1917ef7d208dab1bcf0f8be86e0bf376d0c1b023156b54c32dd5b512e126`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:44:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Mon, 16 Mar 2026 23:42:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:a59dab062b6e61bf7c8c44e3e14585d36526de4560825ba7d4c8196503c6eb87`  
		Last Modified: Mon, 16 Mar 2026 21:53:40 GMT  
		Size: 50.8 MB (50818792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:027db2aaf35fd2a2c9adf573b12a548dde1e9e6733b0a9d987c465038a81dcb2`  
		Last Modified: Mon, 16 Mar 2026 22:44:31 GMT  
		Size: 26.8 MB (26783539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd35fd6ac345d92e539dc7dc49dc31742923ebf394762120d349ae52e655e6ff`  
		Last Modified: Mon, 16 Mar 2026 23:42:21 GMT  
		Size: 69.8 MB (69795316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:fdf4fef02040e0be6707273b6ad7a68301962c7f54bcea4e0249619c98a88746
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7771895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ae613962dd03a5fcfd176d95fa8dfed2786ea28e17fe8cfc831dfd5804c0ca7`

```dockerfile
```

-	Layers:
	-	`sha256:1aa2d22eddae191876d89fe3010f10279a91c83c4d539b195422fe1642ba59ed`  
		Last Modified: Mon, 16 Mar 2026 23:42:20 GMT  
		Size: 7.8 MB (7764345 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3652cd3b2ec6395daa9a5410c5a65e5f8cd25de50795c1fd4525324b25f65299`  
		Last Modified: Mon, 16 Mar 2026 23:42:19 GMT  
		Size: 7.5 KB (7550 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:5c46fb39891cc25749b8ce456a659ac36b3d16043188db369ce60f4ce73a26c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.1 MB (153138761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:791ef6cc3ffb872227c8014aebcca6d5ab1ea3751805b7deda2980278f33253a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 21:23:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 25 Feb 2026 02:58:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:468eb7cd0e9ceb9e5b1c4c9daadd36c2fd1f1ee82c667dc1a7d70fa95600a20f`  
		Last Modified: Tue, 24 Feb 2026 18:45:11 GMT  
		Size: 53.1 MB (53112261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b88c878e5079331d2b0e1bf13313604e6e446232728ee7b159499795ff9def2`  
		Last Modified: Tue, 24 Feb 2026 21:23:39 GMT  
		Size: 27.0 MB (27004375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8078b8ed13f55a8d2e3bc098e87fe680e2a4289c11315d3e460db7bcd51cc93f`  
		Last Modified: Wed, 25 Feb 2026 02:59:03 GMT  
		Size: 73.0 MB (73022125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8d9c25312ca3ed45ed92c060683c69cf3e1c4d8ab7630fa7f1cf9b71309706d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7782877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c4debd16e8b28830ece4e96dbaf091844dace361447d90d3f7ec0d598b0e2e4`

```dockerfile
```

-	Layers:
	-	`sha256:0c369ba15e705bf80af245fc99671305cf0da65c3b6276aaa5d8bbcf48886499`  
		Last Modified: Wed, 25 Feb 2026 02:59:01 GMT  
		Size: 7.8 MB (7775262 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e112c00bb236ea8d5e2c9db37b6d10e66c06c608161d780e63cdce518fc68b62`  
		Last Modified: Wed, 25 Feb 2026 02:59:00 GMT  
		Size: 7.6 KB (7615 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:0b90891e67a0ae5c9741a27d9cb38d496c0150dee9509ae48cbe210c952644f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.4 MB (139391128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0368adf4a211d51ccbfde501ba4790c597ee8201f9994fcbb803473f44f08407`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1771804800'
# Thu, 26 Feb 2026 21:43:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Sat, 28 Feb 2026 19:58:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:3be247472b67578a1d05739722d8adeca41098796e5d6210800176db58046fa7`  
		Last Modified: Tue, 24 Feb 2026 18:57:42 GMT  
		Size: 47.8 MB (47776936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:115c3a1cec8ab5f3346656c92bb6a04391222dacf945336ca2f360cb9afa1d32`  
		Last Modified: Thu, 26 Feb 2026 21:45:21 GMT  
		Size: 25.0 MB (24951819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be1aad3c88d849328eee587bd71226c07edf0e2f5081fc7ec8dc66c3ee7e1d0c`  
		Last Modified: Sat, 28 Feb 2026 20:02:17 GMT  
		Size: 66.7 MB (66662373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f13107c4da5dfb26999e015bc0a6ba56a7d7277ab422c18e50a0196ab4ba1b3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7765590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26c7ce93bfeda397cf9ab8bd8631b2e118c051386d2d1675a7442bb17f206ead`

```dockerfile
```

-	Layers:
	-	`sha256:6aa36d0aff359d76287eb9604b6f49ac7a30cd44b0808d54b904bbedf19189f9`  
		Last Modified: Sat, 28 Feb 2026 20:02:07 GMT  
		Size: 7.8 MB (7757975 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2cbbbe97afd462b6ad86611ab1f142d104f9ea9fffad69ed6bb83823de9e3511`  
		Last Modified: Sat, 28 Feb 2026 20:02:05 GMT  
		Size: 7.6 KB (7615 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:c3be472e295245f9ca701442a89d716ddee53f6a6276692f1f419992ebdea2f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.8 MB (144780131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9a99621fba2d7d3b2e4585d90ed1668fb34d234736c77c6d5bcc62dd3794ce2`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 20:59:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 23:53:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:aba9aa950add2749194487d5c63a3069af6daf9dfe54d80cfbe32bfa7a5faa07`  
		Last Modified: Tue, 24 Feb 2026 18:43:53 GMT  
		Size: 49.4 MB (49354534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41b9712b896509afe6ce616cc91aa36b272afd379950384122674a69ff7d6929`  
		Last Modified: Tue, 24 Feb 2026 20:59:42 GMT  
		Size: 26.8 MB (26801071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d62d9ba5f66f052b2790c9aa6ddd7ff161b24db86972e603be616bc922281de`  
		Last Modified: Tue, 24 Feb 2026 23:54:27 GMT  
		Size: 68.6 MB (68624526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b6ae7a023481b7b8f0858052efc2b15756e0c233fb673f3e387d05b930e8ea68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7776627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e496a8b656d1c848f708a56f33226ced3e8cf77e8eed44df33b7a10c63e1c5ea`

```dockerfile
```

-	Layers:
	-	`sha256:ffbbb43fa35e1c94095ddaf6c32e70825f3f510b9b04e4aa828b5bf8d8748719`  
		Last Modified: Tue, 24 Feb 2026 23:54:25 GMT  
		Size: 7.8 MB (7769050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5db77ea50ebcb2b38fb725d013062a26239ac43d36a941b3bf12f030197a96b`  
		Last Modified: Tue, 24 Feb 2026 23:54:25 GMT  
		Size: 7.6 KB (7577 bytes)  
		MIME: application/vnd.in-toto+json
