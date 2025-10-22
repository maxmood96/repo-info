## `sapmachine:21-jre-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:e0b29c85896d4a04ed0f264da0c2547e2480e33c61124e3f997363bcc163e99a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:21-jre-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:a1783e6b73de8bd7117e5c30dcfebbdf513d18436bd778833451629928e7089c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.4 MB (89384640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:931d3645fd9efb834e57c43dc0f6170e76bb18639a2578781507b9fac8a4b8ad`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Oct 2025 07:05:07 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:05:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:05:09 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Wed, 01 Oct 2025 07:05:10 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 21:30:29 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.9 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 21 Oct 2025 21:30:29 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 21 Oct 2025 21:30:29 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9096e1d9be48944edaaa305d20931d923c1ab102384580a13adae3f55e2b72e4`  
		Last Modified: Wed, 22 Oct 2025 02:43:29 GMT  
		Size: 59.8 MB (59847822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:2ded0b9138d48f5756170bbcc5ef56dbed89a67b616cfea691700f9ba4d06fd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2553701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a266dc93a35827241836215f340c16f4c3999568d1f95ffb72a4ef4cf4482808`

```dockerfile
```

-	Layers:
	-	`sha256:f57026b8fd72395313d7737fe0f1f9c58a57c9c750265af354de4d7de66ef4eb`  
		Last Modified: Wed, 22 Oct 2025 06:11:08 GMT  
		Size: 2.5 MB (2544889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e73875391cfd222e4b16310a22d7bb2d4a4efe93ae5926547554735897c5f69`  
		Last Modified: Wed, 22 Oct 2025 06:11:08 GMT  
		Size: 8.8 KB (8812 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:9077c2a7a8c31a2bddd168972a9be0602b1e766a5bdefd0cd2976b0ee383c2fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.4 MB (86368198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b1096d7cb4009ae2c6851d4e724c53f9482508a5250b640208f92ce3358a086`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Oct 2025 07:16:10 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:16:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:16:12 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Wed, 01 Oct 2025 07:16:12 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 21:30:29 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.9 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 21 Oct 2025 21:30:29 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 21 Oct 2025 21:30:29 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11e2af85226c385ec50ee39bcf88133233fd3ac87ad6cbc27ea678763e1b83b6`  
		Last Modified: Wed, 22 Oct 2025 00:06:20 GMT  
		Size: 59.0 MB (58985091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:b5950d5110e4579bde1ccf8428ca7c64939d561d0c9eaf57e61a6de505264b42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2553487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab003ecc787f7dc3be2b5ff2bebe55863a32ba57c3622eb987d532cb6059830f`

```dockerfile
```

-	Layers:
	-	`sha256:e8f51a1a57560f4ee7182c71ac7cd77a8fbaa72c1d0f7589eef10896151a85de`  
		Last Modified: Wed, 22 Oct 2025 03:08:18 GMT  
		Size: 2.5 MB (2544571 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6224927efd46f7e5c36a3260b21ee8d717f6e010fe081f39af683f859e15a88`  
		Last Modified: Wed, 22 Oct 2025 03:08:19 GMT  
		Size: 8.9 KB (8916 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre-ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:9d12910c2697a05bd33b499aeaca05677fa25409dea95e6e14220ddc88eb814e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.4 MB (95408707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d0d3301063fcd3b86044a7eb333c4743c43d2842a3909dec00d4efb21513cf1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Oct 2025 07:06:37 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:06:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:06:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:06:38 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:06:42 GMT
ADD file:0aa9da71877b87fa24e5611ae918040b9e86da1da320091962f21431bce21835 in / 
# Wed, 01 Oct 2025 07:06:43 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 21:30:29 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.9 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 21 Oct 2025 21:30:29 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 21 Oct 2025 21:30:29 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:2fbe0139d4362c4f9e73d9ece05926b347d08fa0942b6a7a53617f13f42d1f91`  
		Last Modified: Thu, 02 Oct 2025 00:24:59 GMT  
		Size: 34.4 MB (34446789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dd4232fb460c9a1645644b37cf3d2c15a5e982e97e5b26bfa1c6911111304a3`  
		Last Modified: Wed, 22 Oct 2025 11:59:46 GMT  
		Size: 61.0 MB (60961918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:41e7db929d40c1af808749a5bbdd740eaeab13b30e969c1ea72c235c0aa8a630
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2551859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aeb5f0c9d2b1532966c9a81c4ca325108fc7c26872553d2f98d61ddf93c31819`

```dockerfile
```

-	Layers:
	-	`sha256:e41277f8316ec07b1144da6f4f17208dfd59712d7f660f1c4af64c49963a8f35`  
		Last Modified: Wed, 22 Oct 2025 15:08:27 GMT  
		Size: 2.5 MB (2543004 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ffed7cfdc8214db27f990ea297e3b0555d5ed5bf7d328a8140f554b8e945cd2c`  
		Last Modified: Wed, 22 Oct 2025 15:08:28 GMT  
		Size: 8.9 KB (8855 bytes)  
		MIME: application/vnd.in-toto+json
