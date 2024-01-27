<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `arangodb`

-	[`arangodb:3.10`](#arangodb310)
-	[`arangodb:3.10.12`](#arangodb31012)
-	[`arangodb:3.11`](#arangodb311)
-	[`arangodb:3.11.6`](#arangodb3116)
-	[`arangodb:latest`](#arangodblatest)

## `arangodb:3.10`

```console
$ docker pull arangodb@sha256:360840ef0e6b68a41d52027b97d84b2f01946b938f745a78388479c068ddda7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `arangodb:3.10` - linux; amd64

```console
$ docker pull arangodb@sha256:3c06dcdb982ffcafbfcb8a0b7091c7c269e568697375e5ec2e9eb71deda62430
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.4 MB (225376369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b7ed0cac6695ea0daee16bbea7a1d0ccd6f807efd0d507cb44b296dfd11f8bd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:09 GMT
ADD file:b308dfeecaa300a430b4e65e312a48eb5f191df7754e93ff4e7b2d04016b3ca7 in / 
# Sat, 27 Jan 2024 00:31:09 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 03:33:45 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Sat, 27 Jan 2024 03:33:45 GMT
ENV ARANGO_VERSION=3.10.12
# Sat, 27 Jan 2024 03:34:13 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb310/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Sat, 27 Jan 2024 03:34:15 GMT
ENV GLIBCXX_FORCE_NEW=1
# Sat, 27 Jan 2024 03:34:15 GMT
RUN echo "UTC" > /etc/timezone
# Sat, 27 Jan 2024 03:34:15 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Sat, 27 Jan 2024 03:34:15 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Sat, 27 Jan 2024 03:34:15 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Sat, 27 Jan 2024 03:34:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 27 Jan 2024 03:34:16 GMT
EXPOSE 8529
# Sat, 27 Jan 2024 03:34:16 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:a88dc8b54e91eb6b19695ef7e04865926d4df23004f414a3ee86978617492d4d`  
		Last Modified: Sat, 27 Jan 2024 00:31:53 GMT  
		Size: 2.8 MB (2807837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5b2424da673a34ffb56be4461c8c86bf18a7fbffb0aaaa57b6314340be0e86c`  
		Last Modified: Sat, 27 Jan 2024 03:35:23 GMT  
		Size: 222.6 MB (222566046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0ae74a791fd39f2605781f59ce2fe6188a99a03755e3daaa8b21bed0a42baa0`  
		Last Modified: Sat, 27 Jan 2024 03:35:01 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:729f3c128473f2f2d8beca67c4b790c734132aec0b3d3f353fc4564658c16010`  
		Last Modified: Sat, 27 Jan 2024 03:35:00 GMT  
		Size: 2.1 KB (2087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df4422c34a64d29b972020b351e533290f0381ef6bf8af502115e54b4205c367`  
		Last Modified: Sat, 27 Jan 2024 03:35:00 GMT  
		Size: 260.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `arangodb:3.10` - linux; arm64 variant v8

```console
$ docker pull arangodb@sha256:eab2bd43fc5540e7acad57993296a4755df75600d7bce88db4e7b85f912b912d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.5 MB (220457487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a19570d8cba559ab820a16e23d97a02eba1589b9e38e515098b7a3986816eb45`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 26 Jan 2024 23:45:05 GMT
ADD file:0808047bc74f297cb13abd2ad67e5778ee4abaa5d69f2c5b133d11c0ce0e51aa in / 
# Fri, 26 Jan 2024 23:45:05 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 00:39:03 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Sat, 27 Jan 2024 00:39:03 GMT
ENV ARANGO_VERSION=3.10.12
# Sat, 27 Jan 2024 00:39:30 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb310/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Sat, 27 Jan 2024 00:39:36 GMT
ENV GLIBCXX_FORCE_NEW=1
# Sat, 27 Jan 2024 00:39:37 GMT
RUN echo "UTC" > /etc/timezone
# Sat, 27 Jan 2024 00:39:37 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Sat, 27 Jan 2024 00:39:37 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Sat, 27 Jan 2024 00:39:37 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Sat, 27 Jan 2024 00:39:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 27 Jan 2024 00:39:37 GMT
EXPOSE 8529
# Sat, 27 Jan 2024 00:39:37 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:550f8bf8502cef18df2424ad36edbc4cc08c7ef11b44f493af59029aab98f61d`  
		Last Modified: Fri, 26 Jan 2024 23:45:48 GMT  
		Size: 2.7 MB (2708283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12ddb39f47947c54f50e1a3f4adaddd1cdebe809d4a390e784f557a5ef0c7228`  
		Last Modified: Sat, 27 Jan 2024 00:40:46 GMT  
		Size: 217.7 MB (217746719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30778fe7a10fca596efed159ed5b44700cfa91a0dcce4f8e7b058738d11c6c38`  
		Last Modified: Sat, 27 Jan 2024 00:40:29 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4629f4803e881d87b55f3ea1c0b461c9061fdea0f55fade164a661c7613e2f5e`  
		Last Modified: Sat, 27 Jan 2024 00:40:29 GMT  
		Size: 2.1 KB (2085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3aca615ab4e223c37bd783437cd9fa9eb90389511ba2817e927c6351c532fa5`  
		Last Modified: Sat, 27 Jan 2024 00:40:29 GMT  
		Size: 261.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:3.10.12`

```console
$ docker pull arangodb@sha256:360840ef0e6b68a41d52027b97d84b2f01946b938f745a78388479c068ddda7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `arangodb:3.10.12` - linux; amd64

```console
$ docker pull arangodb@sha256:3c06dcdb982ffcafbfcb8a0b7091c7c269e568697375e5ec2e9eb71deda62430
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.4 MB (225376369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b7ed0cac6695ea0daee16bbea7a1d0ccd6f807efd0d507cb44b296dfd11f8bd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:09 GMT
ADD file:b308dfeecaa300a430b4e65e312a48eb5f191df7754e93ff4e7b2d04016b3ca7 in / 
# Sat, 27 Jan 2024 00:31:09 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 03:33:45 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Sat, 27 Jan 2024 03:33:45 GMT
ENV ARANGO_VERSION=3.10.12
# Sat, 27 Jan 2024 03:34:13 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb310/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Sat, 27 Jan 2024 03:34:15 GMT
ENV GLIBCXX_FORCE_NEW=1
# Sat, 27 Jan 2024 03:34:15 GMT
RUN echo "UTC" > /etc/timezone
# Sat, 27 Jan 2024 03:34:15 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Sat, 27 Jan 2024 03:34:15 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Sat, 27 Jan 2024 03:34:15 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Sat, 27 Jan 2024 03:34:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 27 Jan 2024 03:34:16 GMT
EXPOSE 8529
# Sat, 27 Jan 2024 03:34:16 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:a88dc8b54e91eb6b19695ef7e04865926d4df23004f414a3ee86978617492d4d`  
		Last Modified: Sat, 27 Jan 2024 00:31:53 GMT  
		Size: 2.8 MB (2807837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5b2424da673a34ffb56be4461c8c86bf18a7fbffb0aaaa57b6314340be0e86c`  
		Last Modified: Sat, 27 Jan 2024 03:35:23 GMT  
		Size: 222.6 MB (222566046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0ae74a791fd39f2605781f59ce2fe6188a99a03755e3daaa8b21bed0a42baa0`  
		Last Modified: Sat, 27 Jan 2024 03:35:01 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:729f3c128473f2f2d8beca67c4b790c734132aec0b3d3f353fc4564658c16010`  
		Last Modified: Sat, 27 Jan 2024 03:35:00 GMT  
		Size: 2.1 KB (2087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df4422c34a64d29b972020b351e533290f0381ef6bf8af502115e54b4205c367`  
		Last Modified: Sat, 27 Jan 2024 03:35:00 GMT  
		Size: 260.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `arangodb:3.10.12` - linux; arm64 variant v8

```console
$ docker pull arangodb@sha256:eab2bd43fc5540e7acad57993296a4755df75600d7bce88db4e7b85f912b912d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.5 MB (220457487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a19570d8cba559ab820a16e23d97a02eba1589b9e38e515098b7a3986816eb45`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 26 Jan 2024 23:45:05 GMT
ADD file:0808047bc74f297cb13abd2ad67e5778ee4abaa5d69f2c5b133d11c0ce0e51aa in / 
# Fri, 26 Jan 2024 23:45:05 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 00:39:03 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Sat, 27 Jan 2024 00:39:03 GMT
ENV ARANGO_VERSION=3.10.12
# Sat, 27 Jan 2024 00:39:30 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb310/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Sat, 27 Jan 2024 00:39:36 GMT
ENV GLIBCXX_FORCE_NEW=1
# Sat, 27 Jan 2024 00:39:37 GMT
RUN echo "UTC" > /etc/timezone
# Sat, 27 Jan 2024 00:39:37 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Sat, 27 Jan 2024 00:39:37 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Sat, 27 Jan 2024 00:39:37 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Sat, 27 Jan 2024 00:39:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 27 Jan 2024 00:39:37 GMT
EXPOSE 8529
# Sat, 27 Jan 2024 00:39:37 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:550f8bf8502cef18df2424ad36edbc4cc08c7ef11b44f493af59029aab98f61d`  
		Last Modified: Fri, 26 Jan 2024 23:45:48 GMT  
		Size: 2.7 MB (2708283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12ddb39f47947c54f50e1a3f4adaddd1cdebe809d4a390e784f557a5ef0c7228`  
		Last Modified: Sat, 27 Jan 2024 00:40:46 GMT  
		Size: 217.7 MB (217746719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30778fe7a10fca596efed159ed5b44700cfa91a0dcce4f8e7b058738d11c6c38`  
		Last Modified: Sat, 27 Jan 2024 00:40:29 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4629f4803e881d87b55f3ea1c0b461c9061fdea0f55fade164a661c7613e2f5e`  
		Last Modified: Sat, 27 Jan 2024 00:40:29 GMT  
		Size: 2.1 KB (2085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3aca615ab4e223c37bd783437cd9fa9eb90389511ba2817e927c6351c532fa5`  
		Last Modified: Sat, 27 Jan 2024 00:40:29 GMT  
		Size: 261.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:3.11`

```console
$ docker pull arangodb@sha256:fe246b1f601b4b01bc5c9f91076a08e8f0fe8836c6a56a31353a1a46094a404e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `arangodb:3.11` - linux; amd64

```console
$ docker pull arangodb@sha256:2926e176b0a7beda276b36ee2fb87d4352773986781f5ddf5eea1ef9db6097ac
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.8 MB (249761169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:810210558f215fe40894c15384c7e2addef699415483684c261dad6e9c6c0dbd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:09 GMT
ADD file:b308dfeecaa300a430b4e65e312a48eb5f191df7754e93ff4e7b2d04016b3ca7 in / 
# Sat, 27 Jan 2024 00:31:09 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 03:33:45 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Sat, 27 Jan 2024 03:34:20 GMT
ENV ARANGO_VERSION=3.11.6
# Sat, 27 Jan 2024 03:34:48 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb311/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Sat, 27 Jan 2024 03:34:50 GMT
ENV GLIBCXX_FORCE_NEW=1
# Sat, 27 Jan 2024 03:34:51 GMT
RUN echo "UTC" > /etc/timezone
# Sat, 27 Jan 2024 03:34:51 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Sat, 27 Jan 2024 03:34:51 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Sat, 27 Jan 2024 03:34:51 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Sat, 27 Jan 2024 03:34:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 27 Jan 2024 03:34:51 GMT
EXPOSE 8529
# Sat, 27 Jan 2024 03:34:51 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:a88dc8b54e91eb6b19695ef7e04865926d4df23004f414a3ee86978617492d4d`  
		Last Modified: Sat, 27 Jan 2024 00:31:53 GMT  
		Size: 2.8 MB (2807837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf7930f60bbebfc0dec4523c98e0635f857cd5fcfc613148657ddb94bf1d9889`  
		Last Modified: Sat, 27 Jan 2024 03:35:53 GMT  
		Size: 247.0 MB (246950845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e1f643d3b38900faeb79ba64d5024fa893d0b37e06fa40f233498112541530a`  
		Last Modified: Sat, 27 Jan 2024 03:35:31 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07e62839698b1d2f091be10c2a5225209efea9b8f09fdd075bf4b104fe54ae1a`  
		Last Modified: Sat, 27 Jan 2024 03:35:31 GMT  
		Size: 2.1 KB (2087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cb353e24fb5fa164f0fc90ffd39965944a0901dbdc3d20ed3b0a391763c2587`  
		Last Modified: Sat, 27 Jan 2024 03:35:31 GMT  
		Size: 261.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `arangodb:3.11` - linux; arm64 variant v8

```console
$ docker pull arangodb@sha256:32c89594c106f83b13257a8a57ce8948f994cd14568ad87df30291289c06fff8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.9 MB (243870267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06d76f2163d78bf1b76f984ccce3eb05720722a482ed3998d57b56783e2e58b7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 26 Jan 2024 23:45:05 GMT
ADD file:0808047bc74f297cb13abd2ad67e5778ee4abaa5d69f2c5b133d11c0ce0e51aa in / 
# Fri, 26 Jan 2024 23:45:05 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 00:39:03 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Sat, 27 Jan 2024 00:39:43 GMT
ENV ARANGO_VERSION=3.11.6
# Sat, 27 Jan 2024 00:40:09 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb311/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Sat, 27 Jan 2024 00:40:16 GMT
ENV GLIBCXX_FORCE_NEW=1
# Sat, 27 Jan 2024 00:40:16 GMT
RUN echo "UTC" > /etc/timezone
# Sat, 27 Jan 2024 00:40:16 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Sat, 27 Jan 2024 00:40:16 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Sat, 27 Jan 2024 00:40:16 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Sat, 27 Jan 2024 00:40:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 27 Jan 2024 00:40:16 GMT
EXPOSE 8529
# Sat, 27 Jan 2024 00:40:16 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:550f8bf8502cef18df2424ad36edbc4cc08c7ef11b44f493af59029aab98f61d`  
		Last Modified: Fri, 26 Jan 2024 23:45:48 GMT  
		Size: 2.7 MB (2708283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07811b3267ce79180a92736166e4a622fbc1f0b5614045d38608192ddf48b873`  
		Last Modified: Sat, 27 Jan 2024 00:41:12 GMT  
		Size: 241.2 MB (241159498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97d038b17d31fbdf8b032e37b9857d47fafe15292c7dd1460e6f0112506636ad`  
		Last Modified: Sat, 27 Jan 2024 00:40:55 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec029480ad3deb03ebfa4b515f71da19cd238abf0f99f31e224b0ea4e0b74e6d`  
		Last Modified: Sat, 27 Jan 2024 00:40:55 GMT  
		Size: 2.1 KB (2085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d172f68ba3795b2cf4ca72962dad22e0126dd213e169abe772ddea0615d5497`  
		Last Modified: Sat, 27 Jan 2024 00:40:55 GMT  
		Size: 262.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:3.11.6`

```console
$ docker pull arangodb@sha256:fe246b1f601b4b01bc5c9f91076a08e8f0fe8836c6a56a31353a1a46094a404e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `arangodb:3.11.6` - linux; amd64

```console
$ docker pull arangodb@sha256:2926e176b0a7beda276b36ee2fb87d4352773986781f5ddf5eea1ef9db6097ac
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.8 MB (249761169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:810210558f215fe40894c15384c7e2addef699415483684c261dad6e9c6c0dbd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:09 GMT
ADD file:b308dfeecaa300a430b4e65e312a48eb5f191df7754e93ff4e7b2d04016b3ca7 in / 
# Sat, 27 Jan 2024 00:31:09 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 03:33:45 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Sat, 27 Jan 2024 03:34:20 GMT
ENV ARANGO_VERSION=3.11.6
# Sat, 27 Jan 2024 03:34:48 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb311/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Sat, 27 Jan 2024 03:34:50 GMT
ENV GLIBCXX_FORCE_NEW=1
# Sat, 27 Jan 2024 03:34:51 GMT
RUN echo "UTC" > /etc/timezone
# Sat, 27 Jan 2024 03:34:51 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Sat, 27 Jan 2024 03:34:51 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Sat, 27 Jan 2024 03:34:51 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Sat, 27 Jan 2024 03:34:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 27 Jan 2024 03:34:51 GMT
EXPOSE 8529
# Sat, 27 Jan 2024 03:34:51 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:a88dc8b54e91eb6b19695ef7e04865926d4df23004f414a3ee86978617492d4d`  
		Last Modified: Sat, 27 Jan 2024 00:31:53 GMT  
		Size: 2.8 MB (2807837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf7930f60bbebfc0dec4523c98e0635f857cd5fcfc613148657ddb94bf1d9889`  
		Last Modified: Sat, 27 Jan 2024 03:35:53 GMT  
		Size: 247.0 MB (246950845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e1f643d3b38900faeb79ba64d5024fa893d0b37e06fa40f233498112541530a`  
		Last Modified: Sat, 27 Jan 2024 03:35:31 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07e62839698b1d2f091be10c2a5225209efea9b8f09fdd075bf4b104fe54ae1a`  
		Last Modified: Sat, 27 Jan 2024 03:35:31 GMT  
		Size: 2.1 KB (2087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cb353e24fb5fa164f0fc90ffd39965944a0901dbdc3d20ed3b0a391763c2587`  
		Last Modified: Sat, 27 Jan 2024 03:35:31 GMT  
		Size: 261.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `arangodb:3.11.6` - linux; arm64 variant v8

```console
$ docker pull arangodb@sha256:32c89594c106f83b13257a8a57ce8948f994cd14568ad87df30291289c06fff8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.9 MB (243870267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06d76f2163d78bf1b76f984ccce3eb05720722a482ed3998d57b56783e2e58b7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 26 Jan 2024 23:45:05 GMT
ADD file:0808047bc74f297cb13abd2ad67e5778ee4abaa5d69f2c5b133d11c0ce0e51aa in / 
# Fri, 26 Jan 2024 23:45:05 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 00:39:03 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Sat, 27 Jan 2024 00:39:43 GMT
ENV ARANGO_VERSION=3.11.6
# Sat, 27 Jan 2024 00:40:09 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb311/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Sat, 27 Jan 2024 00:40:16 GMT
ENV GLIBCXX_FORCE_NEW=1
# Sat, 27 Jan 2024 00:40:16 GMT
RUN echo "UTC" > /etc/timezone
# Sat, 27 Jan 2024 00:40:16 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Sat, 27 Jan 2024 00:40:16 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Sat, 27 Jan 2024 00:40:16 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Sat, 27 Jan 2024 00:40:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 27 Jan 2024 00:40:16 GMT
EXPOSE 8529
# Sat, 27 Jan 2024 00:40:16 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:550f8bf8502cef18df2424ad36edbc4cc08c7ef11b44f493af59029aab98f61d`  
		Last Modified: Fri, 26 Jan 2024 23:45:48 GMT  
		Size: 2.7 MB (2708283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07811b3267ce79180a92736166e4a622fbc1f0b5614045d38608192ddf48b873`  
		Last Modified: Sat, 27 Jan 2024 00:41:12 GMT  
		Size: 241.2 MB (241159498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97d038b17d31fbdf8b032e37b9857d47fafe15292c7dd1460e6f0112506636ad`  
		Last Modified: Sat, 27 Jan 2024 00:40:55 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec029480ad3deb03ebfa4b515f71da19cd238abf0f99f31e224b0ea4e0b74e6d`  
		Last Modified: Sat, 27 Jan 2024 00:40:55 GMT  
		Size: 2.1 KB (2085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d172f68ba3795b2cf4ca72962dad22e0126dd213e169abe772ddea0615d5497`  
		Last Modified: Sat, 27 Jan 2024 00:40:55 GMT  
		Size: 262.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:latest`

```console
$ docker pull arangodb@sha256:fe246b1f601b4b01bc5c9f91076a08e8f0fe8836c6a56a31353a1a46094a404e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `arangodb:latest` - linux; amd64

```console
$ docker pull arangodb@sha256:2926e176b0a7beda276b36ee2fb87d4352773986781f5ddf5eea1ef9db6097ac
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.8 MB (249761169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:810210558f215fe40894c15384c7e2addef699415483684c261dad6e9c6c0dbd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:09 GMT
ADD file:b308dfeecaa300a430b4e65e312a48eb5f191df7754e93ff4e7b2d04016b3ca7 in / 
# Sat, 27 Jan 2024 00:31:09 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 03:33:45 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Sat, 27 Jan 2024 03:34:20 GMT
ENV ARANGO_VERSION=3.11.6
# Sat, 27 Jan 2024 03:34:48 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb311/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Sat, 27 Jan 2024 03:34:50 GMT
ENV GLIBCXX_FORCE_NEW=1
# Sat, 27 Jan 2024 03:34:51 GMT
RUN echo "UTC" > /etc/timezone
# Sat, 27 Jan 2024 03:34:51 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Sat, 27 Jan 2024 03:34:51 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Sat, 27 Jan 2024 03:34:51 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Sat, 27 Jan 2024 03:34:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 27 Jan 2024 03:34:51 GMT
EXPOSE 8529
# Sat, 27 Jan 2024 03:34:51 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:a88dc8b54e91eb6b19695ef7e04865926d4df23004f414a3ee86978617492d4d`  
		Last Modified: Sat, 27 Jan 2024 00:31:53 GMT  
		Size: 2.8 MB (2807837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf7930f60bbebfc0dec4523c98e0635f857cd5fcfc613148657ddb94bf1d9889`  
		Last Modified: Sat, 27 Jan 2024 03:35:53 GMT  
		Size: 247.0 MB (246950845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e1f643d3b38900faeb79ba64d5024fa893d0b37e06fa40f233498112541530a`  
		Last Modified: Sat, 27 Jan 2024 03:35:31 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07e62839698b1d2f091be10c2a5225209efea9b8f09fdd075bf4b104fe54ae1a`  
		Last Modified: Sat, 27 Jan 2024 03:35:31 GMT  
		Size: 2.1 KB (2087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cb353e24fb5fa164f0fc90ffd39965944a0901dbdc3d20ed3b0a391763c2587`  
		Last Modified: Sat, 27 Jan 2024 03:35:31 GMT  
		Size: 261.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `arangodb:latest` - linux; arm64 variant v8

```console
$ docker pull arangodb@sha256:32c89594c106f83b13257a8a57ce8948f994cd14568ad87df30291289c06fff8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.9 MB (243870267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06d76f2163d78bf1b76f984ccce3eb05720722a482ed3998d57b56783e2e58b7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 26 Jan 2024 23:45:05 GMT
ADD file:0808047bc74f297cb13abd2ad67e5778ee4abaa5d69f2c5b133d11c0ce0e51aa in / 
# Fri, 26 Jan 2024 23:45:05 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 00:39:03 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Sat, 27 Jan 2024 00:39:43 GMT
ENV ARANGO_VERSION=3.11.6
# Sat, 27 Jan 2024 00:40:09 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb311/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Sat, 27 Jan 2024 00:40:16 GMT
ENV GLIBCXX_FORCE_NEW=1
# Sat, 27 Jan 2024 00:40:16 GMT
RUN echo "UTC" > /etc/timezone
# Sat, 27 Jan 2024 00:40:16 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Sat, 27 Jan 2024 00:40:16 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Sat, 27 Jan 2024 00:40:16 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Sat, 27 Jan 2024 00:40:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 27 Jan 2024 00:40:16 GMT
EXPOSE 8529
# Sat, 27 Jan 2024 00:40:16 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:550f8bf8502cef18df2424ad36edbc4cc08c7ef11b44f493af59029aab98f61d`  
		Last Modified: Fri, 26 Jan 2024 23:45:48 GMT  
		Size: 2.7 MB (2708283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07811b3267ce79180a92736166e4a622fbc1f0b5614045d38608192ddf48b873`  
		Last Modified: Sat, 27 Jan 2024 00:41:12 GMT  
		Size: 241.2 MB (241159498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97d038b17d31fbdf8b032e37b9857d47fafe15292c7dd1460e6f0112506636ad`  
		Last Modified: Sat, 27 Jan 2024 00:40:55 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec029480ad3deb03ebfa4b515f71da19cd238abf0f99f31e224b0ea4e0b74e6d`  
		Last Modified: Sat, 27 Jan 2024 00:40:55 GMT  
		Size: 2.1 KB (2085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d172f68ba3795b2cf4ca72962dad22e0126dd213e169abe772ddea0615d5497`  
		Last Modified: Sat, 27 Jan 2024 00:40:55 GMT  
		Size: 262.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
