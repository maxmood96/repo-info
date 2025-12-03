## `buildpack-deps:questing-scm`

```console
$ docker pull buildpack-deps@sha256:bff3fcaa3b3fe71364ed7262d81ae0c45677b7ea04b3b3a042b753524e1700d5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:questing-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:067a74a5c0aad368ff881e666f2e17d2411018d1f370cb90eafb7ca59af2cd5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.5 MB (101526007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b80c831a0537d7d6c3c2d7a9360651fcd006255b858446205f82638211450d6c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 27 Nov 2025 23:15:19 GMT
ARG RELEASE
# Thu, 27 Nov 2025 23:15:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Nov 2025 23:15:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Nov 2025 23:15:20 GMT
LABEL org.opencontainers.image.version=25.10
# Thu, 27 Nov 2025 23:15:23 GMT
ADD file:b50ac7284775f5383fad903e47cb3f2ef479d7e44d6f8f04f9bd60504972627c in / 
# Thu, 27 Nov 2025 23:15:23 GMT
CMD ["/bin/bash"]
# Tue, 02 Dec 2025 22:10:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 02 Dec 2025 23:46:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:a206cee1e8395be2f750c7fa3ff5be629dc0dea7ef665cc4c7aceaf244fcf0f8`  
		Last Modified: Tue, 02 Dec 2025 21:29:14 GMT  
		Size: 34.4 MB (34434358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d7fa57b343181bd363b105c946eaab265755eee4a9a8704db66044551df9757`  
		Last Modified: Tue, 02 Dec 2025 22:10:55 GMT  
		Size: 19.0 MB (18957014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91bbc7e5b5f1fe8d02edf38381dc6ba47d6d1aa432a92a95a84c046ac3047f39`  
		Last Modified: Tue, 02 Dec 2025 23:47:25 GMT  
		Size: 48.1 MB (48134635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:questing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a795113c0b91857df55c4387f8e10b475e1506706c4e32bef8ad29a15371222b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5775364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2cb296e751980c4e107a66531729b94a7d4c96de1a9a3c02f7d14aa4a9c77a9`

```dockerfile
```

-	Layers:
	-	`sha256:a0c22e946c8713bbca1464598a95de846887eeab609ca703d8e9d33d931d3c30`  
		Last Modified: Wed, 03 Dec 2025 02:19:55 GMT  
		Size: 5.8 MB (5768083 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3735b359bf9d8bdb8fc8021bf8246a7b8d5fa913a624d756083ac65fff4b5687`  
		Last Modified: Wed, 03 Dec 2025 02:19:56 GMT  
		Size: 7.3 KB (7281 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:questing-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:a56dea3cfb4b4be4e341ae0f8f12fba9e23e6aae8adfca9d597e5b37529f45ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.7 MB (99747396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b195329951c36698f4cea583cf77f28be473966eff65f3e9633594535b2563fb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 27 Nov 2025 23:16:43 GMT
ARG RELEASE
# Thu, 27 Nov 2025 23:16:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Nov 2025 23:16:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Nov 2025 23:16:43 GMT
LABEL org.opencontainers.image.version=25.10
# Thu, 27 Nov 2025 23:16:48 GMT
ADD file:cf3a8be0e74cddf6a500a4cf40ea2e6d1dcfadcb0ae21990673cc37126a3943e in / 
# Thu, 27 Nov 2025 23:16:48 GMT
CMD ["/bin/bash"]
# Tue, 02 Dec 2025 22:10:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 02 Dec 2025 23:11:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:1bb758e80424e5fcb11e548572cf31e928938fa9aa0cae00bcb95c4138a586fb`  
		Last Modified: Tue, 02 Dec 2025 21:29:41 GMT  
		Size: 31.8 MB (31834462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57cdfabd200070feb09fb34b8cf4182a319b4cae7401acb76296f2011517efc6`  
		Last Modified: Tue, 02 Dec 2025 22:11:06 GMT  
		Size: 17.3 MB (17335260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8c7c429cb42506d4ab6d6215597549decc4c87e4366ce23b01aa338a31d47ec`  
		Last Modified: Tue, 02 Dec 2025 23:11:40 GMT  
		Size: 50.6 MB (50577674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:questing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:bff9f20afda92d1b0f6e3e4c4776e773f07fb459118972ee18b8d8214ed27795
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5775927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae8077551bffd1a13ca3ff08a0929feeafbafcc7861fb317c90253662ea70504`

```dockerfile
```

-	Layers:
	-	`sha256:9b59e51627150cc9aa4098b5ee8fce3d436afe651fc6521a42bb72ccccbc6415`  
		Last Modified: Wed, 03 Dec 2025 02:20:01 GMT  
		Size: 5.8 MB (5768582 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e314136aa738fb2e6213d49f9bbfa702913d5434e83352e905dc0b02a5de158`  
		Last Modified: Wed, 03 Dec 2025 02:20:02 GMT  
		Size: 7.3 KB (7345 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:questing-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:2364f917eb37b46dbfeef6d58b2426c48dc6d73fbc502ad08a20f96c61623c07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.3 MB (100301176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62453243377f7adad3523c6494097f0129bfdc6c19895eb5bf4dea2e7e3362d4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 27 Nov 2025 23:18:54 GMT
ARG RELEASE
# Thu, 27 Nov 2025 23:18:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Nov 2025 23:18:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Nov 2025 23:18:54 GMT
LABEL org.opencontainers.image.version=25.10
# Thu, 27 Nov 2025 23:18:59 GMT
ADD file:e9263cd3e11f533dc9f3fb889930c09c631fb75e6ad89ab6a2146821b2cd442e in / 
# Thu, 27 Nov 2025 23:19:00 GMT
CMD ["/bin/bash"]
# Tue, 02 Dec 2025 22:10:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 02 Dec 2025 23:10:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:2f25135cc937748dc7f12ddd61abe8c7cc1f5eedc0322b8a68a7816b40f885d3`  
		Last Modified: Tue, 02 Dec 2025 21:28:44 GMT  
		Size: 34.0 MB (34041785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:862e65d36700e00016fe3e22d70e37e155c00e70952167e3c7d3e9b449c828d1`  
		Last Modified: Tue, 02 Dec 2025 22:11:20 GMT  
		Size: 18.5 MB (18516394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:048cc9d61153ec1806b1122f8553cac7a65d4aa132bb4138225a8def74e5789a`  
		Last Modified: Tue, 02 Dec 2025 23:10:43 GMT  
		Size: 47.7 MB (47742997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:questing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c66b07c639c242b4718d5b17aa1d293d429d4ca1cfe700afffe9cd25536ed523
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5781832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e594b3f49b5eab7fc5ac3ab9b82756d53ad95164ae625857e559b72260163a3b`

```dockerfile
```

-	Layers:
	-	`sha256:1187e899927a2b73325e5a76c681da23efe2203b06b8bc5868d71797edaf1bb6`  
		Last Modified: Wed, 03 Dec 2025 02:20:09 GMT  
		Size: 5.8 MB (5774471 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c7001589722ef42db8b773285384e24d6b0f5b15c1a8c42366af8b5e888909a`  
		Last Modified: Wed, 03 Dec 2025 02:20:10 GMT  
		Size: 7.4 KB (7361 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:questing-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:0b5dc6e66920f8d678f7ae12f49e35a4aac346e99260fbfdb965219900320030
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.1 MB (114111439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc4b3c2742005a29d3562c1dedbccd616d87ff01bf2c6e460c4d1923fe843ad8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 27 Nov 2025 23:18:21 GMT
ARG RELEASE
# Thu, 27 Nov 2025 23:18:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Nov 2025 23:18:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Nov 2025 23:18:22 GMT
LABEL org.opencontainers.image.version=25.10
# Thu, 27 Nov 2025 23:18:26 GMT
ADD file:c60052f4baf0af16960125955d00ffced77f86d7216d8ccc1970073116299473 in / 
# Thu, 27 Nov 2025 23:18:26 GMT
CMD ["/bin/bash"]
# Tue, 02 Dec 2025 22:10:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 02 Dec 2025 23:10:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:052023144ae674b4b4ab26f82f1589773a7bcd1d86cae1f6ad2e372e7cc3e64a`  
		Last Modified: Tue, 02 Dec 2025 21:28:20 GMT  
		Size: 39.6 MB (39595804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10958d3dbb6807fff29fb93bc67ade7a05e527164b7f99ae47430b9d4cb04bcd`  
		Last Modified: Tue, 02 Dec 2025 22:10:53 GMT  
		Size: 21.0 MB (20959974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54ede6d734e59ee38e0d651b3337536943cd79ba605982c13df75fca55379326`  
		Last Modified: Tue, 02 Dec 2025 23:11:08 GMT  
		Size: 53.6 MB (53555661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:questing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9226b7902e29a6d11d5fecf0aff94925ec8210ebf6b7b297ce3750a75dbffc64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5782459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2da417d92621c1fee1f386e2325846ef6f928802847cd59a5f2930a77195a646`

```dockerfile
```

-	Layers:
	-	`sha256:383fd2cc997a52fabeb669d4efe53942ccaa026f6284f43e403d1ac917b0097b`  
		Last Modified: Wed, 03 Dec 2025 02:20:16 GMT  
		Size: 5.8 MB (5775146 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2e99afd9339de7ea36490a20361df42837a13b763fad36940c920483261735b`  
		Last Modified: Wed, 03 Dec 2025 02:20:20 GMT  
		Size: 7.3 KB (7313 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:questing-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:5b564eaed782a4f8c5f7e42ae9c4e73ec405fb0302aa6862aa65e1e31db07f37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.0 MB (104040569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4b7adf5c35de4b2d73f458eff37bfee62514f3c08daf0dca7b2376dbe2997f8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 27 Nov 2025 23:17:10 GMT
ARG RELEASE
# Thu, 27 Nov 2025 23:17:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Nov 2025 23:17:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Nov 2025 23:17:10 GMT
LABEL org.opencontainers.image.version=25.10
# Thu, 27 Nov 2025 23:17:12 GMT
ADD file:6fb7e51cfcb793f6714200cfa953fa57850eda7a571798229cb4ef58cdee6f7f in / 
# Thu, 27 Nov 2025 23:17:12 GMT
CMD ["/bin/bash"]
# Tue, 02 Dec 2025 22:11:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 02 Dec 2025 23:10:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:cacee7f118ad009c16f8f35172dd48a3fb01d421ef7100077e95aeda6405e172`  
		Last Modified: Tue, 02 Dec 2025 21:28:22 GMT  
		Size: 34.1 MB (34096846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cb10874e9a431a6859624a2b833fad01e6c85500deb89ea0e98f035ed285469`  
		Last Modified: Tue, 02 Dec 2025 22:11:57 GMT  
		Size: 21.0 MB (20975453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f28df6ca3ee8256c5629448d7dfd54e13e0e140544a4d3aefe1767613f285c46`  
		Last Modified: Tue, 02 Dec 2025 23:11:39 GMT  
		Size: 49.0 MB (48968270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:questing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c9d6a359beb33bf3cdb34b90d3425a7f0462c919ca7ebcae29fb736365e070a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5776901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:056853ccf797dba9e7b5f4574762c0255ee22dd933fc62ba49e3f02c2bafd771`

```dockerfile
```

-	Layers:
	-	`sha256:1070f4add8a8366b3ed27744bd5d18105062523e900bb507e64673cb48b7c41b`  
		Last Modified: Wed, 03 Dec 2025 02:20:37 GMT  
		Size: 5.8 MB (5769620 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8909e873e8334b1d230ec86ee01aaf879bc5c95719a5fcc458ab470b9820f3a`  
		Last Modified: Wed, 03 Dec 2025 02:20:38 GMT  
		Size: 7.3 KB (7281 bytes)  
		MIME: application/vnd.in-toto+json
