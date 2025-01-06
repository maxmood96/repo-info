## `sapmachine:jre-ubuntu-20.04`

```console
$ docker pull sapmachine@sha256:0b61775478db19456dc5584e32ee3378dee495f28ce58cf1796facf29303d318
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:jre-ubuntu-20.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:0f634a4851a72bea4af3786d463ac9cbe0fc466002ab3e1429f6cecffb6c1cda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.8 MB (86753930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8740338cb79f70e609a339f61913b08c9b981df457905d48e35a5ee6793ca3ea`
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
# Wed, 16 Oct 2024 12:49:19 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-23-jre=23.0.1     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Wed, 16 Oct 2024 12:49:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29ab2a8f785c8a590888c470a127fb4d3bf7758ff57eb900e68b55f1b25fe819`  
		Last Modified: Wed, 16 Oct 2024 18:58:36 GMT  
		Size: 59.2 MB (59242870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:9641fcf9213bf892fe73a2781c831e629fc3ebf937f7cc66f353dfeb645ae55c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2298732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69c63a9a07c2ac1762922bd4bf10c938dc38cbb91efb6b34118dc34507cb972a`

```dockerfile
```

-	Layers:
	-	`sha256:cd3993e73d78ffcfe0e2b0297df5d8184d8818172a5fc8b6e9bc2d984c23f53c`  
		Last Modified: Wed, 16 Oct 2024 18:58:35 GMT  
		Size: 2.3 MB (2289484 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b72a69066c42d853b0e49c8533f726c3e358463b7e0a8ebad0067f8b1f63fd03`  
		Size: 9.2 KB (9248 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jre-ubuntu-20.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:8bbcf1d959a1d2abbd3adba0b4dacc4f1acee2445c0c798db3b000e5f844bcb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.3 MB (84259200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0e549ea9a29c1220299a927f29f1e94acf4d7806f97aed0fa52b25b08a8f85f`
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
# Wed, 16 Oct 2024 12:49:19 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-23-jre=23.0.1     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Wed, 16 Oct 2024 12:49:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37c0a724a6ef22c434fefab1624e44f47ba5e989892309121215e7bf04cbc45c`  
		Last Modified: Wed, 16 Oct 2024 19:11:27 GMT  
		Size: 58.3 MB (58285372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:9b067b42e8549a44cf78de6ecfa08dbcaf60bc580d3a9853c74b13004e1c72e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2297883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b962c662a26b69622c2aa478572c5f185dc17cae839a7e9819378da3a06f32a`

```dockerfile
```

-	Layers:
	-	`sha256:b223dc1bb252ae102987916d1e4c457c8e1afb6e1a8895070ba5e2c71050e8e3`  
		Size: 2.3 MB (2288513 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5090be953b36d07ae8b26dcfb4361327ed61ae6081ddd6bd35e591020c55404f`  
		Last Modified: Wed, 16 Oct 2024 19:11:25 GMT  
		Size: 9.4 KB (9370 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jre-ubuntu-20.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:6d531d13962ee2f573ab70a4056719dfb6a41706411727b0c2b85432931a3699
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.4 MB (92374248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3b7f4d1c5d1bb03e456eb3737f2ebec2e3bcfcc1210cdb59b5abc9ff259bfc4`
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
# Wed, 16 Oct 2024 12:49:19 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-23-jre=23.0.1     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Wed, 16 Oct 2024 12:49:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cd720328ce8da41e08a7dd5922261b0c1980c2565df21b810488c55260400f68`  
		Last Modified: Fri, 11 Oct 2024 04:41:42 GMT  
		Size: 32.1 MB (32076506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de445cba1328fab443df1e34cbfd80dcdadcedfe24c289ef6b4177f4407c6f26`  
		Last Modified: Wed, 16 Oct 2024 19:20:59 GMT  
		Size: 60.3 MB (60297742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:f48439c4f54e286385577f6e96a0d005d2e694cb9654523b9edd35a95f85de83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ecf980071abc47e0a17e0ea54ed051b28312322f044c1b66ba8b2102200a3f5`

```dockerfile
```

-	Layers:
	-	`sha256:60aa28467c6d92e6a645d2b0eca061ddd1dd3ee91b43f3aae83050ce53f924e5`  
		Size: 2.3 MB (2292630 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43759deb0350195684e316fe7a78ea0e7effabc4d61c02d81fefd17ca4754895`  
		Last Modified: Wed, 16 Oct 2024 19:20:57 GMT  
		Size: 9.3 KB (9298 bytes)  
		MIME: application/vnd.in-toto+json
