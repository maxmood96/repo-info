## `sapmachine:17-jre-headless-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:43b6e43ecfb7c0e9f306842222e6754f8a960c333ea8334b8174b5b696a6bc5e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jre-headless-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:22cde27c41c3f01f3b01214437ac53b1528afbf750e67c51bc7980c12ba03ab6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.2 MB (82180612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ba992abfb93547fbb0a31792248369da78b376b1d581e409f26899274c9fc57`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 06:09:35 GMT
ARG RELEASE
# Mon, 11 Aug 2025 06:09:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 11 Aug 2025 06:09:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 11 Aug 2025 06:09:35 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 11 Aug 2025 06:09:35 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Mon, 11 Aug 2025 06:09:35 GMT
CMD ["/bin/bash"]
# Mon, 11 Aug 2025 06:09:35 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre-headless=17.0.16 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 11 Aug 2025 06:09:35 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Mon, 11 Aug 2025 06:09:35 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bd5879171323cc4953cd3f76f246e1e7ec231edfcfadb392b772ac8637e2e7d`  
		Last Modified: Thu, 02 Oct 2025 05:20:24 GMT  
		Size: 52.6 MB (52643794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:e6df4e64168d581e904dfcc2e45f43389464893eaf916ab5ab863555cd7aac6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37954eeedb03bb8726b4f2a6174f98f0a36bdf984619670b768a466d9cb52fe3`

```dockerfile
```

-	Layers:
	-	`sha256:9b65f1762c31e2004b675afa12061e463368ea0ad99ee66c164369f5cd22ee9d`  
		Last Modified: Thu, 02 Oct 2025 09:07:12 GMT  
		Size: 2.3 MB (2292859 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c36c4baa87ceb96b6e172920baf8be72dbfbafe263e67696fd0855c5b82a8be8`  
		Last Modified: Thu, 02 Oct 2025 09:07:13 GMT  
		Size: 8.9 KB (8928 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-headless-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:77075cfa3a17d535fbcdbeabf34d2e4521312ccd8080596531e993ac5f49cdb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.4 MB (79411423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33c1c675ae76a22f7315e1ab1d1634b0013dc4e006d91388174619fed33bc021`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 06:09:35 GMT
ARG RELEASE
# Mon, 11 Aug 2025 06:09:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 11 Aug 2025 06:09:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 11 Aug 2025 06:09:35 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 11 Aug 2025 06:09:35 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Mon, 11 Aug 2025 06:09:35 GMT
CMD ["/bin/bash"]
# Mon, 11 Aug 2025 06:09:35 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre-headless=17.0.16 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 11 Aug 2025 06:09:35 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Mon, 11 Aug 2025 06:09:35 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c5fa832160988ae48581c9257490ae880747b76642d14b02d6326e7e0724327`  
		Last Modified: Thu, 02 Oct 2025 01:35:27 GMT  
		Size: 52.0 MB (52028316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:e6d31c4cccbe77648429ad4901e182eff4aeac75517ac3590487dc163c3b1970
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac54a707df62e480685cb24a51d29ad3a30c883cfd12061ba981d913983bef35`

```dockerfile
```

-	Layers:
	-	`sha256:655f14ddb7cbedba5ce6d42213060d8b3c07b3d1c82f78cef78611b0c805982c`  
		Last Modified: Thu, 02 Oct 2025 03:05:29 GMT  
		Size: 2.3 MB (2292531 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:502135e540c44a9fa801f3719f0337679d7c431b8c601769832191d1a5b3d748`  
		Last Modified: Thu, 02 Oct 2025 03:05:30 GMT  
		Size: 9.0 KB (9032 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-headless-ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:6dbcade0cd6d428c1140ec91504ac9b9fc5acc5dbb237c471180ce70712677c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.0 MB (88010029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28d0336fbfc1f2de74e131f212dfab559aec410b38cedc64cb032bf6c8ca3bb2`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 06:09:35 GMT
ARG RELEASE
# Mon, 11 Aug 2025 06:09:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 11 Aug 2025 06:09:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 11 Aug 2025 06:09:35 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 11 Aug 2025 06:09:35 GMT
ADD file:0aa9da71877b87fa24e5611ae918040b9e86da1da320091962f21431bce21835 in / 
# Mon, 11 Aug 2025 06:09:35 GMT
CMD ["/bin/bash"]
# Mon, 11 Aug 2025 06:09:35 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre-headless=17.0.16 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 11 Aug 2025 06:09:35 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Mon, 11 Aug 2025 06:09:35 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:2fbe0139d4362c4f9e73d9ece05926b347d08fa0942b6a7a53617f13f42d1f91`  
		Last Modified: Thu, 02 Oct 2025 00:24:59 GMT  
		Size: 34.4 MB (34446789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77f94a6bf686f5abd256a16f9fe2f6d98acc23793fbee18fde71dda2b62eeebe`  
		Last Modified: Thu, 02 Oct 2025 04:54:58 GMT  
		Size: 53.6 MB (53563240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:4663547cfe8284f4c16d00f73ed925be0621a875faa4b97f8c0e78f3b61e59d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2299856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b74d5019379fc3748b0caf1e7857673c7c532ace118a312f572e777cbe711b79`

```dockerfile
```

-	Layers:
	-	`sha256:423acdd12e0c444f763d6baf95fafa020eb216d2706f432a320afa0873a79583`  
		Last Modified: Thu, 02 Oct 2025 06:05:37 GMT  
		Size: 2.3 MB (2290884 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9808450d256cbcbb8a34d046fe3a2c5c028a508718c7a918d893ec3623a63a94`  
		Last Modified: Thu, 02 Oct 2025 06:05:37 GMT  
		Size: 9.0 KB (8972 bytes)  
		MIME: application/vnd.in-toto+json
