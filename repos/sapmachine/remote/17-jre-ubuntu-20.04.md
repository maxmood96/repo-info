## `sapmachine:17-jre-ubuntu-20.04`

```console
$ docker pull sapmachine@sha256:48f42f4b3a75ead3c6a6019f9b14e14e2dea2b81ea361089c09d606619714606
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jre-ubuntu-20.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:c9c4e9e13a22a69cc0cb84cc9a7d44fdb144039ea6548f6371914945eb7847fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.8 MB (80797556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a356e20c3d36599e031f208bca4549b0d40e687b1e4a303ce36b8dd8973417a9`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:25 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:27 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Fri, 11 Oct 2024 03:38:27 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 12:49:12 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.13     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:12 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 16 Oct 2024 12:49:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f34837219c0ad18973172b8a65022a31b865a52487c1884dab9020938b0addcf`  
		Size: 53.3 MB (53286496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:6a2c83ab331ba813efb3b64a2d6dcacd58f9fcb00c2de4bdfc605eec334c97b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2294905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24ab9a38242866656f8252f7f6ff776608c9d13df3d24dbd49ca5529f2afade5`

```dockerfile
```

-	Layers:
	-	`sha256:aae9de2383d3d67d8ff44aaabbb6b8f2cb97439536b8385b6e9c9a198c20366c`  
		Size: 2.3 MB (2286300 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1f6a597cc8d5e1d2d923e9324c38c1db5ea244d7825e3d0d5d420b415c0aa7b`  
		Last Modified: Wed, 16 Oct 2024 18:59:50 GMT  
		Size: 8.6 KB (8605 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-ubuntu-20.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:87f71abaa53b97420d9e1b588de333a1b3390791cd11075bba105b3162bd446b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.7 MB (78673500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:810e08e22e79730eea4a52387e1dda5fca1b77335c1dcd1bf41b3f3a4f70678d`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 11 Oct 2024 03:39:45 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:39:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:39:47 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Fri, 11 Oct 2024 03:39:47 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 12:49:12 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.13     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:12 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 16 Oct 2024 12:49:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21a7af18ef69eaedc076aa10ab67484588fcab220d9b0669257a2c254b4f3369`  
		Last Modified: Wed, 16 Oct 2024 19:39:49 GMT  
		Size: 52.7 MB (52699672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:efe37b646781b51210980d4292c3c0be6c5a331acc165f7c8f9b9dabe326e4f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2294639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b7db3e3d15ab67ce1b07d10b26fa2452b32b12108b6ad01af118b12a3ba1e6c`

```dockerfile
```

-	Layers:
	-	`sha256:13c57195962102bfb80084e0c0219341706935f7ff7684b067bccee8b9440ebe`  
		Last Modified: Wed, 16 Oct 2024 19:39:48 GMT  
		Size: 2.3 MB (2285936 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75dd6c3cd8db58f62f82c07981187ba7cf1333552a9c50feb27e54b156fdc92d`  
		Last Modified: Wed, 16 Oct 2024 19:39:47 GMT  
		Size: 8.7 KB (8703 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-ubuntu-20.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:1adb3379f3f926d35e4db15102623ec9337a7fc8a68e5ab1d3393ba0ef5ed064
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.5 MB (86484403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17bd80c7f67be66a79b55d5480c7ba0c2e1201b56fc23cf04e58f7b4b4bb2768`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:35 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:35 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:38 GMT
ADD file:869a92a1e06a4985a0281417502ee0c0d8ba6cc4e0b72062dd8e4eb87833bae7 in / 
# Fri, 11 Oct 2024 03:38:39 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 12:49:12 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.13     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:12 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 16 Oct 2024 12:49:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cd720328ce8da41e08a7dd5922261b0c1980c2565df21b810488c55260400f68`  
		Last Modified: Fri, 11 Oct 2024 04:41:42 GMT  
		Size: 32.1 MB (32076506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ae4278278ae06d408c569f415b65dcd36cd10c9758fb8e907b7feccc190f69f`  
		Size: 54.4 MB (54407897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:5514e41f1f15349bd9453606e88e3c400711abfec4dd9a6b1a2dc383872dc00b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2298708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2797b5562d1cb89fe3d706ba94aefd6dd2dfb72d3d23756de301ec69b022a59c`

```dockerfile
```

-	Layers:
	-	`sha256:e798a8c2c079991adabc8e729c17e4d3a82d45fe1d731b1c94cabce9a0a6f2fb`  
		Last Modified: Wed, 16 Oct 2024 20:09:26 GMT  
		Size: 2.3 MB (2290065 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:963e8ae406ca9e190956fba5d5e756ca17aa7625ef3d0a3addb2696a9b643a2b`  
		Last Modified: Wed, 16 Oct 2024 20:09:25 GMT  
		Size: 8.6 KB (8643 bytes)  
		MIME: application/vnd.in-toto+json
