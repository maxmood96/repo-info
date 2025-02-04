## `buildpack-deps:sid-scm`

```console
$ docker pull buildpack-deps@sha256:a864d05c1d128e8ca3f96214f7b1d8b54253e3c8b19537900d59a435893ff79b
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
$ docker pull buildpack-deps@sha256:49050b174b7c280c7397a668862e7b07e65d41029fffd9a4289f0ba89f51830e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.0 MB (141983228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2de9e7ceb22c36a43a1fe888d57519e4006cca29fa80a1a9bbd024ae5aa7a57f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1738540800'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:9a66d07ec06276723a9d844f79110db2c04e99b6e7ca9f2467ee7789a25614bc`  
		Last Modified: Tue, 04 Feb 2025 01:36:30 GMT  
		Size: 48.5 MB (48478504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37249eb6f9b3505b2330ba5132b480155ccfe125c06c5def806fca9a9daeec74`  
		Last Modified: Tue, 04 Feb 2025 04:37:52 GMT  
		Size: 26.0 MB (26036380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48e4fa6b03ff4cb7e858ff5a14c844d64841c23889c0d907ba3b0dff91e9902c`  
		Last Modified: Tue, 04 Feb 2025 05:19:10 GMT  
		Size: 67.5 MB (67468344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:36ce389bcf9326720dbf7ecbf7a2a66e2953fbc3a32824120544ffc68c1a1f76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7666507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7fcf6cb261b3b8b8689b31075e7690f118d26a8b64a4ab267a858e5255a765c`

```dockerfile
```

-	Layers:
	-	`sha256:18e8f73b18c7f8320da0a5c85645371cd9b3056ba3baf871fe86c4167ab951f9`  
		Last Modified: Tue, 04 Feb 2025 05:19:10 GMT  
		Size: 7.7 MB (7659210 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20734c0cd4a50db3c1fe6185badc40dcd0819cdd78875967da043713cbe216fc`  
		Last Modified: Tue, 04 Feb 2025 05:19:09 GMT  
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

### `buildpack-deps:sid-scm` - unknown; unknown

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

### `buildpack-deps:sid-scm` - linux; arm64 variant v8

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

### `buildpack-deps:sid-scm` - unknown; unknown

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

### `buildpack-deps:sid-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:6678694174d4f8eeeffa050f0fc716c554ad11fc7f6a029f8ebb4797c6fbe517
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.5 MB (146471670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80da4043c23e99d797e3ac30aa56c3125b9748c66f5e6d89758cdbf9d9828488`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1738540800'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:51741382468681fc53992e03a5e8ce7f591198e39599d81f3b698e3652a63db4`  
		Last Modified: Tue, 04 Feb 2025 01:36:41 GMT  
		Size: 49.9 MB (49883916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a4227754a1dcb648ed5c4c8f40f8d60f655bb96ef669b5da48ad50132dc9621`  
		Last Modified: Tue, 04 Feb 2025 04:23:42 GMT  
		Size: 27.2 MB (27185942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74bb38fe259cd8a9e1ef2a45c45f0372cb16ddaf5c5facf3363ca9cfcede2c4d`  
		Last Modified: Tue, 04 Feb 2025 05:15:50 GMT  
		Size: 69.4 MB (69401812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:179c2eca5debb1d945c5b9eeaf22c0e8db8339553ed7d92bea95b044f525ea1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7661234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f4a4108ec78cddbd0969cb329e129c9a6c49ee083712bc2b3c5c2803e244549`

```dockerfile
```

-	Layers:
	-	`sha256:7ce5bd96b9500a5bf64ca90b6006bd7805c45b65a27e6928eac71f99c067ff43`  
		Last Modified: Tue, 04 Feb 2025 05:15:49 GMT  
		Size: 7.7 MB (7653959 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d21eccae88899113b9e0126cb64255aca549e84521b34ecc5fc1d7c273a2b36`  
		Last Modified: Tue, 04 Feb 2025 05:15:48 GMT  
		Size: 7.3 KB (7275 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-scm` - linux; mips64le

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

### `buildpack-deps:sid-scm` - unknown; unknown

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

### `buildpack-deps:sid-scm` - unknown; unknown

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
