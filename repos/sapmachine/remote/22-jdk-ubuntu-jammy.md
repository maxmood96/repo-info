## `sapmachine:22-jdk-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:3fa17643b9c5670874d9bb182df79ea2a0aea0cf9746d8fbaf3f1775b4a5378d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:22-jdk-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:8612e18918e1101b6e33a8d287c3b4b35827f5683ae76bc65045590720817391
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.9 MB (242947605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cf837b7601f4969d3f7e0e8ff956aff1ae430f4664265e333be71923fd0b982`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:58 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:58 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 May 2024 10:06:58 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Mon, 13 May 2024 10:06:58 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:58 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jdk=22.0.1     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:58 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Mon, 13 May 2024 10:06:58 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf2b243447edd57911c78c08de9ffa476862279b9da92f084795b6368f8cfacd`  
		Last Modified: Tue, 02 Jul 2024 03:33:23 GMT  
		Size: 213.4 MB (213413550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:22-jdk-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:524458810743bfab93b495c10864744a9396a163e819a7a8b43261aea1976ecf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2456724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16085193d22b058804ca3d8e2900ed8f4e6144b0a26c1241c517b4b3f156e299`

```dockerfile
```

-	Layers:
	-	`sha256:f3819dbd7918d98156f6dd274d7f261fd77456c60f586450859087ad85af2f76`  
		Last Modified: Tue, 02 Jul 2024 03:33:17 GMT  
		Size: 2.4 MB (2445547 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad76be71d606c5829ed417061a97e550035da8300364e8d40ef42411accd893b`  
		Last Modified: Tue, 02 Jul 2024 03:33:17 GMT  
		Size: 11.2 KB (11177 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:22-jdk-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:e7494a9502e24f0c47fb86c6a5aa10d26c9629ea37c69cfd4f569ba60f478b6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.7 MB (238705120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:892840ac69cb2470d66b47222ca83d6c0d0b2f2d382ae973335d69b1230b8d7b`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:58 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:58 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 May 2024 10:06:58 GMT
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
# Mon, 13 May 2024 10:06:58 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:58 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jdk=22.0.1     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:58 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Mon, 13 May 2024 10:06:58 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9b10a938e28486049341cb41134e8c0c141b2e25870896c597e2a54df471acbb`  
		Last Modified: Mon, 03 Jun 2024 10:46:52 GMT  
		Size: 27.4 MB (27361782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51ecc79d71e81a3146db081db4c0d376e11d1b21109fa0f3b2e8b6acf34ef66b`  
		Last Modified: Tue, 25 Jun 2024 23:54:23 GMT  
		Size: 211.3 MB (211343338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:22-jdk-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:2923379be1f96459c51ab5d64d40eca03bff48a8fd73ba5284252c8c60ff25cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2456266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6659bec65f79fc95a402eb69d7c7de43b0e566dc1a45dea923a9dc8517188cd3`

```dockerfile
```

-	Layers:
	-	`sha256:da396193f2f80509e017710c036075379b1812ebd45a70cf3d713f9bc2e0beb5`  
		Last Modified: Tue, 25 Jun 2024 23:54:18 GMT  
		Size: 2.4 MB (2444692 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4ecaeae4e8d8a96f0c616ad255e68f8e099827db16cc92d8ccc75d33afa2d69`  
		Last Modified: Tue, 25 Jun 2024 23:54:18 GMT  
		Size: 11.6 KB (11574 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:22-jdk-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:71ac490e642a3bfd33688b6777501bfd7a08d5d651d248e744c67d650e6ec8e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.9 MB (248938058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1b0080e716896a8b70be778778bdac40d9fd9445427b99c2f7700472c535be1`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:58 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:58 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 May 2024 10:06:58 GMT
ADD file:e2e1e840070a30a93a9141ddf77b416d95fb822ac1f550f7162a64e18e0ade5b in / 
# Mon, 13 May 2024 10:06:58 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:58 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jdk=22.0.1     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:58 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Mon, 13 May 2024 10:06:58 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:dcb5d217f9f18d3486ceb1894319d66c6f49a84670fbf2ac2f4dd47935357bfc`  
		Last Modified: Thu, 27 Jun 2024 20:18:46 GMT  
		Size: 34.5 MB (34461081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e09c20b64d8f903a9dd215c9cfccbcb1d99501ba25b63564fedd9605d5025b5`  
		Last Modified: Tue, 02 Jul 2024 21:19:36 GMT  
		Size: 214.5 MB (214476977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:22-jdk-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:3e3ef8e613b657f4117c5091891a61ff100b63c2a42331bef069684ee02c3d70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2458269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc1f6c248823f68346cf6809d8431f970b76703bb681ee3a47459c992b530611`

```dockerfile
```

-	Layers:
	-	`sha256:8074261dc9c2d05804cbe7eddfa38c2e6e3ecbecabbc9f1df53bede8ae784e5b`  
		Last Modified: Tue, 02 Jul 2024 21:19:31 GMT  
		Size: 2.4 MB (2447006 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d4f97d8d05ddf68682f7cb9ae0f6ba6def83dc8116ecac8a7aa95f5747897ec`  
		Last Modified: Tue, 02 Jul 2024 21:19:30 GMT  
		Size: 11.3 KB (11263 bytes)  
		MIME: application/vnd.in-toto+json
