## `buildpack-deps:unstable-scm`

```console
$ docker pull buildpack-deps@sha256:551ab6b09a122f542163553f4a704bc9287e43b62094cbe968442222f100e856
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

### `buildpack-deps:unstable-scm` - linux; amd64

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

### `buildpack-deps:unstable-scm` - unknown; unknown

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

### `buildpack-deps:unstable-scm` - linux; arm variant v5

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

### `buildpack-deps:unstable-scm` - unknown; unknown

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

### `buildpack-deps:unstable-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:963821eab438cca62a72541d9517491b6b758bd7a71fb9dc131f2537230f081a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.0 MB (131012626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ccae8cf93158ee853f476a9109dd2af22f33d5e8f8bea290aa1078ac2400a30`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'armhf' out/ 'sid' '@1736726400'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:a0e0ff4d5bcbd6e2c25332ca46ec757661e665f67ef593a6f9b269659d2aeab0`  
		Last Modified: Tue, 14 Jan 2025 01:36:57 GMT  
		Size: 44.7 MB (44668351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d6de100729dc42fca6e1da779a5cabf824cb59902a2e776e84fe6b7124d28a0`  
		Last Modified: Tue, 14 Jan 2025 08:59:23 GMT  
		Size: 23.9 MB (23876812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c133cb44b43ce8e0628b481f6d32820f19b92bbcee07e7706966c203b607284a`  
		Last Modified: Tue, 14 Jan 2025 16:17:30 GMT  
		Size: 62.5 MB (62467463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c724c35f72f32fd7ce9fc73e81354004d117302c8a645746010e67cfad7bf7c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7634670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d157cfbee009a2005ad4f645cb3d386e308cd2dc1924ae726097376d3f653d82`

```dockerfile
```

-	Layers:
	-	`sha256:c32c99ffae3952178d8fa4d0f1ea8146402add0c6df485c7af1ff72bd75d8d32`  
		Last Modified: Tue, 14 Jan 2025 16:17:28 GMT  
		Size: 7.6 MB (7627313 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56badd2735f45c4d8768ab030f31de125093b00e7776267191877090d63463cd`  
		Last Modified: Tue, 14 Jan 2025 16:17:27 GMT  
		Size: 7.4 KB (7357 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:99626c55ddc16b23335b0fc1995673efbb918649fbf4fab6f7784e7c96083405
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.7 MB (141722160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:976b9892d2184abc5a382db5e3174b5e6a17000ec2933cce2be8e2e021845720`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1736726400'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:7cef9546887caee4cb752860ee90de96728f638ede0f77bda226ca44ac3e04db`  
		Last Modified: Tue, 14 Jan 2025 01:37:16 GMT  
		Size: 48.8 MB (48760872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94fc550a04d72fdc48fc4716034190ede3de291a338b2c748b32584534d2c3f1`  
		Last Modified: Tue, 14 Jan 2025 07:00:48 GMT  
		Size: 25.5 MB (25487312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97035a0dde45440d902fa525c75a16c6689c0105aa65885137511ec2d09218fb`  
		Last Modified: Tue, 14 Jan 2025 13:32:31 GMT  
		Size: 67.5 MB (67473976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:77aac8c09632d225ec7ad937466487a18fe44b41321162b63a495deb5d7b09bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7642481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb3664716cbc9827e0d4700eb1a943adee7374c4275ebb1f4c2ad10bfc88c09c`

```dockerfile
```

-	Layers:
	-	`sha256:37625ca4e83e7ecc5ab4a9bb6accc1b603a4513f134d31e5077dd26734898763`  
		Last Modified: Tue, 14 Jan 2025 13:32:29 GMT  
		Size: 7.6 MB (7635104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a47b95af4fcf2431e73ac39d0424c1dde7f7ee5b3a2c920721d4584e9afa5e36`  
		Last Modified: Tue, 14 Jan 2025 13:32:28 GMT  
		Size: 7.4 KB (7377 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-scm` - linux; 386

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

### `buildpack-deps:unstable-scm` - unknown; unknown

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

### `buildpack-deps:unstable-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:f77dbb626432088faf0677622876c0ec92e981900c02ed8d56d1e3f06b5437c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.7 MB (140705745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d330c8a9b3041cb1c438700b5ff456851b2af6ac9b9106c526d10f0cba85723c`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'mips64el' out/ 'sid' '@1736726400'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:1ad11d2c3d2c0479cee56b824f2514b710c0c76d88c22da7ef5ec7f2ccc527d0`  
		Last Modified: Tue, 14 Jan 2025 01:35:17 GMT  
		Size: 48.5 MB (48545883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c7625cd98aa6d5c80fb0d1f627561581568ea6f268919dc1e831bfca9d1e853`  
		Last Modified: Tue, 14 Jan 2025 18:12:26 GMT  
		Size: 26.0 MB (26040345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88d41982939111491c6252a19353da998fa5ef416acfaed05792f55a462ab11e`  
		Last Modified: Wed, 15 Jan 2025 02:04:08 GMT  
		Size: 66.1 MB (66119517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1dfe48479ceb60993458a81c57144d64932ad4edaa1a619c135cfbfc993bbfa4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 KB (7129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4940cfb76b69b556878c579c3491c1f9a4221722c4afce5e509358647ed38182`

```dockerfile
```

-	Layers:
	-	`sha256:1b8d88f19bb395c1257b1d2d02adadd9a2f3d61436407f852f9e9f4dbf20d914`  
		Last Modified: Wed, 15 Jan 2025 02:04:01 GMT  
		Size: 7.1 KB (7129 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-scm` - linux; ppc64le

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

### `buildpack-deps:unstable-scm` - unknown; unknown

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

### `buildpack-deps:unstable-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:e6b547fc47ef439ba231cd0aeb3e2acffd083a876ae3da98384a59c2d4bd757e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.9 MB (138871056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c3ff1fee3a430b456bd194b561727110a45e38bbaa54c61efcfdf08a930c28c`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'riscv64' out/ 'sid' '@1736726400'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:8fd872592cd59f544fed4df0eb73d6e2bcb134c250417be481a247576f572a63`  
		Last Modified: Tue, 14 Jan 2025 01:36:16 GMT  
		Size: 46.9 MB (46920939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40f27f58bcdcb67681cc1a3f5317eea016beaa7c816e5c8b7d9d6410796b02d1`  
		Last Modified: Tue, 14 Jan 2025 14:29:46 GMT  
		Size: 25.4 MB (25411216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b4f15fff232ce9f2af98fb869b50c765042c46743ad5b2b938ac709c0c4a741`  
		Last Modified: Tue, 14 Jan 2025 20:39:05 GMT  
		Size: 66.5 MB (66538901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:4313c9080e5122fe81799cef913b7457a6f5fb6253346a033c3f97c003b7ce59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7621862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8b65f55e1c66af8f2f7cba45816c18a488cd4660690b44e9cf9506dff174f92`

```dockerfile
```

-	Layers:
	-	`sha256:2f01cb96715e7f1af045727852ae614a0bcb02f700fecd797ddd3fef2dc67b35`  
		Last Modified: Tue, 14 Jan 2025 20:38:57 GMT  
		Size: 7.6 MB (7614533 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b63d206da90dfd6e97ebb040888a5b29f78dda9aba1a5a05fe7434e1f2530ac`  
		Last Modified: Tue, 14 Jan 2025 20:38:56 GMT  
		Size: 7.3 KB (7329 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-scm` - linux; s390x

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

### `buildpack-deps:unstable-scm` - unknown; unknown

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
