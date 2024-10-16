## `sapmachine:17-jre-ubuntu-20.04`

```console
$ docker pull sapmachine@sha256:c0c4c532ee104fffc6922f37727e0ec407233f8bc4462098b4e2bb51d8d24c8b
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
		Last Modified: Wed, 16 Oct 2024 18:59:51 GMT  
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
		Last Modified: Wed, 16 Oct 2024 18:59:50 GMT  
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
$ docker pull sapmachine@sha256:61a46c16e1d998a22bea649a4d9de33acf4e3a6c741229af5c7fb41f346eeb1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.4 MB (86438720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:207b1a3e0c4fbae132fd8c0a480e8c5ec61036ecd40ea5923ecfc7cf6cd5b4f5`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:21 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 18 Jul 2024 15:16:21 GMT
ADD file:869a92a1e06a4985a0281417502ee0c0d8ba6cc4e0b72062dd8e4eb87833bae7 in / 
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:21 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.12     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cd720328ce8da41e08a7dd5922261b0c1980c2565df21b810488c55260400f68`  
		Last Modified: Fri, 11 Oct 2024 04:41:42 GMT  
		Size: 32.1 MB (32076506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cecaacf742458a4638fab7e9c327f150a969e92925b9a33073bc02c6f5259a96`  
		Last Modified: Wed, 16 Oct 2024 03:06:52 GMT  
		Size: 54.4 MB (54362214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:ce491151b12ade61915198c46bfc17d5a268c95806ae68f7f4aacc626d4eafd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2292062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34f6bb3b60cf8593850f78c3568032d2ad79e742606c9fbe19f11b311e5f515e`

```dockerfile
```

-	Layers:
	-	`sha256:adae2ea448cbf277bd79b6055cf23f8f03104f072f3b117dd102ffa5b2428e0c`  
		Last Modified: Wed, 16 Oct 2024 03:06:50 GMT  
		Size: 2.3 MB (2283419 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ffa7e2008616fd0025f6e1284a192314c27d08440c8168fb6b078148ca382242`  
		Last Modified: Wed, 16 Oct 2024 03:06:50 GMT  
		Size: 8.6 KB (8643 bytes)  
		MIME: application/vnd.in-toto+json
