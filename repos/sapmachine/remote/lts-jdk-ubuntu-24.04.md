## `sapmachine:lts-jdk-ubuntu-24.04`

```console
$ docker pull sapmachine@sha256:2460a6d50f55c1c1d8195faf974cd2a5dcb06d9cc165ac8723c253ec4c286d66
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:lts-jdk-ubuntu-24.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:eb00a6e2a4b59e270293ec41a06efe74515e8a7e0e8c23e7e6f9c8361768eec2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.7 MB (244695580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3934819ef6c59fc91b2aea55eddcbc6bb77f049569ad2d1fa5c86b48f9141c81`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Oct 2024 12:49:09 GMT
ARG RELEASE
# Wed, 16 Oct 2024 12:49:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Oct 2024 12:49:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Oct 2024 12:49:09 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Oct 2024 12:49:09 GMT
ADD file:bcebbf0fddcba5b864d5d267b68dd23bcfb01275e6ec7bcab69bf8b56af14804 in / 
# Wed, 16 Oct 2024 12:49:09 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 12:49:09 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.5     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:09 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 16 Oct 2024 12:49:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:de44b265507ae44b212defcb50694d666f136b35c1090d9709068bc861bb2d64`  
		Last Modified: Tue, 19 Nov 2024 17:38:27 GMT  
		Size: 29.8 MB (29751968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be4665ddf8590cff01ed85dad480fe139cbc7547245750193897acc91288ab5a`  
		Last Modified: Tue, 03 Dec 2024 02:35:49 GMT  
		Size: 214.9 MB (214943612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jdk-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:4cd918608f535a6be0acca02e0e9b45208c45d33def423e59ea363e959bb1481
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2487204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a8af13e4f699aba7c2a910c2cecf7e852b5d0de1ca4037ae1cfb8dc5477090d`

```dockerfile
```

-	Layers:
	-	`sha256:3f36e0079d8c5565fa52be29ea2dca6f0bd240d9424a64c94b715fd72325a761`  
		Last Modified: Tue, 03 Dec 2024 02:35:46 GMT  
		Size: 2.5 MB (2473885 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1323fa76312f0c25914c64fbe1a8477484ee93519643a3e5a1fcf690601a9d5`  
		Last Modified: Tue, 03 Dec 2024 02:35:46 GMT  
		Size: 13.3 KB (13319 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jdk-ubuntu-24.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:40eaf682a1fc213be64aba88fd38854bebb0e8b96ccb66008a819064fac03edd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.0 MB (242037848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:799064659efaa71951a370c9a9ac0a420b6783b108eaec0ee7f6ae9c2108d56d`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Oct 2024 09:25:38 GMT
ARG RELEASE
# Wed, 16 Oct 2024 09:25:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Oct 2024 09:25:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Oct 2024 09:25:38 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Oct 2024 09:25:40 GMT
ADD file:f45100f0b1cac298fb43b06ffef22e36a90991ee414d6dd825694bbea3365d40 in / 
# Wed, 16 Oct 2024 09:25:40 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 12:49:09 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.5     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:09 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 16 Oct 2024 12:49:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e3366dd687552c0533285c7066bb8e937a5aaa2ff3a0c1c7f1305b3310399895`  
		Last Modified: Wed, 16 Oct 2024 12:48:12 GMT  
		Size: 28.9 MB (28892425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c778935a0b47d72cae383e9d4fc4831f38fd060bbaca4476cf0becef046700db`  
		Last Modified: Sat, 16 Nov 2024 03:47:13 GMT  
		Size: 213.1 MB (213145423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jdk-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:776661a1f570b6da1d3f1714399c0565ba1aa5326cc09fa6f5a807c175e01b23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2488091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ba4c416b057e41fa56b0fdfb5e01ea2bb42008dd3ec81657da13aaf939a8f51`

```dockerfile
```

-	Layers:
	-	`sha256:4852b0a1ecd11050405ae253fe60f49b069b92af591b6a916cbe024f996e72b5`  
		Last Modified: Sat, 16 Nov 2024 03:47:09 GMT  
		Size: 2.5 MB (2474500 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12b30814567331cf39bb0b736083724d34994a797cf28bd7dd3f732fce654e0e`  
		Last Modified: Sat, 16 Nov 2024 03:47:08 GMT  
		Size: 13.6 KB (13591 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jdk-ubuntu-24.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:f458f028cfb7a66b11ff4d56656137fb5ed896052c2cdcc2e474ad3d1fa58def
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.8 MB (250783313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d681ddd5198fe5e306f774a0b8ab183ce7d4510793097f4832e4474c3e75dc6`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Oct 2024 09:26:09 GMT
ARG RELEASE
# Wed, 16 Oct 2024 09:26:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Oct 2024 09:26:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Oct 2024 09:26:09 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Oct 2024 09:26:12 GMT
ADD file:8427b57c40c05cd946f6695dbd1754b0a521a98decd2cdc16eeb114c7128804a in / 
# Wed, 16 Oct 2024 09:26:12 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 12:49:09 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.5     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:09 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 16 Oct 2024 12:49:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:991986948126e836a79c1084e3bee33549a43b83cabfe16234aef5b4b30d86f9`  
		Last Modified: Wed, 16 Oct 2024 12:48:24 GMT  
		Size: 34.4 MB (34388822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96987e2d574af7a23758b669715e8b466639934fb1a8b3ad14ad75689377c1d7`  
		Last Modified: Sat, 16 Nov 2024 03:45:56 GMT  
		Size: 216.4 MB (216394491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jdk-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:8654ac5af7f0194366e9e474a8277d4b3ea090739d61e1879a5a325aee222598
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2489384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6513bc96042dea5a3086215e8e4f9d73bbde504269ccef39af1ac24dbdfb1c0`

```dockerfile
```

-	Layers:
	-	`sha256:a7d3dfa0ff9debc8a1a92489e2e2443451036d793b935dc37bacdd910442efdc`  
		Last Modified: Sat, 16 Nov 2024 03:45:51 GMT  
		Size: 2.5 MB (2475937 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1e042f3b588a1e8ef58c2a871ec8b7d4c2fd44d45364a66b44a41e2bf93e864`  
		Last Modified: Sat, 16 Nov 2024 03:45:50 GMT  
		Size: 13.4 KB (13447 bytes)  
		MIME: application/vnd.in-toto+json
