## `buildpack-deps:sid-scm`

```console
$ docker pull buildpack-deps@sha256:a756428d7d041f595ba7a0bb26935cd1ed5d2270c7bb48eb794dd196ba3737ab
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 18
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
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:sid-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:8f9c7e26a9c0a302c1c9f3b709af960a07189c442972fb46a1561f1ee2a3635a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.9 MB (141909694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78ab4df7a95b4f195c254c825bfaed46a226821e4806f8de7569afd3739cc756`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1736726400'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:76be34fccf5c64699db16068e9e561c466873ad6fc8da852c8c21801ed35861d`  
		Last Modified: Tue, 14 Jan 2025 01:33:25 GMT  
		Size: 48.4 MB (48375138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81659ab3e6cea3ecbc9d772f851c94ca5f88bde45b2b1d558924da5b4ef5f256`  
		Last Modified: Tue, 14 Jan 2025 02:33:23 GMT  
		Size: 26.0 MB (26032098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a3ae95ad3a1621d0b6af5d5c8679891f7f4cbcca866d15b1c931112693f34f4`  
		Last Modified: Tue, 14 Jan 2025 03:18:18 GMT  
		Size: 67.5 MB (67502458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5d21afe580f9c237bd1224fbf30e028a23c006601a17662236d386c163bbb417
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7635368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3ebc2d6a9a48cb52a7f8e4ef1f2d52ece1e66ff37d05a49fec4c22d57dc474b`

```dockerfile
```

-	Layers:
	-	`sha256:80d7a14329ffa8bc6333234cf40db0267daf7dcfad806978ba7172462d07fb8d`  
		Last Modified: Tue, 14 Jan 2025 03:18:16 GMT  
		Size: 7.6 MB (7628071 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0e6ad81dfbbe87ab38d322187f63831db496a70720a41656c02afe9eab96917`  
		Last Modified: Tue, 14 Jan 2025 03:18:16 GMT  
		Size: 7.3 KB (7297 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:39bbd7e63e66c178e317cef3b2a6e4ea13c602234fc037a32a4576ecb5d0a005
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.3 MB (136323300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8545e2b3d7da23dd94606cca7ec31c8c7462bec8544863f03a2bcb44e96e945f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'armel' out/ 'sid' '@1736726400'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:9d52a976a3fd7f28c8f846fa169d38eb4f52aab56f9ee1cb5fbdf7c3d31fa88d`  
		Last Modified: Tue, 14 Jan 2025 01:33:50 GMT  
		Size: 46.5 MB (46532542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5f95931378232e134e2433bb5ceaf5ca525339c23b43efde26fa179c793eec5`  
		Last Modified: Tue, 14 Jan 2025 06:09:14 GMT  
		Size: 24.7 MB (24730945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f7964c97d01715538ed3e44479e82eb334202df2c205477a9386994f1307ee2`  
		Last Modified: Tue, 14 Jan 2025 09:33:19 GMT  
		Size: 65.1 MB (65059813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:76f097568823ece943ea86724fd218b94a23666445a09b48269c085baaa392c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7641108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92cc0672880e2f92395180ed5c38bb02444577e61916d8689346b6e324ffc4c2`

```dockerfile
```

-	Layers:
	-	`sha256:02b792d1089f026cfc2cfb1ed65eb9e2786a1c6ae9e3774fdc77e91e6722306f`  
		Last Modified: Tue, 14 Jan 2025 09:33:18 GMT  
		Size: 7.6 MB (7633751 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7caf301f866c055579d761586940320888048a0207ba39c3810aae9f89b56757`  
		Last Modified: Tue, 14 Jan 2025 09:33:17 GMT  
		Size: 7.4 KB (7357 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:eee73af26ed00733360dfc64d7d4e42f53482efb28e71f64ea037d036358ea79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.7 MB (128670300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5120c42a5af4bbfbdd4fc9d74929a06edb0f21e8625d22ca16231b10d863d37`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'armhf' out/ 'sid' '@1734912000'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:fd381bc5446358c906dd1f7ac3878d03bb1e1267963891069c3e6e2c97919218`  
		Last Modified: Tue, 24 Dec 2024 21:35:32 GMT  
		Size: 46.8 MB (46763305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d419ccba1fe0df7cd0c879e1f8261dab91d1fe412b8df835212e60f95b90dbb7`  
		Last Modified: Wed, 25 Dec 2024 03:45:03 GMT  
		Size: 19.6 MB (19608949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:367601bc4f065e38e007f59c54dfa0b3ad1eb3805f4c77d1ffe0c358844eeb5f`  
		Last Modified: Wed, 25 Dec 2024 13:02:51 GMT  
		Size: 62.3 MB (62298046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:3e3ffce5f6e75c6d62335248ac830f81f37e5ec9902e81552c60b038906b77d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7639931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef91ca6162d85641a1db7edcbc2273f1d99456e8b22e8611e0268ceeafa6bd16`

```dockerfile
```

-	Layers:
	-	`sha256:66122bbaa60a08c42b7e78ef0f156af343e42f3f153e787fa2773a865edd97ff`  
		Last Modified: Wed, 25 Dec 2024 13:02:49 GMT  
		Size: 7.6 MB (7632575 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2298d4cbb2eac5a05c766144c3ca706c5e4b5fc5ef9c59f2f5ece3e2f9721246`  
		Last Modified: Wed, 25 Dec 2024 13:02:48 GMT  
		Size: 7.4 KB (7356 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:44c7ae45af3da73e2d51b1b9c5842728745107083c70d34081ebaf17e834dcbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.7 MB (140652595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1340e1963e159f97fab016487d366b374f3f6435f19f15316188646c2e32761b`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1734912000'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5111921f4f194856cc1156a3664c32c64df54cbd5ad15f8c94081cb0e3440253`  
		Last Modified: Tue, 24 Dec 2024 21:35:38 GMT  
		Size: 52.4 MB (52432315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c20d0977c0428e556b738a4854988cc1f65b6192c33c235195555a4b1c8e5d58`  
		Last Modified: Wed, 25 Dec 2024 01:50:20 GMT  
		Size: 21.1 MB (21052154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c053c3d6a126675dc183ace458ad37733e728fe47e857880914a939b478acc30`  
		Last Modified: Wed, 25 Dec 2024 08:13:21 GMT  
		Size: 67.2 MB (67168126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1776e2dc4819df5c6b21711a76f042798ecf466600571e7f8788054e7b76f0bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7649015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57245cfa3b330f641db2bf6b55dd1d75a572ff1cf361bc685276716d090bab09`

```dockerfile
```

-	Layers:
	-	`sha256:dfb2fc27aebe2692bd862d6e7cd63a6252f3028637ce1d68481cd5fec924c256`  
		Last Modified: Wed, 25 Dec 2024 08:13:19 GMT  
		Size: 7.6 MB (7641639 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b96154f5bed0bee9085337acc56c2ec9eced1b611f40f1bf9b8f915d0911856e`  
		Last Modified: Wed, 25 Dec 2024 08:13:18 GMT  
		Size: 7.4 KB (7376 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:6cce49582c3d57bea5fd9af900f9ab9fc7dd1860444150ea90862dac1004936f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.4 MB (146424345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a37eb6df9da7b2b6811dea50f74902c57c5eb0e07bdc682969b94b403b3de728`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1736726400'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:c1e4243a6e921bf817bc744dbf559de39acec531c69436c119d566f9645bf931`  
		Last Modified: Tue, 14 Jan 2025 01:33:25 GMT  
		Size: 49.8 MB (49778367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4499f1145672c6dc66a0a48bab855b0052609dea7a87335a024adaf65cda0b10`  
		Last Modified: Tue, 14 Jan 2025 02:17:21 GMT  
		Size: 27.2 MB (27178007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8346a14ac4c6ebb8fcd6102079a994f8803f83fade3d0db9f898c6c81c8d66e1`  
		Last Modified: Tue, 14 Jan 2025 03:18:13 GMT  
		Size: 69.5 MB (69467971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:60403b96a85651c4c4a99772be8e57c4cc513a984454a42fbdf2add6e991a8ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7630112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f15120b5deb8f7972e7b25409fdd3086ef7f82d9f078c6ce33bcc23a5dcd0f3d`

```dockerfile
```

-	Layers:
	-	`sha256:4ea496d083a631011e978b495c150127a9bf8759f7da4cf94a769280fc8a993a`  
		Last Modified: Tue, 14 Jan 2025 03:18:11 GMT  
		Size: 7.6 MB (7622837 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de5c2d2cdf0d273928b0929255d2b3d2be8aa31acefd7203eb39e7c17302238a`  
		Last Modified: Tue, 14 Jan 2025 03:18:10 GMT  
		Size: 7.3 KB (7275 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:18793d3bf4bf5e25195e4e7de27928138f62bf0bb790532a2bfc90182428a714
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.6 MB (139629522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bb8d2194cbc3c583eaabd739a73c0c7e255ba00b47b5ea0fc1d964876106973`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'mips64el' out/ 'sid' '@1734912000'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:2225e4bf9a501ecd52da3f4301136a4a3ac3273d704acaffdf95ff67153847e7`  
		Last Modified: Tue, 24 Dec 2024 21:33:59 GMT  
		Size: 51.8 MB (51771333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8315cddf1f38d3ec912dd995fc72b7c70105918274b7bd71b5f66a9e8789a52c`  
		Last Modified: Wed, 25 Dec 2024 11:47:53 GMT  
		Size: 21.7 MB (21740832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44bff240cec674232066373df9095fc00a6e03c4199156cd01f197c25fb6340c`  
		Last Modified: Wed, 25 Dec 2024 19:18:25 GMT  
		Size: 66.1 MB (66117357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8d78ee840803aa0c532881eddd9e7a9ca63f637a58e7544fcd6d7a62b2f120ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 KB (7130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d52bd8980b7f832a3915bcd636203274dd25c068aa074efc78e38275a111f98`

```dockerfile
```

-	Layers:
	-	`sha256:ab12b73792d73d13a49f6dc0834b27510c61ed5b5607b2436a20b03a1bbd299e`  
		Last Modified: Wed, 25 Dec 2024 19:18:18 GMT  
		Size: 7.1 KB (7130 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:c9dff46a695bbbd09928df43913acc08b77b33c6e5bbe3c67db3645450f3ec10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.6 MB (152620570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcc5b403b395db45f384452fa3d991abd51cf8f7fcd540f565994f1ccb2e3791`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'sid' '@1736726400'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:fca4ba78a63cac2994d6f3576656e907e3a130a20f935b6a1e2c945c9e7be3af`  
		Last Modified: Tue, 14 Jan 2025 01:38:04 GMT  
		Size: 52.2 MB (52151887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21f2cddc488774629199c39c9010734d4be824e6ca934835a5e2d444a85e0075`  
		Last Modified: Tue, 14 Jan 2025 05:31:14 GMT  
		Size: 27.6 MB (27591847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97154d7b719fe3158c773c51a570d7d8ab1e54dcb04c12ce4e93476ca16bbefc`  
		Last Modified: Tue, 14 Jan 2025 09:43:30 GMT  
		Size: 72.9 MB (72876836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:de4a20ba75e03c0ff75c6080bd0eccad35fae0a9cdd8003b930a1c10359ba01f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7647309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7df2c6e85249573151aa8cd5130afefa5a2b540e14850e3ca08acd68a6e0cd2`

```dockerfile
```

-	Layers:
	-	`sha256:898d5118a17bda22e2ca116218625d18f3e8af744178649f307d32fa82a9375c`  
		Last Modified: Tue, 14 Jan 2025 09:43:28 GMT  
		Size: 7.6 MB (7639980 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d5ea53d9432befce7809da77eac8d34ff51118b643a4b8fa31ef71e00df002d`  
		Last Modified: Tue, 14 Jan 2025 09:43:27 GMT  
		Size: 7.3 KB (7329 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:1c11dc0f6cbccc5b2666d1000b1a8cabfc7e0cd69cf765e6f13551179129bdc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.7 MB (137712618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:050bcd9ec7b82998c38f40a2089324ac25931cc174dd8636cef601e3fb5e5402`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'riscv64' out/ 'sid' '@1734912000'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:34dc7eee421e2547a72cc18fd960cb61e4cc000ae2301ebea5c1db40e2f928c9`  
		Last Modified: Tue, 24 Dec 2024 21:35:00 GMT  
		Size: 50.7 MB (50711803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27b3be9202d049cfd8fab2840745aba862531c266ca24caab8785a1201a2bb14`  
		Last Modified: Tue, 24 Dec 2024 22:26:29 GMT  
		Size: 20.8 MB (20829455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3a9bbab72f01dce27644d4f039f493ac5e6e54ff93d5cddb115f95af7c7ff7d`  
		Last Modified: Tue, 24 Dec 2024 23:21:04 GMT  
		Size: 66.2 MB (66171360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:3045cb2fa1924b6ebe89757d807fcb7e1684649b7dc1197ddcc0b68d6d2237bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7629972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:954774fc0b1411cf87f88c7fddf147a9a67c94c2fbd8a6fb5f40c87de61bc871`

```dockerfile
```

-	Layers:
	-	`sha256:f20d78cb250d0ecf18d1a75ac9fbdbd15ba56aa0cd81ec6ce0c50c55f7c6d087`  
		Last Modified: Tue, 24 Dec 2024 23:20:56 GMT  
		Size: 7.6 MB (7622643 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:865a6e8b3a3ac009d21d4ace920ddce3a7988bccf7b1729f9ae28f1d25db9d8d`  
		Last Modified: Tue, 24 Dec 2024 23:20:54 GMT  
		Size: 7.3 KB (7329 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:546f564ea303b4c00aadb8dbdfd4c1509aa46068687ff6991805a95b19880bdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.2 MB (144164228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56a596ce377c97750b2fc5a7c4bcb6d9b1268b2f41ef87ebf899400d4055e308`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 's390x' out/ 'sid' '@1736726400'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:98a334b3a419c858b25979b9c4fcf97a87431d5b5cddfa6c4c566454b23fcf62`  
		Last Modified: Tue, 14 Jan 2025 01:35:18 GMT  
		Size: 48.4 MB (48434824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d732c90ca5b141c789480c7eea03644a6f254edf6c95ed1e124a245a18b8c3cf`  
		Last Modified: Tue, 14 Jan 2025 05:00:30 GMT  
		Size: 27.2 MB (27196670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c226835589caa484a321d0762131f155a336675c8b326b2fb32917038d1fe871`  
		Last Modified: Tue, 14 Jan 2025 09:11:02 GMT  
		Size: 68.5 MB (68532734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7632eba94e2fe4601b68883b53a69dc82103d32b7130f147bbf933f92d2e8233
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7641199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c498f989de5ed26afbb4e35a4fb25aa01ffe06541f7d70dd224ab8e1ff51fc2f`

```dockerfile
```

-	Layers:
	-	`sha256:b4d23fd11971da7096f1cc74107ace1c6928e542210059f0d84dcf64f93c393c`  
		Last Modified: Tue, 14 Jan 2025 09:11:00 GMT  
		Size: 7.6 MB (7633902 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82ca8a90a650f0fa41d26305dfb96362cc89ad04987107394e370a6cb0d357f6`  
		Last Modified: Tue, 14 Jan 2025 09:11:00 GMT  
		Size: 7.3 KB (7297 bytes)  
		MIME: application/vnd.in-toto+json
