## `sapmachine:17-jre-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:e873f8fbb0ce2521f4467b1802bb281b9d7409867e448151bb688ff7445bea08
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jre-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:284051c51b81401ba7e319d2154d6e6158551e2db997b3810eaa2ef180e378ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.2 MB (83244776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1c89f8390e1b0b649984dabc489e4b12b8188fc515f93c8eaac04eefd3e010f`
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
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.12     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
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
	-	`sha256:4407f7096eaf9f0a2b7d2e81d8b9a7173f8060b1bbc420e615ec4364c034b704`  
		Last Modified: Fri, 19 Jul 2024 18:00:13 GMT  
		Size: 53.7 MB (53710721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:b73437d79ac806cff6b9471f9f834beb120282ee573eb53a6bf088edb520d9f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2395428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de3c9030c8829321b4f9a589f86435177b7896d8e2f7ffbb3870860cdb5cd1d4`

```dockerfile
```

-	Layers:
	-	`sha256:35cf6508907c895a3d2a9cdc3c00d6e4aaf43c8429871d7eb035c144fd6df5d6`  
		Last Modified: Fri, 19 Jul 2024 18:00:12 GMT  
		Size: 2.4 MB (2386862 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38b10397699bd666640da454cb58f64bd6659ef06b5200a9939158ab6a91e1e9`  
		Last Modified: Fri, 19 Jul 2024 18:00:12 GMT  
		Size: 8.6 KB (8566 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-ubuntu-22.04` - linux; arm64 variant v8

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

### `sapmachine:17-jre-ubuntu-22.04` - unknown; unknown

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

### `sapmachine:17-jre-ubuntu-22.04` - linux; ppc64le

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

### `sapmachine:17-jre-ubuntu-22.04` - unknown; unknown

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
