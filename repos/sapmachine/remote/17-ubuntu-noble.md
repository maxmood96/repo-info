## `sapmachine:17-ubuntu-noble`

```console
$ docker pull sapmachine@sha256:7f175a9bbcf33f6f898ebbb821811be2574ac81950be384b2c1e4bdcdcfe08bb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-ubuntu-noble` - linux; amd64

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

### `sapmachine:17-ubuntu-noble` - unknown; unknown

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

### `sapmachine:17-ubuntu-noble` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:942807359b072f1370d497b9a6339bff291c24fdc04dff920e883a06b82d2aac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.1 MB (228072377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0ed2d1783a1dd7476936a76837a377e51594d64818beb1cf12f9bcaa4ae2a08`
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
ADD file:d77dea5c49828eb0de89439d2b631bc8ea27cb9ef774412b56a060ba1673487b in / 
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
	-	`sha256:b8a35db46e38ce87d4e743e1265ff436ed36e01d23246b24a1cbbeaae18ec432`  
		Last Modified: Wed, 01 Oct 2025 15:34:19 GMT  
		Size: 28.9 MB (28861712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00f119ebed45bf397ab621f7a6e24de038052cee618a0af55d0c21cd4038d1d2`  
		Last Modified: Thu, 09 Oct 2025 22:56:21 GMT  
		Size: 199.2 MB (199210665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:75f04587c792b5f34119bbd1a9926325e3650103d492fd6f83a0d67df63e7b4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2616360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f353eeb0aaffac128aa07122abdf35ac6d6bac6f9171e3a541ab89dc611e5211`

```dockerfile
```

-	Layers:
	-	`sha256:663edb8acb30b6838e1abef18a885a1a7c058aa76fcdf60bd7714557c95028d5`  
		Last Modified: Fri, 10 Oct 2025 00:06:18 GMT  
		Size: 2.6 MB (2603462 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea0e4d698faa4dc3b837579ca628e43fafa57064ff8f2c748248e2fc5a6dd49c`  
		Last Modified: Fri, 10 Oct 2025 00:06:20 GMT  
		Size: 12.9 KB (12898 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-ubuntu-noble` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:b3e7f026eb57fb6066a3ca89cbbf1b1813a79f80f7459f954960a16c4aeec29b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.2 MB (238196439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ada26b0925ab7862c12c10ebe3e3398ad2f86d985826aad189a377a9992b9fd`
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
ADD file:c654664ccaf1c501c787c924fddcfab7f9cdc324325d45748f97ee6d5ad63cec in / 
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
	-	`sha256:15a6b79c4fd2f3417787ba4c0a8161183cf898454880102c719eb0c91671c218`  
		Last Modified: Tue, 30 Sep 2025 17:28:16 GMT  
		Size: 34.3 MB (34303547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c54e70067e13d55d84ac5d49b254266a7289ed0966a498afc1ae95ff2565b324`  
		Last Modified: Thu, 02 Oct 2025 06:05:56 GMT  
		Size: 203.9 MB (203892892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:df1fb05037efd4d288851874a755de0130229972e38431399644fcd716bc35db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2611799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98e7816540c8abe3f197d4407cdab22c5588ac1744deb58dd54880136018ecbe`

```dockerfile
```

-	Layers:
	-	`sha256:f41db953ccd2529457a76f8c72b9bad88093567800c7b3bf34d6b4e4c9b79cf3`  
		Last Modified: Thu, 02 Oct 2025 06:04:42 GMT  
		Size: 2.6 MB (2599033 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13555087771aca1f2a2ed7abc4136f1b18cde8a3883d151c2307d40ffcb5894a`  
		Last Modified: Thu, 02 Oct 2025 06:04:42 GMT  
		Size: 12.8 KB (12766 bytes)  
		MIME: application/vnd.in-toto+json
