## `sapmachine:lts-jdk-ubuntu-focal`

```console
$ docker pull sapmachine@sha256:dfaa9f1f7cc8ba4ccc336a9db52d019145f92e45a43e037058c7e04e2a07c9fc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:lts-jdk-ubuntu-focal` - linux; amd64

```console
$ docker pull sapmachine@sha256:d7647ddff383832454adf38a77637352e6e0660bf6200b27832e173350576bca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.7 MB (241702722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f698c0927171d54efaeeadcc96a53a291181f192bfabb8d260ef0bcc02d0a8ec`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 27 Jan 2025 13:39:13 GMT
ARG RELEASE
# Mon, 27 Jan 2025 13:39:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 13:39:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 13:39:13 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 27 Jan 2025 13:39:13 GMT
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
# Mon, 27 Jan 2025 13:39:13 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:13 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.6 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 27 Jan 2025 13:39:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Tue, 08 Apr 2025 11:48:23 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36b100105d524c6526c159b7ebb497f9559d1f6d751ec9418fbd01473b9415ef`  
		Last Modified: Wed, 09 Apr 2025 01:21:54 GMT  
		Size: 214.2 MB (214192328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jdk-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:7dd7b2988137d1e342f2fe47b253b9120257ac36599fd1c4072bbb7241de3892
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2398151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:585a29b051c9dfddd3075d44767ad011a870720eb20768c17afd0f196e50533f`

```dockerfile
```

-	Layers:
	-	`sha256:138ba6362d817ca62330ac1dda9a7625db6d24e150452548cc54a5f344c7d91a`  
		Last Modified: Wed, 09 Apr 2025 01:21:48 GMT  
		Size: 2.4 MB (2386706 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:794b0fbe1252389e4aaae2114e9e8eabc7d5d7fba9596db5da7aae9762bfe47e`  
		Last Modified: Wed, 09 Apr 2025 01:21:48 GMT  
		Size: 11.4 KB (11445 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jdk-ubuntu-focal` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:48799e3d63d475fc32fedf9068876f68de3039ca15b16193089d86726dadf2f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.4 MB (238392769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4155e6ef41c59df114cd3126a9d3dae3964af3856dc7bbae61691456593a3454`
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
# Mon, 27 Jan 2025 13:39:13 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.6 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 27 Jan 2025 13:39:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afa15cedb648ba9ff9bd197fe8bd3f6d2860e2566b5f53b33836ffc5d2d043c1`  
		Last Modified: Tue, 28 Jan 2025 02:43:40 GMT  
		Size: 212.4 MB (212418941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jdk-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:2c6477b3ce0b5f45bacca92922f825692a369a02f05549615bee4d4efa42805a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2397985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37443395919020841106bc99a78296c85bba6bc332a5689dd046e9229f65d71c`

```dockerfile
```

-	Layers:
	-	`sha256:9391d92f11a9c0e611707a9c49a87945a1ef9f95389d30cc57f63c5dba2a66e8`  
		Last Modified: Tue, 28 Jan 2025 02:43:35 GMT  
		Size: 2.4 MB (2386340 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a81db8895caa1756605ed5e5ec369ce160c81659b93f98608843679e10425747`  
		Last Modified: Tue, 28 Jan 2025 02:43:35 GMT  
		Size: 11.6 KB (11645 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jdk-ubuntu-focal` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:aefaaf89b05e25de6f65eb4365ed0a58542bcd98ffe7f276b302e70fb4ff5f15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.2 MB (247184002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66101f2037e5d3645f912202467ca97a029688313b2f9e9cc8dbd2cc54216072`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 27 Jan 2025 13:39:13 GMT
ARG RELEASE
# Mon, 27 Jan 2025 13:39:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 13:39:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 13:39:13 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 27 Jan 2025 13:39:13 GMT
ADD file:d85970cec61787609e3854cb76ce16d54fe420b254cf48fc9ed9ed678717ff28 in / 
# Mon, 27 Jan 2025 13:39:13 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:13 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.6 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 27 Jan 2025 13:39:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:92d54367a68b4f03400315732acb4290d88bb06f8fe1414fd823f93402bec922`  
		Last Modified: Tue, 08 Apr 2025 11:48:44 GMT  
		Size: 32.1 MB (32076946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6d76a75b19be005f99fa4db2c78f2d640066cf4cadbf6fff2ae70af014ed499`  
		Last Modified: Wed, 09 Apr 2025 07:04:16 GMT  
		Size: 215.1 MB (215107056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jdk-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:8c81e537bed5ec759f3387be114add3a4c7a6e45af5946acf4526ccf65fb2a5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2400112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d8c99cd8ce9f0ce471ab34d9025e7b00036294c298f1ad1911c6e4ac4523e34`

```dockerfile
```

-	Layers:
	-	`sha256:2d7ef0c10846dcbe1fbbd8d6dc3bf1c3946e883d6bc0770e421428f1c13f97c0`  
		Last Modified: Wed, 09 Apr 2025 07:04:10 GMT  
		Size: 2.4 MB (2388575 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c21af3d8fc77aad521a25868f9b6301964603ecdc9697d37d97931ea7db4060e`  
		Last Modified: Wed, 09 Apr 2025 07:04:10 GMT  
		Size: 11.5 KB (11537 bytes)  
		MIME: application/vnd.in-toto+json
