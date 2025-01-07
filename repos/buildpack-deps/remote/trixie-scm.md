## `buildpack-deps:trixie-scm`

```console
$ docker pull buildpack-deps@sha256:1a2a1042eace60b3a674f9c1004519d5bb1c6ef39d8e51d97a9c394c78dc35b6
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

### `buildpack-deps:trixie-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:b8c4d19fcdd5c0b9f7b881512d2a832e0e9c6dcb0708b59a510e64b735bed08e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.6 MB (140637122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeb4a493006e190c0b315afcc48fc4931e5562387cc87da4bd2e85e2b38eb2d8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1734912000'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5dc28167de372c586b840aa2cdcf07e2afc8e85b392a5dbb5552be77587eff75`  
		Last Modified: Tue, 24 Dec 2024 21:32:36 GMT  
		Size: 52.2 MB (52212351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bfcdb7af4643d9e902826381436aafc5ca852c439990983daa707960060dbc0`  
		Last Modified: Tue, 24 Dec 2024 22:15:33 GMT  
		Size: 21.4 MB (21406167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:389a305f06858b3033956e0f308da92fdc18e3e15dddb5afd66e1616ffcfefee`  
		Size: 67.0 MB (67018604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7d4871b2ae7aa36acc715a500392660f5689484aceb26b746982b2d288f20a19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7637550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:751f177fd473369962664cbaf2402763f88ed4ca504f306d73d123f57329aff2`

```dockerfile
```

-	Layers:
	-	`sha256:09688db7c2ddf0451b6758d67daee2d4544615d3d39a28715be92acf490dd5ab`  
		Last Modified: Tue, 24 Dec 2024 23:16:09 GMT  
		Size: 7.6 MB (7630236 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82f2e0053dd96bd8cd5b4a230c83c0a7e5257148a9de0bd3d0a3393bdbe84855`  
		Size: 7.3 KB (7314 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:741577e8e26a084526bba4c0ffc323f111b22c4cc35ea9a0cac2ea92e8a1b014
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.5 MB (133502308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:258b9e966c898da2cf25bbeaf06417bdb05114c45627dd3333b7ec6d394c3cd2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1734912000'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:b5a5271e09aab30795789f051d2425121101b650637f36e772bdb80c62bb4833`  
		Size: 48.7 MB (48738917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd230c08c2a8f220f4a7754708d43b365ecaa32d038ae6429f10953c7ef0284c`  
		Last Modified: Wed, 25 Dec 2024 01:32:00 GMT  
		Size: 20.3 MB (20299500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d0bb5fbe3b18f1821e5711e289a996102173dec864a8442d53c9dfe3b763817`  
		Last Modified: Wed, 25 Dec 2024 04:51:05 GMT  
		Size: 64.5 MB (64463891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7d9dc8b7dd6bb6ee676a4cc75a339fe24989d490c4e4a8c2bac81102a09696be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7637884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed1234a4c33cf3dc5fdf65617a8f900b7ca3b63cd99b73997ba1ba047ce4f5d9`

```dockerfile
```

-	Layers:
	-	`sha256:f1bf8f0d44ebba11d199d0b4151d57a847547dad072372a129f88a51d97112ce`  
		Last Modified: Wed, 25 Dec 2024 04:51:04 GMT  
		Size: 7.6 MB (7630510 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d4a9013c8d44395229ae2ce70484fc0d89b290409e786de5724759e8247d2e1`  
		Last Modified: Wed, 25 Dec 2024 04:51:03 GMT  
		Size: 7.4 KB (7374 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:5d175f3c2e2a3219f599577ec61167274201d6f632f5ab2db3c699c6eca97246
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.3 MB (128252179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7e0f30ceec8a9c03fb4eb50ac5e592aefac1a2946b0741f8d4e80226f3399e9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1734912000'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:7dbbd0b59e8fd2a826bed9f5cfe195c9cb61ad138accd85ab45d8f8eb5e53a51`  
		Size: 46.8 MB (46767965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b1a49163ae7afb92f788f8101a5f0b57af46d0766372255bb4e15ef002eddc2`  
		Last Modified: Wed, 25 Dec 2024 03:45:38 GMT  
		Size: 19.6 MB (19597771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b3bbaffabd773ffb28e659f3ce21da08dd9edecbf06a175c763618e87bc80bf`  
		Last Modified: Wed, 25 Dec 2024 13:03:46 GMT  
		Size: 61.9 MB (61886443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:03eab124b261f77b607d4b267ef4cf69448632d93416036ff7669538f6bf6ca7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7637663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c39f113f7336159655025c197969e0ecf6ce5b183085688a405cccb41d6ced62`

```dockerfile
```

-	Layers:
	-	`sha256:b39b44b5696c10b9d713bb96a5228cdc862ef7e8e0eed21d8e575a60d1d31a22`  
		Last Modified: Wed, 25 Dec 2024 13:03:45 GMT  
		Size: 7.6 MB (7630289 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0484a84c997f3e1d0baf6eda0bf8ee2405d276d0113a0651f55f47fea4c5d8e7`  
		Last Modified: Wed, 25 Dec 2024 13:03:44 GMT  
		Size: 7.4 KB (7374 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:3deb684639d7b54f21e051a1fa276059f5316ee47bf8100015d4d7c312c7f8df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.6 MB (140570065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66d9a4ffa4331fd5c6cbf390415cfc0bd5f16309a4ddbbadad06a5a0536e3295`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1734912000'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:655b7ff6f79a823125a6f22dacb056ef3cd9ab7e8eb5ffc6594ff4745e276b8b`  
		Last Modified: Tue, 24 Dec 2024 21:37:11 GMT  
		Size: 52.4 MB (52425570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ff0f4612c729fd6c76a1191b59daef982c8369d9881af926e8193cfc3d012f9`  
		Last Modified: Wed, 25 Dec 2024 01:50:48 GMT  
		Size: 21.0 MB (21033507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e18c9c2923a1302f47d950f9dac6c92729acb289e93f1f208c03390958b352b`  
		Last Modified: Wed, 25 Dec 2024 08:14:04 GMT  
		Size: 67.1 MB (67110988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:be86d35cf5d56b6fc61a832ba647102b0ba8cd29280401cb0092bda48b25c7dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7647384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:728dad499982ec0043f1eee4fbd314deff7b8a800fe179f950fbcccc6c2b2ad7`

```dockerfile
```

-	Layers:
	-	`sha256:3251e44af530693e56231bfb7ef48f02253ca4fe26d053ebca4cabe058280639`  
		Last Modified: Wed, 25 Dec 2024 08:14:02 GMT  
		Size: 7.6 MB (7639990 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6e81fd3e4015178ac0604704673f927ce096984e14bc95a6c3af6438a6de6ed`  
		Last Modified: Wed, 25 Dec 2024 08:14:01 GMT  
		Size: 7.4 KB (7394 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:f97a4184f96456f9ae21ca643b9d4d7c8c0c80119a619b63aed30aec7cd9b90a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.4 MB (144356587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca78dc99df8f96bd24e7db15afb4798413f6e19843a78587b4d6a008ee99ae88`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1734912000'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:099da81c5d3f4771071b424bb19cc8bfc272821672d87e1978f2f206f3040f4f`  
		Last Modified: Tue, 24 Dec 2024 21:32:39 GMT  
		Size: 53.0 MB (53029057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d26fe834ebc7804c0441c6204e790d670676126e97ebaad982188f420a6aa9d5`  
		Last Modified: Tue, 24 Dec 2024 22:14:48 GMT  
		Size: 22.5 MB (22510156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deb826681a9ebc8783590b4b5076ad7abcfca5c59d820cfc6e4d1027f2e2804f`  
		Last Modified: Tue, 24 Dec 2024 23:16:11 GMT  
		Size: 68.8 MB (68817374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5a9b37dd3faa1ecacdf995efc5378d4aef76a0e2c8815c78c9adb645c495ceeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7632277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d9c5fc90344a84dc93fd21caf61f753808fa9ca4126954ad266cefbeea3c445`

```dockerfile
```

-	Layers:
	-	`sha256:d4176d3aee41ac8297cff2ec7c65318a223c554c1a53a52c90b590ab98dbc90a`  
		Last Modified: Tue, 24 Dec 2024 23:16:09 GMT  
		Size: 7.6 MB (7624985 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2bfdb5ac8660a8546888c6f358a1b17678bc0ed0bc11c382e9e3b8483e278c3`  
		Last Modified: Tue, 24 Dec 2024 23:16:09 GMT  
		Size: 7.3 KB (7292 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:5f7be54167182e84cbc19b18ac7f1c5974c1446c9584fd6bcaa7280ee57a58cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.4 MB (139425602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6f26ae159b88b59e727ef4419e83c01c5433cdcdd5fd525dac7b4c55403206b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'mips64el' out/ 'trixie' '@1734912000'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:3c43db2a2d96e4b42b073ee755704e1052dfc08d2fed2bad739906e6663926d9`  
		Last Modified: Tue, 24 Dec 2024 21:35:59 GMT  
		Size: 51.7 MB (51716844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb196cc5b6a238393d49fa4e93d6bc6fb9d8eb10a08514c2266839519f9d3f69`  
		Size: 21.7 MB (21727749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:744f68c6043110a4194987507fa740e27f0945cb8eaa1052f3742a94320b81d1`  
		Last Modified: Wed, 25 Dec 2024 19:21:22 GMT  
		Size: 66.0 MB (65981009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:bab98c3764e30026b20d3b7543e97a1873f6d268db559bb85d72f9798f5ead20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 KB (7145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:272014f6f5d2deb0a5d8d299b5a23f577b4bfa654325db120611212d92569475`

```dockerfile
```

-	Layers:
	-	`sha256:81a738cc1827688250c3572997e0eaa0ea857ad614089fe481bab7678d498283`  
		Last Modified: Wed, 25 Dec 2024 19:21:16 GMT  
		Size: 7.1 KB (7145 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:c0693b04a22623777357afb9be8f3cbfbdc4d9c8ae9015719764f7b161c948b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.4 MB (151362843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d46cbe82e9f27d9446f245f781c6f9dc602157f10dfebd5d9bfebf1c80d000cf`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1734912000'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:7d0c0062851cd41c4b765bee1eaa246592e96d9c4a0268bfea5c5d2a73be0e62`  
		Size: 56.0 MB (56044104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e488722a9275f087219fc61d856ea4c4ed4b328a7554350726557ef4cf4353e`  
		Last Modified: Wed, 25 Dec 2024 06:15:57 GMT  
		Size: 22.8 MB (22784408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5632f8c74ae00f98037831a4cdd3b0a421b4a43e35eb95c52372989b2288740`  
		Last Modified: Wed, 25 Dec 2024 09:46:04 GMT  
		Size: 72.5 MB (72534331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2b06e303b9d694adde4ce23adf32c9f03d41677812488989509f356d139b8493
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7644125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82bbc5dfdbaa6ffab86c567f870ef04f8a121f5ad4a2d579ba56110480cdfcea`

```dockerfile
```

-	Layers:
	-	`sha256:3d221998e22788cb8a2b02540f6857f35bb3cb2f738de6eaabe9b76c2e68c850`  
		Size: 7.6 MB (7636779 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a72d9fd70f2c7fc82d37604332bc4674b24948400a81327450b5900c533a8e8`  
		Last Modified: Wed, 25 Dec 2024 09:46:01 GMT  
		Size: 7.3 KB (7346 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:ac70c87e9381f52ce776562ae586af2726f3f43cef7a85c16385c81ea668c9b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.9 MB (142930571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:192c6e313c3e79056edca61bdb94ec5ab894882dadd45c0b6ca8b7938f823a8b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1734912000'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e1fe280a5056c1901421b5598ff050c78aa067b752ad527583fba85c589bb647`  
		Last Modified: Tue, 24 Dec 2024 21:37:42 GMT  
		Size: 52.2 MB (52167537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:febb20153a9b4c7c97b49477bb7e12772fe5782559f417bb6517d244a48d7108`  
		Last Modified: Wed, 25 Dec 2024 00:18:28 GMT  
		Size: 22.6 MB (22603773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d07fbd06dbc0259f8b92d4683dee4083fe7d2a755f0c0ab5b7d6848714d1ec49`  
		Last Modified: Wed, 25 Dec 2024 03:31:21 GMT  
		Size: 68.2 MB (68159261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1deb1d53abb5b2497f99707bf429f1e7394353b828e6180042524f08a87fcab0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7637969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e7a963a09f80f77dc5e607efb1fd69a71556171a3b95e2e6349a178eef8228d`

```dockerfile
```

-	Layers:
	-	`sha256:b4acacdb0de60835cf6eb931b0139b18df6c0200b4da3188db08206ba326a551`  
		Size: 7.6 MB (7630655 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c7aa0c685a441410c3da89e021f02c99785fa3c91ab5cab3f7588232b8d1062`  
		Size: 7.3 KB (7314 bytes)  
		MIME: application/vnd.in-toto+json
