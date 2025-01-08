## `sapmachine:11-jdk-headless-ubuntu`

```console
$ docker pull sapmachine@sha256:78e5bd6e090b0b1a353e0f4fbc6ca5581fc1f4368e4e0dd0e145c10dcc4d24fc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:11-jdk-headless-ubuntu` - linux; amd64

```console
$ docker pull sapmachine@sha256:3afdc06da9d50d9b74183c7b0310cd6de18b1604939d9e762713038ed7b2e1d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.8 MB (229795047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70486672721b6421dac9463add8ed28767e6d0a05e21b403f7e51b8c6643c2e0`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Oct 2024 12:49:16 GMT
ARG RELEASE
# Wed, 16 Oct 2024 12:49:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Oct 2024 12:49:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Oct 2024 12:49:16 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Oct 2024 12:49:16 GMT
ADD file:bcebbf0fddcba5b864d5d267b68dd23bcfb01275e6ec7bcab69bf8b56af14804 in / 
# Wed, 16 Oct 2024 12:49:16 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 12:49:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk-headless=11.0.25     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Wed, 16 Oct 2024 12:49:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:de44b265507ae44b212defcb50694d666f136b35c1090d9709068bc861bb2d64`  
		Last Modified: Tue, 19 Nov 2024 17:38:27 GMT  
		Size: 29.8 MB (29751968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e29c92d00f392fb723465ad70728b339674afb022a3e594ba549d9aec591264a`  
		Last Modified: Tue, 03 Dec 2024 02:37:09 GMT  
		Size: 200.0 MB (200043079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jdk-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:1ba77738aa557a12c002448f1e0e1b62fc12e441fbba647ca0430b6431f85365
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2252972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37220e00993f5b591ae1f8d15dd8895e0e2a67e729bcadb906e13fd7826d6cf3`

```dockerfile
```

-	Layers:
	-	`sha256:7cc6f198e1653a9809ebf530a58344228e95f27938d61c0601293991bd2a030a`  
		Last Modified: Tue, 03 Dec 2024 02:37:04 GMT  
		Size: 2.2 MB (2243353 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d45ca569df937c84c9c48c7684b454853850253e3b7e7b66a881e27b4238dde`  
		Last Modified: Tue, 03 Dec 2024 02:37:03 GMT  
		Size: 9.6 KB (9619 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-jdk-headless-ubuntu` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:b200a0707f222b762368df4be9915ce59b41a699d7ed4da07e293e46f9630d71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.4 MB (227434193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50c22bba9c03b6c47badf8386d3783b6978f0d9a766bae98710126e08bf6cee1`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Oct 2024 12:49:16 GMT
ARG RELEASE
# Wed, 16 Oct 2024 12:49:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Oct 2024 12:49:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Oct 2024 12:49:16 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Oct 2024 12:49:16 GMT
ADD file:765dfd09ec2ac4870c8b3efd6ef4a994f99695c574d546d7a9a0e69bbb970b03 in / 
# Wed, 16 Oct 2024 12:49:16 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 12:49:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk-headless=11.0.25     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Wed, 16 Oct 2024 12:49:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8bb55f0677778c3027fcc4253dc452bc9c22de989a696391e739fb1cdbbdb4c2`  
		Last Modified: Wed, 08 Jan 2025 00:53:35 GMT  
		Size: 28.9 MB (28892671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0415a3de4336156559c66db53ab51496528bab297d30f2f7c40d2e9cd52c6dee`  
		Last Modified: Tue, 03 Dec 2024 10:56:22 GMT  
		Size: 198.5 MB (198541522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jdk-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:ae0ed46cbee15aeecf20a952c6081d39f88ea761d57cbdce544428c79db62e7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2254209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1a22668319f87ac268f9c9d4b3eca8f6d7ca8ad7dfba197c77bc565857c0b49`

```dockerfile
```

-	Layers:
	-	`sha256:449a1d8f22cd053cfea330884a64ed76cc21ed9e6799bb6e1c4ba6f0d8950fa6`  
		Last Modified: Tue, 03 Dec 2024 10:56:18 GMT  
		Size: 2.2 MB (2244463 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6de94ac5cc40bed29de0d88918685ad9d8534c73a6713201bdc624d0ee50e8ee`  
		Last Modified: Tue, 03 Dec 2024 10:56:18 GMT  
		Size: 9.7 KB (9746 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-jdk-headless-ubuntu` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:04b54ab116d8f56c87f6d61e54f36f168604d4d1caf20f4e35a7ee537b194613
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.0 MB (221037894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a34029c8480c8f07b3e36daeb53cbd68cfd7f0b7af3ed3c39d4ae3aa261615de`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Oct 2024 12:49:16 GMT
ARG RELEASE
# Wed, 16 Oct 2024 12:49:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Oct 2024 12:49:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Oct 2024 12:49:16 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Oct 2024 12:49:16 GMT
ADD file:43ada82586e21a3bec38211b678fc6eb9b5e39f96a2d31fced4653d2b54a553f in / 
# Wed, 16 Oct 2024 12:49:16 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 12:49:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk-headless=11.0.25     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Wed, 16 Oct 2024 12:49:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4e112885c8061d52bcd0f8d99851b65be887b95c74de235a16946b3562526bbb`  
		Last Modified: Tue, 19 Nov 2024 17:38:45 GMT  
		Size: 34.4 MB (34388820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4497fb463231c4698f213ff67f729dbe9a0cb667d59e9aaa629a7125e683615a`  
		Last Modified: Tue, 03 Dec 2024 08:47:21 GMT  
		Size: 186.6 MB (186649074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jdk-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:6c3177ed422faa541c103c897b326e77d736d086106e8a16884da26899c8d1d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2254340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:674179451f3cd0deb7d325c7950f68c9802f342fbad19be09402984aac44e8db`

```dockerfile
```

-	Layers:
	-	`sha256:038970e1d0258d324ba9c0fb0a98f3ff1328346dc7dd54d3fdc6aba79aec6531`  
		Last Modified: Tue, 03 Dec 2024 08:47:16 GMT  
		Size: 2.2 MB (2244665 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0109c90714ff01bb60326f4cce034f633c719c0e284a50619ab01a7d41ace266`  
		Size: 9.7 KB (9675 bytes)  
		MIME: application/vnd.in-toto+json
