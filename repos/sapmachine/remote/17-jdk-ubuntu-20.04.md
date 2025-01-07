## `sapmachine:17-jdk-ubuntu-20.04`

```console
$ docker pull sapmachine@sha256:6d1d692021ecb5f19736ad5c9b9f9360fb34cfbf914a2d729a36d8764417aac1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jdk-ubuntu-20.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:a0fe5e5afd60007d3b7e0fc5c5080c76862522f1ec04539efdb36cdd5264e971
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.9 MB (226873797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1056a0783b1d4a2861efa9f4960dc26f0144b9de459428e9ea06caa45a7a14f`
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
# Wed, 16 Oct 2024 12:49:12 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.13     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:12 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 16 Oct 2024 12:49:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc449285f291602f892b16628845399bc8fdbc3a578e6064947a4baa9f692c6d`  
		Last Modified: Wed, 16 Oct 2024 19:00:18 GMT  
		Size: 199.4 MB (199362737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:25120453d0c49fa41234e7001fecac1b1f1d7f325599ab3492d2971cfcef0bb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2380577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a4b4d9ff58076c64e55f4747b49952a6b909e10771fb669ba199dd1f188d455`

```dockerfile
```

-	Layers:
	-	`sha256:927bc1376bf661447a1d485ed881a66cd469e4a6ef289ed69a81e1e133d96a47`  
		Size: 2.4 MB (2370655 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8efbe551f07b533bad35f1010e80f7642299fb25ac2dc779a55eb5cb3b84e7c8`  
		Last Modified: Wed, 16 Oct 2024 19:00:15 GMT  
		Size: 9.9 KB (9922 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jdk-ubuntu-20.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:648876230d7bfbc9ebafa87b2f84973a390d6ba6e7c85d10fb2f684b21cb36f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.0 MB (224041383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47a2a6aeba29d35eb3dc3b4d7b55374322a50c601423d4fb37af9b2112cca581`
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
# Wed, 16 Oct 2024 12:49:12 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.13     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:12 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 16 Oct 2024 12:49:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ebbfbc401d840288d0c765d1d861797e9beb27c04a0bfd42467da72ed75972c`  
		Last Modified: Wed, 16 Oct 2024 19:37:41 GMT  
		Size: 198.1 MB (198067555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:8c82c865b7e821f53cba8f1907f884ebce5e702c0f974ee8cdc72c27dad5a098
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2380407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76857bbb24dddecae1ed00724400dee5c3c41327c957f8f92bad2d3a0c64c1c8`

```dockerfile
```

-	Layers:
	-	`sha256:46ddffb969f02e7ccb46c02ce802f1baa79023fa034a30b9e73cdb8d48f018bd`  
		Last Modified: Wed, 16 Oct 2024 19:37:37 GMT  
		Size: 2.4 MB (2370339 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01d451e210ffa2396050dc26a4654b5cf69bc7cf5e3b7beedc89d9ea2cbc6da8`  
		Last Modified: Wed, 16 Oct 2024 19:37:37 GMT  
		Size: 10.1 KB (10068 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jdk-ubuntu-20.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:a0ac9cbbebec11bd0c2c778c418a2b762da1f21f2e1a68838e12b6184632db80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.1 MB (232145357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3448e005821aa759a3691a391724f831cd3b583ab7c4072ce8b2230c98d34158`
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
# Wed, 16 Oct 2024 12:49:12 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.13     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:12 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 16 Oct 2024 12:49:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cd720328ce8da41e08a7dd5922261b0c1980c2565df21b810488c55260400f68`  
		Last Modified: Fri, 11 Oct 2024 04:41:42 GMT  
		Size: 32.1 MB (32076506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f17fe9b9ccedcadd38d46116cf3c06b36670cd084ff3c257dc0420d0212acc10`  
		Last Modified: Wed, 16 Oct 2024 20:05:18 GMT  
		Size: 200.1 MB (200068851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:f153b4609eb8d049e4692d5382c20fa0ba7d621c8b860fed6e6cc84df85bb3e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2382479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3736c092c0b69c8b47fcdf13a8b0f9c14e812daf57df329c1a646da3869b0daa`

```dockerfile
```

-	Layers:
	-	`sha256:23b05673d98dc7a76d47292460ee6275bf4716d6162ecf5148a2eedf54c870ce`  
		Last Modified: Wed, 16 Oct 2024 20:05:13 GMT  
		Size: 2.4 MB (2372495 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:873a4c22e7e5584b3adfe750fe839a73d8bf5848b6454319202025c154841cb4`  
		Last Modified: Wed, 16 Oct 2024 20:05:12 GMT  
		Size: 10.0 KB (9984 bytes)  
		MIME: application/vnd.in-toto+json
