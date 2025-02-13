<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `arangodb`

-	[`arangodb:3.11`](#arangodb311)
-	[`arangodb:3.11.12`](#arangodb31112)
-	[`arangodb:3.12`](#arangodb312)
-	[`arangodb:3.12.4`](#arangodb3124)
-	[`arangodb:latest`](#arangodblatest)

## `arangodb:3.11`

```console
$ docker pull arangodb@sha256:0c1a07e71d55b1b8a5a99478774d70405dfee41d5229396172cf69d940a39ae6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `arangodb:3.11` - linux; amd64

```console
$ docker pull arangodb@sha256:09fd61ae7cb0910706f100c0200635dacd8686a0b764c5f20ce659d742fcfb70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.9 MB (199858785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56c9a04e3cdcf577b469763efa82ae1d943513a7e38ca590aeafcf49bab0521a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 13 Dec 2024 15:32:12 GMT
ADD alpine-minirootfs-3.18.11-x86_64.tar.gz / # buildkit
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
	-	`sha256:f54a5150a7602eaef3169b83e73d5927b20aef2fcaefcba18b532bd63b328fff`  
		Last Modified: Tue, 14 Jan 2025 20:33:01 GMT  
		Size: 3.4 MB (3417974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aef056cdadad2ed607933f3c62624d81657d8dc0216cee11c3f24e642d8c913e`  
		Last Modified: Tue, 14 Jan 2025 21:53:37 GMT  
		Size: 196.4 MB (196438330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65d13151d30934e04765b71f4a4fe273b9b8828fef7c68307e73cba1e1a020bb`  
		Last Modified: Tue, 14 Jan 2025 21:53:25 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50c9d321f2afa733000b57882de39d715873893d0bce1fa2e2d51db73533ad49`  
		Last Modified: Tue, 14 Jan 2025 21:21:13 GMT  
		Size: 2.1 KB (2085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f074b44e7c7ad2e7bb668ff7b44d3c33156f44a168b6f3670d8634d934b3f99`  
		Last Modified: Tue, 14 Jan 2025 21:21:13 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:3.11` - unknown; unknown

```console
$ docker pull arangodb@sha256:1389307e05a4db1e5dac48dd0b072e760884d1f4eee3dc917aef6bdd9147c032
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1090078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f622951fac616df32329ea527cabc102f0297a32da4dc975dd8525aa4a976b2`

```dockerfile
```

-	Layers:
	-	`sha256:dc5f2e4b69910e0cc2731c29cfdf1a0e34e1c1da53f2d23ab2c5a315fdf6170e`  
		Last Modified: Thu, 16 Jan 2025 15:15:18 GMT  
		Size: 1.1 MB (1074222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8395b16af09e3eda0bce12f7fe5cbe4614c08d4534f4701f7c4b41b0bda25cb7`  
		Last Modified: Thu, 16 Jan 2025 15:15:18 GMT  
		Size: 15.9 KB (15856 bytes)  
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

## `arangodb:3.11.12`

```console
$ docker pull arangodb@sha256:0c1a07e71d55b1b8a5a99478774d70405dfee41d5229396172cf69d940a39ae6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `arangodb:3.11.12` - linux; amd64

```console
$ docker pull arangodb@sha256:09fd61ae7cb0910706f100c0200635dacd8686a0b764c5f20ce659d742fcfb70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.9 MB (199858785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56c9a04e3cdcf577b469763efa82ae1d943513a7e38ca590aeafcf49bab0521a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 13 Dec 2024 15:32:12 GMT
ADD alpine-minirootfs-3.18.11-x86_64.tar.gz / # buildkit
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
	-	`sha256:f54a5150a7602eaef3169b83e73d5927b20aef2fcaefcba18b532bd63b328fff`  
		Last Modified: Tue, 14 Jan 2025 20:33:01 GMT  
		Size: 3.4 MB (3417974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aef056cdadad2ed607933f3c62624d81657d8dc0216cee11c3f24e642d8c913e`  
		Last Modified: Tue, 14 Jan 2025 21:53:37 GMT  
		Size: 196.4 MB (196438330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65d13151d30934e04765b71f4a4fe273b9b8828fef7c68307e73cba1e1a020bb`  
		Last Modified: Tue, 14 Jan 2025 21:53:25 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50c9d321f2afa733000b57882de39d715873893d0bce1fa2e2d51db73533ad49`  
		Last Modified: Tue, 14 Jan 2025 21:21:13 GMT  
		Size: 2.1 KB (2085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f074b44e7c7ad2e7bb668ff7b44d3c33156f44a168b6f3670d8634d934b3f99`  
		Last Modified: Tue, 14 Jan 2025 21:21:13 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:3.11.12` - unknown; unknown

```console
$ docker pull arangodb@sha256:1389307e05a4db1e5dac48dd0b072e760884d1f4eee3dc917aef6bdd9147c032
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1090078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f622951fac616df32329ea527cabc102f0297a32da4dc975dd8525aa4a976b2`

```dockerfile
```

-	Layers:
	-	`sha256:dc5f2e4b69910e0cc2731c29cfdf1a0e34e1c1da53f2d23ab2c5a315fdf6170e`  
		Last Modified: Thu, 16 Jan 2025 15:15:18 GMT  
		Size: 1.1 MB (1074222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8395b16af09e3eda0bce12f7fe5cbe4614c08d4534f4701f7c4b41b0bda25cb7`  
		Last Modified: Thu, 16 Jan 2025 15:15:18 GMT  
		Size: 15.9 KB (15856 bytes)  
		MIME: application/vnd.in-toto+json

### `arangodb:3.11.12` - linux; arm64 variant v8

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

### `arangodb:3.11.12` - unknown; unknown

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

## `arangodb:3.12`

```console
$ docker pull arangodb@sha256:843b99d2c5db44502ec058b67bb69b30c9ba2a009bfddff3555844d9f9c1050a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `arangodb:3.12` - linux; amd64

```console
$ docker pull arangodb@sha256:bc8d975c5c4d623ecfda6e99740948ea2bd3654ac6002489d46e8670a7d30536
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.8 MB (232804164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad19c4d889a5e9fae8663371719623a7ec39c3b2ac5c5c4f9bc7cd1928577394`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
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
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Tue, 14 Jan 2025 20:33:02 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21cbbaa4ffe75c1fa2ee581499014cda04af03762d814c019aeb5b057409ced5`  
		Last Modified: Mon, 03 Feb 2025 22:38:50 GMT  
		Size: 229.2 MB (229160293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1789fa35d31f5466d129c9f53cf6f9de32eb3de7b5a091e83ca808027759bec4`  
		Last Modified: Mon, 03 Feb 2025 20:35:18 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dff4beaebc6f3bd7bb258dd5dc4fa13d97341ae2804d59cf7b98a67b8247443d`  
		Last Modified: Mon, 03 Feb 2025 20:40:00 GMT  
		Size: 2.0 KB (2016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:3.12` - unknown; unknown

```console
$ docker pull arangodb@sha256:1abc0ae3b9df4e253aff5ba8279514aec44c84df075ef5364c01366e444a714a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **405.4 KB (405438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3285e266c7f04af6a3a9a2305561f812d5e877ea4c1a643d41207187efd7dac`

```dockerfile
```

-	Layers:
	-	`sha256:b3ae0bf81aa0773991934640dbe8c8158f77b65489552355fd3afd131bcda7cb`  
		Last Modified: Thu, 13 Feb 2025 08:58:20 GMT  
		Size: 391.1 KB (391053 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c30e0e20a8ec3e41d05d70284f5111f304bd866a6be83b7d2fcefe60b7badf44`  
		Last Modified: Thu, 13 Feb 2025 08:58:20 GMT  
		Size: 14.4 KB (14385 bytes)  
		MIME: application/vnd.in-toto+json

### `arangodb:3.12` - linux; arm64 variant v8

```console
$ docker pull arangodb@sha256:8e9292e26f360ae00244947ff7ddef294dd243c2a7e24ac50f4f072935c96fb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.5 MB (231494150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9db9559a27854b251ff9d328df983e3d76bf7c39d6782d5b767a39abb79e48a2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
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
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Tue, 14 Jan 2025 20:33:00 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:515a952c8c2ffd929bafe060d52b05e0dca8460c73105534f31e6d3c7fb5e706`  
		Last Modified: Tue, 04 Feb 2025 08:10:27 GMT  
		Size: 227.5 MB (227499636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6729615bb223164967441285bba1fc52be7a38cc152de417e459852d45b5450`  
		Last Modified: Mon, 03 Feb 2025 21:13:17 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f18d1e1ea093090fbc2f2828633e471bb1a2e15ddbdd820532d22956c9b08b00`  
		Last Modified: Tue, 04 Feb 2025 12:01:03 GMT  
		Size: 2.0 KB (2015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:3.12` - unknown; unknown

```console
$ docker pull arangodb@sha256:af3c1d27e6d6c9dda484441a81d392209534988a0ea8c5aae7077de75fd789ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **556.2 KB (556165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c35a419ae7cce3478c1dd4520ec669de4dfca66f075c04e5e2d6cba13e3e7227`

```dockerfile
```

-	Layers:
	-	`sha256:25c6838add58351336f00a30f6634cec375168646d40fc44d4cb93d097ca925c`  
		Last Modified: Thu, 13 Feb 2025 08:58:39 GMT  
		Size: 541.7 KB (541673 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:123f0abbca3a954c871c66c9ef1c9eb76231ec8ccd250aaf63479a3579d10128`  
		Last Modified: Thu, 13 Feb 2025 08:58:38 GMT  
		Size: 14.5 KB (14492 bytes)  
		MIME: application/vnd.in-toto+json

## `arangodb:3.12.4`

```console
$ docker pull arangodb@sha256:843b99d2c5db44502ec058b67bb69b30c9ba2a009bfddff3555844d9f9c1050a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `arangodb:3.12.4` - linux; amd64

```console
$ docker pull arangodb@sha256:bc8d975c5c4d623ecfda6e99740948ea2bd3654ac6002489d46e8670a7d30536
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.8 MB (232804164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad19c4d889a5e9fae8663371719623a7ec39c3b2ac5c5c4f9bc7cd1928577394`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
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
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Tue, 14 Jan 2025 20:33:02 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21cbbaa4ffe75c1fa2ee581499014cda04af03762d814c019aeb5b057409ced5`  
		Last Modified: Mon, 03 Feb 2025 22:38:50 GMT  
		Size: 229.2 MB (229160293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1789fa35d31f5466d129c9f53cf6f9de32eb3de7b5a091e83ca808027759bec4`  
		Last Modified: Mon, 03 Feb 2025 20:35:18 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dff4beaebc6f3bd7bb258dd5dc4fa13d97341ae2804d59cf7b98a67b8247443d`  
		Last Modified: Mon, 03 Feb 2025 20:40:00 GMT  
		Size: 2.0 KB (2016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:3.12.4` - unknown; unknown

```console
$ docker pull arangodb@sha256:1abc0ae3b9df4e253aff5ba8279514aec44c84df075ef5364c01366e444a714a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **405.4 KB (405438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3285e266c7f04af6a3a9a2305561f812d5e877ea4c1a643d41207187efd7dac`

```dockerfile
```

-	Layers:
	-	`sha256:b3ae0bf81aa0773991934640dbe8c8158f77b65489552355fd3afd131bcda7cb`  
		Last Modified: Thu, 13 Feb 2025 08:58:20 GMT  
		Size: 391.1 KB (391053 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c30e0e20a8ec3e41d05d70284f5111f304bd866a6be83b7d2fcefe60b7badf44`  
		Last Modified: Thu, 13 Feb 2025 08:58:20 GMT  
		Size: 14.4 KB (14385 bytes)  
		MIME: application/vnd.in-toto+json

### `arangodb:3.12.4` - linux; arm64 variant v8

```console
$ docker pull arangodb@sha256:8e9292e26f360ae00244947ff7ddef294dd243c2a7e24ac50f4f072935c96fb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.5 MB (231494150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9db9559a27854b251ff9d328df983e3d76bf7c39d6782d5b767a39abb79e48a2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
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
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Tue, 14 Jan 2025 20:33:00 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:515a952c8c2ffd929bafe060d52b05e0dca8460c73105534f31e6d3c7fb5e706`  
		Last Modified: Tue, 04 Feb 2025 08:10:27 GMT  
		Size: 227.5 MB (227499636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6729615bb223164967441285bba1fc52be7a38cc152de417e459852d45b5450`  
		Last Modified: Mon, 03 Feb 2025 21:13:17 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f18d1e1ea093090fbc2f2828633e471bb1a2e15ddbdd820532d22956c9b08b00`  
		Last Modified: Tue, 04 Feb 2025 12:01:03 GMT  
		Size: 2.0 KB (2015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:3.12.4` - unknown; unknown

```console
$ docker pull arangodb@sha256:af3c1d27e6d6c9dda484441a81d392209534988a0ea8c5aae7077de75fd789ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **556.2 KB (556165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c35a419ae7cce3478c1dd4520ec669de4dfca66f075c04e5e2d6cba13e3e7227`

```dockerfile
```

-	Layers:
	-	`sha256:25c6838add58351336f00a30f6634cec375168646d40fc44d4cb93d097ca925c`  
		Last Modified: Thu, 13 Feb 2025 08:58:39 GMT  
		Size: 541.7 KB (541673 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:123f0abbca3a954c871c66c9ef1c9eb76231ec8ccd250aaf63479a3579d10128`  
		Last Modified: Thu, 13 Feb 2025 08:58:38 GMT  
		Size: 14.5 KB (14492 bytes)  
		MIME: application/vnd.in-toto+json

## `arangodb:latest`

```console
$ docker pull arangodb@sha256:843b99d2c5db44502ec058b67bb69b30c9ba2a009bfddff3555844d9f9c1050a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `arangodb:latest` - linux; amd64

```console
$ docker pull arangodb@sha256:bc8d975c5c4d623ecfda6e99740948ea2bd3654ac6002489d46e8670a7d30536
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.8 MB (232804164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad19c4d889a5e9fae8663371719623a7ec39c3b2ac5c5c4f9bc7cd1928577394`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
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
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Tue, 14 Jan 2025 20:33:02 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21cbbaa4ffe75c1fa2ee581499014cda04af03762d814c019aeb5b057409ced5`  
		Last Modified: Mon, 03 Feb 2025 22:38:50 GMT  
		Size: 229.2 MB (229160293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1789fa35d31f5466d129c9f53cf6f9de32eb3de7b5a091e83ca808027759bec4`  
		Last Modified: Mon, 03 Feb 2025 20:35:18 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dff4beaebc6f3bd7bb258dd5dc4fa13d97341ae2804d59cf7b98a67b8247443d`  
		Last Modified: Mon, 03 Feb 2025 20:40:00 GMT  
		Size: 2.0 KB (2016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:latest` - unknown; unknown

```console
$ docker pull arangodb@sha256:1abc0ae3b9df4e253aff5ba8279514aec44c84df075ef5364c01366e444a714a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **405.4 KB (405438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3285e266c7f04af6a3a9a2305561f812d5e877ea4c1a643d41207187efd7dac`

```dockerfile
```

-	Layers:
	-	`sha256:b3ae0bf81aa0773991934640dbe8c8158f77b65489552355fd3afd131bcda7cb`  
		Last Modified: Thu, 13 Feb 2025 08:58:20 GMT  
		Size: 391.1 KB (391053 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c30e0e20a8ec3e41d05d70284f5111f304bd866a6be83b7d2fcefe60b7badf44`  
		Last Modified: Thu, 13 Feb 2025 08:58:20 GMT  
		Size: 14.4 KB (14385 bytes)  
		MIME: application/vnd.in-toto+json

### `arangodb:latest` - linux; arm64 variant v8

```console
$ docker pull arangodb@sha256:8e9292e26f360ae00244947ff7ddef294dd243c2a7e24ac50f4f072935c96fb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.5 MB (231494150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9db9559a27854b251ff9d328df983e3d76bf7c39d6782d5b767a39abb79e48a2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
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
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Tue, 14 Jan 2025 20:33:00 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:515a952c8c2ffd929bafe060d52b05e0dca8460c73105534f31e6d3c7fb5e706`  
		Last Modified: Tue, 04 Feb 2025 08:10:27 GMT  
		Size: 227.5 MB (227499636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6729615bb223164967441285bba1fc52be7a38cc152de417e459852d45b5450`  
		Last Modified: Mon, 03 Feb 2025 21:13:17 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f18d1e1ea093090fbc2f2828633e471bb1a2e15ddbdd820532d22956c9b08b00`  
		Last Modified: Tue, 04 Feb 2025 12:01:03 GMT  
		Size: 2.0 KB (2015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:latest` - unknown; unknown

```console
$ docker pull arangodb@sha256:af3c1d27e6d6c9dda484441a81d392209534988a0ea8c5aae7077de75fd789ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **556.2 KB (556165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c35a419ae7cce3478c1dd4520ec669de4dfca66f075c04e5e2d6cba13e3e7227`

```dockerfile
```

-	Layers:
	-	`sha256:25c6838add58351336f00a30f6634cec375168646d40fc44d4cb93d097ca925c`  
		Last Modified: Thu, 13 Feb 2025 08:58:39 GMT  
		Size: 541.7 KB (541673 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:123f0abbca3a954c871c66c9ef1c9eb76231ec8ccd250aaf63479a3579d10128`  
		Last Modified: Thu, 13 Feb 2025 08:58:38 GMT  
		Size: 14.5 KB (14492 bytes)  
		MIME: application/vnd.in-toto+json
