## `buildpack-deps:stable-scm`

```console
$ docker pull buildpack-deps@sha256:461a369b667f0d8885701d744275cbbd2a9e5e11f0f4602c34038bf33b1dee04
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

### `buildpack-deps:stable-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:425dcc54fcb9c69fc0210aae04da29760e8eee9f59b4a916436443e09b029eed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.7 MB (142685807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1b3ba123271df7ab94dcd6c1a5d3c60deea7cdc865f665d5aec3ecef929b6d2`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:10:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 03:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:2ca1bfae7ba8b9e2a56c1c19a2d14036cae96bf868ca154ca88bc078eaf7c376`  
		Last Modified: Tue, 13 Jan 2026 00:42:23 GMT  
		Size: 49.3 MB (49285621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82e18c5e1c15ff34b31f1443e9327b69daaa0c1bd65a23846328fc3738c7f8f1`  
		Last Modified: Tue, 13 Jan 2026 02:11:21 GMT  
		Size: 25.6 MB (25613410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be442a7e0d6f290b909f8da51840566e06ab51bfbea277c70fbda26c44c8259d`  
		Last Modified: Tue, 13 Jan 2026 03:54:48 GMT  
		Size: 67.8 MB (67786776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f1c9e1a1dbf54fdb14f7d7e11e2bc75ee2fc8adc471da104e2d4a9b96f578f5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7775713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50154ca81df215815014a8068e8d10f8ce29f94781fb03224e19f3f5695eb60c`

```dockerfile
```

-	Layers:
	-	`sha256:3a23003355b7ebcd78be4c677d97a80748284e807a983544ec68b8c92bb29901`  
		Last Modified: Tue, 13 Jan 2026 06:28:41 GMT  
		Size: 7.8 MB (7768137 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14b09c3f3fe0ba0c43e7b6fbf90e60f0a05e6c5e244cc4f18fb2c0c12be988ad`  
		Last Modified: Tue, 13 Jan 2026 06:28:42 GMT  
		Size: 7.6 KB (7576 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:4f94fb84abbcb7492d83a1bf75a55dc3f1ad91045403279a2f521b485ff8674c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.1 MB (137120764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed6d7031a6a1c941930b9acf565d9cdddff9bac8b0ab96480f0e1203a8107956`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:29:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 04:08:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:16d4329ceaa8dc305221873389c356e4c5bf3cdb5b245a79ff75a1b1806f3778`  
		Last Modified: Tue, 13 Jan 2026 00:42:07 GMT  
		Size: 47.4 MB (47448362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad4ac90147d1f1c4bc0ab2c1c245fb4105c9ad56d7e5e75726e8ec474c79f05f`  
		Last Modified: Tue, 13 Jan 2026 02:30:05 GMT  
		Size: 24.4 MB (24353866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0b0fe9087175027e9a76a41e2c394603c9345a19f6296b58e7044e930aafb08`  
		Last Modified: Tue, 13 Jan 2026 04:08:45 GMT  
		Size: 65.3 MB (65318536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a1f0042994ebfb4b7e41112267f73133bc53bdef6f48966443b56f3d59853c19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7776824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81ecde136f92fd4dfbfa668080745ae46cdf2f7da561b5bf380eb41ac738a6cc`

```dockerfile
```

-	Layers:
	-	`sha256:f2f3e5f5271e89d3c02cadb19bdcf21601238fdacb8d74b67b365622925dcab2`  
		Last Modified: Tue, 13 Jan 2026 04:08:27 GMT  
		Size: 7.8 MB (7769175 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26fec3f9028f7ae6c338b5e7e41ffac7e169ed25207e80078a4ba481bb764cae`  
		Last Modified: Tue, 13 Jan 2026 05:24:18 GMT  
		Size: 7.6 KB (7649 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:40fba909d3b863736126156942f75dc81e45ea61cb25216c7eb34dd85bfa6184
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.1 MB (132057869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1e1c09e0d485be2e468d9684df5c008a80bc46e2c56405b40f475da8a3d64ee`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:58:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 04:25:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:0f4296a8ece8abd5a409e5fbdb0cf93258815e4fec9dc768c39a63faf3c16052`  
		Last Modified: Tue, 13 Jan 2026 00:42:25 GMT  
		Size: 45.7 MB (45717820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a8e700e2f18987ab9f97abcd0497d5dfc1706a8c057e685438ce3b71d8067c0`  
		Last Modified: Tue, 13 Jan 2026 02:59:04 GMT  
		Size: 23.6 MB (23626665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bf6f5dfbcc297b2e354e856be84c591ec9f96e89fd8401a4d485596c43b8ed8`  
		Last Modified: Tue, 13 Jan 2026 04:26:15 GMT  
		Size: 62.7 MB (62713384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c1b538054f3ac5e83c03d6cc63616799d27a39d289f6cc3478bacf3b49ec2c44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7776293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f5f2cb95dce8c71046b397ce0e34d9917a85860edde27498db7bf1991ee8178`

```dockerfile
```

-	Layers:
	-	`sha256:79826f10bbce0ed948d9202da82edb7fa8df4677c56e0c3b38ecace5216015e1`  
		Last Modified: Tue, 13 Jan 2026 04:25:56 GMT  
		Size: 7.8 MB (7768644 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db456bca7b291f1bfc89fec724f3f9a3461e4b59ab6ae3ef888a315c7283997b`  
		Last Modified: Tue, 13 Jan 2026 05:24:26 GMT  
		Size: 7.6 KB (7649 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:c77ec5254827c989337bbd0f5110066787cdd2dfad00cbb9c3f91cdf341cb514
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.3 MB (142262232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6463091c9a0147cb03bded1be62a1da53d96f13a23c2e23b12928608c6a70546`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:15:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 03:58:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5582010cab7f00a8f96e076b02666116eaa7e4af9a74eb44f2946a593b50294f`  
		Last Modified: Tue, 13 Jan 2026 00:42:51 GMT  
		Size: 49.6 MB (49648083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:599d5b6b6766fd729045e2e7d0396d1f61fe41c612d4aef6bb3bf5ea7db12ae2`  
		Last Modified: Tue, 13 Jan 2026 02:15:57 GMT  
		Size: 25.0 MB (25022636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9b629762372f548de0ebccf01b8e80ae5ce251dfd36aef6fc3ae8d963493edf`  
		Last Modified: Tue, 13 Jan 2026 03:58:49 GMT  
		Size: 67.6 MB (67591513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b9592677a391ac38ed267f9d56c8f0f574464a6fe5223c1727b2cbbbff78d301
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7783481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b74975f0d4475cce23046c75a0445f56877bf4a074fecfd12e0ff8df0b608a74`

```dockerfile
```

-	Layers:
	-	`sha256:bf4b419de65d0f2ee1addb720ee7d33f1d0bdb35bb50b3823472088cee765d4e`  
		Last Modified: Tue, 13 Jan 2026 03:58:38 GMT  
		Size: 7.8 MB (7775812 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bcf7f6c47b60450d456e1e56a9d049d1a143b574e4c27e32fb691799cc39e18c`  
		Last Modified: Tue, 13 Jan 2026 06:28:42 GMT  
		Size: 7.7 KB (7669 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:eb83bd297d5d536ee27b0deacfaa8f4334fc07df616cf7dbe9f8c4ca83191897
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.4 MB (147380358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:076ac1fc7e734a671d65a5519f0216a2d1a9567ac3230b9a6014315a62b8d490`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:03:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 03:04:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:1f0b243ad587d8f60f107748ba9fe54e338921c7b90e6a5d26e1d50d32f7481b`  
		Last Modified: Tue, 13 Jan 2026 00:43:36 GMT  
		Size: 50.8 MB (50798876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef949cdbd6ae265d5239bd005e65c3d578de54ebe10474ccd2feb9708b6e1843`  
		Last Modified: Tue, 13 Jan 2026 02:03:47 GMT  
		Size: 26.8 MB (26778274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01ad78e3f6c783e58b723e0e1c78c005c2b612d1657c3a40830f5d7d97f9d85c`  
		Last Modified: Tue, 13 Jan 2026 03:04:46 GMT  
		Size: 69.8 MB (69803208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:6fe88ccf372b9243fafc249c488f9a0329345ef6bcf306b5daeb3b9e391987fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7771821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99e736995ab9c4d9c7a0ec0da11ecc0852e472df9fdc7b3c487ebe8a12918e68`

```dockerfile
```

-	Layers:
	-	`sha256:90ea1fde2b6d32a80f5998c27b93d058f06296385ec6722ac90891418cd1c16d`  
		Last Modified: Tue, 13 Jan 2026 03:04:44 GMT  
		Size: 7.8 MB (7764271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db59c0e625f56778af94e83e95d8fd086923d8c2f9dd44368776b9e51de6edfd`  
		Last Modified: Tue, 13 Jan 2026 03:04:44 GMT  
		Size: 7.5 KB (7550 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:e9ef3588e582d716036b46b3cea0a0ef3087d286c7b815803b0decbb02d08f9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.1 MB (153142622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:724533d97ca88754dd019fe93718b23914a53eb407cddf2cbfd6c8e4e0f3297a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 09:15:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 15:18:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:6ff412c1efdf82a2030de7bb593b97f09e02e2b337f615eb1c3faedeef765d44`  
		Last Modified: Tue, 13 Jan 2026 08:45:48 GMT  
		Size: 53.1 MB (53106962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f21554c0ffe7aa9121703873815aca94dbbdf6352a46266dc923fc9e36d0d58a`  
		Last Modified: Tue, 13 Jan 2026 09:18:09 GMT  
		Size: 27.0 MB (26998052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb58d20828d54df35a08218c574236606c9e3ab14d0f2ddf036e12abcf8c85d6`  
		Last Modified: Tue, 13 Jan 2026 15:19:44 GMT  
		Size: 73.0 MB (73037608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:79133d6ea3b15bd38b4ddf35b938acebe8833849debdc608b764df6811a75141
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7782877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44e29c3dc2fecd5f53fe5ecaec87a106a215037149db7ed8b9034c2d62dd0fdf`

```dockerfile
```

-	Layers:
	-	`sha256:680bd22d091af24ea8e1f849f1fba33a962ac2b424501d61c1bdc3fc28f47180`  
		Last Modified: Tue, 13 Jan 2026 17:20:59 GMT  
		Size: 7.8 MB (7775262 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a21380fddd3f94a0c3c6b267d13cf32f3b935972d834a641f6dd56c9e8b264fc`  
		Last Modified: Tue, 13 Jan 2026 17:21:00 GMT  
		Size: 7.6 KB (7615 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:53e1918b4deac0b4598e1fdfbc88769a8f0924d91eac8915b7b22b3a57c21203
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.4 MB (139384293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecb34c3f8fb6ebda9e1cb3c71c7e8eae5dec197cde055e4c9c0f454c5afc829a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1768176000'
# Fri, 16 Jan 2026 06:47:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Sun, 18 Jan 2026 22:58:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:559020494fc8527e77b291bee49cdac1db6bca66f8926cda195e0e4ebe7d2d3d`  
		Last Modified: Tue, 13 Jan 2026 01:06:23 GMT  
		Size: 47.8 MB (47770843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f7f36a5fa281a3384abd9a90a26442f28edb507f1b9c537a07e1f5aaeb769a1`  
		Last Modified: Fri, 16 Jan 2026 06:49:13 GMT  
		Size: 25.0 MB (24952736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c11f745939b2d13a20bc5767dafb02ca8b86a288cc70e3062fa70de76ce5b598`  
		Last Modified: Sun, 18 Jan 2026 23:01:52 GMT  
		Size: 66.7 MB (66660714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2845c2c3ccb02dbec66ac5d9fbade10de664b74c2d072f324623f748e495c74d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7765590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6255002d2707a250f316d37c2b44f689b25717cf0696a16821b21f73cc8c084`

```dockerfile
```

-	Layers:
	-	`sha256:9b842e6b5610b0727d6bdf7f25e7ca60c625e25d3fcd9ed1cd3561529bd9326f`  
		Last Modified: Sun, 18 Jan 2026 23:20:53 GMT  
		Size: 7.8 MB (7757975 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ae934fa04e1af77b7b48d655ea57c1540bde0086341b5a6b4b64c284991b19f`  
		Last Modified: Sun, 18 Jan 2026 23:01:42 GMT  
		Size: 7.6 KB (7615 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:53daade8f1cbc4a6574a02e8981d4c7bdb34ac737f1433ca924f2db975466fe1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.8 MB (144774274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc185d85169425b1a7ca1e53446bb851357271ca572ba53d721266d2f752b2cd`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:11:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 03:15:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:9de0288d81a9602539c9f3015fc521191e25eebfe6442c22cb974ea3a486f3a8`  
		Last Modified: Tue, 13 Jan 2026 00:41:46 GMT  
		Size: 49.3 MB (49348704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:629a9411869af8d59bfb1073c3573138af1f96d808896b3f2fd14cf62fca6dba`  
		Last Modified: Tue, 13 Jan 2026 02:11:26 GMT  
		Size: 26.8 MB (26792892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff54b33211ee85001fc045dcc86b026876894b17d1d6f873a415014f68cb0c9f`  
		Last Modified: Tue, 13 Jan 2026 03:16:21 GMT  
		Size: 68.6 MB (68632678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1d742c91dd1041b258636e4ca88422077d42623bcf93e1be017af95baa4e328f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7776627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0605af8a5f07e4dc60a175fd1cf32ca825e2c06789f4f8d303ec0b1a3ade05e6`

```dockerfile
```

-	Layers:
	-	`sha256:7e7c760003a53c37739e20965a2a49d92e4514abfec6a3cd138ae6eb83f8a61a`  
		Last Modified: Tue, 13 Jan 2026 03:16:05 GMT  
		Size: 7.8 MB (7769050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:407257e03197cd4f72111790fd83f3c5f34e4b4d5901b1c47e806a3448e43790`  
		Last Modified: Tue, 13 Jan 2026 05:25:06 GMT  
		Size: 7.6 KB (7577 bytes)  
		MIME: application/vnd.in-toto+json
