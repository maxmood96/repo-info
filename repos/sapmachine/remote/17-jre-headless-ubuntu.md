## `sapmachine:17-jre-headless-ubuntu`

```console
$ docker pull sapmachine@sha256:9b41d78a550361961192c1d3be27d20a6e0ff1c26e3499bf12cb5c7ff4cb45c0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jre-headless-ubuntu` - linux; amd64

```console
$ docker pull sapmachine@sha256:4b3d1190472cd18e4ce185eb318eca9404d806dbe9b9d2575ed94bddd68c3f2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.6 MB (82608936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0e3b6a34c0e59a4a20a9c58f15b3317c21a42a306138cb4704ce6152f0ac265`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 07 Jun 2024 12:00:06 GMT
ARG RELEASE
# Fri, 07 Jun 2024 12:00:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 12:00:08 GMT
ADD file:5601f441718b0d192d73394b35fd07675342837ec9089ddd52dd1dc0de79630e in / 
# Fri, 07 Jun 2024 12:00:09 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:21 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jre-headless=17.0.12     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9c704ecd0c694c4cbdd85e589ac8d1fc3fd8f890b7f3731769a5b169eb495809`  
		Last Modified: Fri, 07 Jun 2024 12:11:26 GMT  
		Size: 29.7 MB (29705153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87ec5443365884feef2e12ffdb8b72df371aebadd206cdf1ee2cef7b84591a40`  
		Last Modified: Fri, 19 Jul 2024 18:00:07 GMT  
		Size: 52.9 MB (52903783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:609c43d2370d18ae65d3066cd656463ce4113ac601ee3f7a0677c640c3f5b0b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2133470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b62332643458b9bdbf1ce1a517dad9b874290766695ccc8bad0b2b0d4c69a2b`

```dockerfile
```

-	Layers:
	-	`sha256:7530b3acaa8e67eeee22ed234b60b293ff400733d334d83267b321abfb84aaa1`  
		Last Modified: Fri, 19 Jul 2024 18:00:06 GMT  
		Size: 2.1 MB (2124106 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:602fe895e275ef0d60ba85e0ca3da1d8a83fbc45211746b2783e86bc61132f4e`  
		Last Modified: Fri, 19 Jul 2024 18:00:06 GMT  
		Size: 9.4 KB (9364 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-headless-ubuntu` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:41a872ee93735621de629ef39385f982bad9bda393df1e0fa765f5bc6d1f7f89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.1 MB (81076403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:339b2ae2ba6eb53498b7fc22b0193b0fe313f16190c7cbab8fb2eb123c33d88a`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:54 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:54 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 13 May 2024 10:06:54 GMT
ADD file:9018302bda8cbdb55f2f84a40373c46413db64611139a450dbfec3fc55b8e6ea in / 
# Mon, 13 May 2024 10:06:54 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:54 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jre-headless=17.0.11     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Mon, 13 May 2024 10:06:54 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:eed1663d223832f23c8ca8fc0f9b48e2bcb0813b94a692d43b0a0a963e89d20f`  
		Last Modified: Fri, 07 Jun 2024 12:11:33 GMT  
		Size: 28.8 MB (28843043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:489a49204807361c2ffbc3cb3c2b12e0fa3a368f01886e281fbea25d39507f5d`  
		Last Modified: Wed, 26 Jun 2024 00:17:35 GMT  
		Size: 52.2 MB (52233360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:062d5a499771c1d024694310ecd70ae809620d318f88471e5324201b97a2aa4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2109853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0d1666e7d3fe0e44ea95747eb5b1f2c4c6f88ce40fd66ced5bf4039c09b4b6d`

```dockerfile
```

-	Layers:
	-	`sha256:b00e6e3c8fa530cb1a85aa577a3bbfc9509a46809091ee4b7d271e47d1fcc435`  
		Last Modified: Wed, 26 Jun 2024 00:17:33 GMT  
		Size: 2.1 MB (2100147 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:920309ec51160f70b1540878703c23f943f99106776368309012ab3c1978d7c8`  
		Last Modified: Wed, 26 Jun 2024 00:17:33 GMT  
		Size: 9.7 KB (9706 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-headless-ubuntu` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:8f249e557dc023b2eaffcbc9f8096ebb34c03699b570f963cb6962bc044865ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.8 MB (88780496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:306a9b30c4fc7f6d8fbc413b947df5067f10c2c760994fd25b688ba85d0bfe71`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:54 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:54 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 13 May 2024 10:06:54 GMT
ADD file:e767a66d1508f3628411abaff75d39ed1d6261596c668fa88252ed9a584e7fa4 in / 
# Mon, 13 May 2024 10:06:54 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:54 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jre-headless=17.0.11     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Mon, 13 May 2024 10:06:54 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:875c01bc1b3e6b966440b42d40365968bfdd742c762026b5739c5d1f493510d7`  
		Last Modified: Fri, 07 Jun 2024 12:11:45 GMT  
		Size: 34.5 MB (34506029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0afdb39c450c89764df05df70b802357f05c699800b528f56e642b046df9275e`  
		Last Modified: Wed, 26 Jun 2024 00:51:45 GMT  
		Size: 54.3 MB (54274467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:dad0a39e30c18ff55f10cf61f5ef225ec5ec64735ce3a910458f3b68aae436a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2112983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2a8b24eb8cedb1ac2ef81e3b7cd7b3e45068a419d9797d19328f2e3f07cebeb`

```dockerfile
```

-	Layers:
	-	`sha256:b681f52208028730c5deeadcbf12fb32d9de7df355e29106c6f93ee957096276`  
		Last Modified: Wed, 26 Jun 2024 00:51:43 GMT  
		Size: 2.1 MB (2103551 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a9b6d1ed2728fd087db5bced0fd65446f1905efe668720089cd19f81384be9e`  
		Last Modified: Wed, 26 Jun 2024 00:51:43 GMT  
		Size: 9.4 KB (9432 bytes)  
		MIME: application/vnd.in-toto+json
