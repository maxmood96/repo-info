## `buildpack-deps:bookworm-scm`

```console
$ docker pull buildpack-deps@sha256:97ffa09976ccaf8010bc65bae8c0fdbee77a70439e15e7f72edd30f30e77e6bb
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
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:bookworm-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:081b378225dd3efe7d85a0720370cbfd29b95001f7a0fb7073af54694ac974b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.8 MB (136754594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf470aba1a92d0771a65417e8a1beca6b311c9d18bcc12eb965032af2ee32b8a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:fdf894e782a221820acf469d425b802be26aedb5e5d26ea80a650ff6a974d488`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 48.5 MB (48497210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bd71677db44bb63b94de61b6f1f95d5540b4ba2d6a8a6bc4d19f422b25e0c2b`  
		Last Modified: Tue, 03 Dec 2024 02:28:49 GMT  
		Size: 23.9 MB (23865876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:551df7f94f9c131f2fec0e8063142411365f0a1c88b935b9fac22be91af227e0`  
		Last Modified: Tue, 03 Dec 2024 03:17:14 GMT  
		Size: 64.4 MB (64391508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:20e125aea8586458a38f6d6b5fc4e799b157c40f6827bcdeede53d9deae5face
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7770849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ed90e1697fb72676df77dcda5236274c90f61c17282ceccfc72e15b82f41da6`

```dockerfile
```

-	Layers:
	-	`sha256:012f88be9d04d99db39c2e75975d319894fe143e2f1d2c6b22032f733dc8c9a2`  
		Last Modified: Tue, 03 Dec 2024 03:17:12 GMT  
		Size: 7.8 MB (7763194 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ffa6b104b3f4a17660de0197b48ec8fbd2132b50b103011b72bafd123a894939`  
		Last Modified: Tue, 03 Dec 2024 03:17:12 GMT  
		Size: 7.7 KB (7655 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:9a1f00aee35fdbfc3bbef35f7b430afe4b7d61335911b8ca883d4ee277540158
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.1 MB (132068934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f28e47e232c9eb35167cfd394f5c0f26dd9550bca5ee8ac3a7fb762992cd8e96`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:895d07844c9c09054971f530ffd0794c329a785344079a01ce24e3d51727407e`  
		Last Modified: Tue, 12 Nov 2024 00:54:43 GMT  
		Size: 47.3 MB (47338750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93efb128382700f7090be7bec74d12308eb11ced11717aae4403b7bccde20f24`  
		Last Modified: Tue, 12 Nov 2024 06:28:08 GMT  
		Size: 22.7 MB (22733304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f5d34c31582cec80127fc538f65a56104fac2a20c87dbcaafc70b88f7a0a8b7`  
		Last Modified: Tue, 12 Nov 2024 11:29:42 GMT  
		Size: 62.0 MB (61996880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:146afff14da66d2415f7e870a0b5475327d3b8c5c3012e0e73e9929ce55432aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7773719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1139b21f47128807aca40d8f91d82ce8acf1684a9f67bba7bd10747e93444a31`

```dockerfile
```

-	Layers:
	-	`sha256:e5dc3d0311f5fe151c6c570f37bed7153cdc58ca55dc3f8244a7b0463ad6f4b5`  
		Last Modified: Tue, 12 Nov 2024 11:29:41 GMT  
		Size: 7.8 MB (7765996 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3878cd87f19cd6baf6f4baacf94bb729da9783cc7ba94a83e2575efb914f143`  
		Last Modified: Tue, 12 Nov 2024 11:29:40 GMT  
		Size: 7.7 KB (7723 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:a1a7d7b2ed0d74c7edcc906946a895b12bc703515f59b7cd3c2f80574576b92b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.8 MB (126752072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f29cddf530323d1831b929fa166f4322a1ff2ff5aa607bbafb8ff47657c9ed1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:46618ec96098836cac7950050ba554a969ebf8e9938d85d5f0d97015d3d25076`  
		Last Modified: Tue, 12 Nov 2024 00:56:14 GMT  
		Size: 45.2 MB (45150563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df9660b2b46aa0c77f5dd078f4e57432faf3dbcda91672b9e3f8c1b7892e0ee2`  
		Last Modified: Tue, 12 Nov 2024 15:59:18 GMT  
		Size: 22.0 MB (21960017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b55e7c0c5dd07ea67f173b9a9aa1ca29ae1ec286d0ed6813853bdaca8b1caeac`  
		Last Modified: Wed, 13 Nov 2024 07:37:50 GMT  
		Size: 59.6 MB (59641492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e81242a212ee50dd07a2de65d9ddb3c8375566532d787a1d71c83c483165b4bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7773446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0821de40bb134ad4c5de19b6e1b3f3cbc7a73d01c6dfad7a612804c07e1c123`

```dockerfile
```

-	Layers:
	-	`sha256:d70a741654943520f905a495fde4b165325a7a7f381b8afb3e2c9b8d8f4c245b`  
		Last Modified: Wed, 13 Nov 2024 07:37:49 GMT  
		Size: 7.8 MB (7765723 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7bf508a28326d76e5bb56cc5fb92b642419e7820332eefd105977a8adaf6042`  
		Last Modified: Wed, 13 Nov 2024 07:37:48 GMT  
		Size: 7.7 KB (7723 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:3351606a35eac6cc308876e2ec72862fe2ae4147581ccc4a10373c8d334c78c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.5 MB (137533154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ba5446467f88455a37f4e0de47bd59a0acaa9bc8f4806e4b5d9f2f0be94f096`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:1a3f1864ec54b1398987bbe673e93d8b09842ecd51e86ab87d64857b70d188b1`  
		Last Modified: Tue, 12 Nov 2024 00:56:20 GMT  
		Size: 49.6 MB (49587201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:464f864cfaa846fbe1b8a889827404e18374f805d29d77c288a813ae8c4f6d91`  
		Last Modified: Tue, 12 Nov 2024 11:16:03 GMT  
		Size: 23.6 MB (23598253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bc6ea9985d6735252067a2041e797c0dedef261a9695671fa4ef7891a96e4b5`  
		Last Modified: Wed, 13 Nov 2024 02:41:57 GMT  
		Size: 64.3 MB (64347700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:843e9778a42f9970fed06a3f8c5a4cbd883f9644c9fa7a5c4d522215421a16fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7778599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:440b7e24477949ac81a0a5b81b11b0d617759f6cafdb18274008a0c58bbb9945`

```dockerfile
```

-	Layers:
	-	`sha256:8b7b279db4f831921cf736f9c31c4260537b484b19a9a8d3e46241ff2b8c33f8`  
		Last Modified: Wed, 13 Nov 2024 02:41:55 GMT  
		Size: 7.8 MB (7770853 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6430e8df847f56490b7f4d0756e60d304be7d3079b7e5b70f08cc6049acad00`  
		Last Modified: Wed, 13 Nov 2024 02:41:55 GMT  
		Size: 7.7 KB (7746 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:efadcac373fc964d9e687e3c3acd546ed1243f3de78c4dfaa3cab0c1c44164bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.4 MB (140394239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24c6c2127f1e3c3cff2f2545cac8268fc28d1eca7e5f18ebd9811301efedbc12`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1733097600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:53769c348e57d646b1ec110dabf9d81a3f570afdb3b8216d1178515e4ea4ce1f`  
		Last Modified: Tue, 03 Dec 2024 01:27:09 GMT  
		Size: 49.5 MB (49476152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96b0c73f75a815ce87bbf2841b694fdc4c29bcd072480b8752e8e91f0b59097b`  
		Last Modified: Tue, 03 Dec 2024 03:23:49 GMT  
		Size: 24.7 MB (24706896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a2cf0351f309a0cf554972555b46b2ed97868d801e25eeed28a9f742a5e555c`  
		Last Modified: Tue, 03 Dec 2024 04:29:18 GMT  
		Size: 66.2 MB (66211191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:90045c81ec640293d6faa0394f96a1a985df7ff3d81fada2cfde8db780172edb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7766897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e344e02c870074180a5c7834575f4d8030d1e8969592d6bfa37194677c4d8bf3`

```dockerfile
```

-	Layers:
	-	`sha256:9855bce4e2e113f8c216ac6ecdad8a6af90932e14bc9bf28815c4fa67b760275`  
		Last Modified: Tue, 03 Dec 2024 04:29:16 GMT  
		Size: 7.8 MB (7759270 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:487dfc9a24b2a2d5a2e18670b6601e6e1927433744a4d83a1dd8813646329b52`  
		Last Modified: Tue, 03 Dec 2024 04:29:16 GMT  
		Size: 7.6 KB (7627 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:4263070c1d01e62040fb628f2a0e84added651437840c8032ee49007f97cb613
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.5 MB (136492842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee7cda17c176138bb4f82255724318a26b8a5de6e7a8b33926bd029c9c9c9a21`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:17191dc8a469e4ef93330c5c8402fa0c0761218a5fa02ad2db7b34508d0e995c`  
		Last Modified: Tue, 12 Nov 2024 00:57:16 GMT  
		Size: 49.6 MB (49559181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf888157372a89189e8193ccb502b1003341993a439a6f526f90dc05a6100692`  
		Last Modified: Tue, 12 Nov 2024 18:00:45 GMT  
		Size: 23.7 MB (23652171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45aa8c732dc480c917c006c596db2d04829d92a5899b87a988672ce7b03cfd6e`  
		Last Modified: Wed, 13 Nov 2024 02:02:53 GMT  
		Size: 63.3 MB (63281490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1815c228b1a9324712d262b76b2a31d5b19774193af5df4588a1245b5d317aa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 KB (7497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb219e4e67d188f17ee3301316582cbb8154cacde53f13906dcf77c16081d5dd`

```dockerfile
```

-	Layers:
	-	`sha256:3f719efdd956f4e8ce0d26ee6a810760a93a742a43f22e1c44fac6e11781904a`  
		Last Modified: Wed, 13 Nov 2024 02:02:46 GMT  
		Size: 7.5 KB (7497 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:4a4289d5bc6db05198984f4e81697f55cc0d7ac6720bdcbdb13af2b5b385c231
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.1 MB (149085096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3875cb156e725ad37ee97b98abf0f972f2ac10c4ff305204b30071a468158a4f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:9170cd93e372271efe7b34bbee8de26bbb094efba80a15cff49f580f87e5fe40`  
		Last Modified: Tue, 12 Nov 2024 00:57:37 GMT  
		Size: 53.6 MB (53555270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92051d5a3f7afdf0c89db06ce83fb963b8719a7024153e1520472673570e9d51`  
		Last Modified: Tue, 12 Nov 2024 08:29:09 GMT  
		Size: 25.7 MB (25717543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:913acd64029d37b20e9e161bb8659516cb78a99cfd56eb921fc4ccd76ae7c0c7`  
		Last Modified: Tue, 12 Nov 2024 16:09:31 GMT  
		Size: 69.8 MB (69812283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c21374c30e5f547aa9e66b04b1997909f699921da61d213ed3fb3d2a7de64c0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7779842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a315c2156e595de5e483e597dd3ea85ea0533d0e98f410011d7326f27679968f`

```dockerfile
```

-	Layers:
	-	`sha256:d9c5acd4f7b46ec0c9c2839752d6be8030b1bcc4d58b67483ad71a717d9899cb`  
		Last Modified: Tue, 12 Nov 2024 16:09:28 GMT  
		Size: 7.8 MB (7772149 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1014f338054fa217964a7cd584f29304bb70ac47f3c759f554c010e2b966ee4`  
		Last Modified: Tue, 12 Nov 2024 16:09:27 GMT  
		Size: 7.7 KB (7693 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:ac0fcc866f0bdbe302f3f3af142a52f456f2b7a383fcd80b14be2dbb2503880c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.5 MB (135470532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d56a382b5f8ca4bed953d08497d208b58150b01a03cadd9b1b2d05961d6027a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:9f9f8fa8b12064144bd5037b70d4d9ac4fcbcd94f2921feb1e017764a273f798`  
		Last Modified: Tue, 12 Nov 2024 00:58:23 GMT  
		Size: 47.9 MB (47938688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e53b034664a3d7aeeede4479f8aebfb2fff094119ae93ccf99e62d557e92b31f`  
		Last Modified: Tue, 12 Nov 2024 09:01:46 GMT  
		Size: 24.1 MB (24057883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c404d777567f321c549501c18afd08de2ba33359f57a5f517f6d5cc81747dbfa`  
		Last Modified: Tue, 12 Nov 2024 23:32:38 GMT  
		Size: 63.5 MB (63473961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:cc194e2aaabc6c701a089bd4b3693bc3dcd880153d27675d889c6498766762da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7771303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:102496b32b26dcae7bab66c6796673dccc90e13106628933ae54964b9aa776fc`

```dockerfile
```

-	Layers:
	-	`sha256:36a0bfb5fe3f2fbf77dd8b6aff1e54f0e3f67c5d41916e91dd4721999c98b109`  
		Last Modified: Tue, 12 Nov 2024 23:32:37 GMT  
		Size: 7.8 MB (7763648 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d4ae32354829745ed39bdbfb67312fc8163b11116273353815fbfcbdb924906`  
		Last Modified: Tue, 12 Nov 2024 23:32:36 GMT  
		Size: 7.7 KB (7655 bytes)  
		MIME: application/vnd.in-toto+json
