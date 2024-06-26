## `sapmachine:17-jre-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:b1fe7c16bb8ae714db3ed622dacb32753dfe345095a11e2e83bc8549e910dcc8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jre-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:295d738dfa9de6000e72999effeaa30d851859dbf58b409ac560811c58f94cf4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.2 MB (83196136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74665ef9ec7fa08d10046815cdb53b35259c6a7664d5d6243d331d1bb0c1f92c`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:54 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:54 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 May 2024 10:06:54 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Mon, 13 May 2024 10:06:54 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:54 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.11     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Mon, 13 May 2024 10:06:54 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7646c8da332499ae416b15479ce832db32e39a501c662e24324f595509a0d3db`  
		Last Modified: Mon, 03 Jun 2024 10:46:44 GMT  
		Size: 29.5 MB (29533754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eadeff8dba3f0b506ace2616c351030371b7fbd5b0b2deed50f7e61027affef4`  
		Last Modified: Tue, 25 Jun 2024 22:58:44 GMT  
		Size: 53.7 MB (53662382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:e1fa2d9ea216666341ce0a5055d7c0b86c4ea610510b2d31bf34b0ab0327a369
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2366001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60c792edbebf4f7a4f71313923dcd3de54232643bc19053b803a8c34c31a94d5`

```dockerfile
```

-	Layers:
	-	`sha256:0acd6d2bab82066c7905aa39652c1a78b40efd3d8acafac1a1146a78c344a0bf`  
		Last Modified: Tue, 25 Jun 2024 22:58:44 GMT  
		Size: 2.4 MB (2357416 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4cba8be75c3a8555da6b6a8a011fe34913ea1f812ec6384dfbe297898d14df08`  
		Last Modified: Tue, 25 Jun 2024 22:58:44 GMT  
		Size: 8.6 KB (8585 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:1887a6e3edf0fc42232457d048cbe101d6104f15e6ad6a890b7ada0edec3c68d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.4 MB (80350792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73927c3d0343740023daa3f6fe099d262c8caa4369e73b8db980c759dc834646`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:54 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:54 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 May 2024 10:06:54 GMT
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
# Mon, 13 May 2024 10:06:54 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:54 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.11     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Mon, 13 May 2024 10:06:54 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9b10a938e28486049341cb41134e8c0c141b2e25870896c597e2a54df471acbb`  
		Last Modified: Mon, 03 Jun 2024 10:46:52 GMT  
		Size: 27.4 MB (27361782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d16c07111ef3d695770efc38d0ffd468b05bee4c5723bd73dbc7de8993d9b7d`  
		Last Modified: Wed, 26 Jun 2024 00:20:56 GMT  
		Size: 53.0 MB (52989010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:8b17dd840a51cd8b2885e1d55cdb8915b1fe2f33e5bddf9a07801a89e7e02731
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2365981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6889da4e6aa338df9ca56b4908bfba1b583bd9893934600247480e92153408ef`

```dockerfile
```

-	Layers:
	-	`sha256:73ca8b924c32e03533aae4ad1f31efc893f3c100625c43e230a26497476013a5`  
		Last Modified: Wed, 26 Jun 2024 00:20:54 GMT  
		Size: 2.4 MB (2357096 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3026aee966b73e41412b8087438d48685ce8f379d63a85e08b9b86ae85bc126`  
		Last Modified: Wed, 26 Jun 2024 00:20:54 GMT  
		Size: 8.9 KB (8885 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:597c6c8c1b37a7f28c8e68d359a468057f8cdebf32bbba8bb3da7216c8892bcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.6 MB (89596885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:692ef6a8954b1dd1dba6d176a5116a445559e8ad57bad698b93291398a48f9c5`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:54 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:54 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 May 2024 10:06:54 GMT
ADD file:a220ef67c41f76acc5934568443ce6faeaeba3de0ab529ab7b3b3172122c9adb in / 
# Mon, 13 May 2024 10:06:54 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:54 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.11     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Mon, 13 May 2024 10:06:54 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:53046b5e4efb6dbf3a776302592f40c8d0ac09b5738be07d28c7f3be6b7e1e08`  
		Last Modified: Mon, 03 Jun 2024 10:47:05 GMT  
		Size: 34.5 MB (34460693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7adc8001b0692991b898872029f11e409b314e9feb97ef5ad16d9398545a06d4`  
		Last Modified: Wed, 26 Jun 2024 00:57:03 GMT  
		Size: 55.1 MB (55136192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:40969993637c2f71327fce1eec639a5672da0880b7af33269ad45c7480716bf6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2370018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:240f62f096a8d7e0a3681697fd48b7c452bca5a80978b9bf607289c2fe004def`

```dockerfile
```

-	Layers:
	-	`sha256:a0cb36574a5a98b6125fbc2ca88fb89d86ba06a1c2bd3b4f1be410c745fb5135`  
		Last Modified: Wed, 26 Jun 2024 00:57:01 GMT  
		Size: 2.4 MB (2361395 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d947fe567f490337263bd671bd75096db3e6d0ca9c00fcadb5d7605bff09852`  
		Last Modified: Wed, 26 Jun 2024 00:57:01 GMT  
		Size: 8.6 KB (8623 bytes)  
		MIME: application/vnd.in-toto+json
