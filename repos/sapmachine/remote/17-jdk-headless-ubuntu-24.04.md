## `sapmachine:17-jdk-headless-ubuntu-24.04`

```console
$ docker pull sapmachine@sha256:8ae14ecc13c904c397c63f940f6b04f353709bd94b3760ff69dce997cb9327d0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jdk-headless-ubuntu-24.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:312fdb78cf5a6534e224e6523f4d978be4ddf22b6fdeed695f1957ded24c100f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.2 MB (229204547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de2d2cd214624f27d1649065a6675f9f27205ff2b4e9e5dbcc6ea83d86188383`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 13 Jan 2026 05:37:25 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:37:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:37:27 GMT
ADD file:3077ee44db3cc7d38740d60a05c81418dd3825a007db473658464f52689e867b in / 
# Tue, 13 Jan 2026 05:37:27 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:44:42 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk-headless=17.0.17 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:44:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 15 Jan 2026 22:44:42 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a3629ac5b9f4680dc2032439ff2354e73b06aecc2e68f0035a2d7c001c8b4114`  
		Last Modified: Tue, 13 Jan 2026 06:35:38 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac59642400917c88abb4681ebb47807f2644cc9fc9281ad4bfdc698c801edca9`  
		Last Modified: Thu, 15 Jan 2026 22:45:04 GMT  
		Size: 199.5 MB (199478536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:eceac54f6a4ad006d09dd542d00eff4827be24e32a68214257dd442bb9d903de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2364718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f37636b8700fb604d1be6bc5f34ae5c85aeda8cb929aa42ec6a560cb3ab0d070`

```dockerfile
```

-	Layers:
	-	`sha256:7fd2dbfde6e52c50785292b2728391a5c2343fc1972159dd4c68baf7a9cdf16b`  
		Last Modified: Fri, 16 Jan 2026 01:07:56 GMT  
		Size: 2.4 MB (2354484 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0fed7b4b054fcaf77dce9d05f39f8374ded202afc8b30d385f192b176e8125b`  
		Last Modified: Thu, 15 Jan 2026 22:45:00 GMT  
		Size: 10.2 KB (10234 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jdk-headless-ubuntu-24.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:9d98e170441814fdcddc3913475221e23f63a4e6808f735037bd20b0dc3bcbb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.1 MB (227064959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a6a80e1c9349f5b3bdb7d684b525d2618ef6101ce775b3da67bd44450e7dcf2`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 13 Jan 2026 05:40:13 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:40:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:40:17 GMT
ADD file:6089c6bede9eca8ec4f424e5798a0ae0712a6fe38c9b97f9afb9d24d9675024e in / 
# Tue, 13 Jan 2026 05:40:17 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:47:38 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk-headless=17.0.17 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:47:38 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 15 Jan 2026 22:47:38 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:36bf709aa36d66b784b0ba1aa3276848f28501175eeb4d7a310b1a98578f8558`  
		Last Modified: Tue, 13 Jan 2026 07:03:33 GMT  
		Size: 28.9 MB (28863824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:533719d81b7c29d1392c3676979b7cc71ed163858bb3954c47c2da4be0370b25`  
		Last Modified: Thu, 15 Jan 2026 22:48:01 GMT  
		Size: 198.2 MB (198201135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:5f8cf11635d389c8cb4056f2368cdf6e9f90ff7658d17a74d476a13b0cfe29fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2365377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c708f9960bf7f03f1205f254d24caef36551808b17852eb0eca85e8f6633bcef`

```dockerfile
```

-	Layers:
	-	`sha256:0afe2ca93a8aabab5d41a3d94b1174e3b6a54aa690a706344d76d8b8dfe114e9`  
		Last Modified: Fri, 16 Jan 2026 01:08:00 GMT  
		Size: 2.4 MB (2354991 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:efd9f20698eab3249b78a0e874b4dc775768e0ba920ab6481c984366783829cf`  
		Last Modified: Thu, 15 Jan 2026 22:47:57 GMT  
		Size: 10.4 KB (10386 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jdk-headless-ubuntu-24.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:0987cbe20a8853ddb66d5b60664b53f7641fb75b8db5f3ab42cc6c036890a39f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.4 MB (234390781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a2aa03ccbd5289f7c9f59c8200525a7ad0650beff909cb7c86c9a121c0c81a8`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 13 Jan 2026 05:39:44 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:39:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:39:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:39:44 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:39:47 GMT
ADD file:2f07f2a41a0f9535d0bb4dbf76ba28288335a19d601419d55d8004fa2b0faf12 in / 
# Tue, 13 Jan 2026 05:39:48 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 23:42:39 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk-headless=17.0.17 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 23:42:39 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 15 Jan 2026 23:42:39 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0dea13cf1fe062734821309e5f773a18c9ad629d9e93e3eba340bea036bccd8a`  
		Last Modified: Tue, 13 Jan 2026 06:35:59 GMT  
		Size: 34.3 MB (34306159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:677104334d66faddbdb6731171488994f3bc15965676601010500256eb37d8c3`  
		Last Modified: Thu, 15 Jan 2026 23:43:52 GMT  
		Size: 200.1 MB (200084622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:8080e2f67becfabcd557e89979f9177016062001b739cfa00b53f2c80e952698
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2360840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfd6e0ba8e92212acf59240c7ac66a73e77eb390d9ebae9ff2a37f4854c38b61`

```dockerfile
```

-	Layers:
	-	`sha256:3b06396977cb4b4ff92d74146e3b5f406c24cb0fd1709f374c8aa213d3616b98`  
		Last Modified: Thu, 15 Jan 2026 23:43:20 GMT  
		Size: 2.4 MB (2350538 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44f17959ffab5ecb05908884920ed7b85ba995b4d20a72a2b13c869b2ead0415`  
		Last Modified: Fri, 16 Jan 2026 01:08:07 GMT  
		Size: 10.3 KB (10302 bytes)  
		MIME: application/vnd.in-toto+json
