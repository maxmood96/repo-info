## `sapmachine:jre-headless`

```console
$ docker pull sapmachine@sha256:7619fbfa65f08b2d7051e1dcabbe56ea156349baeea775378d923d7643c5a188
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:jre-headless` - linux; amd64

```console
$ docker pull sapmachine@sha256:55d027fa1adcd30d558c68ee07f516b357d101699ec2a8cc4e39645a58f58a6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.3 MB (86281979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3a1fbffeed18719bacd1ab58c9935f46c590028fc8a99613664e6a3e85c3ba8`
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
# Tue, 17 Feb 2026 20:33:24 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jre-headless=25.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:33:24 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Tue, 17 Feb 2026 20:33:24 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:01d7766a2e4a62b74e0bebf2cd12c47e675e9221174f6570854203e84ffe68b0`  
		Last Modified: Tue, 10 Feb 2026 17:41:34 GMT  
		Size: 29.7 MB (29727611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cb03d43cfa501ec08bfbb23954eee089730e18a46bcdf46a1056c1fdd313856`  
		Last Modified: Tue, 17 Feb 2026 20:33:37 GMT  
		Size: 56.6 MB (56554368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-headless` - unknown; unknown

```console
$ docker pull sapmachine@sha256:9a2e9f91a45ff6dd1a9c824ad4e75c2a60bf0ada46ad805ce0c6354a1d755b30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2295324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98bd0869a6e9e8bf7bbaf60c425e6bef71b3ff53cf3206aee5c6bac87dcd44a9`

```dockerfile
```

-	Layers:
	-	`sha256:44b6f71cdbc188768fc6f58caa61870daebedd13c2ab499e20a4535a10c719b6`  
		Last Modified: Tue, 17 Feb 2026 20:33:35 GMT  
		Size: 2.3 MB (2282722 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c01825b6c0e1e6a269aae75b2121c6f0bf353b23a236f28fe5e8f833373349f`  
		Last Modified: Tue, 17 Feb 2026 20:33:35 GMT  
		Size: 12.6 KB (12602 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jre-headless` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:ae5eea4ce94c3af70d7581a0929ad60360cde8f41dbefa0eb4d03a359daded3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.4 MB (84368843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc81aaf1e0fbc930c8bd926edabc3ca4920267e94f481c711bf9d31d4cb0460a`
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
# Tue, 17 Feb 2026 20:33:24 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jre-headless=25.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:33:24 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Tue, 17 Feb 2026 20:33:24 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:66a4bbbfab887561d75f1fdb3c6221c974346f82c9229f5ef99f96b7e6c25704`  
		Last Modified: Tue, 10 Feb 2026 17:41:42 GMT  
		Size: 28.9 MB (28865120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b72843606f2e47f413168f59006e8ef2d3d3ee2218b88cfc30eb7249adb0fee`  
		Last Modified: Tue, 17 Feb 2026 20:33:37 GMT  
		Size: 55.5 MB (55503723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-headless` - unknown; unknown

```console
$ docker pull sapmachine@sha256:07610dbbee7306425ba5ac444251a0c71b642c0e151c842038acf5db0513a49e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2296148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24ef95d0de1a92e13bbbdb3e197f40fe443c52ae361538be552916c06da6a378`

```dockerfile
```

-	Layers:
	-	`sha256:e656214c6915c362f33bcba395605ce3229cc3a1fc217ce24563d8df8c3b9c78`  
		Last Modified: Tue, 17 Feb 2026 20:33:36 GMT  
		Size: 2.3 MB (2283310 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5dc5ac50b6f43b7c8fe06cfc4eeaaecb5793f1cecff37a4549d4f31c6563217f`  
		Last Modified: Tue, 17 Feb 2026 20:33:36 GMT  
		Size: 12.8 KB (12838 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jre-headless` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:c0e2f23cd5dc5ba437a0c8e3d40bb38681f4de992d8202cedf7c5a8863e166e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.7 MB (91665751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef8ad1dbbc91eb3561a834ddde4e1d9174316e088ca4bcb395393cd96236aae8`
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
# Tue, 17 Feb 2026 21:20:47 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jre-headless=25.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 21:20:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Tue, 17 Feb 2026 21:20:47 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:de86bbb8cdc5c52dc9167f3fab22b2f39424ccbfd06ab6c7b34bb3456cf0ad43`  
		Last Modified: Tue, 10 Feb 2026 17:41:57 GMT  
		Size: 34.3 MB (34306906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24d10c023ff280a854a7eb6ea707adf9c8988df843748bbcb118ab89acaea468`  
		Last Modified: Tue, 17 Feb 2026 21:21:16 GMT  
		Size: 57.4 MB (57358845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-headless` - unknown; unknown

```console
$ docker pull sapmachine@sha256:3148b10a8229afba00631a72c1ab51efa222bd12d78625bcda3badb5012b8e53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2294263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34b90502f1d12c389fbb7b4b68f867ae958ce5d373fe36763ed3e60fe91d9fbd`

```dockerfile
```

-	Layers:
	-	`sha256:ae3b319e23e168cc739b298bf145da09afd23ffb3bbf232efd527f9fddc78c3f`  
		Last Modified: Tue, 17 Feb 2026 21:21:15 GMT  
		Size: 2.3 MB (2281551 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d06713e5fd0f1d107851f3f39d032a95f24c36d2d06531d04825d76716c4c172`  
		Last Modified: Tue, 17 Feb 2026 21:21:14 GMT  
		Size: 12.7 KB (12712 bytes)  
		MIME: application/vnd.in-toto+json
