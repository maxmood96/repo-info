<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `arangodb`

-	[`arangodb:3.11`](#arangodb311)
-	[`arangodb:3.11.12`](#arangodb31112)
-	[`arangodb:3.12`](#arangodb312)
-	[`arangodb:3.12.3`](#arangodb3123)
-	[`arangodb:latest`](#arangodblatest)

## `arangodb:3.11`

```console
$ docker pull arangodb@sha256:7c9360b3fa68ddbe716683d186ea837a0919ec1ae6831f9fe0b0aa980a83665f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `arangodb:3.11` - linux; amd64

```console
$ docker pull arangodb@sha256:70dc40bb8c692d451c10fa1abb064e6b74c2a84adb95bad0bdeb2ce4ea9628ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.8 MB (199785440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:796ea94a1af8c1efc023f3d5910cf4599973ca8ca593fb1cff4238c39296dd08`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 06 Sep 2024 12:03:22 GMT
ADD alpine-minirootfs-3.18.9-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:03:22 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 15:32:12 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Fri, 13 Dec 2024 15:32:12 GMT
ENV ARANGO_VERSION=3.11.12
# Fri, 13 Dec 2024 15:32:12 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8003EDF6F05459984878D4A6C04AD0FD86FEC04D &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb311/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg # buildkit
# Fri, 13 Dec 2024 15:32:12 GMT
ENV GLIBCXX_FORCE_NEW=1
# Fri, 13 Dec 2024 15:32:12 GMT
RUN echo "UTC" > /etc/timezone # buildkit
# Fri, 13 Dec 2024 15:32:12 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Fri, 13 Dec 2024 15:32:12 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 13 Dec 2024 15:32:12 GMT
COPY docker-foxx.sh /usr/bin/foxx # buildkit
# Fri, 13 Dec 2024 15:32:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 13 Dec 2024 15:32:12 GMT
EXPOSE map[8529/tcp:{}]
# Fri, 13 Dec 2024 15:32:12 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:dc0decf4841d19b14e836c2d82bd5cb9540fb5e0d1359549ca243f49036557e9`  
		Last Modified: Mon, 09 Sep 2024 07:02:43 GMT  
		Size: 3.4 MB (3416401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45f17cede5bdc04f484ba1810f73078fd3bca8108386cd20628bf8d92e13db7c`  
		Last Modified: Fri, 13 Dec 2024 22:27:44 GMT  
		Size: 196.4 MB (196366554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b790a8d1ad32ba7ee3b100786d019e1f17b05ce14aed5e1e6a22bc6f62bf724`  
		Last Modified: Fri, 13 Dec 2024 22:27:41 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e80a781f9073f0535004918fb58b6c470b972b81da5d7d30fc3160ff14cdb4`  
		Last Modified: Fri, 13 Dec 2024 22:27:41 GMT  
		Size: 2.1 KB (2086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c33c7b88075b05861a6248d41dbc51bce4b936160275c4c728d8c23cf49bc12f`  
		Last Modified: Fri, 13 Dec 2024 22:27:41 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:3.11` - unknown; unknown

```console
$ docker pull arangodb@sha256:acc94806a78ee7c55a8321afbd031f6757eeb962a69859c7354ef5608c6320fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1082775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c949bf1acba75e332e343bf08e8b4f41a151a8b1c8ded609b0f3aa06a82d268`

```dockerfile
```

-	Layers:
	-	`sha256:6c4a834ee2b1bc19af42ff28bd9df99203b7f771f14e194f1acd2b1d6d03a531`  
		Last Modified: Fri, 13 Dec 2024 22:27:41 GMT  
		Size: 1.1 MB (1066919 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7de48459d033d09a7225423437d56a2854bbe4527a99944720ad308122edcdae`  
		Last Modified: Fri, 13 Dec 2024 22:27:41 GMT  
		Size: 15.9 KB (15856 bytes)  
		MIME: application/vnd.in-toto+json

### `arangodb:3.11` - linux; arm64 variant v8

```console
$ docker pull arangodb@sha256:e838a8706270b751ce562441182832a3a869c61ec44daf2eedd89c8d6597dcd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.5 MB (203507316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:427289401dfe720159abec716ab5c1a6443e5c15cf3c8224845bb31a2d33fbfd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 06 Sep 2024 12:03:22 GMT
ADD alpine-minirootfs-3.18.9-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:03:22 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 15:32:12 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Fri, 13 Dec 2024 15:32:12 GMT
ENV ARANGO_VERSION=3.11.12
# Fri, 13 Dec 2024 15:32:12 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8003EDF6F05459984878D4A6C04AD0FD86FEC04D &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb311/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg # buildkit
# Fri, 13 Dec 2024 15:32:12 GMT
ENV GLIBCXX_FORCE_NEW=1
# Fri, 13 Dec 2024 15:32:12 GMT
RUN echo "UTC" > /etc/timezone # buildkit
# Fri, 13 Dec 2024 15:32:12 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Fri, 13 Dec 2024 15:32:12 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 13 Dec 2024 15:32:12 GMT
COPY docker-foxx.sh /usr/bin/foxx # buildkit
# Fri, 13 Dec 2024 15:32:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 13 Dec 2024 15:32:12 GMT
EXPOSE map[8529/tcp:{}]
# Fri, 13 Dec 2024 15:32:12 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:0dfcae9cb3f09031e3687535f2d3e3c2f08533799b67ed61076e79e4ed1c7c4a`  
		Last Modified: Mon, 09 Sep 2024 07:02:44 GMT  
		Size: 3.3 MB (3340451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7893112d62c0be137ef37ad04d80ff3e16f8e5b2434ee588046abf752d7826a6`  
		Last Modified: Fri, 13 Dec 2024 22:28:47 GMT  
		Size: 200.2 MB (200164382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6360aec695091327287a581f5d80deb5d9eb06dcef669e783eb33668cb1f663a`  
		Last Modified: Fri, 13 Dec 2024 22:28:43 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05506ea46e24a5e93ef96f0d7e4fd11bc1c6c6f677e13916310d9d1a9a138ebd`  
		Last Modified: Fri, 13 Dec 2024 22:28:43 GMT  
		Size: 2.1 KB (2086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d40d91524f0d28dd5d02071b31b26473655f1d1f68c535a1ecc14b0b3bbc861d`  
		Last Modified: Fri, 13 Dec 2024 22:28:43 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:3.11` - unknown; unknown

```console
$ docker pull arangodb@sha256:d1cd7d7941a99543ce887167863b8ba9d1e98291560154fe34f931eaf4f14179
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1188157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f720e020972070122377bd932dbe6e07feeefe6379b4ea7cc6fadebd6fe8290d`

```dockerfile
```

-	Layers:
	-	`sha256:499b4287086b48351d5f77315026d31fdf24a0a664e5c0a7cd6ee68cbe9b5bfb`  
		Last Modified: Fri, 13 Dec 2024 22:28:43 GMT  
		Size: 1.2 MB (1172206 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed8544a43fc1b2a6717909f620c47b3410c4cf2ee82e7ab2b434ea5b56f05d6e`  
		Last Modified: Fri, 13 Dec 2024 22:28:43 GMT  
		Size: 16.0 KB (15951 bytes)  
		MIME: application/vnd.in-toto+json

## `arangodb:3.11.12`

```console
$ docker pull arangodb@sha256:7c9360b3fa68ddbe716683d186ea837a0919ec1ae6831f9fe0b0aa980a83665f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `arangodb:3.11.12` - linux; amd64

```console
$ docker pull arangodb@sha256:70dc40bb8c692d451c10fa1abb064e6b74c2a84adb95bad0bdeb2ce4ea9628ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.8 MB (199785440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:796ea94a1af8c1efc023f3d5910cf4599973ca8ca593fb1cff4238c39296dd08`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 06 Sep 2024 12:03:22 GMT
ADD alpine-minirootfs-3.18.9-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:03:22 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 15:32:12 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Fri, 13 Dec 2024 15:32:12 GMT
ENV ARANGO_VERSION=3.11.12
# Fri, 13 Dec 2024 15:32:12 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8003EDF6F05459984878D4A6C04AD0FD86FEC04D &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb311/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg # buildkit
# Fri, 13 Dec 2024 15:32:12 GMT
ENV GLIBCXX_FORCE_NEW=1
# Fri, 13 Dec 2024 15:32:12 GMT
RUN echo "UTC" > /etc/timezone # buildkit
# Fri, 13 Dec 2024 15:32:12 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Fri, 13 Dec 2024 15:32:12 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 13 Dec 2024 15:32:12 GMT
COPY docker-foxx.sh /usr/bin/foxx # buildkit
# Fri, 13 Dec 2024 15:32:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 13 Dec 2024 15:32:12 GMT
EXPOSE map[8529/tcp:{}]
# Fri, 13 Dec 2024 15:32:12 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:dc0decf4841d19b14e836c2d82bd5cb9540fb5e0d1359549ca243f49036557e9`  
		Last Modified: Mon, 09 Sep 2024 07:02:43 GMT  
		Size: 3.4 MB (3416401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45f17cede5bdc04f484ba1810f73078fd3bca8108386cd20628bf8d92e13db7c`  
		Last Modified: Fri, 13 Dec 2024 22:27:44 GMT  
		Size: 196.4 MB (196366554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b790a8d1ad32ba7ee3b100786d019e1f17b05ce14aed5e1e6a22bc6f62bf724`  
		Last Modified: Fri, 13 Dec 2024 22:27:41 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e80a781f9073f0535004918fb58b6c470b972b81da5d7d30fc3160ff14cdb4`  
		Last Modified: Fri, 13 Dec 2024 22:27:41 GMT  
		Size: 2.1 KB (2086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c33c7b88075b05861a6248d41dbc51bce4b936160275c4c728d8c23cf49bc12f`  
		Last Modified: Fri, 13 Dec 2024 22:27:41 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:3.11.12` - unknown; unknown

```console
$ docker pull arangodb@sha256:acc94806a78ee7c55a8321afbd031f6757eeb962a69859c7354ef5608c6320fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1082775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c949bf1acba75e332e343bf08e8b4f41a151a8b1c8ded609b0f3aa06a82d268`

```dockerfile
```

-	Layers:
	-	`sha256:6c4a834ee2b1bc19af42ff28bd9df99203b7f771f14e194f1acd2b1d6d03a531`  
		Last Modified: Fri, 13 Dec 2024 22:27:41 GMT  
		Size: 1.1 MB (1066919 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7de48459d033d09a7225423437d56a2854bbe4527a99944720ad308122edcdae`  
		Last Modified: Fri, 13 Dec 2024 22:27:41 GMT  
		Size: 15.9 KB (15856 bytes)  
		MIME: application/vnd.in-toto+json

### `arangodb:3.11.12` - linux; arm64 variant v8

```console
$ docker pull arangodb@sha256:e838a8706270b751ce562441182832a3a869c61ec44daf2eedd89c8d6597dcd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.5 MB (203507316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:427289401dfe720159abec716ab5c1a6443e5c15cf3c8224845bb31a2d33fbfd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 06 Sep 2024 12:03:22 GMT
ADD alpine-minirootfs-3.18.9-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:03:22 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 15:32:12 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Fri, 13 Dec 2024 15:32:12 GMT
ENV ARANGO_VERSION=3.11.12
# Fri, 13 Dec 2024 15:32:12 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8003EDF6F05459984878D4A6C04AD0FD86FEC04D &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb311/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg # buildkit
# Fri, 13 Dec 2024 15:32:12 GMT
ENV GLIBCXX_FORCE_NEW=1
# Fri, 13 Dec 2024 15:32:12 GMT
RUN echo "UTC" > /etc/timezone # buildkit
# Fri, 13 Dec 2024 15:32:12 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Fri, 13 Dec 2024 15:32:12 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 13 Dec 2024 15:32:12 GMT
COPY docker-foxx.sh /usr/bin/foxx # buildkit
# Fri, 13 Dec 2024 15:32:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 13 Dec 2024 15:32:12 GMT
EXPOSE map[8529/tcp:{}]
# Fri, 13 Dec 2024 15:32:12 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:0dfcae9cb3f09031e3687535f2d3e3c2f08533799b67ed61076e79e4ed1c7c4a`  
		Last Modified: Mon, 09 Sep 2024 07:02:44 GMT  
		Size: 3.3 MB (3340451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7893112d62c0be137ef37ad04d80ff3e16f8e5b2434ee588046abf752d7826a6`  
		Last Modified: Fri, 13 Dec 2024 22:28:47 GMT  
		Size: 200.2 MB (200164382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6360aec695091327287a581f5d80deb5d9eb06dcef669e783eb33668cb1f663a`  
		Last Modified: Fri, 13 Dec 2024 22:28:43 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05506ea46e24a5e93ef96f0d7e4fd11bc1c6c6f677e13916310d9d1a9a138ebd`  
		Last Modified: Fri, 13 Dec 2024 22:28:43 GMT  
		Size: 2.1 KB (2086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d40d91524f0d28dd5d02071b31b26473655f1d1f68c535a1ecc14b0b3bbc861d`  
		Last Modified: Fri, 13 Dec 2024 22:28:43 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:3.11.12` - unknown; unknown

```console
$ docker pull arangodb@sha256:d1cd7d7941a99543ce887167863b8ba9d1e98291560154fe34f931eaf4f14179
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1188157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f720e020972070122377bd932dbe6e07feeefe6379b4ea7cc6fadebd6fe8290d`

```dockerfile
```

-	Layers:
	-	`sha256:499b4287086b48351d5f77315026d31fdf24a0a664e5c0a7cd6ee68cbe9b5bfb`  
		Last Modified: Fri, 13 Dec 2024 22:28:43 GMT  
		Size: 1.2 MB (1172206 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed8544a43fc1b2a6717909f620c47b3410c4cf2ee82e7ab2b434ea5b56f05d6e`  
		Last Modified: Fri, 13 Dec 2024 22:28:43 GMT  
		Size: 16.0 KB (15951 bytes)  
		MIME: application/vnd.in-toto+json

## `arangodb:3.12`

```console
$ docker pull arangodb@sha256:adeaa727f37b9c53bf1e58551812774ab01f8729a9a1317d4e0aa9be668660a2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `arangodb:3.12` - linux; amd64

```console
$ docker pull arangodb@sha256:967dc76e9507b9671ae315180c23dcf83c945ea4af4d141f41c7a0ee014f55fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.0 MB (304980753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0c14a24222eb26d9677a9f423fc3a0255e73b9dce0c9a640e8c6d3508df4ff2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 06 Sep 2024 12:03:22 GMT
ADD alpine-minirootfs-3.18.9-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:03:22 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 15:32:12 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Fri, 13 Dec 2024 15:32:12 GMT
ENV ARANGO_VERSION=3.12.3
# Fri, 13 Dec 2024 15:32:12 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8003EDF6F05459984878D4A6C04AD0FD86FEC04D &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb312/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg # buildkit
# Fri, 13 Dec 2024 15:32:12 GMT
ENV GLIBCXX_FORCE_NEW=1
# Fri, 13 Dec 2024 15:32:12 GMT
RUN echo "UTC" > /etc/timezone # buildkit
# Fri, 13 Dec 2024 15:32:12 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Fri, 13 Dec 2024 15:32:12 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 13 Dec 2024 15:32:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 13 Dec 2024 15:32:12 GMT
EXPOSE map[8529/tcp:{}]
# Fri, 13 Dec 2024 15:32:12 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:dc0decf4841d19b14e836c2d82bd5cb9540fb5e0d1359549ca243f49036557e9`  
		Last Modified: Mon, 09 Sep 2024 07:02:43 GMT  
		Size: 3.4 MB (3416401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e14e191d0c9dfa842273ab598994dd6b2096bcfcea1264a43a6b729037b28669`  
		Last Modified: Fri, 13 Dec 2024 22:27:59 GMT  
		Size: 301.6 MB (301562196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be08d90dbea18c6a8a8df8d03a510cde742483f9718dafe9f7228a8a9aad0dde`  
		Last Modified: Fri, 13 Dec 2024 22:27:52 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:454e295c1ca40e9283f772c20807e853a125e69e0cce1761cdf8a26744439e47`  
		Last Modified: Fri, 13 Dec 2024 22:27:52 GMT  
		Size: 2.0 KB (2016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:3.12` - unknown; unknown

```console
$ docker pull arangodb@sha256:7a7c14147663bafb1435addff25ec1dcd42539f3a37e485f6d0d03fb22913eab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **377.0 KB (376978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50b84f6bcda6a96189a5dbd6c5ba99b53bf5e0499702bb4e6bb0f4458356b379`

```dockerfile
```

-	Layers:
	-	`sha256:72dceff12dcd619058f21847ede4eb18a18aafadb08d4ac0b464618a6ae5c075`  
		Last Modified: Fri, 13 Dec 2024 22:27:52 GMT  
		Size: 362.6 KB (362557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db71984b14eb46e9a0729136b86ae4d1414134e6b014cbe3c2c7107e82a74372`  
		Last Modified: Fri, 13 Dec 2024 22:27:52 GMT  
		Size: 14.4 KB (14421 bytes)  
		MIME: application/vnd.in-toto+json

### `arangodb:3.12` - linux; arm64 variant v8

```console
$ docker pull arangodb@sha256:a6c730c5b6450dc07d880df0bca51dc1eed54250938dd4b201d1c106990b466b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.0 MB (307022235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51a89ed54d108b80c6f24f6b4d4b4af0fe7c3492af2b3701818729a1f9910ef7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 06 Sep 2024 12:03:22 GMT
ADD alpine-minirootfs-3.18.9-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:03:22 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 15:32:12 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Fri, 13 Dec 2024 15:32:12 GMT
ENV ARANGO_VERSION=3.12.3
# Fri, 13 Dec 2024 15:32:12 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8003EDF6F05459984878D4A6C04AD0FD86FEC04D &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb312/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg # buildkit
# Fri, 13 Dec 2024 15:32:12 GMT
ENV GLIBCXX_FORCE_NEW=1
# Fri, 13 Dec 2024 15:32:12 GMT
RUN echo "UTC" > /etc/timezone # buildkit
# Fri, 13 Dec 2024 15:32:12 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Fri, 13 Dec 2024 15:32:12 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 13 Dec 2024 15:32:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 13 Dec 2024 15:32:12 GMT
EXPOSE map[8529/tcp:{}]
# Fri, 13 Dec 2024 15:32:12 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:0dfcae9cb3f09031e3687535f2d3e3c2f08533799b67ed61076e79e4ed1c7c4a`  
		Last Modified: Mon, 09 Sep 2024 07:02:44 GMT  
		Size: 3.3 MB (3340451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9f28796bd11769c801303bffc3deb305dc81ffe1c1ea61f9745261a37282287`  
		Last Modified: Fri, 13 Dec 2024 22:27:37 GMT  
		Size: 303.7 MB (303679629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:537a98245e53bbd806aba6b3ab77f00c98d14efb3ca146af8950b05091be46c9`  
		Last Modified: Fri, 13 Dec 2024 22:27:30 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c64b585c9406e1fdbb6d3626b4591005fe8330f7c08e9cb8a86a56d84e55678`  
		Size: 2.0 KB (2015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:3.12` - unknown; unknown

```console
$ docker pull arangodb@sha256:8d412bd91489c98b2a4f94ff2ba75d8a57e03a5cac5dc29acf8e8768da6d6aba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **482.4 KB (482383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dff883a2d4cac838cbc8db71c3b237afa24632a1388209dff45a421b61d4558f`

```dockerfile
```

-	Layers:
	-	`sha256:989f2e74055d5e3986c0b18203c1966b4f109ef8b0d6c5aef00548a734aaf55c`  
		Last Modified: Fri, 13 Dec 2024 22:27:31 GMT  
		Size: 467.9 KB (467856 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df6d1a704125cb70cedba44b4915f006ddd00d7b4f840e6168b29b54d7fa4744`  
		Last Modified: Fri, 13 Dec 2024 22:27:30 GMT  
		Size: 14.5 KB (14527 bytes)  
		MIME: application/vnd.in-toto+json

## `arangodb:3.12.3`

```console
$ docker pull arangodb@sha256:adeaa727f37b9c53bf1e58551812774ab01f8729a9a1317d4e0aa9be668660a2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `arangodb:3.12.3` - linux; amd64

```console
$ docker pull arangodb@sha256:967dc76e9507b9671ae315180c23dcf83c945ea4af4d141f41c7a0ee014f55fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.0 MB (304980753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0c14a24222eb26d9677a9f423fc3a0255e73b9dce0c9a640e8c6d3508df4ff2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 06 Sep 2024 12:03:22 GMT
ADD alpine-minirootfs-3.18.9-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:03:22 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 15:32:12 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Fri, 13 Dec 2024 15:32:12 GMT
ENV ARANGO_VERSION=3.12.3
# Fri, 13 Dec 2024 15:32:12 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8003EDF6F05459984878D4A6C04AD0FD86FEC04D &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb312/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg # buildkit
# Fri, 13 Dec 2024 15:32:12 GMT
ENV GLIBCXX_FORCE_NEW=1
# Fri, 13 Dec 2024 15:32:12 GMT
RUN echo "UTC" > /etc/timezone # buildkit
# Fri, 13 Dec 2024 15:32:12 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Fri, 13 Dec 2024 15:32:12 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 13 Dec 2024 15:32:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 13 Dec 2024 15:32:12 GMT
EXPOSE map[8529/tcp:{}]
# Fri, 13 Dec 2024 15:32:12 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:dc0decf4841d19b14e836c2d82bd5cb9540fb5e0d1359549ca243f49036557e9`  
		Last Modified: Mon, 09 Sep 2024 07:02:43 GMT  
		Size: 3.4 MB (3416401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e14e191d0c9dfa842273ab598994dd6b2096bcfcea1264a43a6b729037b28669`  
		Last Modified: Fri, 13 Dec 2024 22:27:59 GMT  
		Size: 301.6 MB (301562196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be08d90dbea18c6a8a8df8d03a510cde742483f9718dafe9f7228a8a9aad0dde`  
		Last Modified: Fri, 13 Dec 2024 22:27:52 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:454e295c1ca40e9283f772c20807e853a125e69e0cce1761cdf8a26744439e47`  
		Last Modified: Fri, 13 Dec 2024 22:27:52 GMT  
		Size: 2.0 KB (2016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:3.12.3` - unknown; unknown

```console
$ docker pull arangodb@sha256:7a7c14147663bafb1435addff25ec1dcd42539f3a37e485f6d0d03fb22913eab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **377.0 KB (376978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50b84f6bcda6a96189a5dbd6c5ba99b53bf5e0499702bb4e6bb0f4458356b379`

```dockerfile
```

-	Layers:
	-	`sha256:72dceff12dcd619058f21847ede4eb18a18aafadb08d4ac0b464618a6ae5c075`  
		Last Modified: Fri, 13 Dec 2024 22:27:52 GMT  
		Size: 362.6 KB (362557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db71984b14eb46e9a0729136b86ae4d1414134e6b014cbe3c2c7107e82a74372`  
		Last Modified: Fri, 13 Dec 2024 22:27:52 GMT  
		Size: 14.4 KB (14421 bytes)  
		MIME: application/vnd.in-toto+json

### `arangodb:3.12.3` - linux; arm64 variant v8

```console
$ docker pull arangodb@sha256:a6c730c5b6450dc07d880df0bca51dc1eed54250938dd4b201d1c106990b466b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.0 MB (307022235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51a89ed54d108b80c6f24f6b4d4b4af0fe7c3492af2b3701818729a1f9910ef7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 06 Sep 2024 12:03:22 GMT
ADD alpine-minirootfs-3.18.9-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:03:22 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 15:32:12 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Fri, 13 Dec 2024 15:32:12 GMT
ENV ARANGO_VERSION=3.12.3
# Fri, 13 Dec 2024 15:32:12 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8003EDF6F05459984878D4A6C04AD0FD86FEC04D &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb312/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg # buildkit
# Fri, 13 Dec 2024 15:32:12 GMT
ENV GLIBCXX_FORCE_NEW=1
# Fri, 13 Dec 2024 15:32:12 GMT
RUN echo "UTC" > /etc/timezone # buildkit
# Fri, 13 Dec 2024 15:32:12 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Fri, 13 Dec 2024 15:32:12 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 13 Dec 2024 15:32:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 13 Dec 2024 15:32:12 GMT
EXPOSE map[8529/tcp:{}]
# Fri, 13 Dec 2024 15:32:12 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:0dfcae9cb3f09031e3687535f2d3e3c2f08533799b67ed61076e79e4ed1c7c4a`  
		Last Modified: Mon, 09 Sep 2024 07:02:44 GMT  
		Size: 3.3 MB (3340451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9f28796bd11769c801303bffc3deb305dc81ffe1c1ea61f9745261a37282287`  
		Last Modified: Fri, 13 Dec 2024 22:27:37 GMT  
		Size: 303.7 MB (303679629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:537a98245e53bbd806aba6b3ab77f00c98d14efb3ca146af8950b05091be46c9`  
		Last Modified: Fri, 13 Dec 2024 22:27:30 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c64b585c9406e1fdbb6d3626b4591005fe8330f7c08e9cb8a86a56d84e55678`  
		Size: 2.0 KB (2015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:3.12.3` - unknown; unknown

```console
$ docker pull arangodb@sha256:8d412bd91489c98b2a4f94ff2ba75d8a57e03a5cac5dc29acf8e8768da6d6aba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **482.4 KB (482383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dff883a2d4cac838cbc8db71c3b237afa24632a1388209dff45a421b61d4558f`

```dockerfile
```

-	Layers:
	-	`sha256:989f2e74055d5e3986c0b18203c1966b4f109ef8b0d6c5aef00548a734aaf55c`  
		Last Modified: Fri, 13 Dec 2024 22:27:31 GMT  
		Size: 467.9 KB (467856 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df6d1a704125cb70cedba44b4915f006ddd00d7b4f840e6168b29b54d7fa4744`  
		Last Modified: Fri, 13 Dec 2024 22:27:30 GMT  
		Size: 14.5 KB (14527 bytes)  
		MIME: application/vnd.in-toto+json

## `arangodb:latest`

```console
$ docker pull arangodb@sha256:adeaa727f37b9c53bf1e58551812774ab01f8729a9a1317d4e0aa9be668660a2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `arangodb:latest` - linux; amd64

```console
$ docker pull arangodb@sha256:967dc76e9507b9671ae315180c23dcf83c945ea4af4d141f41c7a0ee014f55fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.0 MB (304980753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0c14a24222eb26d9677a9f423fc3a0255e73b9dce0c9a640e8c6d3508df4ff2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 06 Sep 2024 12:03:22 GMT
ADD alpine-minirootfs-3.18.9-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:03:22 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 15:32:12 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Fri, 13 Dec 2024 15:32:12 GMT
ENV ARANGO_VERSION=3.12.3
# Fri, 13 Dec 2024 15:32:12 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8003EDF6F05459984878D4A6C04AD0FD86FEC04D &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb312/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg # buildkit
# Fri, 13 Dec 2024 15:32:12 GMT
ENV GLIBCXX_FORCE_NEW=1
# Fri, 13 Dec 2024 15:32:12 GMT
RUN echo "UTC" > /etc/timezone # buildkit
# Fri, 13 Dec 2024 15:32:12 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Fri, 13 Dec 2024 15:32:12 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 13 Dec 2024 15:32:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 13 Dec 2024 15:32:12 GMT
EXPOSE map[8529/tcp:{}]
# Fri, 13 Dec 2024 15:32:12 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:dc0decf4841d19b14e836c2d82bd5cb9540fb5e0d1359549ca243f49036557e9`  
		Last Modified: Mon, 09 Sep 2024 07:02:43 GMT  
		Size: 3.4 MB (3416401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e14e191d0c9dfa842273ab598994dd6b2096bcfcea1264a43a6b729037b28669`  
		Last Modified: Fri, 13 Dec 2024 22:27:59 GMT  
		Size: 301.6 MB (301562196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be08d90dbea18c6a8a8df8d03a510cde742483f9718dafe9f7228a8a9aad0dde`  
		Last Modified: Fri, 13 Dec 2024 22:27:52 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:454e295c1ca40e9283f772c20807e853a125e69e0cce1761cdf8a26744439e47`  
		Last Modified: Fri, 13 Dec 2024 22:27:52 GMT  
		Size: 2.0 KB (2016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:latest` - unknown; unknown

```console
$ docker pull arangodb@sha256:7a7c14147663bafb1435addff25ec1dcd42539f3a37e485f6d0d03fb22913eab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **377.0 KB (376978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50b84f6bcda6a96189a5dbd6c5ba99b53bf5e0499702bb4e6bb0f4458356b379`

```dockerfile
```

-	Layers:
	-	`sha256:72dceff12dcd619058f21847ede4eb18a18aafadb08d4ac0b464618a6ae5c075`  
		Last Modified: Fri, 13 Dec 2024 22:27:52 GMT  
		Size: 362.6 KB (362557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db71984b14eb46e9a0729136b86ae4d1414134e6b014cbe3c2c7107e82a74372`  
		Last Modified: Fri, 13 Dec 2024 22:27:52 GMT  
		Size: 14.4 KB (14421 bytes)  
		MIME: application/vnd.in-toto+json

### `arangodb:latest` - linux; arm64 variant v8

```console
$ docker pull arangodb@sha256:a6c730c5b6450dc07d880df0bca51dc1eed54250938dd4b201d1c106990b466b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.0 MB (307022235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51a89ed54d108b80c6f24f6b4d4b4af0fe7c3492af2b3701818729a1f9910ef7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 06 Sep 2024 12:03:22 GMT
ADD alpine-minirootfs-3.18.9-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:03:22 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 15:32:12 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Fri, 13 Dec 2024 15:32:12 GMT
ENV ARANGO_VERSION=3.12.3
# Fri, 13 Dec 2024 15:32:12 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8003EDF6F05459984878D4A6C04AD0FD86FEC04D &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb312/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg # buildkit
# Fri, 13 Dec 2024 15:32:12 GMT
ENV GLIBCXX_FORCE_NEW=1
# Fri, 13 Dec 2024 15:32:12 GMT
RUN echo "UTC" > /etc/timezone # buildkit
# Fri, 13 Dec 2024 15:32:12 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Fri, 13 Dec 2024 15:32:12 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 13 Dec 2024 15:32:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 13 Dec 2024 15:32:12 GMT
EXPOSE map[8529/tcp:{}]
# Fri, 13 Dec 2024 15:32:12 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:0dfcae9cb3f09031e3687535f2d3e3c2f08533799b67ed61076e79e4ed1c7c4a`  
		Last Modified: Mon, 09 Sep 2024 07:02:44 GMT  
		Size: 3.3 MB (3340451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9f28796bd11769c801303bffc3deb305dc81ffe1c1ea61f9745261a37282287`  
		Last Modified: Fri, 13 Dec 2024 22:27:37 GMT  
		Size: 303.7 MB (303679629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:537a98245e53bbd806aba6b3ab77f00c98d14efb3ca146af8950b05091be46c9`  
		Last Modified: Fri, 13 Dec 2024 22:27:30 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c64b585c9406e1fdbb6d3626b4591005fe8330f7c08e9cb8a86a56d84e55678`  
		Size: 2.0 KB (2015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:latest` - unknown; unknown

```console
$ docker pull arangodb@sha256:8d412bd91489c98b2a4f94ff2ba75d8a57e03a5cac5dc29acf8e8768da6d6aba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **482.4 KB (482383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dff883a2d4cac838cbc8db71c3b237afa24632a1388209dff45a421b61d4558f`

```dockerfile
```

-	Layers:
	-	`sha256:989f2e74055d5e3986c0b18203c1966b4f109ef8b0d6c5aef00548a734aaf55c`  
		Last Modified: Fri, 13 Dec 2024 22:27:31 GMT  
		Size: 467.9 KB (467856 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df6d1a704125cb70cedba44b4915f006ddd00d7b4f840e6168b29b54d7fa4744`  
		Last Modified: Fri, 13 Dec 2024 22:27:30 GMT  
		Size: 14.5 KB (14527 bytes)  
		MIME: application/vnd.in-toto+json
