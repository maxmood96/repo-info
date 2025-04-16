## `sapmachine:17-jre-ubuntu-20.04`

```console
$ docker pull sapmachine@sha256:52881684928278ba2d0b04180522937a04eedc425f369b99a716beeaa55e6488
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
$ docker pull sapmachine@sha256:7b36be1766dd330bedfa4982866207f20d8b5fd0da38ca36fb02255d3fdd330b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.9 MB (80880483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44ef8f6d744f03c52e794942e273401be13b10c683da92fc0195fe8cab610b58`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 08 Apr 2025 10:42:46 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:42:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:42:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:42:46 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 08 Apr 2025 10:42:48 GMT
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
# Tue, 08 Apr 2025 10:42:48 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:41 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.15 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 16 Apr 2025 10:34:41 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Tue, 08 Apr 2025 11:48:23 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:967e27c71ecb890ca3be55455ba8360fefac0fee560cd6338533b473ad5e559d`  
		Last Modified: Wed, 16 Apr 2025 16:14:18 GMT  
		Size: 53.4 MB (53370089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:445e0a40d80b2ce3ee72ed2a91201b0661d6275262bee691c9b028ce2fcbc8ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2308123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f847cb9d09bbc7bed5c0c7dc26491d58f38af096c7c393fb494aca772cf9525`

```dockerfile
```

-	Layers:
	-	`sha256:346c2cd3e353f41c1a392b2b38444e60395c5257e22d3270c5e88dfedab03b66`  
		Last Modified: Wed, 16 Apr 2025 16:14:16 GMT  
		Size: 2.3 MB (2299303 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a47ee2d9c8379c821dcf32f79e040a7f5399fcbe7591f39965d37970b24b271`  
		Last Modified: Wed, 16 Apr 2025 16:14:16 GMT  
		Size: 8.8 KB (8820 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-ubuntu-20.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:b1db1914354a068d7d1f930d58ebce083a645e454f999317418c3aad4062491b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.8 MB (78779323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf9592121ca04fc9144b2627c3c069146950c349d50307e7504f4871f9c65867`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 08 Apr 2025 10:46:43 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:46:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:46:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:46:43 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 08 Apr 2025 10:46:45 GMT
ADD file:2c90d89e4dd4e1d2473deca816f585a78ced2a0c5c799399810f86fdbb17ac7e in / 
# Tue, 08 Apr 2025 10:46:45 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:41 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.15 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 16 Apr 2025 10:34:41 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ecd83b6c354452b6a9979c7666bba16927f1e60e2afbfe6401dd6f87d5db8576`  
		Last Modified: Tue, 08 Apr 2025 11:48:29 GMT  
		Size: 26.0 MB (25977661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:949cabec6f2f2096f515c0dc3cc0b9308f185cd5e613553f7700a24996c1e8d0`  
		Last Modified: Wed, 16 Apr 2025 16:45:52 GMT  
		Size: 52.8 MB (52801662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:22b4f845b752a255a19f908b3514724d7a4ee7b6c39ee2739e8bc429c0ccb20e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2307866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c7495574851ce615faab45a49b031fd833e2eb47cf61144b56f92746395715f`

```dockerfile
```

-	Layers:
	-	`sha256:59e5b06ed57c8215a4e4ef13a59059778c9c744a8e8f9b728aee8fe5f0615a5f`  
		Last Modified: Wed, 16 Apr 2025 16:45:50 GMT  
		Size: 2.3 MB (2298941 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1dcea589d6449d99454bcfd6194eb99a73534ac773a02c7cbd0f33a99d49e2a7`  
		Last Modified: Wed, 16 Apr 2025 16:45:50 GMT  
		Size: 8.9 KB (8925 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-ubuntu-20.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:35cce1cd5f974a42f04088c71e794db57b0a8a73e41d6244a743be9d74f769f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.6 MB (86568866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e1a2582d4995fd45860401d83fcc111932e8da383c0ed619723e6c1835f7055`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 27 Jan 2025 13:39:16 GMT
ARG RELEASE
# Mon, 27 Jan 2025 13:39:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 13:39:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 13:39:16 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 27 Jan 2025 13:39:16 GMT
ADD file:d85970cec61787609e3854cb76ce16d54fe420b254cf48fc9ed9ed678717ff28 in / 
# Mon, 27 Jan 2025 13:39:16 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:16 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.14 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Mon, 27 Jan 2025 13:39:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:92d54367a68b4f03400315732acb4290d88bb06f8fe1414fd823f93402bec922`  
		Last Modified: Tue, 08 Apr 2025 11:48:44 GMT  
		Size: 32.1 MB (32076946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:447f9667ab1a5e764472e603d65ef06224080c91bf812ef9913f17b43059a49f`  
		Last Modified: Wed, 09 Apr 2025 07:26:54 GMT  
		Size: 54.5 MB (54491920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:490fc60192195c515455667c57b8d4cec7da6e2197c5c0ee3cf332dd52b340b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2311935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b28410025674bc965bb1ec1b7056355346675ed63cf3a2f66b56863aceb39104`

```dockerfile
```

-	Layers:
	-	`sha256:4a362123ce800f80781abc7f62db1996df137e1f288ebf66d7163bd9b12d0872`  
		Last Modified: Wed, 09 Apr 2025 07:26:53 GMT  
		Size: 2.3 MB (2303070 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69d6a5efda1e96fee0775a00a3193998d2446ba2be3da5e8e1786839bd8f8a1f`  
		Last Modified: Wed, 09 Apr 2025 07:26:52 GMT  
		Size: 8.9 KB (8865 bytes)  
		MIME: application/vnd.in-toto+json
