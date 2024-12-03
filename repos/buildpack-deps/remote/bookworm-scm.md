## `buildpack-deps:bookworm-scm`

```console
$ docker pull buildpack-deps@sha256:ae04bc8be910095456a39a5ab3cf41088108162cffe14aa06923336ffec6376e
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
$ docker pull buildpack-deps@sha256:9b05d826a9aea2d34ea09a27fa55a3c9149103ac03323af230c8d2fcbcc8c5b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.6 MB (130561570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:220e7a63ad00370b6e1c4651783b941fd094c6d2f66623cc356f07353ced08c9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1733097600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a8ab0b752e573ceb3480052f24bc5fe3f4f4665c13a338db39c1d51f749528e9`  
		Last Modified: Tue, 03 Dec 2024 01:27:04 GMT  
		Size: 46.0 MB (46024374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ff6779451547ba3f0647f15a65068290fed53b6a4ac506257de98e02857bea6`  
		Last Modified: Tue, 03 Dec 2024 05:23:42 GMT  
		Size: 22.5 MB (22540382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:536c3cdef529f6d2993cf137c109a079266cd3effbffc602a136a2a60ee743a0`  
		Last Modified: Tue, 03 Dec 2024 08:40:08 GMT  
		Size: 62.0 MB (61996814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ba33181894b95455834717fb83a3cab2650b256f61a539f7419fc4f2e9c101c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7772471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f49b76ea2636dae7de0703b48ca2f666e83f0a87977aff0a7884206898bf9654`

```dockerfile
```

-	Layers:
	-	`sha256:7b65f3800eb2add9f15ccf14f61be70696d82161b63f30b569972b0c8bd6a72e`  
		Last Modified: Tue, 03 Dec 2024 08:40:07 GMT  
		Size: 7.8 MB (7764748 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4172764014ee95b8731a943cfba1e0f4e0e07007f8a4395720c1e0f1339fcccc`  
		Last Modified: Tue, 03 Dec 2024 08:40:06 GMT  
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
$ docker pull buildpack-deps@sha256:4b4fd9f631b9294a9c2600d58e03ea6aabe8064c9023517e3c004147a248c706
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.1 MB (136079345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:294a87bc6560e0bb4acbf480b18930ca99a2863c50d4817579003ad59c8dcf5b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1733097600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:82312fccb35f18983647c1ea71154b98ae9893fb61ca4febe12d584a3ea9ad6d`  
		Last Modified: Tue, 03 Dec 2024 01:29:57 GMT  
		Size: 48.3 MB (48325680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ac722d9cf93b238dec2480278a2df5f8ccb672c97ec39f191191fd39f6721a8`  
		Last Modified: Tue, 03 Dec 2024 05:38:46 GMT  
		Size: 23.4 MB (23405813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:261351ed796deb9fdad22dc734919eaf6726dd79a8dea99327d9e1376ecdcbce`  
		Last Modified: Tue, 03 Dec 2024 11:50:22 GMT  
		Size: 64.3 MB (64347852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:296b38d3b5682f620d8d350576747bedddd836671036ca931158e5fcc0abeba6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7777352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6feeb02a68d010871c1233be105b538ae59e9b1d4fc972aaf364445fbcb678bd`

```dockerfile
```

-	Layers:
	-	`sha256:52070a7e355cffc4a9d0da8f0dc19e32ab40a808d402a964b8802456ba6e889f`  
		Last Modified: Tue, 03 Dec 2024 11:50:20 GMT  
		Size: 7.8 MB (7769605 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:559dec8b2f1952ab63dd3ad11af3f0cab12b2904ee9ac16805ff6743224ac486`  
		Last Modified: Tue, 03 Dec 2024 11:50:19 GMT  
		Size: 7.7 KB (7747 bytes)  
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
$ docker pull buildpack-deps@sha256:f41ac76702c18986d7791e88468e69b4dc78c623d28e1a490e6c0cbbfc6b1082
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.7 MB (147664451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:514cb07cf8569c7b8531ad437622c499eedef341c3f377fe235d298f7e8ac991`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1733097600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c84d784fe3c6c2bd95dea1c0d6eeba7c981bfb75bd53f81e83bcaadd87bba6f9`  
		Last Modified: Tue, 03 Dec 2024 01:28:03 GMT  
		Size: 52.3 MB (52328222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84f0cfea13db30ebc69124696ada25182d1141398cd301a47a2cbf3c10d7fa9b`  
		Last Modified: Tue, 03 Dec 2024 04:36:57 GMT  
		Size: 25.5 MB (25523892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac73bc765d61ec6125ff5203c6c3d44543e6c3030684bfed0cb8f169640ae757`  
		Last Modified: Tue, 03 Dec 2024 09:41:44 GMT  
		Size: 69.8 MB (69812337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2a89a02d7b0a3fc01937338322a3adbfec4f8acf6ca3ccbf611a6bfea596fec7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7778593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:296a47c62b0745a03c2b02e5a3f2df0ebe6f985dc10f4132e1e9b9ea44ffc350`

```dockerfile
```

-	Layers:
	-	`sha256:4b033dd73e35183deec51e3e2b0975d4838f1627c9589d8d0a263fdb61430e94`  
		Last Modified: Tue, 03 Dec 2024 09:41:42 GMT  
		Size: 7.8 MB (7770901 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1815558343ccce9363e7d65977e06bb87d6b20878e7dfbcffc07133ed7dee487`  
		Last Modified: Tue, 03 Dec 2024 09:41:41 GMT  
		Size: 7.7 KB (7692 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:3b238b3a7258d279b52146096b4beb7f45782123399ba1107028fffcda72845a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.5 MB (134487608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55812b2c5a9e20ae6c6e47ae8abb5ecd135751de9755ada12406aef2a0ded189`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1733097600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:53a5c0dbd93a4a7f540e18bbe49ba3d7fadaa390ebbce009c756e34c5b1ae048`  
		Last Modified: Tue, 03 Dec 2024 01:27:55 GMT  
		Size: 47.1 MB (47149767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ded5bb0b377b736e6c5f45164fe8916ada3485441e963fe2fc0671949650049`  
		Last Modified: Tue, 03 Dec 2024 04:07:42 GMT  
		Size: 23.9 MB (23864625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b626037a925f80e453161d124c98cc5578e9d47f3f90a050168552e9727a34e`  
		Last Modified: Tue, 03 Dec 2024 07:53:40 GMT  
		Size: 63.5 MB (63473216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2006631c59dc1f6d83026dc68c6f3367d6c4a1954eaaa7c817120bfb69572ef7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7770055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba9c6b8467b7d857fa1c079d9b3e0091c74f5fa80c8cc76afe7c7a05ea96e216`

```dockerfile
```

-	Layers:
	-	`sha256:fcf08fd6e06e7a3eb093b7470b9f4abc277ecb5601672f6d97c6e6712c678832`  
		Last Modified: Tue, 03 Dec 2024 07:53:39 GMT  
		Size: 7.8 MB (7762400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f3eab35b34c262dbc9b817602d68d99ea2c9634756836744ea2d6a546474acd`  
		Last Modified: Tue, 03 Dec 2024 07:53:39 GMT  
		Size: 7.7 KB (7655 bytes)  
		MIME: application/vnd.in-toto+json
