## `sapmachine:11-jdk-headless-ubuntu`

```console
$ docker pull sapmachine@sha256:98f6467f0c11cd47ebaa1e1141d47d319432f33a8d1b97ac49c8d8e25ec49dd7
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
$ docker pull sapmachine@sha256:d208db2b097cf88022faa300bd2a03ccd86ddc9155240ca902369be89be9ee19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.8 MB (229789388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74f9d5d6c23c37254163bb9b9941d8f3675cd9f5cc2c002041c7680e651e3fc6`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 27 Jan 2025 04:14:00 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:14:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:14:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:14:00 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:14:03 GMT
ADD file:6df775300d76441aa33f31b22c1afce8dfe35c8ffbc14ef27c27009235b12a95 in / 
# Mon, 27 Jan 2025 04:14:03 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:19 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-11-jdk-headless=11.0.26 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Mon, 27 Jan 2025 13:39:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88b281393ccc196237c6a8a46cb42710298e26bfa5a5ef70b6e3d6c5c3fdba36`  
		Last Modified: Tue, 04 Feb 2025 04:50:02 GMT  
		Size: 200.0 MB (200035098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jdk-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:4b93b02a438d2752a6ee887b64f8dd797a2dae93de10e6d716ee79fad95de2d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2255953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ecddd8afd14fb7a05029786bc94ac550d0ce087dab4bf14df6f673a050750f7`

```dockerfile
```

-	Layers:
	-	`sha256:dcf52b1b36c8cfd06e860e4c17a13bb625c3cdaf6e23002728c78ded03a6e3c0`  
		Last Modified: Tue, 04 Feb 2025 04:49:59 GMT  
		Size: 2.2 MB (2246334 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19848d286745356c5f278f69efa589acf54266097d34f972ee32db2adbf288aa`  
		Last Modified: Tue, 04 Feb 2025 04:49:59 GMT  
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
		Last Modified: Tue, 19 Nov 2024 17:38:33 GMT  
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
		Last Modified: Tue, 03 Dec 2024 08:47:15 GMT  
		Size: 9.7 KB (9675 bytes)  
		MIME: application/vnd.in-toto+json
