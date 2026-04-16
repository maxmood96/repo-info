## `buildpack-deps:noble-scm`

```console
$ docker pull buildpack-deps@sha256:ee5b1cebfa3528c2499cec5a2cb0ed2fad707495c2634e02a86e13cd22b79450
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:noble-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:09085ccad062ae8b25aae13e165b358644ba8435acbbf7d76f9a83d333f46bff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.8 MB (88792574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cce2deea2b5fccb72f4d919709a38a9e2e0cee3516d5c4dc282df4d0564b2bf0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:24:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 15 Apr 2026 21:27:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e74df823fab1fa1733bb08c58699bfce01bda744a452f47ad2c43b3cb1cb4fe`  
		Last Modified: Wed, 15 Apr 2026 20:24:53 GMT  
		Size: 13.6 MB (13631097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c0aa64884f4ff5a623a43a69d75755b4dad0f1c84794c329a1953cf17751886`  
		Last Modified: Wed, 15 Apr 2026 21:27:20 GMT  
		Size: 45.4 MB (45428499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5402a21c28fe25adfe42e753fccbd179febd98dbf41b74efda83d59677622d37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5281881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5a75bbb166fec0e990507521fdd03e92fe8e6e7385660b9e10502b35087d84c`

```dockerfile
```

-	Layers:
	-	`sha256:29c854dfbd4249c1c93c177a5e0cce8c77495660559e4b14c02d4562d3f864fa`  
		Last Modified: Wed, 15 Apr 2026 21:27:19 GMT  
		Size: 5.3 MB (5274622 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c461cd15c3be039ee528cf6560efe6df02b437b8c23fb0f451dd255b04d38bc`  
		Last Modified: Wed, 15 Apr 2026 21:27:19 GMT  
		Size: 7.3 KB (7259 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:6dcf314152d24dee65cd5e5d7cfa7882067edd924f715e59864094261b9a20e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.6 MB (88616610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e6b1e0f13f78b11ebe5a63d3c89acdb6fe71e4f3cbd83a1410c3a96c6d50ccd`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:30 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:30 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:33 GMT
ADD file:341ecc672c4413d50e9543a8a38e44f8686dbdcc696b241b06e6b5b3a3ad57f6 in / 
# Fri, 10 Apr 2026 06:56:33 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:31:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 15 Apr 2026 21:32:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:03a6f28563c3f1bd861a0bd521bea32abc15b3b1362797f0ee963f0cfbe31325`  
		Last Modified: Fri, 10 Apr 2026 09:34:31 GMT  
		Size: 26.9 MB (26859689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2f3e21fdc9215469f529d0fa2ee012a5f88e6043f758465a59a06e69a9de344`  
		Last Modified: Wed, 15 Apr 2026 20:31:42 GMT  
		Size: 12.8 MB (12788413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ef3036a855c36f50253e679ca26adb48ab0975b36631e86abde826e9e2d50be`  
		Last Modified: Wed, 15 Apr 2026 21:32:36 GMT  
		Size: 49.0 MB (48968508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:45a21249cee7d66f01242d30fb684682ce8f65059189887054e1e53e39eb2ad3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5283246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff3851f3349dcc48cd97c789d458a717b797435a9675d982835f3f14f3b6cdab`

```dockerfile
```

-	Layers:
	-	`sha256:8de22131579bf3ba065031c58e55a15345404b0723765c8a7c3233b9091f4879`  
		Last Modified: Wed, 15 Apr 2026 21:32:35 GMT  
		Size: 5.3 MB (5275920 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a690ea07855a099c7792d285e5ad3b943bcd4ec612bb4e91df0a9ea492507681`  
		Last Modified: Wed, 15 Apr 2026 21:32:35 GMT  
		Size: 7.3 KB (7326 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:12edc82505de3380baab0a41b9001bfff6af246adc5683315db4ba211e1718f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.7 MB (87712271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6359ad80b7e8376c2537e070550bb3c7fc49cc71329195d7621298db8750c982`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:24:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 15 Apr 2026 21:40:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c8b8b2f453f0d9452e916f03dc2b34e96c8d3134d2f4fcf82ae53ea25628624`  
		Last Modified: Wed, 15 Apr 2026 20:24:23 GMT  
		Size: 13.5 MB (13466086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b7159a1df570cf04cb92b3a56ad91564b51623bf1f07fcff2bb9db97c713a4f`  
		Last Modified: Wed, 15 Apr 2026 21:40:28 GMT  
		Size: 45.4 MB (45370400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f4454bbbdaac67dec0dc62d0d4bd765ce8d6d8dfd94e2c06337b40212852591b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5289156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38a53eb231b2867ef706baec9f68da9c09134a17949b759eb0b0c283a3c51a69`

```dockerfile
```

-	Layers:
	-	`sha256:dde3a5e202d533853232a0ab099310e1370d90ed53803475f6640921b37516d5`  
		Last Modified: Wed, 15 Apr 2026 21:40:26 GMT  
		Size: 5.3 MB (5281814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb73da00e223eaa07e55cd3ee774f7964e175ad40dadedd3b2f7db6fafc9671e`  
		Last Modified: Wed, 15 Apr 2026 21:40:26 GMT  
		Size: 7.3 KB (7342 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:ae823a74229a59c9920348c67389a55e7aaf3eb71c54687abd28a005aa8676a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.7 MB (100690499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1bf61be42973efe47e1a4f76a1449db19d7cb97db29ff00f93791cdbfee398b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Apr 2026 06:58:39 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:58:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:58:39 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:58:42 GMT
ADD file:6c2e3684306335751e9b4f6c791c789b8a34813a48130b98adb259dbddc23bfb in / 
# Fri, 10 Apr 2026 06:58:43 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:11:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Thu, 16 Apr 2026 00:10:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:9b9e74108592a4e6bb74cdb3f96d255d3bfd39193b9030da034ebfc871cd90ea`  
		Last Modified: Fri, 10 Apr 2026 09:34:38 GMT  
		Size: 34.3 MB (34314178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6be9ec9f5316bf8d44e4d3d478b428c7bfc290d15dded4de8144bd7c334deb7d`  
		Last Modified: Wed, 15 Apr 2026 21:11:42 GMT  
		Size: 16.0 MB (15960709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:235c8af642371f9d6d7a048503470e8c4f36ee18f5e745207516b9098c2c2d31`  
		Last Modified: Thu, 16 Apr 2026 00:11:06 GMT  
		Size: 50.4 MB (50415612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:49ea2217d5e5c650ffa2e19e3dc8c75a3b53cffd11c7deba81db177e3fd8c641
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5289770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fd793bfb3f2da0829ce6cbff600ca220a547f9276592454dc761757d5f3fe59`

```dockerfile
```

-	Layers:
	-	`sha256:131f1c4c9d76d0c71a0cc2c1bafb1722f2944d298d52e6e392cda1cc1478020e`  
		Last Modified: Thu, 16 Apr 2026 00:11:05 GMT  
		Size: 5.3 MB (5282476 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:613a159a9bc4c6a7dda4d8fec8285239c69e4e1c4781e7b4abb0b09ddd5ccfc2`  
		Last Modified: Thu, 16 Apr 2026 00:11:05 GMT  
		Size: 7.3 KB (7294 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:81ccb86e17a410fc4f838bd35135e4780f2345968e6b6c7c03ff3b511d8fddbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.3 MB (101292606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:560be37159e0c58d3eb7885459c25ba22bbc484443a4f0f872cfa7d2077e5f85`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 03 Apr 2026 15:35:32 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:35:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:35:33 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:36:09 GMT
ADD file:59e78909d1b1cd9a524f68d8ff44bb077ea09f4f39da5e046d635b48da9d33bf in / 
# Fri, 03 Apr 2026 15:36:13 GMT
CMD ["/bin/bash"]
# Thu, 09 Apr 2026 01:53:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Sat, 11 Apr 2026 03:05:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:23ef52cbd4674ce4f8269086177a6a1fc3abbc052567212551b8169743067808`  
		Last Modified: Fri, 03 Apr 2026 15:56:59 GMT  
		Size: 31.0 MB (30963791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2f90ac4813ec6bbeb96b9ca1324f326cb79250eaeb56ecd108a3a0d03888dc3`  
		Last Modified: Thu, 09 Apr 2026 01:54:59 GMT  
		Size: 16.4 MB (16443158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:458c23f88fd80cd62b142ca8ede0942ed13340c22bab3bade167a2b7ad9289ef`  
		Last Modified: Sat, 11 Apr 2026 03:07:53 GMT  
		Size: 53.9 MB (53885657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c7f739ea05732d8e9c1777c0487c4fa8fd1d9370bb64c0b5cfee42943c957acd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5272312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaac9327e271ff4b74456bd1fc5d8445a320fc101e90535cfda1078eeb5dc3e1`

```dockerfile
```

-	Layers:
	-	`sha256:36970915303d81db363a43589d9ad1781c8af01e233c02e86ed52a4322ab631c`  
		Last Modified: Sat, 11 Apr 2026 03:07:46 GMT  
		Size: 5.3 MB (5265018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5170b9abf30cb1a46d3d8de9d55a75f016a98eb0d957a3103876e0f0a1251f06`  
		Last Modified: Sat, 11 Apr 2026 03:07:45 GMT  
		Size: 7.3 KB (7294 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:e050093c42daf894cfe173a93a2bbd031b937f19f1db6fe1ab86abe0a019d07d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.7 MB (91708507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d671745e77a1d4ed5a750a7c74a318aa282f2bf03b55e8842db9f99c36ab987`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Apr 2026 06:50:27 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:50:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:50:27 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:50:29 GMT
ADD file:41defd98c44eed6fc946fd94496a94164879f2ad4f63d66a5c1e213cc2259ad1 in / 
# Fri, 10 Apr 2026 06:50:29 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:43:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 15 Apr 2026 23:50:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:ef1c26d09a5f9962879f732e212c4246a41e8473f6120efb435886357c85dd5a`  
		Last Modified: Fri, 10 Apr 2026 09:34:53 GMT  
		Size: 29.9 MB (29912147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cea3ed85815c2b508fa34b7db8f31db4239744b73fdd23934c915d3fbedf18f4`  
		Last Modified: Wed, 15 Apr 2026 20:43:37 GMT  
		Size: 14.9 MB (14943412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bc35b736c6cf28a949f8edc48103ec926096a015294dd9e75e3273d9f17f774`  
		Last Modified: Wed, 15 Apr 2026 23:50:55 GMT  
		Size: 46.9 MB (46852948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:6cf7e0bc96675c11a0c667b0d8f2109093877b04da8352aa652d3ee9819025b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5284216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24281a4498f8d4481ddfbf03a8af8d45bc8aea633e2185bd645859d2951f083f`

```dockerfile
```

-	Layers:
	-	`sha256:939ec489ad9f2b90d2be808430b3f1b559c8880d029b1ffa7bd9953615521092`  
		Last Modified: Wed, 15 Apr 2026 23:50:54 GMT  
		Size: 5.3 MB (5276954 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c7f6f1129c16f46bb5e322f93fc394c923bdaf50c05ce913765067488572a556`  
		Last Modified: Wed, 15 Apr 2026 23:50:54 GMT  
		Size: 7.3 KB (7262 bytes)  
		MIME: application/vnd.in-toto+json
