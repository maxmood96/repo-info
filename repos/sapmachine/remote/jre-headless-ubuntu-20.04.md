## `sapmachine:jre-headless-ubuntu-20.04`

```console
$ docker pull sapmachine@sha256:8e64fe1b8f30ef99fe17c8350462017e0d40f5bed106f83f3e70825db7ce8f46
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:jre-headless-ubuntu-20.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:d87ec9a5701991ee974c8e9a919f8eeabdff8f45ce8b989c2f3d5608ae0be10d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.6 MB (85622677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b71a9527413d07c227255715e41523aca786e117151e066ada76262ab7661b9`
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
# Mon, 27 Jan 2025 13:39:22 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-23-jre-headless=23.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Mon, 27 Jan 2025 13:39:22 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc5e97eaca472d398242b04c539d896e551248ac52d04bfbfd9a16144884f2b8`  
		Last Modified: Tue, 28 Jan 2025 01:29:59 GMT  
		Size: 58.1 MB (58111617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-headless-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:bde801831288ea0d8b5f3d5cee795d518606b3ad330fc1d5f627cb75b991dfa2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2074187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15a19eb97a79965eeecd78da8e7c5328bf8b30015e5ddc62b529c6fc4a4b83dc`

```dockerfile
```

-	Layers:
	-	`sha256:d437d8526e0c4a6af9a3240510d7ad698cc84ef4cfbe88ff6072cee0929be645`  
		Last Modified: Tue, 28 Jan 2025 01:29:57 GMT  
		Size: 2.1 MB (2064576 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a89042b22a6c6483e3721a37795e9a5b5bc4b54bdc798af7ba75dcebe27f014e`  
		Last Modified: Tue, 28 Jan 2025 01:29:57 GMT  
		Size: 9.6 KB (9611 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jre-headless-ubuntu-20.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:6371d80361a13d1a6d2f9724dcca67d5261a7477ad25667f09b1d2c01e22a7c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.2 MB (83162222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42226817ce8a8460940ef4b84541ee9a4042f057d7de19c617249802ce535d83`
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
# Mon, 27 Jan 2025 13:39:22 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-23-jre-headless=23.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Mon, 27 Jan 2025 13:39:22 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99bcb28d9d122cbb883693f66fcb1cafc1bfe0d236160e043764605ac129e02f`  
		Last Modified: Tue, 28 Jan 2025 02:34:20 GMT  
		Size: 57.2 MB (57188394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-headless-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:6ccdc80c1bf537d04bf31b2219cdaa173bcd89e9e6eb30f0c83b4813090edec7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2073338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0843180b1de5bb0a9a655cb4f57dd3c5b5199adaabfdeff4b928ce6bffabcd7`

```dockerfile
```

-	Layers:
	-	`sha256:1e200dd745fa5fc20df4ecb4d8240f525c58c2a872cb2f2e056e78b4eff4c8f5`  
		Last Modified: Tue, 28 Jan 2025 02:34:18 GMT  
		Size: 2.1 MB (2063599 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81f19943dac1612d010ba73ba855d831c72c5721a0d260cfdc4c2565d58b91f7`  
		Last Modified: Tue, 28 Jan 2025 02:34:18 GMT  
		Size: 9.7 KB (9739 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jre-headless-ubuntu-20.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:d5bdcbbec0509bff09cdd2d1b9c27129ea8e813ad41d15a30acacf3d6b857ca7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.1 MB (91104575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a77788654b27890765ac360c969a07eb8a61f3ad04b8c003fce9c915e02474e8`
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
# Mon, 27 Jan 2025 13:39:22 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-23-jre-headless=23.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Mon, 27 Jan 2025 13:39:22 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cd720328ce8da41e08a7dd5922261b0c1980c2565df21b810488c55260400f68`  
		Last Modified: Fri, 11 Oct 2024 04:41:42 GMT  
		Size: 32.1 MB (32076506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9ed39e05322022bb478ec5e6370457164af77d954d9f83c1babf16709b4c729`  
		Last Modified: Tue, 28 Jan 2025 05:40:38 GMT  
		Size: 59.0 MB (59028069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-headless-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:9890bf57f0fa92585c3b27f67030e21fa08f6b5e60726c8c0efb4afdeacbc174
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2077328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72b3b6083509fa98f1c205fb7db57839ecf12847d7de490dc0574d960339eac8`

```dockerfile
```

-	Layers:
	-	`sha256:147489344dd09a3c6ba3f335d10f06d64bb5e548790ec4e3ec8a066b9fd84935`  
		Last Modified: Tue, 28 Jan 2025 05:40:36 GMT  
		Size: 2.1 MB (2067662 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5b95f0ebe4049c8d44428052a4c2d6d6dfb147db081b51bb82e23d4492f530f`  
		Last Modified: Tue, 28 Jan 2025 05:40:36 GMT  
		Size: 9.7 KB (9666 bytes)  
		MIME: application/vnd.in-toto+json
