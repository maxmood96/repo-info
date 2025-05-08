## `sapmachine:24-ubuntu-focal`

```console
$ docker pull sapmachine@sha256:4a3aac9b6542305fabafe42304cf9a8e112dc268a9b8a908ea94de0af721666f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:24-ubuntu-focal` - linux; amd64

```console
$ docker pull sapmachine@sha256:3ce8a361ced5b2e6b3bbf79447fe902564edc76e220371841922ee181e09a6a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.1 MB (259103838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c72b6e41c8616bf022a1a6294e93233a4c5d8e55b9244f615fdf28004b069627`
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
# Wed, 16 Apr 2025 10:34:47 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jdk=24.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfd18b45c345772425eadb91ee23f3daf3744ca4b47df8e5668db727c737b383`  
		Last Modified: Wed, 16 Apr 2025 16:14:23 GMT  
		Size: 231.6 MB (231593444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:24-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:d3ccdafeb4b4125491e8ec2f1660467efab049d9f37c098f9f8e61e290a81c98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2388813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8be082182691f8f703478e9de6f4e80f1287eefeebda2fe48bfa4219769f8e19`

```dockerfile
```

-	Layers:
	-	`sha256:83899bc4936906bab1e82f6451f08bfe7bd65eaf5600be8e5b3f0e4ff756c9b5`  
		Last Modified: Wed, 16 Apr 2025 16:14:20 GMT  
		Size: 2.4 MB (2377400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:873b225fba238c208591474f9c438c2594ae0f301533efaa9c3b5b96c7ad4d40`  
		Last Modified: Wed, 16 Apr 2025 16:14:20 GMT  
		Size: 11.4 KB (11413 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:24-ubuntu-focal` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:9b1cb9dc3f30d1b3dc6ff73860714d6ad8eabee8ebac5ff6395274b92a881b21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.5 MB (255477465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9820a8e5b9da0afc66ae0fd3b23a0d842788a6e86de8d56ef451470ed98b7718`
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
# Wed, 16 Apr 2025 10:34:47 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jdk=24.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ecd83b6c354452b6a9979c7666bba16927f1e60e2afbfe6401dd6f87d5db8576`  
		Last Modified: Thu, 08 May 2025 17:05:17 GMT  
		Size: 26.0 MB (25977661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a8fe4247b7f22be15eb3fb32ed44a0942c685870bdc0a64bc4b005675178b40`  
		Last Modified: Wed, 16 Apr 2025 16:22:17 GMT  
		Size: 229.5 MB (229499804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:24-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:7cb62ce824a578e2c0069262fbf2b9925c745514a956dfbe54e5aaa13dc0abb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2388744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fb099ae577179aaa000e287314510d0ebf8033fce4a77ca5c51d64230df5859`

```dockerfile
```

-	Layers:
	-	`sha256:8707da0d627c371a403ba251b03c3f9e1a7dcf460f43dd6179bc3b9c7d164fbe`  
		Last Modified: Wed, 16 Apr 2025 16:22:12 GMT  
		Size: 2.4 MB (2377131 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0070842cc483f2eb39a16cb8538b326abc76c88b9879d391c527d45140e0a0e9`  
		Last Modified: Wed, 16 Apr 2025 16:22:11 GMT  
		Size: 11.6 KB (11613 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:24-ubuntu-focal` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:60016e63cd44c6898e8f1318c37a0fd60590ee951e52e2fc93e1f3877f913e52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.5 MB (264500820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbbe353b08c63b7b7aaeea0e7258cd8d9d43788dc872057e6fae4b2152654536`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 08 Apr 2025 10:47:01 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:47:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:47:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:47:01 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 08 Apr 2025 10:47:04 GMT
ADD file:d85970cec61787609e3854cb76ce16d54fe420b254cf48fc9ed9ed678717ff28 in / 
# Tue, 08 Apr 2025 10:47:05 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:47 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jdk=24.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:92d54367a68b4f03400315732acb4290d88bb06f8fe1414fd823f93402bec922`  
		Last Modified: Tue, 08 Apr 2025 11:48:44 GMT  
		Size: 32.1 MB (32076946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09e89c8180e42b82300ce4b0ea31e360271cb787b9da12edcc64fb7a8aa44ae3`  
		Last Modified: Wed, 16 Apr 2025 16:32:39 GMT  
		Size: 232.4 MB (232423874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:24-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:62593b8f07b492db00d4b007934e0f50ddba9217857e26c5513508aebbdea7c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2390155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bf0ed729ceeb79dc22caade6911c4dc83ff5d63cfb8ad4baa885cbb11aefaa6`

```dockerfile
```

-	Layers:
	-	`sha256:79cd3cf20ad04ff9e6a25f3ad58271a3bb04e55eb68b286040cb4df5cad47d9a`  
		Last Modified: Wed, 16 Apr 2025 16:32:31 GMT  
		Size: 2.4 MB (2378651 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65b29f3ac0dd9a4964b4bc6dbe843e5797c3ee1777ed9df71d6a2a9e8fd657a7`  
		Last Modified: Wed, 16 Apr 2025 16:32:31 GMT  
		Size: 11.5 KB (11504 bytes)  
		MIME: application/vnd.in-toto+json
