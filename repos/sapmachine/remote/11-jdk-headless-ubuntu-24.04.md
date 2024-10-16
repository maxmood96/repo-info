## `sapmachine:11-jdk-headless-ubuntu-24.04`

```console
$ docker pull sapmachine@sha256:b2dd8bb46701d90d800d82f76aa4d76b5e6649d1791c7b4e8536e4adba7736fd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:11-jdk-headless-ubuntu-24.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:bcd45b56d678a18dc57c7e0106efccc7e9792874ebf6b34f231a4c01eff16b4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.8 MB (229793152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edbff0fa1b13a272b876ce04ceb1ee2e891cf515f5d7684a993dc1d863290609`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 11 Oct 2024 03:48:01 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:48:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:48:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:48:01 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 11 Oct 2024 03:48:03 GMT
ADD file:34dc4f3ab7a694ecde47ff7a610be18591834c45f1d7251813267798412604e5 in / 
# Fri, 11 Oct 2024 03:48:04 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 12:49:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk-headless=11.0.25     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Wed, 16 Oct 2024 12:49:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ff65ddf9395be21bfe1f320b7705e539ee44c1053034f801b1a3cbbf2d0f4056`  
		Last Modified: Fri, 11 Oct 2024 05:07:18 GMT  
		Size: 29.8 MB (29750363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bc790c87a3afaa0d70792bbc62c9c8870d1f7f570f4d678812a3b1d1997d6a5`  
		Last Modified: Wed, 16 Oct 2024 18:59:50 GMT  
		Size: 200.0 MB (200042789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jdk-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:a74e7d69ec9c05b40e70f62a46742355d8dbccd2d3216d5337a3bd1c558cb6f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2238961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec1807f4e4aa14b47a62866678ffdddbf13523e1aaf45d87bcdcafdc645b3617`

```dockerfile
```

-	Layers:
	-	`sha256:9c9d85837f8dc4c49cd26cea92bbd1a4aedda4d2a8e0a0df7a5de221767476f5`  
		Last Modified: Wed, 16 Oct 2024 18:59:48 GMT  
		Size: 2.2 MB (2229558 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66e41ffaf19a554c9e3c5f6564726074d5759ba6771564f80fc844b79f5da7f6`  
		Last Modified: Wed, 16 Oct 2024 18:59:48 GMT  
		Size: 9.4 KB (9403 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-jdk-headless-ubuntu-24.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:cbdb3e8f666cb70adc55f4274ba5ef50f0f1b2d6e58b90cfe395e9772289779a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.4 MB (227427319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecdb9c444fccd54deabb50f99f102e0e3e0d072d0080e188f72e781f9b57d39a`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 11 Oct 2024 03:52:53 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:52:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:52:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:52:53 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 11 Oct 2024 03:52:55 GMT
ADD file:b14427a5ec8028ba993a0ff27f9e398456229f9113c9c39f3cc7a0f96c15943b in / 
# Fri, 11 Oct 2024 03:52:55 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 12:49:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk-headless=11.0.25     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Wed, 16 Oct 2024 12:49:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1f630473117188fe348ebdcf0da5e93138275af14007f15baf79967a365e647a`  
		Last Modified: Fri, 11 Oct 2024 05:07:24 GMT  
		Size: 28.9 MB (28885845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9442ee04ff80b887fe8ca2bd786fafd58aba556dcb8e56fda02e3fe7135d9ef8`  
		Last Modified: Wed, 16 Oct 2024 19:43:21 GMT  
		Size: 198.5 MB (198541474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jdk-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:1ed419e4d44513d5f76a84438aba0069c28a25b5134607c7432716f10bc5c15c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2240193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0744f9e66d4a27a037c450e3af4597ad07440855a5ae259177d2c6d36ed34596`

```dockerfile
```

-	Layers:
	-	`sha256:870e153137874e73414321e7226f9286610147e4304a2f51a98c119896ad28db`  
		Last Modified: Wed, 16 Oct 2024 19:43:16 GMT  
		Size: 2.2 MB (2230668 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe7863a89668a0da0c5ace88627934021c60386d551932c5ad3362056365482d`  
		Last Modified: Wed, 16 Oct 2024 19:43:16 GMT  
		Size: 9.5 KB (9525 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-jdk-headless-ubuntu-24.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:f7559b651b818d843b1a7641fb968ef5c9ddb78bc858d99c80f13d565afc6581
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.9 MB (220907767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62abf298d57c3991d1a74502e07cb5c70593c839d337c610b8380579d9f9d38a`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:19 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 18 Jul 2024 15:16:19 GMT
ADD file:536f7d2a284525103973196c539c45f59251ee1d6bbd34f1d92ff9d6187da127 in / 
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:19 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk-headless=11.0.24     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5f3161c1c329da2d67fc0650c9fd31e151f03956f8a0cb901012dc9bf6029cbc`  
		Last Modified: Fri, 11 Oct 2024 05:07:35 GMT  
		Size: 34.4 MB (34388969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d32c6f321a6aed82b34ea5887a7f3c9d53a12bd1c0f08880acb935441713c84`  
		Last Modified: Wed, 16 Oct 2024 06:10:58 GMT  
		Size: 186.5 MB (186518798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jdk-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:32028e653789c1f604cdfad3dce3e844d7ced7af6ea6e3f3a0e8a581433e895e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2239054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a75e63bf0439013d0f420a421d5f63161313c4b150586e67f677e2c244100da1`

```dockerfile
```

-	Layers:
	-	`sha256:8fba7510921f855925d809e56c6a752f5c93ee1248ceab46a1a9e892e8cb1cad`  
		Last Modified: Wed, 16 Oct 2024 06:10:53 GMT  
		Size: 2.2 MB (2229602 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5399d709164f648b209ed6eefac99539b1dab0f446888ba3da824150d1aa030`  
		Last Modified: Wed, 16 Oct 2024 06:10:53 GMT  
		Size: 9.5 KB (9452 bytes)  
		MIME: application/vnd.in-toto+json
