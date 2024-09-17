## `sapmachine:21-jre-headless-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:c99e3df1f11cdac02c3096d492a80cf18c175af166f645ff79a0010e65392bd1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:21-jre-headless-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:fb1c423a724c06e2026dec58e15d1333bf97ab1ec55c87f543adb2f3841c7d2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.3 MB (88262100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25f5aec634e48f2f052abc5775005d0b537da73df547933ad367150fe9292b57`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:16 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 18 Jul 2024 15:16:16 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.4     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbebd286ab9fe1c68d065057513544ced0f15387b9beb7904a271ad5d0b0529d`  
		Last Modified: Tue, 17 Sep 2024 01:00:49 GMT  
		Size: 58.7 MB (58726412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:63d8f13d29b40e4729f86b57ac578ea9a2fe3075d3c179270e7f872704a8f5b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.5 KB (12534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7231b391fc3f23c2b72811a020473cb652d38846eced699c6aba1015f50626a`

```dockerfile
```

-	Layers:
	-	`sha256:26a3d55897c4af81a2038ba16c83cb8a24e5b2b100dceeb2e1b0cc92b013ca9d`  
		Last Modified: Tue, 17 Sep 2024 01:00:47 GMT  
		Size: 3.2 KB (3163 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3c60ef2fe719552725cd6a142e03ef4a3add5d13fe34ea4442976249b221c2c`  
		Last Modified: Tue, 17 Sep 2024 01:00:47 GMT  
		Size: 9.4 KB (9371 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre-headless-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:bac00d0958dbcef634b081250bce0b8d5d779c53ae86190b912af91417c89fc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.1 MB (85137162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:310ed0934876d9624829a059bb0f0ef963eb80d19056a22b2695d704ff6d2c6c`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:16 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 18 Jul 2024 15:16:16 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.4     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55efae7246fdd6886c8b9c658dbbd05ce4f08935019c545d9c4c3e9997429903`  
		Last Modified: Tue, 17 Sep 2024 03:24:32 GMT  
		Size: 57.8 MB (57778833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:599f20a575400be2c905ad522d4fde6968e41c4f9fe5d9e19d10132b5ed1cda8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2156907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:644de82913d834b88297ff1be2ad4794c6b008add7765c8c2884d7425aa62f45`

```dockerfile
```

-	Layers:
	-	`sha256:c7553d62abf6a0164f5d9db09122ddfa806c02f519d537aeda55fb0bee45ab3c`  
		Last Modified: Tue, 17 Sep 2024 03:24:30 GMT  
		Size: 2.1 MB (2147209 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e77800c6d3774de1c96ff0d33d1359ea1d7d6ef70b4d85f97a17a03934545c0f`  
		Last Modified: Tue, 17 Sep 2024 03:24:30 GMT  
		Size: 9.7 KB (9698 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre-headless-ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:8154a75df719f807adfcf2a274495d70bc0b4b0796d7711c04e19637d1c24962
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 MB (94560649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1114158044f6a24a3df87b0d4c0143560f464aa3d7daa0ce2ce0ef0ab6dbb322`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:16 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 18 Jul 2024 15:16:16 GMT
ADD file:8b71bf5e48ac3a761ff94511892207fd277c013e3c67b735b87f7338e62bb1f3 in / 
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.4     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dba61ec1b6dd390886f1d76b35eca5781c6c10a4708e19be61254f66bf4fe530`  
		Last Modified: Tue, 17 Sep 2024 02:42:36 GMT  
		Size: 60.1 MB (60112407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:cedeb4879cc938d1bd813139721d79eb07a01b7065a95074f62ef903e36ffc37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2160859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3e106b29664155625649c4a15b2924064c4db7a1563ad4f3980fd9ada0b8ef0`

```dockerfile
```

-	Layers:
	-	`sha256:6b0d0092888e31e442265fec72059c53168c587b8342342123709be26662f1da`  
		Last Modified: Tue, 17 Sep 2024 02:42:34 GMT  
		Size: 2.2 MB (2151436 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42ec7c62dcc4d0afd480e08ca7fbabfc7056b06970c6dc055023e59bbb06cd40`  
		Last Modified: Tue, 17 Sep 2024 02:42:34 GMT  
		Size: 9.4 KB (9423 bytes)  
		MIME: application/vnd.in-toto+json
