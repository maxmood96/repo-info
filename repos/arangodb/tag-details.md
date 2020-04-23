<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `arangodb`

-	[`arangodb:2.8`](#arangodb28)
-	[`arangodb:2.8.11`](#arangodb2811)
-	[`arangodb:3.2`](#arangodb32)
-	[`arangodb:3.2.17`](#arangodb3217)
-	[`arangodb:3.3`](#arangodb33)
-	[`arangodb:3.3.25`](#arangodb3325)
-	[`arangodb:3.4`](#arangodb34)
-	[`arangodb:3.4.9`](#arangodb349)
-	[`arangodb:3.5`](#arangodb35)
-	[`arangodb:3.5.4`](#arangodb354)
-	[`arangodb:3.6`](#arangodb36)
-	[`arangodb:3.6.3`](#arangodb363)
-	[`arangodb:latest`](#arangodblatest)

## `arangodb:2.8`

```console
$ docker pull arangodb@sha256:ecf03b9d25c642de4a11f2a210a43ada2c5812a802334fac51afcf939d1eeb79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `arangodb:2.8` - linux; amd64

```console
$ docker pull arangodb@sha256:1b977574238fc94ca9eaeeebc97a0c809259c27bf4e004b501cbce7ed8678343
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 MB (115105960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a789cd31bc216e39c8df0a564ed61365153f1f7c24cca2cf9f56c37187129de4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Thu, 23 Apr 2020 00:20:45 GMT
ADD file:545fa4a7e3efbc02fd93b103a922af1496dafa1358953302d1e9112772a46c6d in / 
# Thu, 23 Apr 2020 00:20:45 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 01:07:28 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Thu, 23 Apr 2020 01:07:29 GMT
RUN gpg --keyserver ha.pool.sks-keyservers.net --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B
# Thu, 23 Apr 2020 01:07:29 GMT
ENV ARCHITECTURE=amd64
# Thu, 23 Apr 2020 01:07:29 GMT
ENV ARANGO_VERSION=2.8.11
# Thu, 23 Apr 2020 01:07:29 GMT
ENV ARANGO_URL=https://download.arangodb.com/arangodb2/Debian_8.0
# Thu, 23 Apr 2020 01:07:29 GMT
ENV ARANGO_PACKAGE=arangodb_2.8.11_amd64.deb
# Thu, 23 Apr 2020 01:07:29 GMT
ENV ARANGO_PACKAGE_URL=https://download.arangodb.com/arangodb2/Debian_8.0/amd64/arangodb_2.8.11_amd64.deb
# Thu, 23 Apr 2020 01:07:30 GMT
ENV ARANGO_SIGNATURE_URL=https://download.arangodb.com/arangodb2/Debian_8.0/amd64/arangodb_2.8.11_amd64.deb.asc
# Thu, 23 Apr 2020 01:09:42 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         libgoogle-perftools4         ca-certificates         pwgen         wget     &&     rm -rf /var/lib/apt/lists/* &&     wget ${ARANGO_SIGNATURE_URL} &&           wget ${ARANGO_PACKAGE_URL} &&             gpg --verify ${ARANGO_PACKAGE}.asc &&     dpkg -i ${ARANGO_PACKAGE} &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=).*!\1 -!'         -e 's!^#\s*uid\s*=.*!uid = arangodb!'         -e 's!^#\s*gid\s*=.*!gid = arangodb!'         /etc/arangodb/arangod.conf     &&     apt-get purge -y --auto-remove ca-certificates wget &&     rm -f ${ARANGO_PACKAGE}*
# Thu, 23 Apr 2020 01:09:44 GMT
RUN chown arangodb:arangodb /var/lib/arangodb &&   chown arangodb:arangodb /var/lib/arangodb-apps
# Thu, 23 Apr 2020 01:09:44 GMT
VOLUME [/var/lib/arangodb /var/lib/arangodb-apps]
# Thu, 23 Apr 2020 01:09:44 GMT
COPY file:9a5bd6b5ab4e3a7842ac5f3e59bb9907920e9e2dc31d297c3676110b569a9d7e in /entrypoint.sh 
# Thu, 23 Apr 2020 01:09:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Apr 2020 01:09:44 GMT
EXPOSE 8529
# Thu, 23 Apr 2020 01:09:45 GMT
USER arangodb
# Thu, 23 Apr 2020 01:09:45 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:f4cbd35197708a9e2a08a980f6184996202108f81f5a0a2639bba1f4e070c56b`  
		Last Modified: Thu, 23 Apr 2020 00:25:23 GMT  
		Size: 54.4 MB (54390774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2550d3fda2993c9c325ca643a10ec8ed40b46aea06a2eb9ae5339277318db0d1`  
		Last Modified: Thu, 23 Apr 2020 01:11:49 GMT  
		Size: 8.6 KB (8594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b68bdcc4ec6efc00debbc3da6941a9f6aecffba728ff3923f59b6169ea4003de`  
		Last Modified: Thu, 23 Apr 2020 01:11:59 GMT  
		Size: 60.7 MB (60705330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfde3ac1940d49ac32e5c7d910d8bd7ab452ee2c3e0328fc97ab60a012443e91`  
		Last Modified: Thu, 23 Apr 2020 01:11:49 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1d7cde26ed084e761ee2a4184266296accba05582a4ef830a386f2c23153a24`  
		Last Modified: Thu, 23 Apr 2020 01:11:49 GMT  
		Size: 1.1 KB (1092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:2.8.11`

```console
$ docker pull arangodb@sha256:ecf03b9d25c642de4a11f2a210a43ada2c5812a802334fac51afcf939d1eeb79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `arangodb:2.8.11` - linux; amd64

```console
$ docker pull arangodb@sha256:1b977574238fc94ca9eaeeebc97a0c809259c27bf4e004b501cbce7ed8678343
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 MB (115105960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a789cd31bc216e39c8df0a564ed61365153f1f7c24cca2cf9f56c37187129de4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Thu, 23 Apr 2020 00:20:45 GMT
ADD file:545fa4a7e3efbc02fd93b103a922af1496dafa1358953302d1e9112772a46c6d in / 
# Thu, 23 Apr 2020 00:20:45 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 01:07:28 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Thu, 23 Apr 2020 01:07:29 GMT
RUN gpg --keyserver ha.pool.sks-keyservers.net --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B
# Thu, 23 Apr 2020 01:07:29 GMT
ENV ARCHITECTURE=amd64
# Thu, 23 Apr 2020 01:07:29 GMT
ENV ARANGO_VERSION=2.8.11
# Thu, 23 Apr 2020 01:07:29 GMT
ENV ARANGO_URL=https://download.arangodb.com/arangodb2/Debian_8.0
# Thu, 23 Apr 2020 01:07:29 GMT
ENV ARANGO_PACKAGE=arangodb_2.8.11_amd64.deb
# Thu, 23 Apr 2020 01:07:29 GMT
ENV ARANGO_PACKAGE_URL=https://download.arangodb.com/arangodb2/Debian_8.0/amd64/arangodb_2.8.11_amd64.deb
# Thu, 23 Apr 2020 01:07:30 GMT
ENV ARANGO_SIGNATURE_URL=https://download.arangodb.com/arangodb2/Debian_8.0/amd64/arangodb_2.8.11_amd64.deb.asc
# Thu, 23 Apr 2020 01:09:42 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         libgoogle-perftools4         ca-certificates         pwgen         wget     &&     rm -rf /var/lib/apt/lists/* &&     wget ${ARANGO_SIGNATURE_URL} &&           wget ${ARANGO_PACKAGE_URL} &&             gpg --verify ${ARANGO_PACKAGE}.asc &&     dpkg -i ${ARANGO_PACKAGE} &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=).*!\1 -!'         -e 's!^#\s*uid\s*=.*!uid = arangodb!'         -e 's!^#\s*gid\s*=.*!gid = arangodb!'         /etc/arangodb/arangod.conf     &&     apt-get purge -y --auto-remove ca-certificates wget &&     rm -f ${ARANGO_PACKAGE}*
# Thu, 23 Apr 2020 01:09:44 GMT
RUN chown arangodb:arangodb /var/lib/arangodb &&   chown arangodb:arangodb /var/lib/arangodb-apps
# Thu, 23 Apr 2020 01:09:44 GMT
VOLUME [/var/lib/arangodb /var/lib/arangodb-apps]
# Thu, 23 Apr 2020 01:09:44 GMT
COPY file:9a5bd6b5ab4e3a7842ac5f3e59bb9907920e9e2dc31d297c3676110b569a9d7e in /entrypoint.sh 
# Thu, 23 Apr 2020 01:09:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Apr 2020 01:09:44 GMT
EXPOSE 8529
# Thu, 23 Apr 2020 01:09:45 GMT
USER arangodb
# Thu, 23 Apr 2020 01:09:45 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:f4cbd35197708a9e2a08a980f6184996202108f81f5a0a2639bba1f4e070c56b`  
		Last Modified: Thu, 23 Apr 2020 00:25:23 GMT  
		Size: 54.4 MB (54390774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2550d3fda2993c9c325ca643a10ec8ed40b46aea06a2eb9ae5339277318db0d1`  
		Last Modified: Thu, 23 Apr 2020 01:11:49 GMT  
		Size: 8.6 KB (8594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b68bdcc4ec6efc00debbc3da6941a9f6aecffba728ff3923f59b6169ea4003de`  
		Last Modified: Thu, 23 Apr 2020 01:11:59 GMT  
		Size: 60.7 MB (60705330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfde3ac1940d49ac32e5c7d910d8bd7ab452ee2c3e0328fc97ab60a012443e91`  
		Last Modified: Thu, 23 Apr 2020 01:11:49 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1d7cde26ed084e761ee2a4184266296accba05582a4ef830a386f2c23153a24`  
		Last Modified: Thu, 23 Apr 2020 01:11:49 GMT  
		Size: 1.1 KB (1092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:3.2`

```console
$ docker pull arangodb@sha256:0bd774aeb929c0ea8d8329d24a8bcf44f7c97d7f20ec402afb75ee9bedf80bd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `arangodb:3.2` - linux; amd64

```console
$ docker pull arangodb@sha256:efcc00f8d9c409abd38966ac1d4df3a44e8722797b474ce574a2b203d0d8e750
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.5 MB (113546265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daf582c07dc8edf0d9648148445d56c3fd704521dcab0d22a1f98266b12acb8f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Thu, 23 Apr 2020 00:22:48 GMT
ADD file:21bf6969c2166c361350c07b1089a1a4b34b7cd3e802a602385d83c49f44a7f6 in / 
# Thu, 23 Apr 2020 00:22:48 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 01:09:59 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Thu, 23 Apr 2020 01:09:59 GMT
ENV ARCHITECTURE=amd64
# Thu, 23 Apr 2020 01:09:59 GMT
ENV DEB_PACKAGE_VERSION=1
# Thu, 23 Apr 2020 01:09:59 GMT
ENV ARANGO_VERSION=3.2.17
# Thu, 23 Apr 2020 01:10:00 GMT
ENV ARANGO_URL=https://download.arangodb.com/arangodb32/Debian_9.0
# Thu, 23 Apr 2020 01:10:00 GMT
ENV ARANGO_PACKAGE=arangodb3-3.2.17-1_amd64.deb
# Thu, 23 Apr 2020 01:10:00 GMT
ENV ARANGO_PACKAGE_URL=https://download.arangodb.com/arangodb32/Debian_9.0/amd64/arangodb3-3.2.17-1_amd64.deb
# Thu, 23 Apr 2020 01:10:00 GMT
ENV ARANGO_SIGNATURE_URL=https://download.arangodb.com/arangodb32/Debian_9.0/amd64/arangodb3-3.2.17-1_amd64.deb.asc
# Thu, 23 Apr 2020 01:10:07 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends gpg dirmngr     &&     rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 01:10:14 GMT
RUN gpg --keyserver hkps://hkps.pool.sks-keyservers.net --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B
# Thu, 23 Apr 2020 01:10:24 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         libjemalloc1         ca-certificates         pwgen         curl         numactl     &&     rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 01:10:25 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 23 Apr 2020 01:10:38 GMT
RUN curl --fail -O ${ARANGO_SIGNATURE_URL} &&           curl --fail -O ${ARANGO_PACKAGE_URL} &&             gpg --verify ${ARANGO_PACKAGE}.asc &&     (echo arangodb3 arangodb3/password password test | debconf-set-selections) &&     (echo arangodb3 arangodb3/password_again password test | debconf-set-selections) &&     DEBIAN_FRONTEND="noninteractive" dpkg -i ${ARANGO_PACKAGE} &&     rm -rf /var/lib/arangodb3/* &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf     && chgrp 0 /var/lib/arangodb3 /var/lib/arangodb3-apps     && chmod 775 /var/lib/arangodb3 /var/lib/arangodb3-apps     &&     rm -f ${ARANGO_PACKAGE}*
# Thu, 23 Apr 2020 01:10:39 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Thu, 23 Apr 2020 01:10:39 GMT
COPY file:01bdd453b032c9d383e66c7e6332049490bb7877724d3bb90d185f11336934d2 in /entrypoint.sh 
# Thu, 23 Apr 2020 01:10:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Apr 2020 01:10:39 GMT
EXPOSE 8529
# Thu, 23 Apr 2020 01:10:40 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:99760bc62448fbba69f6f0981d09bb4b7532e17362ecfb709141a7195d9b01d3`  
		Last Modified: Thu, 23 Apr 2020 00:27:35 GMT  
		Size: 45.4 MB (45375951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcb96a1b58efbed508b38c2c51fa4e97b4ca6271362f4536853685e525a1f3cb`  
		Last Modified: Thu, 23 Apr 2020 01:12:06 GMT  
		Size: 6.6 MB (6566497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0034c2f90c785ce1e7e80a3d317a225e41584f69f9ea25757a455a9ba4071574`  
		Last Modified: Thu, 23 Apr 2020 01:12:03 GMT  
		Size: 4.4 KB (4448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f995319d86afdd99bf584a04386ef70e48ca65d0320d6c20dac90d27ba2e955`  
		Last Modified: Thu, 23 Apr 2020 01:12:05 GMT  
		Size: 7.5 MB (7461604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e9579bdd0ff9f1470616155b94e3b5f3155762120aa2bce307fe6c363ec5180`  
		Last Modified: Thu, 23 Apr 2020 01:12:03 GMT  
		Size: 113.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8dc85393773effde62af3218d1b3e36e678a9e3ff558ecede0403efff0cac6f`  
		Last Modified: Thu, 23 Apr 2020 01:12:15 GMT  
		Size: 54.1 MB (54135614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f95b60fac063268004e554d3bae6f4a80db3861baaeedb001b8d4095d8d3055`  
		Last Modified: Thu, 23 Apr 2020 01:12:03 GMT  
		Size: 2.0 KB (2038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:3.2.17`

```console
$ docker pull arangodb@sha256:0bd774aeb929c0ea8d8329d24a8bcf44f7c97d7f20ec402afb75ee9bedf80bd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `arangodb:3.2.17` - linux; amd64

```console
$ docker pull arangodb@sha256:efcc00f8d9c409abd38966ac1d4df3a44e8722797b474ce574a2b203d0d8e750
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.5 MB (113546265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daf582c07dc8edf0d9648148445d56c3fd704521dcab0d22a1f98266b12acb8f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Thu, 23 Apr 2020 00:22:48 GMT
ADD file:21bf6969c2166c361350c07b1089a1a4b34b7cd3e802a602385d83c49f44a7f6 in / 
# Thu, 23 Apr 2020 00:22:48 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 01:09:59 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Thu, 23 Apr 2020 01:09:59 GMT
ENV ARCHITECTURE=amd64
# Thu, 23 Apr 2020 01:09:59 GMT
ENV DEB_PACKAGE_VERSION=1
# Thu, 23 Apr 2020 01:09:59 GMT
ENV ARANGO_VERSION=3.2.17
# Thu, 23 Apr 2020 01:10:00 GMT
ENV ARANGO_URL=https://download.arangodb.com/arangodb32/Debian_9.0
# Thu, 23 Apr 2020 01:10:00 GMT
ENV ARANGO_PACKAGE=arangodb3-3.2.17-1_amd64.deb
# Thu, 23 Apr 2020 01:10:00 GMT
ENV ARANGO_PACKAGE_URL=https://download.arangodb.com/arangodb32/Debian_9.0/amd64/arangodb3-3.2.17-1_amd64.deb
# Thu, 23 Apr 2020 01:10:00 GMT
ENV ARANGO_SIGNATURE_URL=https://download.arangodb.com/arangodb32/Debian_9.0/amd64/arangodb3-3.2.17-1_amd64.deb.asc
# Thu, 23 Apr 2020 01:10:07 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends gpg dirmngr     &&     rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 01:10:14 GMT
RUN gpg --keyserver hkps://hkps.pool.sks-keyservers.net --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B
# Thu, 23 Apr 2020 01:10:24 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         libjemalloc1         ca-certificates         pwgen         curl         numactl     &&     rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 01:10:25 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 23 Apr 2020 01:10:38 GMT
RUN curl --fail -O ${ARANGO_SIGNATURE_URL} &&           curl --fail -O ${ARANGO_PACKAGE_URL} &&             gpg --verify ${ARANGO_PACKAGE}.asc &&     (echo arangodb3 arangodb3/password password test | debconf-set-selections) &&     (echo arangodb3 arangodb3/password_again password test | debconf-set-selections) &&     DEBIAN_FRONTEND="noninteractive" dpkg -i ${ARANGO_PACKAGE} &&     rm -rf /var/lib/arangodb3/* &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf     && chgrp 0 /var/lib/arangodb3 /var/lib/arangodb3-apps     && chmod 775 /var/lib/arangodb3 /var/lib/arangodb3-apps     &&     rm -f ${ARANGO_PACKAGE}*
# Thu, 23 Apr 2020 01:10:39 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Thu, 23 Apr 2020 01:10:39 GMT
COPY file:01bdd453b032c9d383e66c7e6332049490bb7877724d3bb90d185f11336934d2 in /entrypoint.sh 
# Thu, 23 Apr 2020 01:10:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Apr 2020 01:10:39 GMT
EXPOSE 8529
# Thu, 23 Apr 2020 01:10:40 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:99760bc62448fbba69f6f0981d09bb4b7532e17362ecfb709141a7195d9b01d3`  
		Last Modified: Thu, 23 Apr 2020 00:27:35 GMT  
		Size: 45.4 MB (45375951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcb96a1b58efbed508b38c2c51fa4e97b4ca6271362f4536853685e525a1f3cb`  
		Last Modified: Thu, 23 Apr 2020 01:12:06 GMT  
		Size: 6.6 MB (6566497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0034c2f90c785ce1e7e80a3d317a225e41584f69f9ea25757a455a9ba4071574`  
		Last Modified: Thu, 23 Apr 2020 01:12:03 GMT  
		Size: 4.4 KB (4448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f995319d86afdd99bf584a04386ef70e48ca65d0320d6c20dac90d27ba2e955`  
		Last Modified: Thu, 23 Apr 2020 01:12:05 GMT  
		Size: 7.5 MB (7461604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e9579bdd0ff9f1470616155b94e3b5f3155762120aa2bce307fe6c363ec5180`  
		Last Modified: Thu, 23 Apr 2020 01:12:03 GMT  
		Size: 113.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8dc85393773effde62af3218d1b3e36e678a9e3ff558ecede0403efff0cac6f`  
		Last Modified: Thu, 23 Apr 2020 01:12:15 GMT  
		Size: 54.1 MB (54135614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f95b60fac063268004e554d3bae6f4a80db3861baaeedb001b8d4095d8d3055`  
		Last Modified: Thu, 23 Apr 2020 01:12:03 GMT  
		Size: 2.0 KB (2038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:3.3`

```console
$ docker pull arangodb@sha256:12536d8cfbb9f20f5c081670690d787986fa3c1bd31254c95943f614f2abdb45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `arangodb:3.3` - linux; amd64

```console
$ docker pull arangodb@sha256:977755e1641f2a8c40f4aecc3c52f474e89b40b5b701e579eb59c083360cd880
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.2 MB (117195910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:146055e3dff9d87be9bbe1514382284715ee6e73547b24435c87fd8de655b40c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Thu, 23 Apr 2020 00:22:48 GMT
ADD file:21bf6969c2166c361350c07b1089a1a4b34b7cd3e802a602385d83c49f44a7f6 in / 
# Thu, 23 Apr 2020 00:22:48 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 01:09:59 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Thu, 23 Apr 2020 01:09:59 GMT
ENV ARCHITECTURE=amd64
# Thu, 23 Apr 2020 01:09:59 GMT
ENV DEB_PACKAGE_VERSION=1
# Thu, 23 Apr 2020 01:10:45 GMT
ENV ARANGO_VERSION=3.3.25
# Thu, 23 Apr 2020 01:10:45 GMT
ENV ARANGO_URL=https://download.arangodb.com/arangodb33/Debian_9.0
# Thu, 23 Apr 2020 01:10:46 GMT
ENV ARANGO_PACKAGE=arangodb3-3.3.25-1_amd64.deb
# Thu, 23 Apr 2020 01:10:46 GMT
ENV ARANGO_PACKAGE_URL=https://download.arangodb.com/arangodb33/Debian_9.0/amd64/arangodb3-3.3.25-1_amd64.deb
# Thu, 23 Apr 2020 01:10:46 GMT
ENV ARANGO_SIGNATURE_URL=https://download.arangodb.com/arangodb33/Debian_9.0/amd64/arangodb3-3.3.25-1_amd64.deb.asc
# Thu, 23 Apr 2020 01:10:52 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         dirmngr         gpg     && rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 01:10:59 GMT
RUN gpg --keyserver hkps://hkps.pool.sks-keyservers.net --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B
# Thu, 23 Apr 2020 01:11:08 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         curl         libjemalloc1         libtasn1-6         numactl         openssl         pwgen         sensible-utils     && rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 01:11:09 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 23 Apr 2020 01:11:22 GMT
RUN curl --fail -O ${ARANGO_SIGNATURE_URL} &&           curl --fail -O ${ARANGO_PACKAGE_URL} &&             gpg --verify ${ARANGO_PACKAGE}.asc &&     (echo arangodb3 arangodb3/password password test | debconf-set-selections) &&     (echo arangodb3 arangodb3/password_again password test | debconf-set-selections) &&     DEBIAN_FRONTEND="noninteractive" dpkg -i ${ARANGO_PACKAGE} &&     rm -rf /var/lib/arangodb3/* &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf     && chgrp 0 /var/lib/arangodb3 /var/lib/arangodb3-apps     && chmod 775 /var/lib/arangodb3 /var/lib/arangodb3-apps     &&     rm -f ${ARANGO_PACKAGE}*
# Thu, 23 Apr 2020 01:11:23 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Thu, 23 Apr 2020 01:11:23 GMT
COPY file:01bdd453b032c9d383e66c7e6332049490bb7877724d3bb90d185f11336934d2 in /entrypoint.sh 
# Thu, 23 Apr 2020 01:11:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Apr 2020 01:11:24 GMT
EXPOSE 8529
# Thu, 23 Apr 2020 01:11:24 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:99760bc62448fbba69f6f0981d09bb4b7532e17362ecfb709141a7195d9b01d3`  
		Last Modified: Thu, 23 Apr 2020 00:27:35 GMT  
		Size: 45.4 MB (45375951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2051286653efb82132ee816c540901ff603e40e23d0eb4031cd503bc57d8257`  
		Last Modified: Thu, 23 Apr 2020 01:12:23 GMT  
		Size: 6.6 MB (6566541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16f25a00bba51380ca3a16a4d615c707fb1da19f32045b7205f1b6d14ccf7977`  
		Last Modified: Thu, 23 Apr 2020 01:12:20 GMT  
		Size: 4.4 KB (4446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acb2b6b94c57c7017260472d51b830bc63de4f0bad57d3d2f6aa20139e0616f7`  
		Last Modified: Thu, 23 Apr 2020 01:12:22 GMT  
		Size: 7.5 MB (7461511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d225e74d25cad7dc171284ca95e7d8e7c811d61a216ea9b9cfa8633fdf6d857e`  
		Last Modified: Thu, 23 Apr 2020 01:12:20 GMT  
		Size: 113.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05f6031a76cb1bd70f96c8f456323b1b8499af6156634d7ea9a9e351e0960c98`  
		Last Modified: Thu, 23 Apr 2020 01:12:36 GMT  
		Size: 57.8 MB (57785310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d1dda4b237bddf1be2c2a36a17e7e4ff297ab3476b950276c8ca7b598b3d4ee`  
		Last Modified: Thu, 23 Apr 2020 01:12:20 GMT  
		Size: 2.0 KB (2038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:3.3.25`

```console
$ docker pull arangodb@sha256:12536d8cfbb9f20f5c081670690d787986fa3c1bd31254c95943f614f2abdb45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `arangodb:3.3.25` - linux; amd64

```console
$ docker pull arangodb@sha256:977755e1641f2a8c40f4aecc3c52f474e89b40b5b701e579eb59c083360cd880
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.2 MB (117195910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:146055e3dff9d87be9bbe1514382284715ee6e73547b24435c87fd8de655b40c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Thu, 23 Apr 2020 00:22:48 GMT
ADD file:21bf6969c2166c361350c07b1089a1a4b34b7cd3e802a602385d83c49f44a7f6 in / 
# Thu, 23 Apr 2020 00:22:48 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 01:09:59 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Thu, 23 Apr 2020 01:09:59 GMT
ENV ARCHITECTURE=amd64
# Thu, 23 Apr 2020 01:09:59 GMT
ENV DEB_PACKAGE_VERSION=1
# Thu, 23 Apr 2020 01:10:45 GMT
ENV ARANGO_VERSION=3.3.25
# Thu, 23 Apr 2020 01:10:45 GMT
ENV ARANGO_URL=https://download.arangodb.com/arangodb33/Debian_9.0
# Thu, 23 Apr 2020 01:10:46 GMT
ENV ARANGO_PACKAGE=arangodb3-3.3.25-1_amd64.deb
# Thu, 23 Apr 2020 01:10:46 GMT
ENV ARANGO_PACKAGE_URL=https://download.arangodb.com/arangodb33/Debian_9.0/amd64/arangodb3-3.3.25-1_amd64.deb
# Thu, 23 Apr 2020 01:10:46 GMT
ENV ARANGO_SIGNATURE_URL=https://download.arangodb.com/arangodb33/Debian_9.0/amd64/arangodb3-3.3.25-1_amd64.deb.asc
# Thu, 23 Apr 2020 01:10:52 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         dirmngr         gpg     && rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 01:10:59 GMT
RUN gpg --keyserver hkps://hkps.pool.sks-keyservers.net --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B
# Thu, 23 Apr 2020 01:11:08 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         curl         libjemalloc1         libtasn1-6         numactl         openssl         pwgen         sensible-utils     && rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 01:11:09 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 23 Apr 2020 01:11:22 GMT
RUN curl --fail -O ${ARANGO_SIGNATURE_URL} &&           curl --fail -O ${ARANGO_PACKAGE_URL} &&             gpg --verify ${ARANGO_PACKAGE}.asc &&     (echo arangodb3 arangodb3/password password test | debconf-set-selections) &&     (echo arangodb3 arangodb3/password_again password test | debconf-set-selections) &&     DEBIAN_FRONTEND="noninteractive" dpkg -i ${ARANGO_PACKAGE} &&     rm -rf /var/lib/arangodb3/* &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf     && chgrp 0 /var/lib/arangodb3 /var/lib/arangodb3-apps     && chmod 775 /var/lib/arangodb3 /var/lib/arangodb3-apps     &&     rm -f ${ARANGO_PACKAGE}*
# Thu, 23 Apr 2020 01:11:23 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Thu, 23 Apr 2020 01:11:23 GMT
COPY file:01bdd453b032c9d383e66c7e6332049490bb7877724d3bb90d185f11336934d2 in /entrypoint.sh 
# Thu, 23 Apr 2020 01:11:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Apr 2020 01:11:24 GMT
EXPOSE 8529
# Thu, 23 Apr 2020 01:11:24 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:99760bc62448fbba69f6f0981d09bb4b7532e17362ecfb709141a7195d9b01d3`  
		Last Modified: Thu, 23 Apr 2020 00:27:35 GMT  
		Size: 45.4 MB (45375951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2051286653efb82132ee816c540901ff603e40e23d0eb4031cd503bc57d8257`  
		Last Modified: Thu, 23 Apr 2020 01:12:23 GMT  
		Size: 6.6 MB (6566541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16f25a00bba51380ca3a16a4d615c707fb1da19f32045b7205f1b6d14ccf7977`  
		Last Modified: Thu, 23 Apr 2020 01:12:20 GMT  
		Size: 4.4 KB (4446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acb2b6b94c57c7017260472d51b830bc63de4f0bad57d3d2f6aa20139e0616f7`  
		Last Modified: Thu, 23 Apr 2020 01:12:22 GMT  
		Size: 7.5 MB (7461511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d225e74d25cad7dc171284ca95e7d8e7c811d61a216ea9b9cfa8633fdf6d857e`  
		Last Modified: Thu, 23 Apr 2020 01:12:20 GMT  
		Size: 113.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05f6031a76cb1bd70f96c8f456323b1b8499af6156634d7ea9a9e351e0960c98`  
		Last Modified: Thu, 23 Apr 2020 01:12:36 GMT  
		Size: 57.8 MB (57785310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d1dda4b237bddf1be2c2a36a17e7e4ff297ab3476b950276c8ca7b598b3d4ee`  
		Last Modified: Thu, 23 Apr 2020 01:12:20 GMT  
		Size: 2.0 KB (2038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:3.4`

```console
$ docker pull arangodb@sha256:c32bcd08a60c1da2e96b02fa8db1ac2bde22b899245a4699c6449d16fe736e49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `arangodb:3.4` - linux; amd64

```console
$ docker pull arangodb@sha256:f354f9650ae0c94def2826c2aa13b289f6007fec9d4cd575d66e2a13a591456b
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.0 MB (101990383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a8bbe8672ebba1abbf2225666e1dfc2e153874340c4fa52b0b08755e5d85ad7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:06 GMT
ADD file:d48cac34fac385cbc1de6adfdd88300f76f9bbe346cd17e64fd834d042a98326 in / 
# Thu, 23 Jan 2020 16:53:06 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 17:09:20 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Sat, 25 Jan 2020 01:19:37 GMT
ENV ARANGO_VERSION=3.4.9
# Sat, 25 Jan 2020 01:19:38 GMT
ENV ARANGO_URL=https://download.arangodb.com/arangodb34/DEBIAN/amd64
# Sat, 25 Jan 2020 01:19:38 GMT
ENV ARANGO_PACKAGE=arangodb3_3.4.9-1_amd64.deb
# Sat, 25 Jan 2020 01:19:38 GMT
ENV ARANGO_PACKAGE_URL=https://download.arangodb.com/arangodb34/DEBIAN/amd64/arangodb3_3.4.9-1_amd64.deb
# Sat, 25 Jan 2020 01:19:38 GMT
ENV ARANGO_SIGNATURE_URL=https://download.arangodb.com/arangodb34/DEBIAN/amd64/arangodb3_3.4.9-1_amd64.deb.asc
# Sat, 25 Jan 2020 01:20:01 GMT
RUN apk add --no-cache gnupg pwgen nodejs npm binutils numactl &&     npm install -g foxx-cli &&     rm -rf /root/.npm &&     gpg --batch --keyserver hkps://hkps.pool.sks-keyservers.net --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     echo chgrp 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     echo chmod 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Sat, 25 Jan 2020 01:20:02 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Sat, 25 Jan 2020 01:20:02 GMT
COPY file:912d8c5e20cd837dbed0bf2608b1376ffffdd2d6de3e5b0af4cc869508443235 in /entrypoint.sh 
# Sat, 25 Jan 2020 01:20:02 GMT
COPY file:62d691f3a389929940df44ad84590c9019bdc0c8ce47667d5eb5dab0b2e66954 in /usr/bin/foxx 
# Sat, 25 Jan 2020 01:20:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 25 Jan 2020 01:20:03 GMT
EXPOSE 8529
# Sat, 25 Jan 2020 01:20:03 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:4167d3e149762ea326c26fc2fd4e36fdeb7d4e639408ad30f37b8f25ac285a98`  
		Last Modified: Thu, 23 Jan 2020 16:53:38 GMT  
		Size: 2.8 MB (2786962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd71998e0104b799cecf1dc84120cc5f654bcf1b1a01fec4714dd1b9e417ca52`  
		Last Modified: Sat, 25 Jan 2020 01:20:42 GMT  
		Size: 99.2 MB (99200973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fccb3bc7bf0a313e2619890c9ae7742e6e557d431b852716e5dd195d3808f442`  
		Last Modified: Sat, 25 Jan 2020 01:20:24 GMT  
		Size: 2.2 KB (2204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1993e49cf3e237fbc357190ae1df3b0b9b49ec93e21d2e4fb7f92d762443632`  
		Last Modified: Sat, 25 Jan 2020 01:20:24 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:3.4.9`

```console
$ docker pull arangodb@sha256:c32bcd08a60c1da2e96b02fa8db1ac2bde22b899245a4699c6449d16fe736e49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `arangodb:3.4.9` - linux; amd64

```console
$ docker pull arangodb@sha256:f354f9650ae0c94def2826c2aa13b289f6007fec9d4cd575d66e2a13a591456b
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.0 MB (101990383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a8bbe8672ebba1abbf2225666e1dfc2e153874340c4fa52b0b08755e5d85ad7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:06 GMT
ADD file:d48cac34fac385cbc1de6adfdd88300f76f9bbe346cd17e64fd834d042a98326 in / 
# Thu, 23 Jan 2020 16:53:06 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 17:09:20 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Sat, 25 Jan 2020 01:19:37 GMT
ENV ARANGO_VERSION=3.4.9
# Sat, 25 Jan 2020 01:19:38 GMT
ENV ARANGO_URL=https://download.arangodb.com/arangodb34/DEBIAN/amd64
# Sat, 25 Jan 2020 01:19:38 GMT
ENV ARANGO_PACKAGE=arangodb3_3.4.9-1_amd64.deb
# Sat, 25 Jan 2020 01:19:38 GMT
ENV ARANGO_PACKAGE_URL=https://download.arangodb.com/arangodb34/DEBIAN/amd64/arangodb3_3.4.9-1_amd64.deb
# Sat, 25 Jan 2020 01:19:38 GMT
ENV ARANGO_SIGNATURE_URL=https://download.arangodb.com/arangodb34/DEBIAN/amd64/arangodb3_3.4.9-1_amd64.deb.asc
# Sat, 25 Jan 2020 01:20:01 GMT
RUN apk add --no-cache gnupg pwgen nodejs npm binutils numactl &&     npm install -g foxx-cli &&     rm -rf /root/.npm &&     gpg --batch --keyserver hkps://hkps.pool.sks-keyservers.net --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     echo chgrp 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     echo chmod 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Sat, 25 Jan 2020 01:20:02 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Sat, 25 Jan 2020 01:20:02 GMT
COPY file:912d8c5e20cd837dbed0bf2608b1376ffffdd2d6de3e5b0af4cc869508443235 in /entrypoint.sh 
# Sat, 25 Jan 2020 01:20:02 GMT
COPY file:62d691f3a389929940df44ad84590c9019bdc0c8ce47667d5eb5dab0b2e66954 in /usr/bin/foxx 
# Sat, 25 Jan 2020 01:20:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 25 Jan 2020 01:20:03 GMT
EXPOSE 8529
# Sat, 25 Jan 2020 01:20:03 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:4167d3e149762ea326c26fc2fd4e36fdeb7d4e639408ad30f37b8f25ac285a98`  
		Last Modified: Thu, 23 Jan 2020 16:53:38 GMT  
		Size: 2.8 MB (2786962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd71998e0104b799cecf1dc84120cc5f654bcf1b1a01fec4714dd1b9e417ca52`  
		Last Modified: Sat, 25 Jan 2020 01:20:42 GMT  
		Size: 99.2 MB (99200973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fccb3bc7bf0a313e2619890c9ae7742e6e557d431b852716e5dd195d3808f442`  
		Last Modified: Sat, 25 Jan 2020 01:20:24 GMT  
		Size: 2.2 KB (2204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1993e49cf3e237fbc357190ae1df3b0b9b49ec93e21d2e4fb7f92d762443632`  
		Last Modified: Sat, 25 Jan 2020 01:20:24 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:3.5`

```console
$ docker pull arangodb@sha256:b935728c194b217f0e7a1cb91fd35d7d638034394d2a683879a2cf0a67c7e68c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `arangodb:3.5` - linux; amd64

```console
$ docker pull arangodb@sha256:62b5c1907ccfa74533c35e299f4e868f87d2efbf2a0761f8dfc7af99e14520e6
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.5 MB (110503803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:044bb2b6b89c3b4d8bfe2a489ed097fcf0c6a5729dc26a2fdc97e435be972cff`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:06 GMT
ADD file:d48cac34fac385cbc1de6adfdd88300f76f9bbe346cd17e64fd834d042a98326 in / 
# Thu, 23 Jan 2020 16:53:06 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 17:09:20 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Thu, 23 Jan 2020 17:09:53 GMT
ENV ARANGO_VERSION=3.5.4
# Thu, 23 Jan 2020 17:09:53 GMT
ENV ARANGO_URL=https://download.arangodb.com/arangodb35/DEBIAN/amd64
# Thu, 23 Jan 2020 17:09:53 GMT
ENV ARANGO_PACKAGE=arangodb3_3.5.4-1_amd64.deb
# Thu, 23 Jan 2020 17:09:53 GMT
ENV ARANGO_PACKAGE_URL=https://download.arangodb.com/arangodb35/DEBIAN/amd64/arangodb3_3.5.4-1_amd64.deb
# Thu, 23 Jan 2020 17:09:53 GMT
ENV ARANGO_SIGNATURE_URL=https://download.arangodb.com/arangodb35/DEBIAN/amd64/arangodb3_3.5.4-1_amd64.deb.asc
# Thu, 23 Jan 2020 17:10:18 GMT
RUN apk add --no-cache gnupg pwgen nodejs npm binutils numactl numactl-tools &&     npm install -g foxx-cli &&     rm -rf /root/.npm &&     gpg --batch --keyserver hkps://hkps.pool.sks-keyservers.net --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     echo chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     echo chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Thu, 23 Jan 2020 17:10:19 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Thu, 23 Jan 2020 17:10:19 GMT
COPY file:912d8c5e20cd837dbed0bf2608b1376ffffdd2d6de3e5b0af4cc869508443235 in /entrypoint.sh 
# Thu, 23 Jan 2020 17:10:19 GMT
COPY file:62d691f3a389929940df44ad84590c9019bdc0c8ce47667d5eb5dab0b2e66954 in /usr/bin/foxx 
# Thu, 23 Jan 2020 17:10:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Jan 2020 17:10:19 GMT
EXPOSE 8529
# Thu, 23 Jan 2020 17:10:19 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:4167d3e149762ea326c26fc2fd4e36fdeb7d4e639408ad30f37b8f25ac285a98`  
		Last Modified: Thu, 23 Jan 2020 16:53:38 GMT  
		Size: 2.8 MB (2786962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6b894beb4738887c1152b7d7f1549123f4b522147acd9c92006b54013e40134`  
		Last Modified: Thu, 23 Jan 2020 17:11:48 GMT  
		Size: 107.7 MB (107714396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f36e3ba3ee3abb406b1eb2d88f2e4f920861b71d868af63b966e113f57b22c5b`  
		Last Modified: Thu, 23 Jan 2020 17:11:29 GMT  
		Size: 2.2 KB (2204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ded7a88e79982f58478fb0b3dddd36d284712c45855b584ed2a356730b471f91`  
		Last Modified: Thu, 23 Jan 2020 17:11:30 GMT  
		Size: 241.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:3.5.4`

```console
$ docker pull arangodb@sha256:b935728c194b217f0e7a1cb91fd35d7d638034394d2a683879a2cf0a67c7e68c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `arangodb:3.5.4` - linux; amd64

```console
$ docker pull arangodb@sha256:62b5c1907ccfa74533c35e299f4e868f87d2efbf2a0761f8dfc7af99e14520e6
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.5 MB (110503803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:044bb2b6b89c3b4d8bfe2a489ed097fcf0c6a5729dc26a2fdc97e435be972cff`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:06 GMT
ADD file:d48cac34fac385cbc1de6adfdd88300f76f9bbe346cd17e64fd834d042a98326 in / 
# Thu, 23 Jan 2020 16:53:06 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 17:09:20 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Thu, 23 Jan 2020 17:09:53 GMT
ENV ARANGO_VERSION=3.5.4
# Thu, 23 Jan 2020 17:09:53 GMT
ENV ARANGO_URL=https://download.arangodb.com/arangodb35/DEBIAN/amd64
# Thu, 23 Jan 2020 17:09:53 GMT
ENV ARANGO_PACKAGE=arangodb3_3.5.4-1_amd64.deb
# Thu, 23 Jan 2020 17:09:53 GMT
ENV ARANGO_PACKAGE_URL=https://download.arangodb.com/arangodb35/DEBIAN/amd64/arangodb3_3.5.4-1_amd64.deb
# Thu, 23 Jan 2020 17:09:53 GMT
ENV ARANGO_SIGNATURE_URL=https://download.arangodb.com/arangodb35/DEBIAN/amd64/arangodb3_3.5.4-1_amd64.deb.asc
# Thu, 23 Jan 2020 17:10:18 GMT
RUN apk add --no-cache gnupg pwgen nodejs npm binutils numactl numactl-tools &&     npm install -g foxx-cli &&     rm -rf /root/.npm &&     gpg --batch --keyserver hkps://hkps.pool.sks-keyservers.net --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     echo chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     echo chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Thu, 23 Jan 2020 17:10:19 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Thu, 23 Jan 2020 17:10:19 GMT
COPY file:912d8c5e20cd837dbed0bf2608b1376ffffdd2d6de3e5b0af4cc869508443235 in /entrypoint.sh 
# Thu, 23 Jan 2020 17:10:19 GMT
COPY file:62d691f3a389929940df44ad84590c9019bdc0c8ce47667d5eb5dab0b2e66954 in /usr/bin/foxx 
# Thu, 23 Jan 2020 17:10:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Jan 2020 17:10:19 GMT
EXPOSE 8529
# Thu, 23 Jan 2020 17:10:19 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:4167d3e149762ea326c26fc2fd4e36fdeb7d4e639408ad30f37b8f25ac285a98`  
		Last Modified: Thu, 23 Jan 2020 16:53:38 GMT  
		Size: 2.8 MB (2786962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6b894beb4738887c1152b7d7f1549123f4b522147acd9c92006b54013e40134`  
		Last Modified: Thu, 23 Jan 2020 17:11:48 GMT  
		Size: 107.7 MB (107714396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f36e3ba3ee3abb406b1eb2d88f2e4f920861b71d868af63b966e113f57b22c5b`  
		Last Modified: Thu, 23 Jan 2020 17:11:29 GMT  
		Size: 2.2 KB (2204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ded7a88e79982f58478fb0b3dddd36d284712c45855b584ed2a356730b471f91`  
		Last Modified: Thu, 23 Jan 2020 17:11:30 GMT  
		Size: 241.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:3.6`

```console
$ docker pull arangodb@sha256:cfa7fa806d66aa2677034100b42ec87d479dc9c6600d83aa1e4a12310c3fb3b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `arangodb:3.6` - linux; amd64

```console
$ docker pull arangodb@sha256:d10f34e0f53e9d1a1f5fd79856253a632269791fc03f38eea5eac4ed0e4ddc33
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.7 MB (110717994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4178648ffd4bbe76b16899ad5a0bdc735963d7658e3c47a610de29c28c9ef7e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:06 GMT
ADD file:d48cac34fac385cbc1de6adfdd88300f76f9bbe346cd17e64fd834d042a98326 in / 
# Thu, 23 Jan 2020 16:53:06 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 17:09:20 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Wed, 22 Apr 2020 23:20:49 GMT
ENV ARANGO_VERSION=3.6.3
# Wed, 22 Apr 2020 23:20:49 GMT
ENV ARANGO_URL=https://download.arangodb.com/arangodb36/DEBIAN/amd64
# Wed, 22 Apr 2020 23:20:50 GMT
ENV ARANGO_PACKAGE=arangodb3_3.6.3-1_amd64.deb
# Wed, 22 Apr 2020 23:20:50 GMT
ENV ARANGO_PACKAGE_URL=https://download.arangodb.com/arangodb36/DEBIAN/amd64/arangodb3_3.6.3-1_amd64.deb
# Wed, 22 Apr 2020 23:20:50 GMT
ENV ARANGO_SIGNATURE_URL=https://download.arangodb.com/arangodb36/DEBIAN/amd64/arangodb3_3.6.3-1_amd64.deb.asc
# Wed, 22 Apr 2020 23:21:14 GMT
RUN apk add --no-cache gnupg pwgen nodejs npm binutils numactl numactl-tools &&     npm install -g foxx-cli &&     rm -rf /root/.npm &&     gpg --batch --keyserver hkps://hkps.pool.sks-keyservers.net --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     echo chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     echo chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Wed, 22 Apr 2020 23:21:14 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Wed, 22 Apr 2020 23:21:15 GMT
COPY file:912d8c5e20cd837dbed0bf2608b1376ffffdd2d6de3e5b0af4cc869508443235 in /entrypoint.sh 
# Wed, 22 Apr 2020 23:21:15 GMT
COPY file:62d691f3a389929940df44ad84590c9019bdc0c8ce47667d5eb5dab0b2e66954 in /usr/bin/foxx 
# Wed, 22 Apr 2020 23:21:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Apr 2020 23:21:15 GMT
EXPOSE 8529
# Wed, 22 Apr 2020 23:21:15 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:4167d3e149762ea326c26fc2fd4e36fdeb7d4e639408ad30f37b8f25ac285a98`  
		Last Modified: Thu, 23 Jan 2020 16:53:38 GMT  
		Size: 2.8 MB (2786962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ad5ab8ff5bda63b2d74cddeca87157dc16158cabe1ae0042e7389a4bf90ec77`  
		Last Modified: Wed, 22 Apr 2020 23:21:48 GMT  
		Size: 107.9 MB (107928588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7437ce257aeecca0baec1488aecef796f734a25a972cf2eae7d586766d0c6854`  
		Last Modified: Wed, 22 Apr 2020 23:21:30 GMT  
		Size: 2.2 KB (2202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90ff9411eaece6ebcf7b7fb929cbee662ddd493b9cf2c10427a4b602c9ba32c3`  
		Last Modified: Wed, 22 Apr 2020 23:21:29 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:3.6.3`

```console
$ docker pull arangodb@sha256:cfa7fa806d66aa2677034100b42ec87d479dc9c6600d83aa1e4a12310c3fb3b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `arangodb:3.6.3` - linux; amd64

```console
$ docker pull arangodb@sha256:d10f34e0f53e9d1a1f5fd79856253a632269791fc03f38eea5eac4ed0e4ddc33
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.7 MB (110717994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4178648ffd4bbe76b16899ad5a0bdc735963d7658e3c47a610de29c28c9ef7e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:06 GMT
ADD file:d48cac34fac385cbc1de6adfdd88300f76f9bbe346cd17e64fd834d042a98326 in / 
# Thu, 23 Jan 2020 16:53:06 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 17:09:20 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Wed, 22 Apr 2020 23:20:49 GMT
ENV ARANGO_VERSION=3.6.3
# Wed, 22 Apr 2020 23:20:49 GMT
ENV ARANGO_URL=https://download.arangodb.com/arangodb36/DEBIAN/amd64
# Wed, 22 Apr 2020 23:20:50 GMT
ENV ARANGO_PACKAGE=arangodb3_3.6.3-1_amd64.deb
# Wed, 22 Apr 2020 23:20:50 GMT
ENV ARANGO_PACKAGE_URL=https://download.arangodb.com/arangodb36/DEBIAN/amd64/arangodb3_3.6.3-1_amd64.deb
# Wed, 22 Apr 2020 23:20:50 GMT
ENV ARANGO_SIGNATURE_URL=https://download.arangodb.com/arangodb36/DEBIAN/amd64/arangodb3_3.6.3-1_amd64.deb.asc
# Wed, 22 Apr 2020 23:21:14 GMT
RUN apk add --no-cache gnupg pwgen nodejs npm binutils numactl numactl-tools &&     npm install -g foxx-cli &&     rm -rf /root/.npm &&     gpg --batch --keyserver hkps://hkps.pool.sks-keyservers.net --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     echo chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     echo chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Wed, 22 Apr 2020 23:21:14 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Wed, 22 Apr 2020 23:21:15 GMT
COPY file:912d8c5e20cd837dbed0bf2608b1376ffffdd2d6de3e5b0af4cc869508443235 in /entrypoint.sh 
# Wed, 22 Apr 2020 23:21:15 GMT
COPY file:62d691f3a389929940df44ad84590c9019bdc0c8ce47667d5eb5dab0b2e66954 in /usr/bin/foxx 
# Wed, 22 Apr 2020 23:21:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Apr 2020 23:21:15 GMT
EXPOSE 8529
# Wed, 22 Apr 2020 23:21:15 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:4167d3e149762ea326c26fc2fd4e36fdeb7d4e639408ad30f37b8f25ac285a98`  
		Last Modified: Thu, 23 Jan 2020 16:53:38 GMT  
		Size: 2.8 MB (2786962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ad5ab8ff5bda63b2d74cddeca87157dc16158cabe1ae0042e7389a4bf90ec77`  
		Last Modified: Wed, 22 Apr 2020 23:21:48 GMT  
		Size: 107.9 MB (107928588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7437ce257aeecca0baec1488aecef796f734a25a972cf2eae7d586766d0c6854`  
		Last Modified: Wed, 22 Apr 2020 23:21:30 GMT  
		Size: 2.2 KB (2202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90ff9411eaece6ebcf7b7fb929cbee662ddd493b9cf2c10427a4b602c9ba32c3`  
		Last Modified: Wed, 22 Apr 2020 23:21:29 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:latest`

```console
$ docker pull arangodb@sha256:cfa7fa806d66aa2677034100b42ec87d479dc9c6600d83aa1e4a12310c3fb3b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `arangodb:latest` - linux; amd64

```console
$ docker pull arangodb@sha256:d10f34e0f53e9d1a1f5fd79856253a632269791fc03f38eea5eac4ed0e4ddc33
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.7 MB (110717994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4178648ffd4bbe76b16899ad5a0bdc735963d7658e3c47a610de29c28c9ef7e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:06 GMT
ADD file:d48cac34fac385cbc1de6adfdd88300f76f9bbe346cd17e64fd834d042a98326 in / 
# Thu, 23 Jan 2020 16:53:06 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 17:09:20 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Wed, 22 Apr 2020 23:20:49 GMT
ENV ARANGO_VERSION=3.6.3
# Wed, 22 Apr 2020 23:20:49 GMT
ENV ARANGO_URL=https://download.arangodb.com/arangodb36/DEBIAN/amd64
# Wed, 22 Apr 2020 23:20:50 GMT
ENV ARANGO_PACKAGE=arangodb3_3.6.3-1_amd64.deb
# Wed, 22 Apr 2020 23:20:50 GMT
ENV ARANGO_PACKAGE_URL=https://download.arangodb.com/arangodb36/DEBIAN/amd64/arangodb3_3.6.3-1_amd64.deb
# Wed, 22 Apr 2020 23:20:50 GMT
ENV ARANGO_SIGNATURE_URL=https://download.arangodb.com/arangodb36/DEBIAN/amd64/arangodb3_3.6.3-1_amd64.deb.asc
# Wed, 22 Apr 2020 23:21:14 GMT
RUN apk add --no-cache gnupg pwgen nodejs npm binutils numactl numactl-tools &&     npm install -g foxx-cli &&     rm -rf /root/.npm &&     gpg --batch --keyserver hkps://hkps.pool.sks-keyservers.net --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     echo chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     echo chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Wed, 22 Apr 2020 23:21:14 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Wed, 22 Apr 2020 23:21:15 GMT
COPY file:912d8c5e20cd837dbed0bf2608b1376ffffdd2d6de3e5b0af4cc869508443235 in /entrypoint.sh 
# Wed, 22 Apr 2020 23:21:15 GMT
COPY file:62d691f3a389929940df44ad84590c9019bdc0c8ce47667d5eb5dab0b2e66954 in /usr/bin/foxx 
# Wed, 22 Apr 2020 23:21:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Apr 2020 23:21:15 GMT
EXPOSE 8529
# Wed, 22 Apr 2020 23:21:15 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:4167d3e149762ea326c26fc2fd4e36fdeb7d4e639408ad30f37b8f25ac285a98`  
		Last Modified: Thu, 23 Jan 2020 16:53:38 GMT  
		Size: 2.8 MB (2786962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ad5ab8ff5bda63b2d74cddeca87157dc16158cabe1ae0042e7389a4bf90ec77`  
		Last Modified: Wed, 22 Apr 2020 23:21:48 GMT  
		Size: 107.9 MB (107928588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7437ce257aeecca0baec1488aecef796f734a25a972cf2eae7d586766d0c6854`  
		Last Modified: Wed, 22 Apr 2020 23:21:30 GMT  
		Size: 2.2 KB (2202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90ff9411eaece6ebcf7b7fb929cbee662ddd493b9cf2c10427a4b602c9ba32c3`  
		Last Modified: Wed, 22 Apr 2020 23:21:29 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
