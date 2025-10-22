## `sapmachine:17-ubuntu-24.04`

```console
$ docker pull sapmachine@sha256:d0f3496c0ddd7b6059ea22f945054912f501bd9493e4106d22ee442b3cf6c99d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-ubuntu-24.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:ba4be7509e420195f9dfa6f73413ed2046b8cd486f4a9ad986d19460e90d459b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.2 MB (230216024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdda1f2852ea23b0097db962b644629df40b89bf9d1a47bd66f9707173935b54`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:11 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:11 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 15 Jul 2025 19:58:11 GMT
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
# Tue, 15 Jul 2025 19:58:11 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:11 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.16 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:11 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 15 Jul 2025 19:58:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:842810a0b72d9b82398131fab9e93afc46d84d01f96052d41d6ffea9e7f85e64`  
		Last Modified: Thu, 09 Oct 2025 22:54:49 GMT  
		Size: 200.5 MB (200492877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:fc738d0c78b2b60e0f2faab7b6da15c4012b78a9aef11f45ce10670eee39b33c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2615500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89a22f1c34123371665ef5c09d16e92cfe803fa619304d9a987cc2de41e52bfd`

```dockerfile
```

-	Layers:
	-	`sha256:091e5146cbcb6aba47374f1525337cb1bfe5655a43ffe66c28ba3c030b56872a`  
		Last Modified: Fri, 10 Oct 2025 00:05:54 GMT  
		Size: 2.6 MB (2602850 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd792465b773a1c6e8b88aaf3406dc395c6ac3fbe38a90360c4ff8268a514cab`  
		Last Modified: Fri, 10 Oct 2025 00:05:57 GMT  
		Size: 12.7 KB (12650 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-ubuntu-24.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:8144b3a6d7af24614a3a3f6b2e1ac522c5cfe619332b606143f5135e1b707292
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.3 MB (228254141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44b2ac78385257800432e00808ee96c82b31a36178212232397b7c58f4acd244`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 01 Oct 2025 13:01:38 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:01:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:01:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:01:38 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:01:40 GMT
ADD file:d77dea5c49828eb0de89439d2b631bc8ea27cb9ef774412b56a060ba1673487b in / 
# Wed, 01 Oct 2025 13:01:40 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 21:30:22 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.17 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 21 Oct 2025 21:30:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 21 Oct 2025 21:30:22 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b8a35db46e38ce87d4e743e1265ff436ed36e01d23246b24a1cbbeaae18ec432`  
		Last Modified: Wed, 01 Oct 2025 15:34:19 GMT  
		Size: 28.9 MB (28861712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62e816a710be6f87c0980f72e7428cd2c2093e166632d004bae89a0953a6f6d0`  
		Last Modified: Wed, 22 Oct 2025 00:09:58 GMT  
		Size: 199.4 MB (199392429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:4282550567e3657212068d0013efe2415c2c75b8c811d9fc44c4abf5b2d8b809
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2616359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e9cd2c9bb856b924605aa6feeb6def78c6fb5ff6f822a980d8fefa73df24600`

```dockerfile
```

-	Layers:
	-	`sha256:6b813529c619ffc2b0627780bff6bf65221721f5c1d067c110f5e10aba108fc1`  
		Last Modified: Wed, 22 Oct 2025 02:28:29 GMT  
		Size: 2.6 MB (2603462 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6208984899feb2afdc65822b4f45221a5bbe665fb75ee7ed93be25c2da1caebf`  
		Last Modified: Wed, 22 Oct 2025 02:28:30 GMT  
		Size: 12.9 KB (12897 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-ubuntu-24.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:992c7dcc9c59328aea25c518f224b41686c7f5e64728af5f27aa8e76d1e27977
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.6 MB (235573923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:368b250a521404e6d3500635dd71abad9c67cf5a6cd3ea49965cb7cca635be1a`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:11 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:11 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 15 Jul 2025 19:58:11 GMT
ADD file:e06669c9bfb72bbbaf1c25efab4729831236db24361c42e37dbbc7b4eff7a82a in / 
# Tue, 15 Jul 2025 19:58:11 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:11 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.16 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:11 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 15 Jul 2025 19:58:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:199e3830c89a37cc6980743d7c9e0e355251d050c55eb838183c9cf64fac375b`  
		Last Modified: Wed, 01 Oct 2025 17:22:52 GMT  
		Size: 34.3 MB (34303525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63f0128722015361ed22ec71e7fb78c100410c8e346934e4d52c09b2016f0370`  
		Last Modified: Fri, 10 Oct 2025 03:12:26 GMT  
		Size: 201.3 MB (201270398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:39fd4ebc0f2bd9a2bc5a065c26e2737a0776398c9b312a5c20192b0fe1fa9ec4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2611799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acb868122beaace0ad935136dffb721827698cc7bb6ced254d9d9a85a47f1040`

```dockerfile
```

-	Layers:
	-	`sha256:244422ce1a8d7d0953f938ad735ea8ba28c17503f977ddb7cf3b919c1f37696a`  
		Last Modified: Fri, 10 Oct 2025 00:07:00 GMT  
		Size: 2.6 MB (2599033 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:663cc9b5232dd1ad38fb5984128675beb8f93636c1f6444a6ff5bdfeebe9a55f`  
		Last Modified: Fri, 10 Oct 2025 00:07:01 GMT  
		Size: 12.8 KB (12766 bytes)  
		MIME: application/vnd.in-toto+json
