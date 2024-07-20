## `sapmachine:17-jdk-headless-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:ef74204649b2ff7e1ffd14ce54fc53770c029f71d4dbb2de04fab27b0d36ee12
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jdk-headless-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:49cf7708f48cc2ee744a979ff7caac5f95cc84dfc059c9a5d47a6484b65c296d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.4 MB (228360351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eda3f0d0ea9f0222484b5b424e710dc04748dcced1cde0a02a07403db84b4526`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 27 Jun 2024 20:10:10 GMT
ARG RELEASE
# Thu, 27 Jun 2024 20:10:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 20:10:12 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Thu, 27 Jun 2024 20:10:12 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:21 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk-headless=17.0.12     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8004e5a9d5e0a972410f599e574e80008644edc080a9c46b8498b33dbd64b1e6`  
		Last Modified: Fri, 19 Jul 2024 18:00:27 GMT  
		Size: 198.8 MB (198826296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:d72e76e68962d77a6869ab742339a4084c06d251c2f1cf591309ff2f04b4dd59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2236633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae6ec0ce83270f4583742edac086b62da347a21352dd6c19dfa50db746ccd610`

```dockerfile
```

-	Layers:
	-	`sha256:19fc463f17ed9373e3b94f08d768633419dc55bf8e5e520f618807111f1b9744`  
		Last Modified: Fri, 19 Jul 2024 18:00:23 GMT  
		Size: 2.2 MB (2227955 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2984c1123a4ee195aa211db4eb6b6c5a10363b32de0be4ad686ff3b7788d32d`  
		Last Modified: Fri, 19 Jul 2024 18:00:23 GMT  
		Size: 8.7 KB (8678 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jdk-headless-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:d7cb4880428ea30881f8e80d53186be2361bcee8fa5ae33e04c950671552c591
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.8 MB (224785928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:006532c46e6b0cab867970e3f15eb47066e85106782bafd546eaf66551e738b8`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 27 Jun 2024 19:23:22 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:23:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:23:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:23:22 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:23:26 GMT
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
# Thu, 27 Jun 2024 19:23:26 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:21 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk-headless=17.0.12     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4ce000a43472e4a2527834764b5044674760f1e2a766480798d03a93b51a0b39`  
		Last Modified: Thu, 27 Jun 2024 20:18:34 GMT  
		Size: 27.4 MB (27360025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faa7045cf5622b8a3c913a3bc32cf6382b48bc06a4a478fe27b3d81e44f2235c`  
		Last Modified: Sat, 20 Jul 2024 00:27:17 GMT  
		Size: 197.4 MB (197425903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:16cc015eb272c5f8b8d1499378a396fe5303e1bd257208627a7ee79a2df1e23e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2236605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09ab03dcc2a9860b221ee0681981f0c545758e6d9f0077c09b1abaf0d38ad2a9`

```dockerfile
```

-	Layers:
	-	`sha256:36c3962a4b9821f8f17d7ac4395936392e1386ba92113039a210c11bceb986c5`  
		Last Modified: Sat, 20 Jul 2024 00:27:13 GMT  
		Size: 2.2 MB (2227625 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2128f056671e7e2b0794029e5dd8f3ced024a23f443aceb2d59f0681d507371`  
		Last Modified: Sat, 20 Jul 2024 00:27:12 GMT  
		Size: 9.0 KB (8980 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jdk-headless-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:99d3e42c8f1352f0d060d875b615e16d0684d44c5ff866b56bd5675a90164809
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.2 MB (234195327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:691afc8424fac2765d728fbadf5a61cb116938fe35f02580643bf507df3699a3`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 27 Jun 2024 19:22:59 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:22:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:22:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:22:59 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:23:03 GMT
ADD file:e2e1e840070a30a93a9141ddf77b416d95fb822ac1f550f7162a64e18e0ade5b in / 
# Thu, 27 Jun 2024 19:23:03 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:21 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk-headless=17.0.12     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:dcb5d217f9f18d3486ceb1894319d66c6f49a84670fbf2ac2f4dd47935357bfc`  
		Last Modified: Thu, 27 Jun 2024 20:18:46 GMT  
		Size: 34.5 MB (34461081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebdd9430a82b115d7ad8d1b66a4979ac68f330c0e028a2747992f6c0db2797a1`  
		Last Modified: Fri, 19 Jul 2024 23:39:25 GMT  
		Size: 199.7 MB (199734246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:e5b9de52785108b933a4c569444ee62104cfa9f9d03e03f88632029893b5c3aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2238632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d93d11c0bcc7e61adf056f82d087b8145e7e5c4e2816d215084531aaa472e4a4`

```dockerfile
```

-	Layers:
	-	`sha256:9dfa0abdd07e9bb36709e0d5a4540e5a13a7ee94a20ed7675a7b702c0eba1430`  
		Last Modified: Fri, 19 Jul 2024 23:39:19 GMT  
		Size: 2.2 MB (2229915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e999204b3d07ae22b16dd480ca11af1c72bf9d30a7184fcae9ea0dc148c8393f`  
		Last Modified: Fri, 19 Jul 2024 23:39:18 GMT  
		Size: 8.7 KB (8717 bytes)  
		MIME: application/vnd.in-toto+json
