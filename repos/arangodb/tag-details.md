<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `arangodb`

-	[`arangodb:3.11`](#arangodb311)
-	[`arangodb:3.11.13`](#arangodb31113)
-	[`arangodb:3.12`](#arangodb312)
-	[`arangodb:3.12.4`](#arangodb3124)
-	[`arangodb:latest`](#arangodblatest)

## `arangodb:3.11`

```console
$ docker pull arangodb@sha256:1eb3c173fffac06850b3ad04ea71962e31aa8adcdf98d278f413965e10ceedc6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `arangodb:3.11` - linux; amd64

```console
$ docker pull arangodb@sha256:14d4cf963173f6d0cb1f5df6e6c00c9f5403ffa8cf6c206b48fd5ed3fb129330
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.8 MB (207791730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fe39c991e590fb9b17db87df45d2817ce5d3dba04a0d461a946c4c57cdb7c9b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 14 Feb 2025 15:05:04 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Fri, 14 Feb 2025 15:05:04 GMT
ENV ARANGO_VERSION=3.11.13
# Fri, 14 Feb 2025 15:05:04 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8003EDF6F05459984878D4A6C04AD0FD86FEC04D &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb311/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg # buildkit
# Fri, 14 Feb 2025 15:05:04 GMT
ENV GLIBCXX_FORCE_NEW=1
# Fri, 14 Feb 2025 15:05:04 GMT
RUN echo "UTC" > /etc/timezone # buildkit
# Fri, 14 Feb 2025 15:05:04 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Fri, 14 Feb 2025 15:05:04 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 14 Feb 2025 15:05:04 GMT
COPY docker-foxx.sh /usr/bin/foxx # buildkit
# Fri, 14 Feb 2025 15:05:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 14 Feb 2025 15:05:04 GMT
EXPOSE map[8529/tcp:{}]
# Fri, 14 Feb 2025 15:05:04 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f7bd5f6389b77c24b69a9f39ef1aea79863361d0aa9f36681a1aabdec398254`  
		Last Modified: Sat, 15 Feb 2025 01:13:55 GMT  
		Size: 204.1 MB (204146999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a58fd14c9ac2e19981435b18776d552556666ec1b07e695886fa9cd4899ac0cc`  
		Last Modified: Sat, 15 Feb 2025 01:13:51 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03ab2495fb8a6cc1e9829e9561221eff60c011f3a9c05ebe5e3a201d6a5484d7`  
		Last Modified: Sat, 15 Feb 2025 01:13:50 GMT  
		Size: 2.1 KB (2087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28ebe21f9a7b14e60989be24660d4a0ce7461c76e732dd1c4dbee8f0172cb2ba`  
		Last Modified: Sat, 15 Feb 2025 01:13:51 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:3.11` - unknown; unknown

```console
$ docker pull arangodb@sha256:905d609f2c7dd7cf11fc580b06d8c0035d1208fd954b1945471a873e786a191e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1141438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be64196f7c3927d47f0964a8a5503afef9cf15da303fd5d02b99f29008c78514`

```dockerfile
```

-	Layers:
	-	`sha256:c8a8ab69e438b4e7b9570594b11aadbff1d0b78fee5c9ef8afca45afb90c524b`  
		Last Modified: Sat, 15 Feb 2025 01:13:15 GMT  
		Size: 1.1 MB (1125618 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0412bf095645ad3b18313f96b15e5997051c74a7983ff897111cbb211339776`  
		Last Modified: Sat, 15 Feb 2025 01:13:16 GMT  
		Size: 15.8 KB (15820 bytes)  
		MIME: application/vnd.in-toto+json

### `arangodb:3.11` - linux; arm64 variant v8

```console
$ docker pull arangodb@sha256:71121f10a03430fb6e4f04cec5f31d7d1552bd59ab59f71a6ea922fb48c2f902
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.5 MB (203539306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21cfe3262535b13406a0523bfc113badd2914972701d69753b403ee4f09c5b9a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 13 Dec 2024 15:32:12 GMT
ADD alpine-minirootfs-3.18.11-aarch64.tar.gz / # buildkit
# Fri, 13 Dec 2024 15:32:12 GMT
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
	-	`sha256:f6b431426dd566e612639f03cd46e521b3133a043bb6b60edeeeef80d513e870`  
		Last Modified: Tue, 14 Jan 2025 20:34:06 GMT  
		Size: 3.3 MB (3341861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f708f8274a5b9157fb1e71dd5c98f681f28e0ea59f623ca21e6b8aa8e2ef5cc`  
		Last Modified: Wed, 15 Jan 2025 08:40:21 GMT  
		Size: 200.2 MB (200194961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b350b2fea45c6255316ab07d3c03344e96d1dee4c3c0d479b4984f67f27ceb0`  
		Last Modified: Wed, 15 Jan 2025 08:40:01 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8f4977d42619c3b6639c180fc098661b231bf619ba14fad2a0bafcc58336d28`  
		Last Modified: Wed, 15 Jan 2025 08:40:02 GMT  
		Size: 2.1 KB (2087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeb90dd2fc7e451c220ef5aec3d594bdd68e5fc555adb95ab662dea67ea2cf1e`  
		Last Modified: Wed, 15 Jan 2025 08:40:02 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:3.11` - unknown; unknown

```console
$ docker pull arangodb@sha256:8d1908e97e37a1cc072cb169f99b4fe1df1004315d2958379d2a9db9fd7a98a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1195298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6675ea21a25c3ce521f67c64d02c20dd6bef0c7212eb0fa4f1b644b74d3ad4d7`

```dockerfile
```

-	Layers:
	-	`sha256:09bba5bb8a09e3a51d796f55c56e84d536f652a8962ec4a1bb4650790ef294bb`  
		Last Modified: Thu, 16 Jan 2025 15:15:18 GMT  
		Size: 1.2 MB (1179347 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3421c84a8adc2f226ddeeb50afe20d2bd124ed43d3ffca32b8ca0f225cf55838`  
		Last Modified: Thu, 16 Jan 2025 15:15:18 GMT  
		Size: 16.0 KB (15951 bytes)  
		MIME: application/vnd.in-toto+json

## `arangodb:3.11.13`

```console
$ docker pull arangodb@sha256:c5261a44ec82e36e4db0901737a464b7893576acc64503e07f49d695fe9f16dd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `arangodb:3.11.13` - linux; amd64

```console
$ docker pull arangodb@sha256:14d4cf963173f6d0cb1f5df6e6c00c9f5403ffa8cf6c206b48fd5ed3fb129330
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.8 MB (207791730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fe39c991e590fb9b17db87df45d2817ce5d3dba04a0d461a946c4c57cdb7c9b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 14 Feb 2025 15:05:04 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Fri, 14 Feb 2025 15:05:04 GMT
ENV ARANGO_VERSION=3.11.13
# Fri, 14 Feb 2025 15:05:04 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8003EDF6F05459984878D4A6C04AD0FD86FEC04D &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb311/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg # buildkit
# Fri, 14 Feb 2025 15:05:04 GMT
ENV GLIBCXX_FORCE_NEW=1
# Fri, 14 Feb 2025 15:05:04 GMT
RUN echo "UTC" > /etc/timezone # buildkit
# Fri, 14 Feb 2025 15:05:04 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Fri, 14 Feb 2025 15:05:04 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 14 Feb 2025 15:05:04 GMT
COPY docker-foxx.sh /usr/bin/foxx # buildkit
# Fri, 14 Feb 2025 15:05:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 14 Feb 2025 15:05:04 GMT
EXPOSE map[8529/tcp:{}]
# Fri, 14 Feb 2025 15:05:04 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f7bd5f6389b77c24b69a9f39ef1aea79863361d0aa9f36681a1aabdec398254`  
		Last Modified: Sat, 15 Feb 2025 01:13:55 GMT  
		Size: 204.1 MB (204146999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a58fd14c9ac2e19981435b18776d552556666ec1b07e695886fa9cd4899ac0cc`  
		Last Modified: Sat, 15 Feb 2025 01:13:51 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03ab2495fb8a6cc1e9829e9561221eff60c011f3a9c05ebe5e3a201d6a5484d7`  
		Last Modified: Sat, 15 Feb 2025 01:13:50 GMT  
		Size: 2.1 KB (2087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28ebe21f9a7b14e60989be24660d4a0ce7461c76e732dd1c4dbee8f0172cb2ba`  
		Last Modified: Sat, 15 Feb 2025 01:13:51 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:3.11.13` - unknown; unknown

```console
$ docker pull arangodb@sha256:905d609f2c7dd7cf11fc580b06d8c0035d1208fd954b1945471a873e786a191e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1141438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be64196f7c3927d47f0964a8a5503afef9cf15da303fd5d02b99f29008c78514`

```dockerfile
```

-	Layers:
	-	`sha256:c8a8ab69e438b4e7b9570594b11aadbff1d0b78fee5c9ef8afca45afb90c524b`  
		Last Modified: Sat, 15 Feb 2025 01:13:15 GMT  
		Size: 1.1 MB (1125618 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0412bf095645ad3b18313f96b15e5997051c74a7983ff897111cbb211339776`  
		Last Modified: Sat, 15 Feb 2025 01:13:16 GMT  
		Size: 15.8 KB (15820 bytes)  
		MIME: application/vnd.in-toto+json

## `arangodb:3.12`

```console
$ docker pull arangodb@sha256:b7cc8dbf5f24c0fe235b6e50a26dbcfaebaf9abe0d322acefcf3dab63b5a0102
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `arangodb:3.12` - linux; amd64

```console
$ docker pull arangodb@sha256:8ec63e60fcb954e7108a308795f562dafd285552aaf0d4f9824782b8be6d48b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.8 MB (232804659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c91f56b449ee93e28fb334072fb8b1d23a6baacdf73a7285467265899a878fdd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Wed, 29 Jan 2025 11:48:08 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Wed, 29 Jan 2025 11:48:08 GMT
CMD ["/bin/sh"]
# Wed, 29 Jan 2025 11:48:08 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Wed, 29 Jan 2025 11:48:08 GMT
ENV ARANGO_VERSION=3.12.4
# Wed, 29 Jan 2025 11:48:08 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8003EDF6F05459984878D4A6C04AD0FD86FEC04D &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb312/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg # buildkit
# Wed, 29 Jan 2025 11:48:08 GMT
ENV GLIBCXX_FORCE_NEW=1
# Wed, 29 Jan 2025 11:48:08 GMT
RUN echo "UTC" > /etc/timezone # buildkit
# Wed, 29 Jan 2025 11:48:08 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Wed, 29 Jan 2025 11:48:08 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 29 Jan 2025 11:48:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 29 Jan 2025 11:48:08 GMT
EXPOSE map[8529/tcp:{}]
# Wed, 29 Jan 2025 11:48:08 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6c74b8fc358e5cd758a39a8cb609904e55b1fc5f7fa5831fb157886e5599e47`  
		Last Modified: Fri, 14 Feb 2025 22:14:01 GMT  
		Size: 229.2 MB (229160256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05a93864b83fa1e50e6679ffd3ad565a60e92a6ed51e33d4f97667acffa48834`  
		Last Modified: Fri, 14 Feb 2025 22:13:53 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a82bed114865afd11ccf2719c7cca1f6e79c860b76f327275324d060bf7f6f1`  
		Last Modified: Fri, 14 Feb 2025 22:13:53 GMT  
		Size: 2.0 KB (2016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:3.12` - unknown; unknown

```console
$ docker pull arangodb@sha256:796bd3496b11301bed127244ec2f4cb75f998fdfcc7e981826f25d4951d76d8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **405.4 KB (405444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1d1012c5cef89ed733f225e7dab0c7e42e53d770f4f9861e05964ae3cf438b6`

```dockerfile
```

-	Layers:
	-	`sha256:76ae3dd6fddf6a30bdc1192b7249277400a0fe27ad5c6158f64fbfed5d26a80d`  
		Last Modified: Fri, 14 Feb 2025 22:13:18 GMT  
		Size: 391.1 KB (391059 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:041b9a4b47fdc7120dafb59c96a339c2165eb20a6893b6915b4b98f94c9fe9c1`  
		Last Modified: Fri, 14 Feb 2025 22:13:18 GMT  
		Size: 14.4 KB (14385 bytes)  
		MIME: application/vnd.in-toto+json

### `arangodb:3.12` - linux; arm64 variant v8

```console
$ docker pull arangodb@sha256:eb4a6a29676756240e3cdce070139b2e3155f8a816c27003def644fbb95f482f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.5 MB (231494960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee653d3b531327ae13507d3ddc31087149e283ea91975c05fe8eca7d6a3d8cba`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Wed, 29 Jan 2025 11:48:08 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Wed, 29 Jan 2025 11:48:08 GMT
CMD ["/bin/sh"]
# Wed, 29 Jan 2025 11:48:08 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Wed, 29 Jan 2025 11:48:08 GMT
ENV ARANGO_VERSION=3.12.4
# Wed, 29 Jan 2025 11:48:08 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8003EDF6F05459984878D4A6C04AD0FD86FEC04D &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb312/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg # buildkit
# Wed, 29 Jan 2025 11:48:08 GMT
ENV GLIBCXX_FORCE_NEW=1
# Wed, 29 Jan 2025 11:48:08 GMT
RUN echo "UTC" > /etc/timezone # buildkit
# Wed, 29 Jan 2025 11:48:08 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Wed, 29 Jan 2025 11:48:08 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 29 Jan 2025 11:48:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 29 Jan 2025 11:48:08 GMT
EXPOSE map[8529/tcp:{}]
# Wed, 29 Jan 2025 11:48:08 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:200038a661537fcff0a106bde53fd78550efad67a7943fb5b6cbc76e592187c9`  
		Last Modified: Sat, 15 Feb 2025 02:48:13 GMT  
		Size: 227.5 MB (227499775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fd41fcf3c0c1828661abc790d0bab8793bb4e0ea394065dfd7381511992bc19`  
		Last Modified: Sat, 15 Feb 2025 02:47:58 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01e675dad5f2faa04d96bd057f106ac8ac5a80c5a751331e2cd44ad62d68cc38`  
		Last Modified: Sat, 15 Feb 2025 02:47:57 GMT  
		Size: 2.0 KB (2016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:3.12` - unknown; unknown

```console
$ docker pull arangodb@sha256:e857d3c5c582fe3d1b9e3e20b35cefe52d002a216addcdccacf5dfe5a8c487d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **556.2 KB (556171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:897976928a4a0fd826ed46b0e3f1f679e8777939ecaa1e29bdf47bfbe024ecfa`

```dockerfile
```

-	Layers:
	-	`sha256:6bd6932583253630ac0c585e0f75db374b5ed452702f8b6a65c2c82f9e4e9680`  
		Last Modified: Sat, 15 Feb 2025 01:13:22 GMT  
		Size: 541.7 KB (541679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1dd2c8a40fbee90edcae77ffd82986510207e2b9ba75ea65b8fc637cdcbca5f6`  
		Last Modified: Sat, 15 Feb 2025 01:13:22 GMT  
		Size: 14.5 KB (14492 bytes)  
		MIME: application/vnd.in-toto+json

## `arangodb:3.12.4`

```console
$ docker pull arangodb@sha256:b7cc8dbf5f24c0fe235b6e50a26dbcfaebaf9abe0d322acefcf3dab63b5a0102
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `arangodb:3.12.4` - linux; amd64

```console
$ docker pull arangodb@sha256:8ec63e60fcb954e7108a308795f562dafd285552aaf0d4f9824782b8be6d48b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.8 MB (232804659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c91f56b449ee93e28fb334072fb8b1d23a6baacdf73a7285467265899a878fdd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Wed, 29 Jan 2025 11:48:08 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Wed, 29 Jan 2025 11:48:08 GMT
CMD ["/bin/sh"]
# Wed, 29 Jan 2025 11:48:08 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Wed, 29 Jan 2025 11:48:08 GMT
ENV ARANGO_VERSION=3.12.4
# Wed, 29 Jan 2025 11:48:08 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8003EDF6F05459984878D4A6C04AD0FD86FEC04D &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb312/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg # buildkit
# Wed, 29 Jan 2025 11:48:08 GMT
ENV GLIBCXX_FORCE_NEW=1
# Wed, 29 Jan 2025 11:48:08 GMT
RUN echo "UTC" > /etc/timezone # buildkit
# Wed, 29 Jan 2025 11:48:08 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Wed, 29 Jan 2025 11:48:08 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 29 Jan 2025 11:48:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 29 Jan 2025 11:48:08 GMT
EXPOSE map[8529/tcp:{}]
# Wed, 29 Jan 2025 11:48:08 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6c74b8fc358e5cd758a39a8cb609904e55b1fc5f7fa5831fb157886e5599e47`  
		Last Modified: Fri, 14 Feb 2025 22:14:01 GMT  
		Size: 229.2 MB (229160256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05a93864b83fa1e50e6679ffd3ad565a60e92a6ed51e33d4f97667acffa48834`  
		Last Modified: Fri, 14 Feb 2025 22:13:53 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a82bed114865afd11ccf2719c7cca1f6e79c860b76f327275324d060bf7f6f1`  
		Last Modified: Fri, 14 Feb 2025 22:13:53 GMT  
		Size: 2.0 KB (2016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:3.12.4` - unknown; unknown

```console
$ docker pull arangodb@sha256:796bd3496b11301bed127244ec2f4cb75f998fdfcc7e981826f25d4951d76d8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **405.4 KB (405444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1d1012c5cef89ed733f225e7dab0c7e42e53d770f4f9861e05964ae3cf438b6`

```dockerfile
```

-	Layers:
	-	`sha256:76ae3dd6fddf6a30bdc1192b7249277400a0fe27ad5c6158f64fbfed5d26a80d`  
		Last Modified: Fri, 14 Feb 2025 22:13:18 GMT  
		Size: 391.1 KB (391059 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:041b9a4b47fdc7120dafb59c96a339c2165eb20a6893b6915b4b98f94c9fe9c1`  
		Last Modified: Fri, 14 Feb 2025 22:13:18 GMT  
		Size: 14.4 KB (14385 bytes)  
		MIME: application/vnd.in-toto+json

### `arangodb:3.12.4` - linux; arm64 variant v8

```console
$ docker pull arangodb@sha256:eb4a6a29676756240e3cdce070139b2e3155f8a816c27003def644fbb95f482f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.5 MB (231494960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee653d3b531327ae13507d3ddc31087149e283ea91975c05fe8eca7d6a3d8cba`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Wed, 29 Jan 2025 11:48:08 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Wed, 29 Jan 2025 11:48:08 GMT
CMD ["/bin/sh"]
# Wed, 29 Jan 2025 11:48:08 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Wed, 29 Jan 2025 11:48:08 GMT
ENV ARANGO_VERSION=3.12.4
# Wed, 29 Jan 2025 11:48:08 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8003EDF6F05459984878D4A6C04AD0FD86FEC04D &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb312/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg # buildkit
# Wed, 29 Jan 2025 11:48:08 GMT
ENV GLIBCXX_FORCE_NEW=1
# Wed, 29 Jan 2025 11:48:08 GMT
RUN echo "UTC" > /etc/timezone # buildkit
# Wed, 29 Jan 2025 11:48:08 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Wed, 29 Jan 2025 11:48:08 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 29 Jan 2025 11:48:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 29 Jan 2025 11:48:08 GMT
EXPOSE map[8529/tcp:{}]
# Wed, 29 Jan 2025 11:48:08 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:200038a661537fcff0a106bde53fd78550efad67a7943fb5b6cbc76e592187c9`  
		Last Modified: Sat, 15 Feb 2025 02:48:13 GMT  
		Size: 227.5 MB (227499775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fd41fcf3c0c1828661abc790d0bab8793bb4e0ea394065dfd7381511992bc19`  
		Last Modified: Sat, 15 Feb 2025 02:47:58 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01e675dad5f2faa04d96bd057f106ac8ac5a80c5a751331e2cd44ad62d68cc38`  
		Last Modified: Sat, 15 Feb 2025 02:47:57 GMT  
		Size: 2.0 KB (2016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:3.12.4` - unknown; unknown

```console
$ docker pull arangodb@sha256:e857d3c5c582fe3d1b9e3e20b35cefe52d002a216addcdccacf5dfe5a8c487d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **556.2 KB (556171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:897976928a4a0fd826ed46b0e3f1f679e8777939ecaa1e29bdf47bfbe024ecfa`

```dockerfile
```

-	Layers:
	-	`sha256:6bd6932583253630ac0c585e0f75db374b5ed452702f8b6a65c2c82f9e4e9680`  
		Last Modified: Sat, 15 Feb 2025 01:13:22 GMT  
		Size: 541.7 KB (541679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1dd2c8a40fbee90edcae77ffd82986510207e2b9ba75ea65b8fc637cdcbca5f6`  
		Last Modified: Sat, 15 Feb 2025 01:13:22 GMT  
		Size: 14.5 KB (14492 bytes)  
		MIME: application/vnd.in-toto+json

## `arangodb:latest`

```console
$ docker pull arangodb@sha256:b7cc8dbf5f24c0fe235b6e50a26dbcfaebaf9abe0d322acefcf3dab63b5a0102
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `arangodb:latest` - linux; amd64

```console
$ docker pull arangodb@sha256:8ec63e60fcb954e7108a308795f562dafd285552aaf0d4f9824782b8be6d48b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.8 MB (232804659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c91f56b449ee93e28fb334072fb8b1d23a6baacdf73a7285467265899a878fdd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Wed, 29 Jan 2025 11:48:08 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Wed, 29 Jan 2025 11:48:08 GMT
CMD ["/bin/sh"]
# Wed, 29 Jan 2025 11:48:08 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Wed, 29 Jan 2025 11:48:08 GMT
ENV ARANGO_VERSION=3.12.4
# Wed, 29 Jan 2025 11:48:08 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8003EDF6F05459984878D4A6C04AD0FD86FEC04D &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb312/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg # buildkit
# Wed, 29 Jan 2025 11:48:08 GMT
ENV GLIBCXX_FORCE_NEW=1
# Wed, 29 Jan 2025 11:48:08 GMT
RUN echo "UTC" > /etc/timezone # buildkit
# Wed, 29 Jan 2025 11:48:08 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Wed, 29 Jan 2025 11:48:08 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 29 Jan 2025 11:48:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 29 Jan 2025 11:48:08 GMT
EXPOSE map[8529/tcp:{}]
# Wed, 29 Jan 2025 11:48:08 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6c74b8fc358e5cd758a39a8cb609904e55b1fc5f7fa5831fb157886e5599e47`  
		Last Modified: Fri, 14 Feb 2025 22:14:01 GMT  
		Size: 229.2 MB (229160256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05a93864b83fa1e50e6679ffd3ad565a60e92a6ed51e33d4f97667acffa48834`  
		Last Modified: Fri, 14 Feb 2025 22:13:53 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a82bed114865afd11ccf2719c7cca1f6e79c860b76f327275324d060bf7f6f1`  
		Last Modified: Fri, 14 Feb 2025 22:13:53 GMT  
		Size: 2.0 KB (2016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:latest` - unknown; unknown

```console
$ docker pull arangodb@sha256:796bd3496b11301bed127244ec2f4cb75f998fdfcc7e981826f25d4951d76d8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **405.4 KB (405444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1d1012c5cef89ed733f225e7dab0c7e42e53d770f4f9861e05964ae3cf438b6`

```dockerfile
```

-	Layers:
	-	`sha256:76ae3dd6fddf6a30bdc1192b7249277400a0fe27ad5c6158f64fbfed5d26a80d`  
		Last Modified: Fri, 14 Feb 2025 22:13:18 GMT  
		Size: 391.1 KB (391059 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:041b9a4b47fdc7120dafb59c96a339c2165eb20a6893b6915b4b98f94c9fe9c1`  
		Last Modified: Fri, 14 Feb 2025 22:13:18 GMT  
		Size: 14.4 KB (14385 bytes)  
		MIME: application/vnd.in-toto+json

### `arangodb:latest` - linux; arm64 variant v8

```console
$ docker pull arangodb@sha256:eb4a6a29676756240e3cdce070139b2e3155f8a816c27003def644fbb95f482f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.5 MB (231494960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee653d3b531327ae13507d3ddc31087149e283ea91975c05fe8eca7d6a3d8cba`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Wed, 29 Jan 2025 11:48:08 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Wed, 29 Jan 2025 11:48:08 GMT
CMD ["/bin/sh"]
# Wed, 29 Jan 2025 11:48:08 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Wed, 29 Jan 2025 11:48:08 GMT
ENV ARANGO_VERSION=3.12.4
# Wed, 29 Jan 2025 11:48:08 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8003EDF6F05459984878D4A6C04AD0FD86FEC04D &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb312/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg # buildkit
# Wed, 29 Jan 2025 11:48:08 GMT
ENV GLIBCXX_FORCE_NEW=1
# Wed, 29 Jan 2025 11:48:08 GMT
RUN echo "UTC" > /etc/timezone # buildkit
# Wed, 29 Jan 2025 11:48:08 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Wed, 29 Jan 2025 11:48:08 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 29 Jan 2025 11:48:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 29 Jan 2025 11:48:08 GMT
EXPOSE map[8529/tcp:{}]
# Wed, 29 Jan 2025 11:48:08 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:200038a661537fcff0a106bde53fd78550efad67a7943fb5b6cbc76e592187c9`  
		Last Modified: Sat, 15 Feb 2025 02:48:13 GMT  
		Size: 227.5 MB (227499775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fd41fcf3c0c1828661abc790d0bab8793bb4e0ea394065dfd7381511992bc19`  
		Last Modified: Sat, 15 Feb 2025 02:47:58 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01e675dad5f2faa04d96bd057f106ac8ac5a80c5a751331e2cd44ad62d68cc38`  
		Last Modified: Sat, 15 Feb 2025 02:47:57 GMT  
		Size: 2.0 KB (2016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:latest` - unknown; unknown

```console
$ docker pull arangodb@sha256:e857d3c5c582fe3d1b9e3e20b35cefe52d002a216addcdccacf5dfe5a8c487d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **556.2 KB (556171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:897976928a4a0fd826ed46b0e3f1f679e8777939ecaa1e29bdf47bfbe024ecfa`

```dockerfile
```

-	Layers:
	-	`sha256:6bd6932583253630ac0c585e0f75db374b5ed452702f8b6a65c2c82f9e4e9680`  
		Last Modified: Sat, 15 Feb 2025 01:13:22 GMT  
		Size: 541.7 KB (541679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1dd2c8a40fbee90edcae77ffd82986510207e2b9ba75ea65b8fc637cdcbca5f6`  
		Last Modified: Sat, 15 Feb 2025 01:13:22 GMT  
		Size: 14.5 KB (14492 bytes)  
		MIME: application/vnd.in-toto+json
