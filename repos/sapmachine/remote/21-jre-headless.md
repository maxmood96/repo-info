## `sapmachine:21-jre-headless`

```console
$ docker pull sapmachine@sha256:735a0ebedddada2b18e98bb10cc84e846d334d20435de759767ae9ee83899e63
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:21-jre-headless` - linux; amd64

```console
$ docker pull sapmachine@sha256:6c4219d58de75daa8e1861f6c4944e994a5518f5d43cb985dfcb648139d5fa6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.2 MB (89226831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71b5217df14a62af26fe556e16c6104252b22ec0bd513e95d2a70026afdc1f8e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Feb 2026 16:49:54 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:49:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:49:56 GMT
ADD file:1ae27d2ef4369361104b699712f3897141e394785df5d193d67b44626f57eb87 in / 
# Tue, 10 Feb 2026 16:49:57 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:34:33 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.10 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:34:33 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 17 Feb 2026 20:34:33 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:01d7766a2e4a62b74e0bebf2cd12c47e675e9221174f6570854203e84ffe68b0`  
		Last Modified: Tue, 10 Feb 2026 17:41:34 GMT  
		Size: 29.7 MB (29727611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58e4456f43ae20c2c1fe66bda9a498651bd2eaba9ad1cf6f89a5704d8b2f0184`  
		Last Modified: Tue, 17 Feb 2026 20:34:47 GMT  
		Size: 59.5 MB (59499220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-headless` - unknown; unknown

```console
$ docker pull sapmachine@sha256:75a5555d5face8440df9daa5e8eb80660fa887aa9551cc26a8881f50d7f293fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2285427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef23fa6eaae49d121a53822747cac3f76f5fee701274092c9bf9d4b56ba8a8d6`

```dockerfile
```

-	Layers:
	-	`sha256:ea32375161dfcf7d8fb4e9107ab938e3227f79db5ef334a7f63f880380ca5b73`  
		Last Modified: Tue, 17 Feb 2026 20:34:45 GMT  
		Size: 2.3 MB (2275198 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3687e646a6318a16033befccb0cace210171579405133debcf54b28338abd70`  
		Last Modified: Tue, 17 Feb 2026 20:34:45 GMT  
		Size: 10.2 KB (10229 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre-headless` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:373ff370873595c6a5fceecb2506a2a9dc3026a78b662368b02007dab8076932
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.5 MB (87539524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baada1d49b7532222595604de1131616c6c61164e61f8f6e564baec2e0643e55`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Feb 2026 16:52:26 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:52:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:52:29 GMT
ADD file:25d708bf0b30ddee20c0b2764034e065aca922cafd48eb9c662e35ba02ccf1de in / 
# Tue, 10 Feb 2026 16:52:29 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:33:29 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.10 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:33:29 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 17 Feb 2026 20:33:29 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:66a4bbbfab887561d75f1fdb3c6221c974346f82c9229f5ef99f96b7e6c25704`  
		Last Modified: Tue, 10 Feb 2026 17:41:42 GMT  
		Size: 28.9 MB (28865120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b9dbfdca5b78933a30226e088b8bd20bba76233458e7fa7cb2506f627f404a2`  
		Last Modified: Tue, 17 Feb 2026 20:33:43 GMT  
		Size: 58.7 MB (58674404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-headless` - unknown; unknown

```console
$ docker pull sapmachine@sha256:fa6ae67439e971feaa229c57a93d2b0bfa7f1fa75ca6cc1438905ae8d406b12b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2286086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9af61c3864487a410c620ed34a4b8d447d119e63a043a960270bc4c55cc224f`

```dockerfile
```

-	Layers:
	-	`sha256:ad6cee9d48757dc5fb5ccd96c58bf974beb854432eb1d6388a8dc12f23216732`  
		Last Modified: Tue, 17 Feb 2026 20:33:41 GMT  
		Size: 2.3 MB (2275705 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5e0fc9e877123fd0fcb181a3e0630daad3f87c2bb59e4a82125e39cd937f811`  
		Last Modified: Tue, 17 Feb 2026 20:33:41 GMT  
		Size: 10.4 KB (10381 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre-headless` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:0787ae04f3557fe5902a80960b741bac79c0fffb3d842eea3009182fab0a5b19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.9 MB (94933261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b841cbef3a3345a314e63233ffab3c4e90e3633e02785d702c673a41f3ff1cc8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Feb 2026 16:50:31 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:50:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:50:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:50:31 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:50:35 GMT
ADD file:993db8d05f03953198d71fcb66f9a9dca68dcfd7ca7b3e4a866954aa297b35ce in / 
# Tue, 10 Feb 2026 16:50:35 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 21:27:50 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.10 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 21:27:50 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 17 Feb 2026 21:27:50 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:de86bbb8cdc5c52dc9167f3fab22b2f39424ccbfd06ab6c7b34bb3456cf0ad43`  
		Last Modified: Tue, 10 Feb 2026 17:41:57 GMT  
		Size: 34.3 MB (34306906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:105d682c6946583464b176309f3e4c64c14fb58428d527a6f564119fc5c82bbd`  
		Last Modified: Tue, 17 Feb 2026 21:28:18 GMT  
		Size: 60.6 MB (60626355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-headless` - unknown; unknown

```console
$ docker pull sapmachine@sha256:b015ff73079c1350aa81624e672f00af1c7f069be6a4a9d34b7be7b045e05012
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2284912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f1e174baa27797524225ef075f34eabc67ea501f24e60b92eb94d956548bf9d`

```dockerfile
```

-	Layers:
	-	`sha256:d2df22d7cdd039ffd54f3fde7a1dd13d59eaf678a09410e602c018ecc13f93c9`  
		Last Modified: Tue, 17 Feb 2026 21:28:17 GMT  
		Size: 2.3 MB (2274615 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b62930a550362b7b3931b9f1824e21969d27a32f22bc8a93c367f0146e3d1f2b`  
		Last Modified: Tue, 17 Feb 2026 21:28:16 GMT  
		Size: 10.3 KB (10297 bytes)  
		MIME: application/vnd.in-toto+json
