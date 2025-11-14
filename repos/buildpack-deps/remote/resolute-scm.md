## `buildpack-deps:resolute-scm`

```console
$ docker pull buildpack-deps@sha256:1fc7e7c73c7fbdb74c4241dbec8e01591a4f75eddd9e6b9181aff9298f077335
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:resolute-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:faeb0fae13e435f8005c0cd404de053483182ebf49ce26b54eddc7055cc554bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.3 MB (101295122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b20e66677fdfc72694b600b0c3e43567983d6052475a7888f69f5be0386beba`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Nov 2025 16:26:15 GMT
ARG RELEASE
# Mon, 03 Nov 2025 16:26:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Nov 2025 16:26:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Nov 2025 16:26:15 GMT
LABEL org.opencontainers.image.version=26.04
# Mon, 03 Nov 2025 16:26:18 GMT
ADD file:66147c6f676f9f213a555a39746cf19931aaab10b3b1d4e204c77f9ad595f3c7 in / 
# Mon, 03 Nov 2025 16:26:18 GMT
CMD ["/bin/bash"]
# Fri, 14 Nov 2025 01:12:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Fri, 14 Nov 2025 02:17:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:bf861ca04e51abe6e211f1d7adf78b6800e3ccddf6669442247314d2cbcac184`  
		Last Modified: Thu, 13 Nov 2025 23:04:12 GMT  
		Size: 34.5 MB (34536159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1bf8f500dde3b1a37fde334af1e9bed56a0f7b19d93b694d9dc9a6097d7e7d2`  
		Last Modified: Fri, 14 Nov 2025 01:12:43 GMT  
		Size: 18.6 MB (18563951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6af585b07f92d2bce246cb20ac6fbebf437547418401a784d08780ed5c2999a`  
		Last Modified: Fri, 14 Nov 2025 02:18:02 GMT  
		Size: 48.2 MB (48195012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:resolute-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:4906b7557d42bc7281481b48bff4db76539c23658b3fc286a163a9d5085bd1d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5761044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:771a43dd3fb2e10df9df56420c07ffdbce536d3dbb509154ab647d334f48b12e`

```dockerfile
```

-	Layers:
	-	`sha256:8501222a09dd3dba44b1307c429cd0bc62ad35268dfd04a3ed3daa4a831373cf`  
		Last Modified: Fri, 14 Nov 2025 05:20:06 GMT  
		Size: 5.8 MB (5753764 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b96187f2727c25a106fceaf1791bef98c167ae0e116429daf0a96ed635f6297e`  
		Last Modified: Fri, 14 Nov 2025 05:20:07 GMT  
		Size: 7.3 KB (7280 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:resolute-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:279f2a0b0d962793642fec6d201dabfc9aa0804ad6298193d99532d13798e9a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.4 MB (99378872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d91cd904193b7f6d6ecf0006478a2e4c55ca911a0f6e1ab2355dac6dbed7fa64`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Nov 2025 16:29:08 GMT
ARG RELEASE
# Mon, 03 Nov 2025 16:29:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Nov 2025 16:29:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Nov 2025 16:29:08 GMT
LABEL org.opencontainers.image.version=26.04
# Mon, 03 Nov 2025 16:29:18 GMT
ADD file:b5205c826c7c3a6374a9466a98138ed499f3832207208fa02f5929bd90a79717 in / 
# Mon, 03 Nov 2025 16:29:18 GMT
CMD ["/bin/bash"]
# Fri, 14 Nov 2025 01:02:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Fri, 14 Nov 2025 01:08:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:a4edfc31f2f766770f61ea46a0f4f1fd53dacedd2336abb49820c8c4368e9405`  
		Last Modified: Thu, 13 Nov 2025 23:03:49 GMT  
		Size: 31.8 MB (31756944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0ebd3cc0b0d366216373a9d97fee336363125c0fb40eaf46a136ed5b085c17f`  
		Last Modified: Fri, 14 Nov 2025 01:02:39 GMT  
		Size: 17.0 MB (17043524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a330e9013ab0e736ac9941a3f10a187cdd8455d91096aef8b896682f821ccf3`  
		Last Modified: Fri, 14 Nov 2025 01:09:04 GMT  
		Size: 50.6 MB (50578404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:resolute-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8047f47a22f574b655cdefcd3cce49da94917068a46138f1108e9370802a5f5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5761608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:786e466f3900ea3617a43395c2d8c57485279bacd9c88952743e52ddfa03eb3d`

```dockerfile
```

-	Layers:
	-	`sha256:aac6e3a0c2648a41c70e83f59c07cec5bbd39d9076f56fd90a29a7dc0011ee64`  
		Last Modified: Fri, 14 Nov 2025 02:21:35 GMT  
		Size: 5.8 MB (5754263 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:199774efc4f361dc10352af81a1ff6b92e9fb6b5bda643f1f650db95edb998ca`  
		Last Modified: Fri, 14 Nov 2025 02:21:36 GMT  
		Size: 7.3 KB (7345 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:resolute-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:9051279966186b2625925a3e3e51fc80f647c5b8cb1de7d4ccd0f36840ef2a03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.1 MB (100128017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1deb736b8c08a976d56ba58750df78e39efbb4d619c0e9f9f0b8ff60d8381d36`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Nov 2025 16:35:21 GMT
ARG RELEASE
# Mon, 03 Nov 2025 16:35:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Nov 2025 16:35:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Nov 2025 16:35:21 GMT
LABEL org.opencontainers.image.version=26.04
# Mon, 03 Nov 2025 16:35:25 GMT
ADD file:fa5fb78e75e38181f1a81bb9dceb17207c748aa204ca8bf3f8304812e06e03af in / 
# Mon, 03 Nov 2025 16:35:26 GMT
CMD ["/bin/bash"]
# Fri, 14 Nov 2025 01:28:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Fri, 14 Nov 2025 02:21:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:2f462b7fc45d3e233f44ee8478d5fcda8587f606880626a20f9b95dceb29563b`  
		Last Modified: Thu, 13 Nov 2025 23:03:12 GMT  
		Size: 34.1 MB (34136045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c026b9e95920b8b24682c9f532e99585180cd18a0ffd9ca4d5df8a76df296786`  
		Last Modified: Fri, 14 Nov 2025 01:28:46 GMT  
		Size: 18.1 MB (18121238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8273c9c4dd5714ffb067a8d9fde7b789e40ef78c133b6276ffcbfcc39334af6f`  
		Last Modified: Fri, 14 Nov 2025 02:21:55 GMT  
		Size: 47.9 MB (47870734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:resolute-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:72210cf073f2b5ce4d99f5117802b3013117485b7a2b2d645fdffb3e78d42f80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5767513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ce0535357c772911c72c6872c8f4bd877e10a89d6a470ecb8891a63c967c66d`

```dockerfile
```

-	Layers:
	-	`sha256:06df43e5f094d0612eafcc0e31f3896d699045dfddeb3cae93ebbc757b6cdc6c`  
		Last Modified: Fri, 14 Nov 2025 05:20:15 GMT  
		Size: 5.8 MB (5760152 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76cfb5739c6407dcc42e4aa3112c3746415fae2d079121990ca33f1a226328da`  
		Last Modified: Fri, 14 Nov 2025 05:20:16 GMT  
		Size: 7.4 KB (7361 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:resolute-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:c1d795d11804c2e3c7997c73e2bb3068c3a9de8288b504d87e98fc2054f3cb90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.1 MB (102083818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31573c2e433238b808d09c034902e0703d6a1b6dcf4567a1f2143f26e4485497`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Nov 2025 16:26:18 GMT
ARG RELEASE
# Mon, 03 Nov 2025 16:26:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Nov 2025 16:26:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Nov 2025 16:26:18 GMT
LABEL org.opencontainers.image.version=26.04
# Mon, 03 Nov 2025 16:26:20 GMT
ADD file:9822bf6c1b19da666ab2a2953f39d343703c0f91143fd537124e1c6d0f7987ae in / 
# Mon, 03 Nov 2025 16:26:20 GMT
CMD ["/bin/bash"]
# Fri, 14 Nov 2025 01:36:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Fri, 14 Nov 2025 03:05:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:20fe16e1688741ad12b12d15198947fc2acdf6a49eb1c8b9d560287f1e19adcd`  
		Last Modified: Thu, 13 Nov 2025 23:31:39 GMT  
		Size: 34.2 MB (34160088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb0baf195a9a3968ffc48a15ac31621700b1063bab9bc664d01abe205acfdcd7`  
		Last Modified: Fri, 14 Nov 2025 01:37:21 GMT  
		Size: 19.0 MB (18953137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b10cb9fb4094b50c98c187427b215a87987ab798ef10c436225d9db35400308c`  
		Last Modified: Fri, 14 Nov 2025 03:06:24 GMT  
		Size: 49.0 MB (48970593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:resolute-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:432019f2b2980e5ec9de310a28de44ea39638e953c0b447be500288737250601
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5762581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34e205f21156e79b97f0cd2a1ecde7732bb1fa6e26604f64916af1b2eec8a6aa`

```dockerfile
```

-	Layers:
	-	`sha256:0133f48f0964b6cdbb228b6931fff6c56b91acc22421170cf37fb13507c9f152`  
		Last Modified: Fri, 14 Nov 2025 05:20:21 GMT  
		Size: 5.8 MB (5755301 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:859f8ee2f65ba78d1b9294342360124281c0c37225367bfa830b5f7bb7412e4c`  
		Last Modified: Fri, 14 Nov 2025 05:20:22 GMT  
		Size: 7.3 KB (7280 bytes)  
		MIME: application/vnd.in-toto+json
