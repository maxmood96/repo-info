## `sapmachine:17-jre-headless-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:1bee0b97642ac0ea02859d7754bd7907a97839ab3f3ab46cc6145f6aa52f0df2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jre-headless-ubuntu-jammy` - linux; amd64

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

### `sapmachine:17-jre-headless-ubuntu-jammy` - unknown; unknown

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

### `sapmachine:17-jre-headless-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:02c2f80f81ae40d082a70c0044c255fa6cd5abfd6b01d836a2c7f1083d7c8807
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.5 MB (79475946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f701fc842bc42abe40a4610ff0b73357ad57cdcd57b89e32e85505c36c777c68`
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
# Tue, 21 Oct 2025 21:30:22 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre-headless=17.0.17 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 21 Oct 2025 21:30:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 21 Oct 2025 21:30:22 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ddd1286b773ac266966e16756e954d6da4b2f9aaf39626d05af66f3d17ae5b2`  
		Last Modified: Wed, 22 Oct 2025 00:06:54 GMT  
		Size: 52.1 MB (52092839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:200cad9bcb8d5b70860a261312024d825d7c73ad7823eb06534cadc9f7a86f92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0fa9e688aaaf76e0ad2f074a44fa0f835a81dd2bb9bfe30121fa8abb761b45b`

```dockerfile
```

-	Layers:
	-	`sha256:ae34dc90580072f16ef54d32e1fa8f84d378cc689e6ea3f6dd655a0702d06735`  
		Last Modified: Wed, 22 Oct 2025 03:05:27 GMT  
		Size: 2.3 MB (2292531 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05dd6b2588d8d395d0d86f678d1a6b337f42ac94c4a9a35e409f29371696d676`  
		Last Modified: Wed, 22 Oct 2025 03:05:28 GMT  
		Size: 9.0 KB (9032 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-headless-ubuntu-jammy` - linux; ppc64le

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

### `sapmachine:17-jre-headless-ubuntu-jammy` - unknown; unknown

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
