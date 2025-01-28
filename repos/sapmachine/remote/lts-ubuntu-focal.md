## `sapmachine:lts-ubuntu-focal`

```console
$ docker pull sapmachine@sha256:8e7e90bd91052219bc8e2ad85992cb08b02b184e61bb8f785a203945bfb70de8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:lts-ubuntu-focal` - linux; amd64

```console
$ docker pull sapmachine@sha256:d75d3dd18f5238a01a68b51f4381ffba1091dbfbebf3a6d9945fa121244e0786
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.7 MB (241703280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ee45338f8e3a217d6967bc734aec84ce655425f5eb2d99e2795bcca9c10fb2e`
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
# Mon, 27 Jan 2025 13:39:13 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.6 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 27 Jan 2025 13:39:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe59a98d1ddabeab0f2d9b9feeb2d5d5c9de8fbcfceb299a61869c22228ce12a`  
		Last Modified: Tue, 28 Jan 2025 01:30:17 GMT  
		Size: 214.2 MB (214192220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:b110db1bc7251b97a5898bb1c2d1d040e407bafbaa6763170e7a51bf776699ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2398048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bd1fc93fd0b90c856553429d6495612056d8aa515fe7334e9000bed99d82bc0`

```dockerfile
```

-	Layers:
	-	`sha256:56a98adaa86028d7fc02b5fdcf864a60b24279fc2f3d6af0f72a575d99a003fb`  
		Last Modified: Tue, 28 Jan 2025 01:30:12 GMT  
		Size: 2.4 MB (2386606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a89b3b5900a4b3068f902e1e3c42be2702cb14e81560948ec00ab182b4537bf4`  
		Last Modified: Tue, 28 Jan 2025 01:30:12 GMT  
		Size: 11.4 KB (11442 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-ubuntu-focal` - linux; arm64 variant v8

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

### `sapmachine:lts-ubuntu-focal` - unknown; unknown

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

### `sapmachine:lts-ubuntu-focal` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:d724525004862bbd2c2b6ff4ce6072e9aa1e24b5813a623a8761d10eaaab0273
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.2 MB (247183448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4982c08e309de13011a9c8ac7ea72d168a2497a91e404c7db8bd7c492bf1201`
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
# Mon, 27 Jan 2025 13:39:13 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.6 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 27 Jan 2025 13:39:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cd720328ce8da41e08a7dd5922261b0c1980c2565df21b810488c55260400f68`  
		Last Modified: Fri, 11 Oct 2024 04:41:42 GMT  
		Size: 32.1 MB (32076506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a0c5fd917b6effb3e679c5e00f37c53ba7d7385d21d90e5fece1022f35cc98b`  
		Last Modified: Tue, 28 Jan 2025 06:00:01 GMT  
		Size: 215.1 MB (215106942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:910179e2edfc883e706a20fb592a464fac776dfc34f73c2e640e93e19798636b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2400012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35e93133ef2622519517070aebb171586da2753b37654a0e0939ac25af72c337`

```dockerfile
```

-	Layers:
	-	`sha256:ab6c092a1abb2bf794bf00ba86b5c7cd0f6ef9463abe1a84c2678eb664925ea7`  
		Last Modified: Tue, 28 Jan 2025 05:59:56 GMT  
		Size: 2.4 MB (2388475 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9993d58f1293ead3e39dff186996d45db00252a4500d74e3d902702dca35adf2`  
		Last Modified: Tue, 28 Jan 2025 05:59:55 GMT  
		Size: 11.5 KB (11537 bytes)  
		MIME: application/vnd.in-toto+json
