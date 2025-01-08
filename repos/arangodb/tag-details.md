<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `arangodb`

-	[`arangodb:3.11`](#arangodb311)
-	[`arangodb:3.11.12`](#arangodb31112)
-	[`arangodb:3.12`](#arangodb312)
-	[`arangodb:3.12.3`](#arangodb3123)
-	[`arangodb:latest`](#arangodblatest)

## `arangodb:3.11`

```console
$ docker pull arangodb@sha256:57fdfa8f1be2eef80a899ba24d05d1be9096b8c63237e7b90a9024dcd08607c8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `arangodb:3.11` - linux; amd64

```console
$ docker pull arangodb@sha256:e89a7bbf0b2687a4a198a97e6de690d4b88debd72b9c19ad10daf443e7e86bcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.8 MB (199810713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa0be798da9e2528d00742e30304577c4f29dc1b70bed0e0fa0dc87670bd38a8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 13 Dec 2024 15:32:12 GMT
ADD alpine-minirootfs-3.18.10-x86_64.tar.gz / # buildkit
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
	-	`sha256:5fa62e1bbddf13eb6443e20aa8ed938bec91a8a5d5d0a26e58e8eafb3ada9a1c`  
		Last Modified: Tue, 07 Jan 2025 02:28:37 GMT  
		Size: 3.4 MB (3407632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a39edd8bf4a04be80bae72949dc055ecb1192ae8867b4a1da0e9dfe52715f345`  
		Last Modified: Tue, 07 Jan 2025 03:14:47 GMT  
		Size: 196.4 MB (196400595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96ad78f028c0c9ac70da0ac980e98ca04ffb90182390635dd8339ce4bfa49b39`  
		Last Modified: Tue, 07 Jan 2025 03:14:43 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6a1b2a394ff89e587f7da8b03adb406a244896d0a6f8cd4865e7526ff0cbf5f`  
		Last Modified: Tue, 07 Jan 2025 03:14:44 GMT  
		Size: 2.1 KB (2087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7aaa3d42c6f8874a8b060d9b5765011b7dbc401e3bfcb4ea7da38761adeb693`  
		Last Modified: Tue, 07 Jan 2025 03:14:44 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:3.11` - unknown; unknown

```console
$ docker pull arangodb@sha256:81fac46e7c284925d2296d249207a6c28d314068e247dda105137698fd51c0de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1084200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4db5074585c42654f2792f231f4ad2437ce05507b8ff7e242b65c8129640d4b2`

```dockerfile
```

-	Layers:
	-	`sha256:5866639dcff9612bca115cb02bd76f2a04f3ae924dfc3b96c867ae6ec9f5f96e`  
		Last Modified: Tue, 07 Jan 2025 03:14:44 GMT  
		Size: 1.1 MB (1068344 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d4d6191acf40eb9aa7ba62e991f6f3b377c7b7fc828ad094002be2b6b7f1598`  
		Last Modified: Tue, 07 Jan 2025 03:14:43 GMT  
		Size: 15.9 KB (15856 bytes)  
		MIME: application/vnd.in-toto+json

### `arangodb:3.11` - linux; arm64 variant v8

```console
$ docker pull arangodb@sha256:c5b9ba9bf387ce14a9f08a7512c60bac9c11737059ce407fdd2c54bb32732bef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.5 MB (203526325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ed545b20d5d60663c9b3354f7273c6a05c9dad809565a65f1b48255f812bc8b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 13 Dec 2024 15:32:12 GMT
ADD alpine-minirootfs-3.18.10-aarch64.tar.gz / # buildkit
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
	-	`sha256:fb3f1f9d2d6533828602bbf29a9a8cc07ae4a2a3e88846100e68ce43a16d2932`  
		Last Modified: Tue, 07 Jan 2025 03:03:28 GMT  
		Size: 3.3 MB (3337435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1bda0a5261a385467cdd3f99e61c964b08d3db4df5d3ef64b9c5d07fa3c185c`  
		Last Modified: Tue, 07 Jan 2025 03:43:26 GMT  
		Size: 200.2 MB (200186407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fe04edea97a75fce5cd76deb099b38c55d2564e47c9b629d893c65e33bde6d1`  
		Last Modified: Tue, 07 Jan 2025 03:43:21 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dddcf9506869c7d5982e93860a87a69d755f5dd8afef740ce44c7c27b531fb7f`  
		Last Modified: Tue, 07 Jan 2025 03:43:21 GMT  
		Size: 2.1 KB (2086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8567f3cb9dffd22919327bea56bfbf022f8f97d30383a4b3e8b7c195406dca0`  
		Last Modified: Tue, 07 Jan 2025 03:43:22 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:3.11` - unknown; unknown

```console
$ docker pull arangodb@sha256:6fa674f83c6f7ee3e7d73ce8ed237797660ff59d6ed4c5950d7e3736e81c8afe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1189420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:489b75c1f71651a276a3395c720505f46946f530aea4e5372cb39efa0e6b144e`

```dockerfile
```

-	Layers:
	-	`sha256:5ca71e1d72f1835f1ac6551d577ec0144b76ea83dea6a8e95a0a1b05d01fbd98`  
		Last Modified: Tue, 07 Jan 2025 03:43:22 GMT  
		Size: 1.2 MB (1173469 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b1a6aa5104c8ca2361c0c5f471e7c823f9b03e9875837ee4a0609536fae96b4`  
		Last Modified: Tue, 07 Jan 2025 03:43:21 GMT  
		Size: 16.0 KB (15951 bytes)  
		MIME: application/vnd.in-toto+json

## `arangodb:3.11.12`

```console
$ docker pull arangodb@sha256:57fdfa8f1be2eef80a899ba24d05d1be9096b8c63237e7b90a9024dcd08607c8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `arangodb:3.11.12` - linux; amd64

```console
$ docker pull arangodb@sha256:e89a7bbf0b2687a4a198a97e6de690d4b88debd72b9c19ad10daf443e7e86bcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.8 MB (199810713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa0be798da9e2528d00742e30304577c4f29dc1b70bed0e0fa0dc87670bd38a8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 13 Dec 2024 15:32:12 GMT
ADD alpine-minirootfs-3.18.10-x86_64.tar.gz / # buildkit
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
	-	`sha256:5fa62e1bbddf13eb6443e20aa8ed938bec91a8a5d5d0a26e58e8eafb3ada9a1c`  
		Last Modified: Tue, 07 Jan 2025 02:28:37 GMT  
		Size: 3.4 MB (3407632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a39edd8bf4a04be80bae72949dc055ecb1192ae8867b4a1da0e9dfe52715f345`  
		Last Modified: Tue, 07 Jan 2025 03:14:47 GMT  
		Size: 196.4 MB (196400595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96ad78f028c0c9ac70da0ac980e98ca04ffb90182390635dd8339ce4bfa49b39`  
		Last Modified: Tue, 07 Jan 2025 03:14:43 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6a1b2a394ff89e587f7da8b03adb406a244896d0a6f8cd4865e7526ff0cbf5f`  
		Last Modified: Tue, 07 Jan 2025 03:14:44 GMT  
		Size: 2.1 KB (2087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7aaa3d42c6f8874a8b060d9b5765011b7dbc401e3bfcb4ea7da38761adeb693`  
		Last Modified: Tue, 07 Jan 2025 03:14:44 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:3.11.12` - unknown; unknown

```console
$ docker pull arangodb@sha256:81fac46e7c284925d2296d249207a6c28d314068e247dda105137698fd51c0de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1084200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4db5074585c42654f2792f231f4ad2437ce05507b8ff7e242b65c8129640d4b2`

```dockerfile
```

-	Layers:
	-	`sha256:5866639dcff9612bca115cb02bd76f2a04f3ae924dfc3b96c867ae6ec9f5f96e`  
		Last Modified: Tue, 07 Jan 2025 03:14:44 GMT  
		Size: 1.1 MB (1068344 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d4d6191acf40eb9aa7ba62e991f6f3b377c7b7fc828ad094002be2b6b7f1598`  
		Last Modified: Tue, 07 Jan 2025 03:14:43 GMT  
		Size: 15.9 KB (15856 bytes)  
		MIME: application/vnd.in-toto+json

### `arangodb:3.11.12` - linux; arm64 variant v8

```console
$ docker pull arangodb@sha256:c5b9ba9bf387ce14a9f08a7512c60bac9c11737059ce407fdd2c54bb32732bef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.5 MB (203526325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ed545b20d5d60663c9b3354f7273c6a05c9dad809565a65f1b48255f812bc8b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 13 Dec 2024 15:32:12 GMT
ADD alpine-minirootfs-3.18.10-aarch64.tar.gz / # buildkit
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
	-	`sha256:fb3f1f9d2d6533828602bbf29a9a8cc07ae4a2a3e88846100e68ce43a16d2932`  
		Last Modified: Tue, 07 Jan 2025 03:03:28 GMT  
		Size: 3.3 MB (3337435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1bda0a5261a385467cdd3f99e61c964b08d3db4df5d3ef64b9c5d07fa3c185c`  
		Last Modified: Tue, 07 Jan 2025 03:43:26 GMT  
		Size: 200.2 MB (200186407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fe04edea97a75fce5cd76deb099b38c55d2564e47c9b629d893c65e33bde6d1`  
		Last Modified: Tue, 07 Jan 2025 03:43:21 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dddcf9506869c7d5982e93860a87a69d755f5dd8afef740ce44c7c27b531fb7f`  
		Last Modified: Tue, 07 Jan 2025 03:43:21 GMT  
		Size: 2.1 KB (2086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8567f3cb9dffd22919327bea56bfbf022f8f97d30383a4b3e8b7c195406dca0`  
		Last Modified: Tue, 07 Jan 2025 03:43:22 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:3.11.12` - unknown; unknown

```console
$ docker pull arangodb@sha256:6fa674f83c6f7ee3e7d73ce8ed237797660ff59d6ed4c5950d7e3736e81c8afe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1189420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:489b75c1f71651a276a3395c720505f46946f530aea4e5372cb39efa0e6b144e`

```dockerfile
```

-	Layers:
	-	`sha256:5ca71e1d72f1835f1ac6551d577ec0144b76ea83dea6a8e95a0a1b05d01fbd98`  
		Last Modified: Tue, 07 Jan 2025 03:43:22 GMT  
		Size: 1.2 MB (1173469 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b1a6aa5104c8ca2361c0c5f471e7c823f9b03e9875837ee4a0609536fae96b4`  
		Last Modified: Tue, 07 Jan 2025 03:43:21 GMT  
		Size: 16.0 KB (15951 bytes)  
		MIME: application/vnd.in-toto+json

## `arangodb:3.12`

```console
$ docker pull arangodb@sha256:2ee64e9bbd58df86142d6071a64c32a2235503721e8ee37d8a85a878309ba73a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `arangodb:3.12` - linux; amd64

```console
$ docker pull arangodb@sha256:4e628e0f7f6207f61cea4403e4d3f4bd13d56fe1269d43841aa6470b5e284e47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.0 MB (304972016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16f1bc16513cc57b2c1917ca50f8bfc8c858390f0071d1ba24a1e698994424a2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 13 Dec 2024 15:32:12 GMT
ADD alpine-minirootfs-3.18.10-x86_64.tar.gz / # buildkit
# Fri, 13 Dec 2024 15:32:12 GMT
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
	-	`sha256:5fa62e1bbddf13eb6443e20aa8ed938bec91a8a5d5d0a26e58e8eafb3ada9a1c`  
		Last Modified: Tue, 07 Jan 2025 02:28:37 GMT  
		Size: 3.4 MB (3407632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afbf11229f90d63e134ecbba3c7ae2cca5ac5999024c047fee6c57165aab9c24`  
		Last Modified: Tue, 07 Jan 2025 03:14:40 GMT  
		Size: 301.6 MB (301562228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e04f7e25502cc7d4e11aa930e7ea544213c22c7ba8aadec7127d41beb6ae2b2`  
		Last Modified: Tue, 07 Jan 2025 03:14:36 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec376324cb0972efed8b6f9183e6f78ba4f3c069c46d448466c95a672f5319e9`  
		Last Modified: Tue, 07 Jan 2025 03:14:36 GMT  
		Size: 2.0 KB (2016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:3.12` - unknown; unknown

```console
$ docker pull arangodb@sha256:7743a6731316c56510e09981baef0ef09042e7fbcb315e3630806b467cb6b6e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **376.7 KB (376740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ff6780334b88ef7de3dd06bee4ce614f5313057111cc5c70c0425e8d731c722`

```dockerfile
```

-	Layers:
	-	`sha256:269bab6665f1b334c1f34c22e3d6363bd8bf0cd24e55b7d69591df0c8e75494b`  
		Last Modified: Tue, 07 Jan 2025 03:14:36 GMT  
		Size: 362.3 KB (362320 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ccd09f6814ef304a72499307a47a1590ccb224300202e5b95d7a10944ff97431`  
		Last Modified: Tue, 07 Jan 2025 03:14:36 GMT  
		Size: 14.4 KB (14420 bytes)  
		MIME: application/vnd.in-toto+json

### `arangodb:3.12` - linux; arm64 variant v8

```console
$ docker pull arangodb@sha256:441577c0d15f95f6c9d7cbe369940f9a29ac3a04aa9fd31de66e2640fd6f002c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.0 MB (307019115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a30e916709f2ff63811f2a26daef81d1d6dbaa8a39d04ddfacd66334b1032eb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 13 Dec 2024 15:32:12 GMT
ADD alpine-minirootfs-3.18.10-aarch64.tar.gz / # buildkit
# Fri, 13 Dec 2024 15:32:12 GMT
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
	-	`sha256:fb3f1f9d2d6533828602bbf29a9a8cc07ae4a2a3e88846100e68ce43a16d2932`  
		Last Modified: Tue, 07 Jan 2025 03:03:28 GMT  
		Size: 3.3 MB (3337435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e64b5ce7f2160f9346e9bc078ee073b48fcfd261eda6fe979ef6ebb950c5f591`  
		Last Modified: Tue, 07 Jan 2025 03:44:34 GMT  
		Size: 303.7 MB (303679523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6a04b1ecc0657480f7ca3c9f2d40fc0606c485e640a03e894b7315a9a3eb817`  
		Last Modified: Tue, 07 Jan 2025 03:44:27 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2e288f5200958f847d861466a61a7565f2be2907c60828348da69ca07da9799`  
		Size: 2.0 KB (2017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:3.12` - unknown; unknown

```console
$ docker pull arangodb@sha256:07128f63f7fa261258f840dac632da20f15aa4dc3e61cf20dae4d260b722f638
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **482.0 KB (481985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b6e26febbd73be336bceab1d4497da0169bcdb010bf77923db36dd06299b8df`

```dockerfile
```

-	Layers:
	-	`sha256:d7f522ec481457d4c43d67a321b45f71b1ef4fddb668280077e1d26548fa5261`  
		Last Modified: Tue, 07 Jan 2025 03:44:27 GMT  
		Size: 467.5 KB (467457 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2280ff891e91a875704f6a288c0abf8417111f3278f7283886a96359d1a9fca3`  
		Size: 14.5 KB (14528 bytes)  
		MIME: application/vnd.in-toto+json

## `arangodb:3.12.3`

```console
$ docker pull arangodb@sha256:2ee64e9bbd58df86142d6071a64c32a2235503721e8ee37d8a85a878309ba73a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `arangodb:3.12.3` - linux; amd64

```console
$ docker pull arangodb@sha256:4e628e0f7f6207f61cea4403e4d3f4bd13d56fe1269d43841aa6470b5e284e47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.0 MB (304972016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16f1bc16513cc57b2c1917ca50f8bfc8c858390f0071d1ba24a1e698994424a2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 13 Dec 2024 15:32:12 GMT
ADD alpine-minirootfs-3.18.10-x86_64.tar.gz / # buildkit
# Fri, 13 Dec 2024 15:32:12 GMT
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
	-	`sha256:5fa62e1bbddf13eb6443e20aa8ed938bec91a8a5d5d0a26e58e8eafb3ada9a1c`  
		Last Modified: Tue, 07 Jan 2025 02:28:37 GMT  
		Size: 3.4 MB (3407632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afbf11229f90d63e134ecbba3c7ae2cca5ac5999024c047fee6c57165aab9c24`  
		Last Modified: Tue, 07 Jan 2025 03:14:40 GMT  
		Size: 301.6 MB (301562228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e04f7e25502cc7d4e11aa930e7ea544213c22c7ba8aadec7127d41beb6ae2b2`  
		Last Modified: Tue, 07 Jan 2025 03:14:36 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec376324cb0972efed8b6f9183e6f78ba4f3c069c46d448466c95a672f5319e9`  
		Last Modified: Tue, 07 Jan 2025 03:14:36 GMT  
		Size: 2.0 KB (2016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:3.12.3` - unknown; unknown

```console
$ docker pull arangodb@sha256:7743a6731316c56510e09981baef0ef09042e7fbcb315e3630806b467cb6b6e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **376.7 KB (376740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ff6780334b88ef7de3dd06bee4ce614f5313057111cc5c70c0425e8d731c722`

```dockerfile
```

-	Layers:
	-	`sha256:269bab6665f1b334c1f34c22e3d6363bd8bf0cd24e55b7d69591df0c8e75494b`  
		Last Modified: Tue, 07 Jan 2025 03:14:36 GMT  
		Size: 362.3 KB (362320 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ccd09f6814ef304a72499307a47a1590ccb224300202e5b95d7a10944ff97431`  
		Last Modified: Tue, 07 Jan 2025 03:14:36 GMT  
		Size: 14.4 KB (14420 bytes)  
		MIME: application/vnd.in-toto+json

### `arangodb:3.12.3` - linux; arm64 variant v8

```console
$ docker pull arangodb@sha256:441577c0d15f95f6c9d7cbe369940f9a29ac3a04aa9fd31de66e2640fd6f002c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.0 MB (307019115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a30e916709f2ff63811f2a26daef81d1d6dbaa8a39d04ddfacd66334b1032eb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 13 Dec 2024 15:32:12 GMT
ADD alpine-minirootfs-3.18.10-aarch64.tar.gz / # buildkit
# Fri, 13 Dec 2024 15:32:12 GMT
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
	-	`sha256:fb3f1f9d2d6533828602bbf29a9a8cc07ae4a2a3e88846100e68ce43a16d2932`  
		Last Modified: Tue, 07 Jan 2025 03:03:28 GMT  
		Size: 3.3 MB (3337435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e64b5ce7f2160f9346e9bc078ee073b48fcfd261eda6fe979ef6ebb950c5f591`  
		Last Modified: Tue, 07 Jan 2025 03:44:34 GMT  
		Size: 303.7 MB (303679523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6a04b1ecc0657480f7ca3c9f2d40fc0606c485e640a03e894b7315a9a3eb817`  
		Last Modified: Tue, 07 Jan 2025 03:44:27 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2e288f5200958f847d861466a61a7565f2be2907c60828348da69ca07da9799`  
		Size: 2.0 KB (2017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:3.12.3` - unknown; unknown

```console
$ docker pull arangodb@sha256:07128f63f7fa261258f840dac632da20f15aa4dc3e61cf20dae4d260b722f638
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **482.0 KB (481985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b6e26febbd73be336bceab1d4497da0169bcdb010bf77923db36dd06299b8df`

```dockerfile
```

-	Layers:
	-	`sha256:d7f522ec481457d4c43d67a321b45f71b1ef4fddb668280077e1d26548fa5261`  
		Last Modified: Tue, 07 Jan 2025 03:44:27 GMT  
		Size: 467.5 KB (467457 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2280ff891e91a875704f6a288c0abf8417111f3278f7283886a96359d1a9fca3`  
		Size: 14.5 KB (14528 bytes)  
		MIME: application/vnd.in-toto+json

## `arangodb:latest`

```console
$ docker pull arangodb@sha256:2ee64e9bbd58df86142d6071a64c32a2235503721e8ee37d8a85a878309ba73a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `arangodb:latest` - linux; amd64

```console
$ docker pull arangodb@sha256:4e628e0f7f6207f61cea4403e4d3f4bd13d56fe1269d43841aa6470b5e284e47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.0 MB (304972016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16f1bc16513cc57b2c1917ca50f8bfc8c858390f0071d1ba24a1e698994424a2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 13 Dec 2024 15:32:12 GMT
ADD alpine-minirootfs-3.18.10-x86_64.tar.gz / # buildkit
# Fri, 13 Dec 2024 15:32:12 GMT
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
	-	`sha256:5fa62e1bbddf13eb6443e20aa8ed938bec91a8a5d5d0a26e58e8eafb3ada9a1c`  
		Last Modified: Tue, 07 Jan 2025 02:28:37 GMT  
		Size: 3.4 MB (3407632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afbf11229f90d63e134ecbba3c7ae2cca5ac5999024c047fee6c57165aab9c24`  
		Last Modified: Tue, 07 Jan 2025 03:14:40 GMT  
		Size: 301.6 MB (301562228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e04f7e25502cc7d4e11aa930e7ea544213c22c7ba8aadec7127d41beb6ae2b2`  
		Last Modified: Tue, 07 Jan 2025 03:14:36 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec376324cb0972efed8b6f9183e6f78ba4f3c069c46d448466c95a672f5319e9`  
		Last Modified: Tue, 07 Jan 2025 03:14:36 GMT  
		Size: 2.0 KB (2016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:latest` - unknown; unknown

```console
$ docker pull arangodb@sha256:7743a6731316c56510e09981baef0ef09042e7fbcb315e3630806b467cb6b6e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **376.7 KB (376740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ff6780334b88ef7de3dd06bee4ce614f5313057111cc5c70c0425e8d731c722`

```dockerfile
```

-	Layers:
	-	`sha256:269bab6665f1b334c1f34c22e3d6363bd8bf0cd24e55b7d69591df0c8e75494b`  
		Last Modified: Tue, 07 Jan 2025 03:14:36 GMT  
		Size: 362.3 KB (362320 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ccd09f6814ef304a72499307a47a1590ccb224300202e5b95d7a10944ff97431`  
		Last Modified: Tue, 07 Jan 2025 03:14:36 GMT  
		Size: 14.4 KB (14420 bytes)  
		MIME: application/vnd.in-toto+json

### `arangodb:latest` - linux; arm64 variant v8

```console
$ docker pull arangodb@sha256:441577c0d15f95f6c9d7cbe369940f9a29ac3a04aa9fd31de66e2640fd6f002c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.0 MB (307019115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a30e916709f2ff63811f2a26daef81d1d6dbaa8a39d04ddfacd66334b1032eb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 13 Dec 2024 15:32:12 GMT
ADD alpine-minirootfs-3.18.10-aarch64.tar.gz / # buildkit
# Fri, 13 Dec 2024 15:32:12 GMT
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
	-	`sha256:fb3f1f9d2d6533828602bbf29a9a8cc07ae4a2a3e88846100e68ce43a16d2932`  
		Last Modified: Tue, 07 Jan 2025 03:03:28 GMT  
		Size: 3.3 MB (3337435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e64b5ce7f2160f9346e9bc078ee073b48fcfd261eda6fe979ef6ebb950c5f591`  
		Last Modified: Tue, 07 Jan 2025 03:44:34 GMT  
		Size: 303.7 MB (303679523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6a04b1ecc0657480f7ca3c9f2d40fc0606c485e640a03e894b7315a9a3eb817`  
		Last Modified: Tue, 07 Jan 2025 03:44:27 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2e288f5200958f847d861466a61a7565f2be2907c60828348da69ca07da9799`  
		Size: 2.0 KB (2017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:latest` - unknown; unknown

```console
$ docker pull arangodb@sha256:07128f63f7fa261258f840dac632da20f15aa4dc3e61cf20dae4d260b722f638
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **482.0 KB (481985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b6e26febbd73be336bceab1d4497da0169bcdb010bf77923db36dd06299b8df`

```dockerfile
```

-	Layers:
	-	`sha256:d7f522ec481457d4c43d67a321b45f71b1ef4fddb668280077e1d26548fa5261`  
		Last Modified: Tue, 07 Jan 2025 03:44:27 GMT  
		Size: 467.5 KB (467457 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2280ff891e91a875704f6a288c0abf8417111f3278f7283886a96359d1a9fca3`  
		Size: 14.5 KB (14528 bytes)  
		MIME: application/vnd.in-toto+json
