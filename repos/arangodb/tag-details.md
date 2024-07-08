<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `arangodb`

-	[`arangodb:3.11`](#arangodb311)
-	[`arangodb:3.11.10.1`](#arangodb311101)
-	[`arangodb:3.12`](#arangodb312)
-	[`arangodb:3.12.0.2`](#arangodb31202)
-	[`arangodb:latest`](#arangodblatest)

## `arangodb:3.11`

```console
$ docker pull arangodb@sha256:da7b99887647a8b51f977fcdb6bbdad29e61556b24c4c2837fb5c230ad408d74
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `arangodb:3.11` - linux; amd64

```console
$ docker pull arangodb@sha256:ad82c84912bca05834a66e35ebe062587fa7281ecc4019cb2b60f21d4c2a30d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.8 MB (198846775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e94935f4f4ae2048622c6084844a9a85d37d8a082461def691713eb8d330eee1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Thu, 20 Jun 2024 20:17:15 GMT
ADD file:cbcddefa487fb5085857fbba16854e06e53f93295bbf36ef1968a0b89835cad7 in / 
# Thu, 20 Jun 2024 20:17:16 GMT
CMD ["/bin/sh"]
# Sat, 06 Jul 2024 14:26:56 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Sat, 06 Jul 2024 14:26:56 GMT
ENV ARANGO_VERSION=3.11.10.1
# Sat, 06 Jul 2024 14:26:56 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb311/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg # buildkit
# Sat, 06 Jul 2024 14:26:56 GMT
ENV GLIBCXX_FORCE_NEW=1
# Sat, 06 Jul 2024 14:26:56 GMT
RUN echo "UTC" > /etc/timezone # buildkit
# Sat, 06 Jul 2024 14:26:56 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Sat, 06 Jul 2024 14:26:56 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Sat, 06 Jul 2024 14:26:56 GMT
COPY docker-foxx.sh /usr/bin/foxx # buildkit
# Sat, 06 Jul 2024 14:26:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 06 Jul 2024 14:26:56 GMT
EXPOSE map[8529/tcp:{}]
# Sat, 06 Jul 2024 14:26:56 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:f9202480295a4ef9cc62343dea568a5840b58bc68a1970045d30f3077a46a471`  
		Last Modified: Thu, 20 Jun 2024 20:18:01 GMT  
		Size: 3.4 MB (3389963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7609339653a5f9864d805dbe230da7f1003d92a766f59d07eb2f3235781f2cc3`  
		Last Modified: Mon, 08 Jul 2024 17:56:56 GMT  
		Size: 195.5 MB (195454327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3a9bb6f9fc892a6ce761c3c151e6432dee951f28dcc9c682df8bc89ec8e519a`  
		Last Modified: Mon, 08 Jul 2024 17:56:54 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c729c25cbed33abb7ea630453ca3f9680e0a32ca1021ddb2ac68968efaa7bcf1`  
		Last Modified: Mon, 08 Jul 2024 17:56:53 GMT  
		Size: 2.1 KB (2087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dddcd6cfd398fd1ecaa79922f5221b9393ee64622c2a86e55511cb49b5c7ed40`  
		Last Modified: Mon, 08 Jul 2024 17:56:53 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:3.11` - unknown; unknown

```console
$ docker pull arangodb@sha256:c333d10472fb2cb501e11bb2ae8fa2bfc009785d712163c0e1e418b7ed5f4542
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **906.6 KB (906646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c73f46858e66fd095c94fcec79f2e2adf3423d8328f64c3691b26e6e9d805eb`

```dockerfile
```

-	Layers:
	-	`sha256:4137c350d002997fba19882e4c74ed3a43b8e3be358d0a4ffe297ee0fff5984c`  
		Last Modified: Mon, 08 Jul 2024 17:56:53 GMT  
		Size: 891.0 KB (891036 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e931e6f86c042d712c8ee88ab6396d14c858996d5773cfe3211e2f91d2aa068`  
		Last Modified: Mon, 08 Jul 2024 17:56:53 GMT  
		Size: 15.6 KB (15610 bytes)  
		MIME: application/vnd.in-toto+json

### `arangodb:3.11` - linux; arm64 variant v8

```console
$ docker pull arangodb@sha256:d0eb4aa7d181a53127f639277b3e7e831f86a163b0c67bda75d996d9402d88e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.1 MB (202143840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7065b920e2d6c754c4a3923312efc44cd4654de6cea8f947ad2dde6816873922`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Thu, 20 Jun 2024 17:40:45 GMT
ADD file:deb5b1c3cd4e7a5be179620c767b9d7bfac29f2544596a65b760460e7a645c51 in / 
# Thu, 20 Jun 2024 17:40:45 GMT
CMD ["/bin/sh"]
# Sat, 06 Jul 2024 14:26:56 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Sat, 06 Jul 2024 14:26:56 GMT
ENV ARANGO_VERSION=3.11.10.1
# Sat, 06 Jul 2024 14:26:56 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb311/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg # buildkit
# Sat, 06 Jul 2024 14:26:56 GMT
ENV GLIBCXX_FORCE_NEW=1
# Sat, 06 Jul 2024 14:26:56 GMT
RUN echo "UTC" > /etc/timezone # buildkit
# Sat, 06 Jul 2024 14:26:56 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Sat, 06 Jul 2024 14:26:56 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Sat, 06 Jul 2024 14:26:56 GMT
COPY docker-foxx.sh /usr/bin/foxx # buildkit
# Sat, 06 Jul 2024 14:26:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 06 Jul 2024 14:26:56 GMT
EXPOSE map[8529/tcp:{}]
# Sat, 06 Jul 2024 14:26:56 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:e45a60384f0269bd8514e16cf71591639353996e62a144763c5e519b386ac31c`  
		Last Modified: Thu, 20 Jun 2024 17:41:39 GMT  
		Size: 3.3 MB (3272586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4c06d3c14c0c4fc5eb724f28a4dc7eb91b2ab65468e27d6193db2212155156d`  
		Last Modified: Mon, 08 Jul 2024 18:00:14 GMT  
		Size: 198.9 MB (198868768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e8ac1e50048c8c6a0e5beedc72254068134782f8324eea596e32829d731a069`  
		Last Modified: Mon, 08 Jul 2024 18:00:09 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d3eaa392a9620afd59c847283fe271df8375d3bb402c706ad4f9f09d963f301`  
		Last Modified: Mon, 08 Jul 2024 18:00:09 GMT  
		Size: 2.1 KB (2088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf880ad1b2bf2a85cce8c15c357fa985723be2f8c056535bdfbb83a233e29fed`  
		Last Modified: Mon, 08 Jul 2024 18:00:10 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:3.11` - unknown; unknown

```console
$ docker pull arangodb@sha256:43544065d0a31f854e33ebb77f7a9292b0501e9adff24557a85604b40c5f3ada
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1012210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b7e5fdee0dec565ce725f22e2b44d24be8ac440b89193bb7042b77900d72132`

```dockerfile
```

-	Layers:
	-	`sha256:55e50a4fae6df6f3bad14dd90586952835b99560943873af0ef87d6e008ccd2c`  
		Last Modified: Mon, 08 Jul 2024 18:00:10 GMT  
		Size: 996.3 KB (996323 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a53faa05d6299f14ce549c7203049dc24544fdf9884674b285b0ee891572a999`  
		Last Modified: Mon, 08 Jul 2024 18:00:10 GMT  
		Size: 15.9 KB (15887 bytes)  
		MIME: application/vnd.in-toto+json

## `arangodb:3.11.10.1`

```console
$ docker pull arangodb@sha256:da7b99887647a8b51f977fcdb6bbdad29e61556b24c4c2837fb5c230ad408d74
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `arangodb:3.11.10.1` - linux; amd64

```console
$ docker pull arangodb@sha256:ad82c84912bca05834a66e35ebe062587fa7281ecc4019cb2b60f21d4c2a30d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.8 MB (198846775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e94935f4f4ae2048622c6084844a9a85d37d8a082461def691713eb8d330eee1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Thu, 20 Jun 2024 20:17:15 GMT
ADD file:cbcddefa487fb5085857fbba16854e06e53f93295bbf36ef1968a0b89835cad7 in / 
# Thu, 20 Jun 2024 20:17:16 GMT
CMD ["/bin/sh"]
# Sat, 06 Jul 2024 14:26:56 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Sat, 06 Jul 2024 14:26:56 GMT
ENV ARANGO_VERSION=3.11.10.1
# Sat, 06 Jul 2024 14:26:56 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb311/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg # buildkit
# Sat, 06 Jul 2024 14:26:56 GMT
ENV GLIBCXX_FORCE_NEW=1
# Sat, 06 Jul 2024 14:26:56 GMT
RUN echo "UTC" > /etc/timezone # buildkit
# Sat, 06 Jul 2024 14:26:56 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Sat, 06 Jul 2024 14:26:56 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Sat, 06 Jul 2024 14:26:56 GMT
COPY docker-foxx.sh /usr/bin/foxx # buildkit
# Sat, 06 Jul 2024 14:26:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 06 Jul 2024 14:26:56 GMT
EXPOSE map[8529/tcp:{}]
# Sat, 06 Jul 2024 14:26:56 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:f9202480295a4ef9cc62343dea568a5840b58bc68a1970045d30f3077a46a471`  
		Last Modified: Thu, 20 Jun 2024 20:18:01 GMT  
		Size: 3.4 MB (3389963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7609339653a5f9864d805dbe230da7f1003d92a766f59d07eb2f3235781f2cc3`  
		Last Modified: Mon, 08 Jul 2024 17:56:56 GMT  
		Size: 195.5 MB (195454327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3a9bb6f9fc892a6ce761c3c151e6432dee951f28dcc9c682df8bc89ec8e519a`  
		Last Modified: Mon, 08 Jul 2024 17:56:54 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c729c25cbed33abb7ea630453ca3f9680e0a32ca1021ddb2ac68968efaa7bcf1`  
		Last Modified: Mon, 08 Jul 2024 17:56:53 GMT  
		Size: 2.1 KB (2087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dddcd6cfd398fd1ecaa79922f5221b9393ee64622c2a86e55511cb49b5c7ed40`  
		Last Modified: Mon, 08 Jul 2024 17:56:53 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:3.11.10.1` - unknown; unknown

```console
$ docker pull arangodb@sha256:c333d10472fb2cb501e11bb2ae8fa2bfc009785d712163c0e1e418b7ed5f4542
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **906.6 KB (906646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c73f46858e66fd095c94fcec79f2e2adf3423d8328f64c3691b26e6e9d805eb`

```dockerfile
```

-	Layers:
	-	`sha256:4137c350d002997fba19882e4c74ed3a43b8e3be358d0a4ffe297ee0fff5984c`  
		Last Modified: Mon, 08 Jul 2024 17:56:53 GMT  
		Size: 891.0 KB (891036 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e931e6f86c042d712c8ee88ab6396d14c858996d5773cfe3211e2f91d2aa068`  
		Last Modified: Mon, 08 Jul 2024 17:56:53 GMT  
		Size: 15.6 KB (15610 bytes)  
		MIME: application/vnd.in-toto+json

### `arangodb:3.11.10.1` - linux; arm64 variant v8

```console
$ docker pull arangodb@sha256:d0eb4aa7d181a53127f639277b3e7e831f86a163b0c67bda75d996d9402d88e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.1 MB (202143840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7065b920e2d6c754c4a3923312efc44cd4654de6cea8f947ad2dde6816873922`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Thu, 20 Jun 2024 17:40:45 GMT
ADD file:deb5b1c3cd4e7a5be179620c767b9d7bfac29f2544596a65b760460e7a645c51 in / 
# Thu, 20 Jun 2024 17:40:45 GMT
CMD ["/bin/sh"]
# Sat, 06 Jul 2024 14:26:56 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Sat, 06 Jul 2024 14:26:56 GMT
ENV ARANGO_VERSION=3.11.10.1
# Sat, 06 Jul 2024 14:26:56 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb311/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg # buildkit
# Sat, 06 Jul 2024 14:26:56 GMT
ENV GLIBCXX_FORCE_NEW=1
# Sat, 06 Jul 2024 14:26:56 GMT
RUN echo "UTC" > /etc/timezone # buildkit
# Sat, 06 Jul 2024 14:26:56 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Sat, 06 Jul 2024 14:26:56 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Sat, 06 Jul 2024 14:26:56 GMT
COPY docker-foxx.sh /usr/bin/foxx # buildkit
# Sat, 06 Jul 2024 14:26:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 06 Jul 2024 14:26:56 GMT
EXPOSE map[8529/tcp:{}]
# Sat, 06 Jul 2024 14:26:56 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:e45a60384f0269bd8514e16cf71591639353996e62a144763c5e519b386ac31c`  
		Last Modified: Thu, 20 Jun 2024 17:41:39 GMT  
		Size: 3.3 MB (3272586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4c06d3c14c0c4fc5eb724f28a4dc7eb91b2ab65468e27d6193db2212155156d`  
		Last Modified: Mon, 08 Jul 2024 18:00:14 GMT  
		Size: 198.9 MB (198868768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e8ac1e50048c8c6a0e5beedc72254068134782f8324eea596e32829d731a069`  
		Last Modified: Mon, 08 Jul 2024 18:00:09 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d3eaa392a9620afd59c847283fe271df8375d3bb402c706ad4f9f09d963f301`  
		Last Modified: Mon, 08 Jul 2024 18:00:09 GMT  
		Size: 2.1 KB (2088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf880ad1b2bf2a85cce8c15c357fa985723be2f8c056535bdfbb83a233e29fed`  
		Last Modified: Mon, 08 Jul 2024 18:00:10 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:3.11.10.1` - unknown; unknown

```console
$ docker pull arangodb@sha256:43544065d0a31f854e33ebb77f7a9292b0501e9adff24557a85604b40c5f3ada
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1012210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b7e5fdee0dec565ce725f22e2b44d24be8ac440b89193bb7042b77900d72132`

```dockerfile
```

-	Layers:
	-	`sha256:55e50a4fae6df6f3bad14dd90586952835b99560943873af0ef87d6e008ccd2c`  
		Last Modified: Mon, 08 Jul 2024 18:00:10 GMT  
		Size: 996.3 KB (996323 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a53faa05d6299f14ce549c7203049dc24544fdf9884674b285b0ee891572a999`  
		Last Modified: Mon, 08 Jul 2024 18:00:10 GMT  
		Size: 15.9 KB (15887 bytes)  
		MIME: application/vnd.in-toto+json

## `arangodb:3.12`

```console
$ docker pull arangodb@sha256:f1fa8f00c87ce7baea6f03085ed2a9cc4e3509dc098e8b2f164c3f2b4866554f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `arangodb:3.12` - linux; amd64

```console
$ docker pull arangodb@sha256:37e593cdb44146fbe64b0e404407a174df22ee9b379262d7cfb5c1e8d9f1d3f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.2 MB (302162975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f22810e5fe7473fcd9e24ea467d0dc5984aad8196b0e3623cbcc2a2ff2df6db4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 03 May 2024 11:13:37 GMT
ADD file:cbcddefa487fb5085857fbba16854e06e53f93295bbf36ef1968a0b89835cad7 in / 
# Fri, 03 May 2024 11:13:37 GMT
CMD ["/bin/sh"]
# Fri, 03 May 2024 11:13:37 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Fri, 03 May 2024 11:13:37 GMT
ENV ARANGO_VERSION=3.12.0.2
# Fri, 03 May 2024 11:13:37 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8003EDF6F05459984878D4A6C04AD0FD86FEC04D &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb312/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg # buildkit
# Fri, 03 May 2024 11:13:37 GMT
ENV GLIBCXX_FORCE_NEW=1
# Fri, 03 May 2024 11:13:37 GMT
RUN echo "UTC" > /etc/timezone # buildkit
# Fri, 03 May 2024 11:13:37 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Fri, 03 May 2024 11:13:37 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 03 May 2024 11:13:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 03 May 2024 11:13:37 GMT
EXPOSE map[8529/tcp:{}]
# Fri, 03 May 2024 11:13:37 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:f9202480295a4ef9cc62343dea568a5840b58bc68a1970045d30f3077a46a471`  
		Last Modified: Thu, 20 Jun 2024 20:18:01 GMT  
		Size: 3.4 MB (3389963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7e27b48c8fe935e54cfe60ef3e46dd5663da75405f18ec14ca26627c4c0ec87`  
		Last Modified: Thu, 20 Jun 2024 20:55:06 GMT  
		Size: 298.8 MB (298770856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6da899acd957c7dde28a69cae008d106b7d9798c02abb60bb68e929e3c61b61d`  
		Last Modified: Thu, 20 Jun 2024 20:55:01 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:162d83bef531a5f2661a61373aec6ef7d443a12b2d9da806265c6d695851db9c`  
		Last Modified: Thu, 20 Jun 2024 20:55:01 GMT  
		Size: 2.0 KB (2016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:3.12` - unknown; unknown

```console
$ docker pull arangodb@sha256:126383c986a5debc5b56aee1ccf6dc3fa57b7577ed67ba73690fda69dcb08261
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.9 KB (334942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee995ef825f2cfe6a628ef9d08c7e986f980253d80e7f85a75fbfaf7bcca8d54`

```dockerfile
```

-	Layers:
	-	`sha256:a3b0687d6d0d3de2777bc0f49d8351560656047f1a5fee01b3ab2aec6f348947`  
		Last Modified: Thu, 20 Jun 2024 20:55:01 GMT  
		Size: 320.8 KB (320773 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9cd4fecd31e6f68f71a9f873f644baa34aa92db09933642d69c17ee6853ee295`  
		Last Modified: Thu, 20 Jun 2024 20:55:01 GMT  
		Size: 14.2 KB (14169 bytes)  
		MIME: application/vnd.in-toto+json

### `arangodb:3.12` - linux; arm64 variant v8

```console
$ docker pull arangodb@sha256:2c16164a6bcc6cd3d9a2db7b22735d444d11b280643f7246798f46ee1a06b4c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.4 MB (304401348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b421284ca5ae90a3b49e7d898574254a6bca120654a639535efafa7c098c7076`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 03 May 2024 11:13:37 GMT
ADD file:deb5b1c3cd4e7a5be179620c767b9d7bfac29f2544596a65b760460e7a645c51 in / 
# Fri, 03 May 2024 11:13:37 GMT
CMD ["/bin/sh"]
# Fri, 03 May 2024 11:13:37 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Fri, 03 May 2024 11:13:37 GMT
ENV ARANGO_VERSION=3.12.0.2
# Fri, 03 May 2024 11:13:37 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8003EDF6F05459984878D4A6C04AD0FD86FEC04D &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb312/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg # buildkit
# Fri, 03 May 2024 11:13:37 GMT
ENV GLIBCXX_FORCE_NEW=1
# Fri, 03 May 2024 11:13:37 GMT
RUN echo "UTC" > /etc/timezone # buildkit
# Fri, 03 May 2024 11:13:37 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Fri, 03 May 2024 11:13:37 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 03 May 2024 11:13:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 03 May 2024 11:13:37 GMT
EXPOSE map[8529/tcp:{}]
# Fri, 03 May 2024 11:13:37 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:e45a60384f0269bd8514e16cf71591639353996e62a144763c5e519b386ac31c`  
		Last Modified: Thu, 20 Jun 2024 17:41:39 GMT  
		Size: 3.3 MB (3272586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77c6c464299418ea712993cb2f3c94ba89286c6e373921a08be6a506bf4e9b11`  
		Last Modified: Fri, 21 Jun 2024 01:57:28 GMT  
		Size: 301.1 MB (301126606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d363ca46bcc2fd49939bce38496b2623eb437a5da829687488a9aef0f12afe2`  
		Last Modified: Fri, 21 Jun 2024 01:57:22 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4484419ad40939d2a8d59586c4c93713ac0f3280c28fcc522b370497d0e10e8d`  
		Last Modified: Fri, 21 Jun 2024 01:57:22 GMT  
		Size: 2.0 KB (2016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:3.12` - unknown; unknown

```console
$ docker pull arangodb@sha256:9b962121ad204153e5b4779d1eaa7351b688a51a9f6b46eb0c2640124f885dc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **440.5 KB (440529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8edef511ac2d4b771c1de30e3cfd542ee56f0b9f6354a23e775c4f9adef7b17`

```dockerfile
```

-	Layers:
	-	`sha256:324d5c14295aef3b00263a4d8dcac0cea131640012528e5053cd58112f15c93d`  
		Last Modified: Fri, 21 Jun 2024 01:57:22 GMT  
		Size: 426.1 KB (426072 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f5a4286706b8b8e91d1a476201e00cd0437499fe79291b058585463add2d374`  
		Last Modified: Fri, 21 Jun 2024 01:57:22 GMT  
		Size: 14.5 KB (14457 bytes)  
		MIME: application/vnd.in-toto+json

## `arangodb:3.12.0.2`

```console
$ docker pull arangodb@sha256:f1fa8f00c87ce7baea6f03085ed2a9cc4e3509dc098e8b2f164c3f2b4866554f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `arangodb:3.12.0.2` - linux; amd64

```console
$ docker pull arangodb@sha256:37e593cdb44146fbe64b0e404407a174df22ee9b379262d7cfb5c1e8d9f1d3f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.2 MB (302162975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f22810e5fe7473fcd9e24ea467d0dc5984aad8196b0e3623cbcc2a2ff2df6db4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 03 May 2024 11:13:37 GMT
ADD file:cbcddefa487fb5085857fbba16854e06e53f93295bbf36ef1968a0b89835cad7 in / 
# Fri, 03 May 2024 11:13:37 GMT
CMD ["/bin/sh"]
# Fri, 03 May 2024 11:13:37 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Fri, 03 May 2024 11:13:37 GMT
ENV ARANGO_VERSION=3.12.0.2
# Fri, 03 May 2024 11:13:37 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8003EDF6F05459984878D4A6C04AD0FD86FEC04D &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb312/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg # buildkit
# Fri, 03 May 2024 11:13:37 GMT
ENV GLIBCXX_FORCE_NEW=1
# Fri, 03 May 2024 11:13:37 GMT
RUN echo "UTC" > /etc/timezone # buildkit
# Fri, 03 May 2024 11:13:37 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Fri, 03 May 2024 11:13:37 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 03 May 2024 11:13:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 03 May 2024 11:13:37 GMT
EXPOSE map[8529/tcp:{}]
# Fri, 03 May 2024 11:13:37 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:f9202480295a4ef9cc62343dea568a5840b58bc68a1970045d30f3077a46a471`  
		Last Modified: Thu, 20 Jun 2024 20:18:01 GMT  
		Size: 3.4 MB (3389963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7e27b48c8fe935e54cfe60ef3e46dd5663da75405f18ec14ca26627c4c0ec87`  
		Last Modified: Thu, 20 Jun 2024 20:55:06 GMT  
		Size: 298.8 MB (298770856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6da899acd957c7dde28a69cae008d106b7d9798c02abb60bb68e929e3c61b61d`  
		Last Modified: Thu, 20 Jun 2024 20:55:01 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:162d83bef531a5f2661a61373aec6ef7d443a12b2d9da806265c6d695851db9c`  
		Last Modified: Thu, 20 Jun 2024 20:55:01 GMT  
		Size: 2.0 KB (2016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:3.12.0.2` - unknown; unknown

```console
$ docker pull arangodb@sha256:126383c986a5debc5b56aee1ccf6dc3fa57b7577ed67ba73690fda69dcb08261
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.9 KB (334942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee995ef825f2cfe6a628ef9d08c7e986f980253d80e7f85a75fbfaf7bcca8d54`

```dockerfile
```

-	Layers:
	-	`sha256:a3b0687d6d0d3de2777bc0f49d8351560656047f1a5fee01b3ab2aec6f348947`  
		Last Modified: Thu, 20 Jun 2024 20:55:01 GMT  
		Size: 320.8 KB (320773 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9cd4fecd31e6f68f71a9f873f644baa34aa92db09933642d69c17ee6853ee295`  
		Last Modified: Thu, 20 Jun 2024 20:55:01 GMT  
		Size: 14.2 KB (14169 bytes)  
		MIME: application/vnd.in-toto+json

### `arangodb:3.12.0.2` - linux; arm64 variant v8

```console
$ docker pull arangodb@sha256:2c16164a6bcc6cd3d9a2db7b22735d444d11b280643f7246798f46ee1a06b4c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.4 MB (304401348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b421284ca5ae90a3b49e7d898574254a6bca120654a639535efafa7c098c7076`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 03 May 2024 11:13:37 GMT
ADD file:deb5b1c3cd4e7a5be179620c767b9d7bfac29f2544596a65b760460e7a645c51 in / 
# Fri, 03 May 2024 11:13:37 GMT
CMD ["/bin/sh"]
# Fri, 03 May 2024 11:13:37 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Fri, 03 May 2024 11:13:37 GMT
ENV ARANGO_VERSION=3.12.0.2
# Fri, 03 May 2024 11:13:37 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8003EDF6F05459984878D4A6C04AD0FD86FEC04D &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb312/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg # buildkit
# Fri, 03 May 2024 11:13:37 GMT
ENV GLIBCXX_FORCE_NEW=1
# Fri, 03 May 2024 11:13:37 GMT
RUN echo "UTC" > /etc/timezone # buildkit
# Fri, 03 May 2024 11:13:37 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Fri, 03 May 2024 11:13:37 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 03 May 2024 11:13:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 03 May 2024 11:13:37 GMT
EXPOSE map[8529/tcp:{}]
# Fri, 03 May 2024 11:13:37 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:e45a60384f0269bd8514e16cf71591639353996e62a144763c5e519b386ac31c`  
		Last Modified: Thu, 20 Jun 2024 17:41:39 GMT  
		Size: 3.3 MB (3272586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77c6c464299418ea712993cb2f3c94ba89286c6e373921a08be6a506bf4e9b11`  
		Last Modified: Fri, 21 Jun 2024 01:57:28 GMT  
		Size: 301.1 MB (301126606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d363ca46bcc2fd49939bce38496b2623eb437a5da829687488a9aef0f12afe2`  
		Last Modified: Fri, 21 Jun 2024 01:57:22 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4484419ad40939d2a8d59586c4c93713ac0f3280c28fcc522b370497d0e10e8d`  
		Last Modified: Fri, 21 Jun 2024 01:57:22 GMT  
		Size: 2.0 KB (2016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:3.12.0.2` - unknown; unknown

```console
$ docker pull arangodb@sha256:9b962121ad204153e5b4779d1eaa7351b688a51a9f6b46eb0c2640124f885dc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **440.5 KB (440529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8edef511ac2d4b771c1de30e3cfd542ee56f0b9f6354a23e775c4f9adef7b17`

```dockerfile
```

-	Layers:
	-	`sha256:324d5c14295aef3b00263a4d8dcac0cea131640012528e5053cd58112f15c93d`  
		Last Modified: Fri, 21 Jun 2024 01:57:22 GMT  
		Size: 426.1 KB (426072 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f5a4286706b8b8e91d1a476201e00cd0437499fe79291b058585463add2d374`  
		Last Modified: Fri, 21 Jun 2024 01:57:22 GMT  
		Size: 14.5 KB (14457 bytes)  
		MIME: application/vnd.in-toto+json

## `arangodb:latest`

```console
$ docker pull arangodb@sha256:f1fa8f00c87ce7baea6f03085ed2a9cc4e3509dc098e8b2f164c3f2b4866554f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `arangodb:latest` - linux; amd64

```console
$ docker pull arangodb@sha256:37e593cdb44146fbe64b0e404407a174df22ee9b379262d7cfb5c1e8d9f1d3f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.2 MB (302162975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f22810e5fe7473fcd9e24ea467d0dc5984aad8196b0e3623cbcc2a2ff2df6db4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 03 May 2024 11:13:37 GMT
ADD file:cbcddefa487fb5085857fbba16854e06e53f93295bbf36ef1968a0b89835cad7 in / 
# Fri, 03 May 2024 11:13:37 GMT
CMD ["/bin/sh"]
# Fri, 03 May 2024 11:13:37 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Fri, 03 May 2024 11:13:37 GMT
ENV ARANGO_VERSION=3.12.0.2
# Fri, 03 May 2024 11:13:37 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8003EDF6F05459984878D4A6C04AD0FD86FEC04D &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb312/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg # buildkit
# Fri, 03 May 2024 11:13:37 GMT
ENV GLIBCXX_FORCE_NEW=1
# Fri, 03 May 2024 11:13:37 GMT
RUN echo "UTC" > /etc/timezone # buildkit
# Fri, 03 May 2024 11:13:37 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Fri, 03 May 2024 11:13:37 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 03 May 2024 11:13:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 03 May 2024 11:13:37 GMT
EXPOSE map[8529/tcp:{}]
# Fri, 03 May 2024 11:13:37 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:f9202480295a4ef9cc62343dea568a5840b58bc68a1970045d30f3077a46a471`  
		Last Modified: Thu, 20 Jun 2024 20:18:01 GMT  
		Size: 3.4 MB (3389963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7e27b48c8fe935e54cfe60ef3e46dd5663da75405f18ec14ca26627c4c0ec87`  
		Last Modified: Thu, 20 Jun 2024 20:55:06 GMT  
		Size: 298.8 MB (298770856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6da899acd957c7dde28a69cae008d106b7d9798c02abb60bb68e929e3c61b61d`  
		Last Modified: Thu, 20 Jun 2024 20:55:01 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:162d83bef531a5f2661a61373aec6ef7d443a12b2d9da806265c6d695851db9c`  
		Last Modified: Thu, 20 Jun 2024 20:55:01 GMT  
		Size: 2.0 KB (2016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:latest` - unknown; unknown

```console
$ docker pull arangodb@sha256:126383c986a5debc5b56aee1ccf6dc3fa57b7577ed67ba73690fda69dcb08261
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.9 KB (334942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee995ef825f2cfe6a628ef9d08c7e986f980253d80e7f85a75fbfaf7bcca8d54`

```dockerfile
```

-	Layers:
	-	`sha256:a3b0687d6d0d3de2777bc0f49d8351560656047f1a5fee01b3ab2aec6f348947`  
		Last Modified: Thu, 20 Jun 2024 20:55:01 GMT  
		Size: 320.8 KB (320773 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9cd4fecd31e6f68f71a9f873f644baa34aa92db09933642d69c17ee6853ee295`  
		Last Modified: Thu, 20 Jun 2024 20:55:01 GMT  
		Size: 14.2 KB (14169 bytes)  
		MIME: application/vnd.in-toto+json

### `arangodb:latest` - linux; arm64 variant v8

```console
$ docker pull arangodb@sha256:2c16164a6bcc6cd3d9a2db7b22735d444d11b280643f7246798f46ee1a06b4c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.4 MB (304401348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b421284ca5ae90a3b49e7d898574254a6bca120654a639535efafa7c098c7076`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 03 May 2024 11:13:37 GMT
ADD file:deb5b1c3cd4e7a5be179620c767b9d7bfac29f2544596a65b760460e7a645c51 in / 
# Fri, 03 May 2024 11:13:37 GMT
CMD ["/bin/sh"]
# Fri, 03 May 2024 11:13:37 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Fri, 03 May 2024 11:13:37 GMT
ENV ARANGO_VERSION=3.12.0.2
# Fri, 03 May 2024 11:13:37 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8003EDF6F05459984878D4A6C04AD0FD86FEC04D &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb312/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg # buildkit
# Fri, 03 May 2024 11:13:37 GMT
ENV GLIBCXX_FORCE_NEW=1
# Fri, 03 May 2024 11:13:37 GMT
RUN echo "UTC" > /etc/timezone # buildkit
# Fri, 03 May 2024 11:13:37 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Fri, 03 May 2024 11:13:37 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 03 May 2024 11:13:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 03 May 2024 11:13:37 GMT
EXPOSE map[8529/tcp:{}]
# Fri, 03 May 2024 11:13:37 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:e45a60384f0269bd8514e16cf71591639353996e62a144763c5e519b386ac31c`  
		Last Modified: Thu, 20 Jun 2024 17:41:39 GMT  
		Size: 3.3 MB (3272586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77c6c464299418ea712993cb2f3c94ba89286c6e373921a08be6a506bf4e9b11`  
		Last Modified: Fri, 21 Jun 2024 01:57:28 GMT  
		Size: 301.1 MB (301126606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d363ca46bcc2fd49939bce38496b2623eb437a5da829687488a9aef0f12afe2`  
		Last Modified: Fri, 21 Jun 2024 01:57:22 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4484419ad40939d2a8d59586c4c93713ac0f3280c28fcc522b370497d0e10e8d`  
		Last Modified: Fri, 21 Jun 2024 01:57:22 GMT  
		Size: 2.0 KB (2016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:latest` - unknown; unknown

```console
$ docker pull arangodb@sha256:9b962121ad204153e5b4779d1eaa7351b688a51a9f6b46eb0c2640124f885dc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **440.5 KB (440529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8edef511ac2d4b771c1de30e3cfd542ee56f0b9f6354a23e775c4f9adef7b17`

```dockerfile
```

-	Layers:
	-	`sha256:324d5c14295aef3b00263a4d8dcac0cea131640012528e5053cd58112f15c93d`  
		Last Modified: Fri, 21 Jun 2024 01:57:22 GMT  
		Size: 426.1 KB (426072 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f5a4286706b8b8e91d1a476201e00cd0437499fe79291b058585463add2d374`  
		Last Modified: Fri, 21 Jun 2024 01:57:22 GMT  
		Size: 14.5 KB (14457 bytes)  
		MIME: application/vnd.in-toto+json
