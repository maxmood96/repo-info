## `sapmachine:17-jre-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:75a1a70eeea919d1ae8d8fae6aac78d5f3fdfc68c853e4ea44ebe94ac54da937
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jre-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:04a805d78d2820771abe9acce5426d20d4c9873a35677fae5c3ba7371755c33e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.2 MB (83196447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d60d05ea9a9d4584b86a52be4304536a85126a9589e2957f074317760b403f1`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:54 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:54 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 May 2024 10:06:54 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Mon, 13 May 2024 10:06:54 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:54 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.11     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Mon, 13 May 2024 10:06:54 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e14e2666327fd4f91e3f7540e64aa07948e300f5d539690cfbf9f1c92da2d3a0`  
		Last Modified: Tue, 02 Jul 2024 03:32:01 GMT  
		Size: 53.7 MB (53662392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:011b3d231005f664a08c2c50ce3dfcc799ccd7779eb28286344fa3671aec74f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2366001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:221e8dea83688a0fa45392845e13d2ae937e06bd0dd1cc7c6b0f4c908b448fb9`

```dockerfile
```

-	Layers:
	-	`sha256:cab2b5b846be753e99a81626e567be48962e72239c2ca0f4fc6869a5895edf6b`  
		Last Modified: Tue, 02 Jul 2024 03:31:59 GMT  
		Size: 2.4 MB (2357416 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b2426289fb8d0a42015852b69a402fb2cd55290c86526e80d16f66ade584f0a`  
		Last Modified: Tue, 02 Jul 2024 03:31:59 GMT  
		Size: 8.6 KB (8585 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:ea0da92d8c0faefd4bffcef834d38e9140b733e7903faa86fbe38e6b800eaf85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.3 MB (80347834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b30cf6dd839eb915495ed28cf3ce99f7c186d4e672d4acc97a5fbb1d9ca834ea`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:54 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:54 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 May 2024 10:06:54 GMT
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
# Mon, 13 May 2024 10:06:54 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:54 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.11     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Mon, 13 May 2024 10:06:54 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4ce000a43472e4a2527834764b5044674760f1e2a766480798d03a93b51a0b39`  
		Last Modified: Thu, 27 Jun 2024 20:18:34 GMT  
		Size: 27.4 MB (27360025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4abbdeb2bced36e0797dd677b7c238b5297951f36f4bf6564a02f16570ba932`  
		Last Modified: Wed, 03 Jul 2024 00:04:25 GMT  
		Size: 53.0 MB (52987809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:68ce096e54ec634049769e247c8063d9444ab5f005f7cbef2a89d1947b303695
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2365982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb920768e192276b35ecb8acc5da7d3fa5811a4843ed62f7ffe2da2bd4013bca`

```dockerfile
```

-	Layers:
	-	`sha256:6d2e3cba5b0bd522eb36e60b398d01a1b8d5ab18268f38d813c6bbb206630220`  
		Last Modified: Wed, 03 Jul 2024 00:04:24 GMT  
		Size: 2.4 MB (2357096 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:351eefb9815dea04905645e87018a244968ba7b8bd336eb43d96bf8fa3c38b9d`  
		Last Modified: Wed, 03 Jul 2024 00:04:24 GMT  
		Size: 8.9 KB (8886 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:a06a0bca2968f2486408825bbfb8d468f9791353e0c4a557278d73a5df730231
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.6 MB (89597250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3247172a4186fa4472fc84fbe6db2d3cc1991b7bced886b38ae20ee744d793d`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:54 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:54 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 May 2024 10:06:54 GMT
ADD file:e2e1e840070a30a93a9141ddf77b416d95fb822ac1f550f7162a64e18e0ade5b in / 
# Mon, 13 May 2024 10:06:54 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:54 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.11     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Mon, 13 May 2024 10:06:54 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:dcb5d217f9f18d3486ceb1894319d66c6f49a84670fbf2ac2f4dd47935357bfc`  
		Last Modified: Thu, 27 Jun 2024 20:18:46 GMT  
		Size: 34.5 MB (34461081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d87d7b6b64bbf0e8c750fe126355d7c642115491aba43a850f128413222617`  
		Last Modified: Tue, 02 Jul 2024 21:34:31 GMT  
		Size: 55.1 MB (55136169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:ad682fc6bfa697cd0d9ccf7784615c55f809de5b91afe2531eb5ebbee2342bea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2370017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:238fe24befbb44598db6b045225caf036456f4f24b28fb4a5fd31b34630e86f6`

```dockerfile
```

-	Layers:
	-	`sha256:09e8bbe7ae1e70e88770ab9f2995d6519021759b0a9d75b93ea2f7eeb86c8230`  
		Last Modified: Tue, 02 Jul 2024 21:34:29 GMT  
		Size: 2.4 MB (2361395 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2dfd4c5294c185e56d2d09115ca8d1b3aa0848744fb9861af03d39c5d7c2cb98`  
		Last Modified: Tue, 02 Jul 2024 21:34:29 GMT  
		Size: 8.6 KB (8622 bytes)  
		MIME: application/vnd.in-toto+json
