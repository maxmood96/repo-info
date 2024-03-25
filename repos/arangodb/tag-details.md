<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `arangodb`

-	[`arangodb:3.10`](#arangodb310)
-	[`arangodb:3.10.13`](#arangodb31013)
-	[`arangodb:3.11`](#arangodb311)
-	[`arangodb:3.11.8`](#arangodb3118)
-	[`arangodb:3.12`](#arangodb312)
-	[`arangodb:3.12.0`](#arangodb3120)
-	[`arangodb:latest`](#arangodblatest)

## `arangodb:3.10`

```console
$ docker pull arangodb@sha256:579f234e5fb0a3df51119fa570ae91991f6a513cc05c09f93455de2191d49e9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `arangodb:3.10` - linux; amd64

```console
$ docker pull arangodb@sha256:26133c97b9a3fe81eea5b05b012c809264f627e2873a7018543d532b1463499c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.9 MB (224870161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a661ab513de166ccb4033fa2ff416d4c522e9d49d715e86a25f021308688ae2f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:09 GMT
ADD file:b308dfeecaa300a430b4e65e312a48eb5f191df7754e93ff4e7b2d04016b3ca7 in / 
# Sat, 27 Jan 2024 00:31:09 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 06:18:53 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Sat, 16 Mar 2024 06:18:53 GMT
ENV ARANGO_VERSION=3.10.13
# Sat, 16 Mar 2024 06:19:21 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb310/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Sat, 16 Mar 2024 06:19:23 GMT
ENV GLIBCXX_FORCE_NEW=1
# Sat, 16 Mar 2024 06:19:24 GMT
RUN echo "UTC" > /etc/timezone
# Sat, 16 Mar 2024 06:19:24 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Sat, 16 Mar 2024 06:19:24 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Sat, 16 Mar 2024 06:19:24 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Sat, 16 Mar 2024 06:19:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 Mar 2024 06:19:24 GMT
EXPOSE 8529
# Sat, 16 Mar 2024 06:19:24 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:a88dc8b54e91eb6b19695ef7e04865926d4df23004f414a3ee86978617492d4d`  
		Last Modified: Sat, 27 Jan 2024 00:31:53 GMT  
		Size: 2.8 MB (2807837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0944a22df89a680fc29c006f041a3a567cd44ec008f5d9cb9e3c0374e63e520`  
		Last Modified: Sat, 16 Mar 2024 06:20:30 GMT  
		Size: 222.1 MB (222059838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6df177555217d9063860aeb57c0238bb794ec1df9a41ecb1cf6fa8d1fd54aa38`  
		Last Modified: Sat, 16 Mar 2024 06:20:08 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b0348faaf3e382522076db041338ad1960ef8f6fdb0d1a642ce020887fa385a`  
		Last Modified: Sat, 16 Mar 2024 06:20:08 GMT  
		Size: 2.1 KB (2086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca535f443f46be87728bc03cebe2327f2b7bf192554d9cfd7b6c282985e71a1e`  
		Last Modified: Sat, 16 Mar 2024 06:20:08 GMT  
		Size: 261.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `arangodb:3.10` - linux; arm64 variant v8

```console
$ docker pull arangodb@sha256:634807d3cb91e6a8acb296d46f6d2ed7c46684a1d81cdb1db7261f132c67356b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.9 MB (219940555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be26c7750c65f4299ce4e22d90312e5f90ec3666ebb766e97fd6ab5515113ece`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 26 Jan 2024 23:45:05 GMT
ADD file:0808047bc74f297cb13abd2ad67e5778ee4abaa5d69f2c5b133d11c0ce0e51aa in / 
# Fri, 26 Jan 2024 23:45:05 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 02:53:30 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Sat, 16 Mar 2024 02:53:30 GMT
ENV ARANGO_VERSION=3.10.13
# Sat, 16 Mar 2024 02:53:54 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb310/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Sat, 16 Mar 2024 02:53:58 GMT
ENV GLIBCXX_FORCE_NEW=1
# Sat, 16 Mar 2024 02:53:58 GMT
RUN echo "UTC" > /etc/timezone
# Sat, 16 Mar 2024 02:53:58 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Sat, 16 Mar 2024 02:53:58 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Sat, 16 Mar 2024 02:53:58 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Sat, 16 Mar 2024 02:53:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 Mar 2024 02:53:58 GMT
EXPOSE 8529
# Sat, 16 Mar 2024 02:53:58 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:550f8bf8502cef18df2424ad36edbc4cc08c7ef11b44f493af59029aab98f61d`  
		Last Modified: Fri, 26 Jan 2024 23:45:48 GMT  
		Size: 2.7 MB (2708283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd0762bfc74eec695cafe3f95133defbb17b3a89a2a4fc37d6b8a16e9a99bdce`  
		Last Modified: Sat, 16 Mar 2024 02:54:59 GMT  
		Size: 217.2 MB (217229783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5431e92bf83c3e8580da45e08e6a2e74e15b73f7e6d55ecee1563019bbc2943`  
		Last Modified: Sat, 16 Mar 2024 02:54:43 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef3ffbbce3f8a84d1f6f17ffdaf07566590168fc5fcb0512f0f8823110e98f40`  
		Last Modified: Sat, 16 Mar 2024 02:54:43 GMT  
		Size: 2.1 KB (2087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b9d4faa3a9cb9feb928be4fd9a42ad00ee488fd8bba14a34b8dcd9b3c7501d7`  
		Last Modified: Sat, 16 Mar 2024 02:54:43 GMT  
		Size: 263.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:3.10.13`

```console
$ docker pull arangodb@sha256:579f234e5fb0a3df51119fa570ae91991f6a513cc05c09f93455de2191d49e9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `arangodb:3.10.13` - linux; amd64

```console
$ docker pull arangodb@sha256:26133c97b9a3fe81eea5b05b012c809264f627e2873a7018543d532b1463499c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.9 MB (224870161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a661ab513de166ccb4033fa2ff416d4c522e9d49d715e86a25f021308688ae2f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:09 GMT
ADD file:b308dfeecaa300a430b4e65e312a48eb5f191df7754e93ff4e7b2d04016b3ca7 in / 
# Sat, 27 Jan 2024 00:31:09 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 06:18:53 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Sat, 16 Mar 2024 06:18:53 GMT
ENV ARANGO_VERSION=3.10.13
# Sat, 16 Mar 2024 06:19:21 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb310/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Sat, 16 Mar 2024 06:19:23 GMT
ENV GLIBCXX_FORCE_NEW=1
# Sat, 16 Mar 2024 06:19:24 GMT
RUN echo "UTC" > /etc/timezone
# Sat, 16 Mar 2024 06:19:24 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Sat, 16 Mar 2024 06:19:24 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Sat, 16 Mar 2024 06:19:24 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Sat, 16 Mar 2024 06:19:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 Mar 2024 06:19:24 GMT
EXPOSE 8529
# Sat, 16 Mar 2024 06:19:24 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:a88dc8b54e91eb6b19695ef7e04865926d4df23004f414a3ee86978617492d4d`  
		Last Modified: Sat, 27 Jan 2024 00:31:53 GMT  
		Size: 2.8 MB (2807837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0944a22df89a680fc29c006f041a3a567cd44ec008f5d9cb9e3c0374e63e520`  
		Last Modified: Sat, 16 Mar 2024 06:20:30 GMT  
		Size: 222.1 MB (222059838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6df177555217d9063860aeb57c0238bb794ec1df9a41ecb1cf6fa8d1fd54aa38`  
		Last Modified: Sat, 16 Mar 2024 06:20:08 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b0348faaf3e382522076db041338ad1960ef8f6fdb0d1a642ce020887fa385a`  
		Last Modified: Sat, 16 Mar 2024 06:20:08 GMT  
		Size: 2.1 KB (2086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca535f443f46be87728bc03cebe2327f2b7bf192554d9cfd7b6c282985e71a1e`  
		Last Modified: Sat, 16 Mar 2024 06:20:08 GMT  
		Size: 261.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `arangodb:3.10.13` - linux; arm64 variant v8

```console
$ docker pull arangodb@sha256:634807d3cb91e6a8acb296d46f6d2ed7c46684a1d81cdb1db7261f132c67356b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.9 MB (219940555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be26c7750c65f4299ce4e22d90312e5f90ec3666ebb766e97fd6ab5515113ece`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 26 Jan 2024 23:45:05 GMT
ADD file:0808047bc74f297cb13abd2ad67e5778ee4abaa5d69f2c5b133d11c0ce0e51aa in / 
# Fri, 26 Jan 2024 23:45:05 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 02:53:30 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Sat, 16 Mar 2024 02:53:30 GMT
ENV ARANGO_VERSION=3.10.13
# Sat, 16 Mar 2024 02:53:54 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb310/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Sat, 16 Mar 2024 02:53:58 GMT
ENV GLIBCXX_FORCE_NEW=1
# Sat, 16 Mar 2024 02:53:58 GMT
RUN echo "UTC" > /etc/timezone
# Sat, 16 Mar 2024 02:53:58 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Sat, 16 Mar 2024 02:53:58 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Sat, 16 Mar 2024 02:53:58 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Sat, 16 Mar 2024 02:53:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 Mar 2024 02:53:58 GMT
EXPOSE 8529
# Sat, 16 Mar 2024 02:53:58 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:550f8bf8502cef18df2424ad36edbc4cc08c7ef11b44f493af59029aab98f61d`  
		Last Modified: Fri, 26 Jan 2024 23:45:48 GMT  
		Size: 2.7 MB (2708283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd0762bfc74eec695cafe3f95133defbb17b3a89a2a4fc37d6b8a16e9a99bdce`  
		Last Modified: Sat, 16 Mar 2024 02:54:59 GMT  
		Size: 217.2 MB (217229783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5431e92bf83c3e8580da45e08e6a2e74e15b73f7e6d55ecee1563019bbc2943`  
		Last Modified: Sat, 16 Mar 2024 02:54:43 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef3ffbbce3f8a84d1f6f17ffdaf07566590168fc5fcb0512f0f8823110e98f40`  
		Last Modified: Sat, 16 Mar 2024 02:54:43 GMT  
		Size: 2.1 KB (2087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b9d4faa3a9cb9feb928be4fd9a42ad00ee488fd8bba14a34b8dcd9b3c7501d7`  
		Last Modified: Sat, 16 Mar 2024 02:54:43 GMT  
		Size: 263.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:3.11`

```console
$ docker pull arangodb@sha256:1e75d74954a49f5c5d45913e81ad278585c7ffd9331bfbfd53c6e9a909d84a64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `arangodb:3.11` - linux; amd64

```console
$ docker pull arangodb@sha256:16893e767f47d28e3297839637741e5c4023e815adf860dfc674e1a36c7c7db0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.4 MB (249404256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2753be2cd85b4b119d5893fe40763b5db14fd62d65e7948ac3e982b415cbe22f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:09 GMT
ADD file:b308dfeecaa300a430b4e65e312a48eb5f191df7754e93ff4e7b2d04016b3ca7 in / 
# Sat, 27 Jan 2024 00:31:09 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 06:18:53 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Sat, 16 Mar 2024 06:19:28 GMT
ENV ARANGO_VERSION=3.11.8
# Sat, 16 Mar 2024 06:19:55 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb311/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Sat, 16 Mar 2024 06:19:57 GMT
ENV GLIBCXX_FORCE_NEW=1
# Sat, 16 Mar 2024 06:19:58 GMT
RUN echo "UTC" > /etc/timezone
# Sat, 16 Mar 2024 06:19:58 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Sat, 16 Mar 2024 06:19:58 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Sat, 16 Mar 2024 06:19:58 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Sat, 16 Mar 2024 06:19:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 Mar 2024 06:19:58 GMT
EXPOSE 8529
# Sat, 16 Mar 2024 06:19:58 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:a88dc8b54e91eb6b19695ef7e04865926d4df23004f414a3ee86978617492d4d`  
		Last Modified: Sat, 27 Jan 2024 00:31:53 GMT  
		Size: 2.8 MB (2807837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76f3f691dd025a65a1f705ffb6d571287717664383a6b9fea0fee6b74430d2a8`  
		Last Modified: Sat, 16 Mar 2024 06:21:00 GMT  
		Size: 246.6 MB (246593932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1be28253d1a0915171fc6f15ba590882a22b37bdef086d7931dd7586c2f1761b`  
		Last Modified: Sat, 16 Mar 2024 06:20:38 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80520ffcf501e8d24f340177e83997d625f414247df98144f076dc22b316c6e4`  
		Last Modified: Sat, 16 Mar 2024 06:20:38 GMT  
		Size: 2.1 KB (2087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a89e0cc1f692c2e4f754606d4a486e127f29d7eb7aa7540a9fdac0c878a257fa`  
		Last Modified: Sat, 16 Mar 2024 06:20:38 GMT  
		Size: 261.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `arangodb:3.11` - linux; arm64 variant v8

```console
$ docker pull arangodb@sha256:3f8be0114b280db211838c5c1eeb7bb3c271d1b8acbcd93e8ffe757ec8b0113d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.5 MB (243547838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d3dec3550f513a45281a571ecea1b3621ceb2a07e997e471d93c4b1abbbd7e7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 26 Jan 2024 23:45:05 GMT
ADD file:0808047bc74f297cb13abd2ad67e5778ee4abaa5d69f2c5b133d11c0ce0e51aa in / 
# Fri, 26 Jan 2024 23:45:05 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 02:53:30 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Sat, 16 Mar 2024 02:54:03 GMT
ENV ARANGO_VERSION=3.11.8
# Sat, 16 Mar 2024 02:54:28 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb311/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Sat, 16 Mar 2024 02:54:32 GMT
ENV GLIBCXX_FORCE_NEW=1
# Sat, 16 Mar 2024 02:54:33 GMT
RUN echo "UTC" > /etc/timezone
# Sat, 16 Mar 2024 02:54:33 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Sat, 16 Mar 2024 02:54:33 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Sat, 16 Mar 2024 02:54:33 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Sat, 16 Mar 2024 02:54:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 Mar 2024 02:54:33 GMT
EXPOSE 8529
# Sat, 16 Mar 2024 02:54:33 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:550f8bf8502cef18df2424ad36edbc4cc08c7ef11b44f493af59029aab98f61d`  
		Last Modified: Fri, 26 Jan 2024 23:45:48 GMT  
		Size: 2.7 MB (2708283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30ed7edc540d36b1d3c35c5f194f5198953fb9ac4f63649afdb98f68c0b3ba81`  
		Last Modified: Sat, 16 Mar 2024 02:55:25 GMT  
		Size: 240.8 MB (240837069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87b2d8588faf04eed3cd34d9a936697948a3f834b3a17cded688b5907562c5ec`  
		Last Modified: Sat, 16 Mar 2024 02:55:08 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:030474d2d49837281cdd335832ce82999f881dd31f3b71d14d49915b3ea19341`  
		Last Modified: Sat, 16 Mar 2024 02:55:08 GMT  
		Size: 2.1 KB (2086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99a7ff06092e552d9d88c89c167e27b859037542d556a711e62ae1e34c3852e1`  
		Last Modified: Sat, 16 Mar 2024 02:55:08 GMT  
		Size: 261.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:3.11.8`

```console
$ docker pull arangodb@sha256:1e75d74954a49f5c5d45913e81ad278585c7ffd9331bfbfd53c6e9a909d84a64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `arangodb:3.11.8` - linux; amd64

```console
$ docker pull arangodb@sha256:16893e767f47d28e3297839637741e5c4023e815adf860dfc674e1a36c7c7db0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.4 MB (249404256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2753be2cd85b4b119d5893fe40763b5db14fd62d65e7948ac3e982b415cbe22f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:09 GMT
ADD file:b308dfeecaa300a430b4e65e312a48eb5f191df7754e93ff4e7b2d04016b3ca7 in / 
# Sat, 27 Jan 2024 00:31:09 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 06:18:53 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Sat, 16 Mar 2024 06:19:28 GMT
ENV ARANGO_VERSION=3.11.8
# Sat, 16 Mar 2024 06:19:55 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb311/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Sat, 16 Mar 2024 06:19:57 GMT
ENV GLIBCXX_FORCE_NEW=1
# Sat, 16 Mar 2024 06:19:58 GMT
RUN echo "UTC" > /etc/timezone
# Sat, 16 Mar 2024 06:19:58 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Sat, 16 Mar 2024 06:19:58 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Sat, 16 Mar 2024 06:19:58 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Sat, 16 Mar 2024 06:19:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 Mar 2024 06:19:58 GMT
EXPOSE 8529
# Sat, 16 Mar 2024 06:19:58 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:a88dc8b54e91eb6b19695ef7e04865926d4df23004f414a3ee86978617492d4d`  
		Last Modified: Sat, 27 Jan 2024 00:31:53 GMT  
		Size: 2.8 MB (2807837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76f3f691dd025a65a1f705ffb6d571287717664383a6b9fea0fee6b74430d2a8`  
		Last Modified: Sat, 16 Mar 2024 06:21:00 GMT  
		Size: 246.6 MB (246593932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1be28253d1a0915171fc6f15ba590882a22b37bdef086d7931dd7586c2f1761b`  
		Last Modified: Sat, 16 Mar 2024 06:20:38 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80520ffcf501e8d24f340177e83997d625f414247df98144f076dc22b316c6e4`  
		Last Modified: Sat, 16 Mar 2024 06:20:38 GMT  
		Size: 2.1 KB (2087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a89e0cc1f692c2e4f754606d4a486e127f29d7eb7aa7540a9fdac0c878a257fa`  
		Last Modified: Sat, 16 Mar 2024 06:20:38 GMT  
		Size: 261.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `arangodb:3.11.8` - linux; arm64 variant v8

```console
$ docker pull arangodb@sha256:3f8be0114b280db211838c5c1eeb7bb3c271d1b8acbcd93e8ffe757ec8b0113d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.5 MB (243547838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d3dec3550f513a45281a571ecea1b3621ceb2a07e997e471d93c4b1abbbd7e7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 26 Jan 2024 23:45:05 GMT
ADD file:0808047bc74f297cb13abd2ad67e5778ee4abaa5d69f2c5b133d11c0ce0e51aa in / 
# Fri, 26 Jan 2024 23:45:05 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 02:53:30 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Sat, 16 Mar 2024 02:54:03 GMT
ENV ARANGO_VERSION=3.11.8
# Sat, 16 Mar 2024 02:54:28 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb311/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Sat, 16 Mar 2024 02:54:32 GMT
ENV GLIBCXX_FORCE_NEW=1
# Sat, 16 Mar 2024 02:54:33 GMT
RUN echo "UTC" > /etc/timezone
# Sat, 16 Mar 2024 02:54:33 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Sat, 16 Mar 2024 02:54:33 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Sat, 16 Mar 2024 02:54:33 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Sat, 16 Mar 2024 02:54:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 Mar 2024 02:54:33 GMT
EXPOSE 8529
# Sat, 16 Mar 2024 02:54:33 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:550f8bf8502cef18df2424ad36edbc4cc08c7ef11b44f493af59029aab98f61d`  
		Last Modified: Fri, 26 Jan 2024 23:45:48 GMT  
		Size: 2.7 MB (2708283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30ed7edc540d36b1d3c35c5f194f5198953fb9ac4f63649afdb98f68c0b3ba81`  
		Last Modified: Sat, 16 Mar 2024 02:55:25 GMT  
		Size: 240.8 MB (240837069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87b2d8588faf04eed3cd34d9a936697948a3f834b3a17cded688b5907562c5ec`  
		Last Modified: Sat, 16 Mar 2024 02:55:08 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:030474d2d49837281cdd335832ce82999f881dd31f3b71d14d49915b3ea19341`  
		Last Modified: Sat, 16 Mar 2024 02:55:08 GMT  
		Size: 2.1 KB (2086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99a7ff06092e552d9d88c89c167e27b859037542d556a711e62ae1e34c3852e1`  
		Last Modified: Sat, 16 Mar 2024 02:55:08 GMT  
		Size: 261.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:3.12`

```console
$ docker pull arangodb@sha256:d7b59ffd036db30e8813be71a4d0e0d930af1ab59480cb8f7666fc9e56d5bf05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `arangodb:3.12` - linux; amd64

```console
$ docker pull arangodb@sha256:7f1fbd60dbf77a4085cfba8c202ea83b523e474c8c22fe6f8f5c76ad3d684ea5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.2 MB (208229724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b60587c2ed005597247dfe74d015d162580bfcdd49cec5824117e8b740543573`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:02 GMT
ADD file:c44c9bd36ba35cc78fb9396304ea008def9f42a3beef76aa33b2cf1fde1c10b3 in / 
# Sat, 27 Jan 2024 00:31:02 GMT
CMD ["/bin/sh"]
# Mon, 25 Mar 2024 19:51:03 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Mon, 25 Mar 2024 19:51:04 GMT
ENV ARANGO_VERSION=3.12.0
# Mon, 25 Mar 2024 19:51:21 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8003EDF6F05459984878D4A6C04AD0FD86FEC04D &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb312/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Mon, 25 Mar 2024 19:51:22 GMT
ENV GLIBCXX_FORCE_NEW=1
# Mon, 25 Mar 2024 19:51:22 GMT
RUN echo "UTC" > /etc/timezone
# Mon, 25 Mar 2024 19:51:22 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Mon, 25 Mar 2024 19:51:22 GMT
COPY file:513375723ea161120e77fe867a15962ee909f21d5ad9010e94f567e75f817d04 in /entrypoint.sh 
# Mon, 25 Mar 2024 19:51:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 25 Mar 2024 19:51:23 GMT
EXPOSE 8529
# Mon, 25 Mar 2024 19:51:23 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:3c854c8cbf469fda815b8f6183300c07cfa2fbb5703859ca79aff93ae934961b`  
		Last Modified: Sat, 27 Jan 2024 00:31:44 GMT  
		Size: 3.4 MB (3379404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ecdd28207d9bd85310dbf913e40d273fb64797a3f1333cdd213571aeff650f8`  
		Last Modified: Mon, 25 Mar 2024 19:51:55 GMT  
		Size: 204.8 MB (204848166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1841e2292362b1cf6a93ff6be80899cd59863261282ee8867197f46705a60f6`  
		Last Modified: Mon, 25 Mar 2024 19:51:37 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0ae8881e8aa2f1c444ade1abd168e516802ca7ffdab5ddf0e2007d384555cdd`  
		Last Modified: Mon, 25 Mar 2024 19:51:37 GMT  
		Size: 2.0 KB (2015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `arangodb:3.12` - linux; arm64 variant v8

```console
$ docker pull arangodb@sha256:209ddde51cbb4ccf144c4fd53ebb8fd449e2713e67c317f76cf7de8d6033a418
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.0 MB (210020640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3eb15430a24d9e671b819d9c79586ad8827f98e4e041269faaa21c7c05b6308`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 26 Jan 2024 23:45:00 GMT
ADD file:c3b6b575eb741f914ec12bd4df43de0cb044a1f2bae7ff15d176e49b5986d903 in / 
# Fri, 26 Jan 2024 23:45:00 GMT
CMD ["/bin/sh"]
# Mon, 25 Mar 2024 20:07:26 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Mon, 25 Mar 2024 20:07:26 GMT
ENV ARANGO_VERSION=3.12.0
# Mon, 25 Mar 2024 20:07:46 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8003EDF6F05459984878D4A6C04AD0FD86FEC04D &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb312/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Mon, 25 Mar 2024 20:07:48 GMT
ENV GLIBCXX_FORCE_NEW=1
# Mon, 25 Mar 2024 20:07:49 GMT
RUN echo "UTC" > /etc/timezone
# Mon, 25 Mar 2024 20:07:49 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Mon, 25 Mar 2024 20:07:49 GMT
COPY file:513375723ea161120e77fe867a15962ee909f21d5ad9010e94f567e75f817d04 in /entrypoint.sh 
# Mon, 25 Mar 2024 20:07:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 25 Mar 2024 20:07:49 GMT
EXPOSE 8529
# Mon, 25 Mar 2024 20:07:49 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:5385a9a590c3e2872b3ed27554a56fb7ce544c694b41b9b95d70fa86f30b0566`  
		Last Modified: Fri, 26 Jan 2024 23:45:40 GMT  
		Size: 3.3 MB (3258283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11fb6132dc2c94d5d221a090bee94fd9e2c67ad29d3253112aa3189d14c0e7ff`  
		Last Modified: Mon, 25 Mar 2024 20:08:19 GMT  
		Size: 206.8 MB (206760203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7205ef234cbfa94927d997e215cf7f9eb1f7df6965cad485533e224133421650`  
		Last Modified: Mon, 25 Mar 2024 20:08:05 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8db282981a6d0c329fe786daca4f84bfd2455c13d5887453ed53e0de0e5a598d`  
		Last Modified: Mon, 25 Mar 2024 20:08:05 GMT  
		Size: 2.0 KB (2015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:3.12.0`

```console
$ docker pull arangodb@sha256:d7b59ffd036db30e8813be71a4d0e0d930af1ab59480cb8f7666fc9e56d5bf05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `arangodb:3.12.0` - linux; amd64

```console
$ docker pull arangodb@sha256:7f1fbd60dbf77a4085cfba8c202ea83b523e474c8c22fe6f8f5c76ad3d684ea5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.2 MB (208229724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b60587c2ed005597247dfe74d015d162580bfcdd49cec5824117e8b740543573`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:02 GMT
ADD file:c44c9bd36ba35cc78fb9396304ea008def9f42a3beef76aa33b2cf1fde1c10b3 in / 
# Sat, 27 Jan 2024 00:31:02 GMT
CMD ["/bin/sh"]
# Mon, 25 Mar 2024 19:51:03 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Mon, 25 Mar 2024 19:51:04 GMT
ENV ARANGO_VERSION=3.12.0
# Mon, 25 Mar 2024 19:51:21 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8003EDF6F05459984878D4A6C04AD0FD86FEC04D &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb312/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Mon, 25 Mar 2024 19:51:22 GMT
ENV GLIBCXX_FORCE_NEW=1
# Mon, 25 Mar 2024 19:51:22 GMT
RUN echo "UTC" > /etc/timezone
# Mon, 25 Mar 2024 19:51:22 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Mon, 25 Mar 2024 19:51:22 GMT
COPY file:513375723ea161120e77fe867a15962ee909f21d5ad9010e94f567e75f817d04 in /entrypoint.sh 
# Mon, 25 Mar 2024 19:51:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 25 Mar 2024 19:51:23 GMT
EXPOSE 8529
# Mon, 25 Mar 2024 19:51:23 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:3c854c8cbf469fda815b8f6183300c07cfa2fbb5703859ca79aff93ae934961b`  
		Last Modified: Sat, 27 Jan 2024 00:31:44 GMT  
		Size: 3.4 MB (3379404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ecdd28207d9bd85310dbf913e40d273fb64797a3f1333cdd213571aeff650f8`  
		Last Modified: Mon, 25 Mar 2024 19:51:55 GMT  
		Size: 204.8 MB (204848166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1841e2292362b1cf6a93ff6be80899cd59863261282ee8867197f46705a60f6`  
		Last Modified: Mon, 25 Mar 2024 19:51:37 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0ae8881e8aa2f1c444ade1abd168e516802ca7ffdab5ddf0e2007d384555cdd`  
		Last Modified: Mon, 25 Mar 2024 19:51:37 GMT  
		Size: 2.0 KB (2015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `arangodb:3.12.0` - linux; arm64 variant v8

```console
$ docker pull arangodb@sha256:209ddde51cbb4ccf144c4fd53ebb8fd449e2713e67c317f76cf7de8d6033a418
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.0 MB (210020640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3eb15430a24d9e671b819d9c79586ad8827f98e4e041269faaa21c7c05b6308`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 26 Jan 2024 23:45:00 GMT
ADD file:c3b6b575eb741f914ec12bd4df43de0cb044a1f2bae7ff15d176e49b5986d903 in / 
# Fri, 26 Jan 2024 23:45:00 GMT
CMD ["/bin/sh"]
# Mon, 25 Mar 2024 20:07:26 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Mon, 25 Mar 2024 20:07:26 GMT
ENV ARANGO_VERSION=3.12.0
# Mon, 25 Mar 2024 20:07:46 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8003EDF6F05459984878D4A6C04AD0FD86FEC04D &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb312/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Mon, 25 Mar 2024 20:07:48 GMT
ENV GLIBCXX_FORCE_NEW=1
# Mon, 25 Mar 2024 20:07:49 GMT
RUN echo "UTC" > /etc/timezone
# Mon, 25 Mar 2024 20:07:49 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Mon, 25 Mar 2024 20:07:49 GMT
COPY file:513375723ea161120e77fe867a15962ee909f21d5ad9010e94f567e75f817d04 in /entrypoint.sh 
# Mon, 25 Mar 2024 20:07:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 25 Mar 2024 20:07:49 GMT
EXPOSE 8529
# Mon, 25 Mar 2024 20:07:49 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:5385a9a590c3e2872b3ed27554a56fb7ce544c694b41b9b95d70fa86f30b0566`  
		Last Modified: Fri, 26 Jan 2024 23:45:40 GMT  
		Size: 3.3 MB (3258283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11fb6132dc2c94d5d221a090bee94fd9e2c67ad29d3253112aa3189d14c0e7ff`  
		Last Modified: Mon, 25 Mar 2024 20:08:19 GMT  
		Size: 206.8 MB (206760203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7205ef234cbfa94927d997e215cf7f9eb1f7df6965cad485533e224133421650`  
		Last Modified: Mon, 25 Mar 2024 20:08:05 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8db282981a6d0c329fe786daca4f84bfd2455c13d5887453ed53e0de0e5a598d`  
		Last Modified: Mon, 25 Mar 2024 20:08:05 GMT  
		Size: 2.0 KB (2015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:latest`

```console
$ docker pull arangodb@sha256:d7b59ffd036db30e8813be71a4d0e0d930af1ab59480cb8f7666fc9e56d5bf05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `arangodb:latest` - linux; amd64

```console
$ docker pull arangodb@sha256:7f1fbd60dbf77a4085cfba8c202ea83b523e474c8c22fe6f8f5c76ad3d684ea5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.2 MB (208229724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b60587c2ed005597247dfe74d015d162580bfcdd49cec5824117e8b740543573`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:02 GMT
ADD file:c44c9bd36ba35cc78fb9396304ea008def9f42a3beef76aa33b2cf1fde1c10b3 in / 
# Sat, 27 Jan 2024 00:31:02 GMT
CMD ["/bin/sh"]
# Mon, 25 Mar 2024 19:51:03 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Mon, 25 Mar 2024 19:51:04 GMT
ENV ARANGO_VERSION=3.12.0
# Mon, 25 Mar 2024 19:51:21 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8003EDF6F05459984878D4A6C04AD0FD86FEC04D &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb312/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Mon, 25 Mar 2024 19:51:22 GMT
ENV GLIBCXX_FORCE_NEW=1
# Mon, 25 Mar 2024 19:51:22 GMT
RUN echo "UTC" > /etc/timezone
# Mon, 25 Mar 2024 19:51:22 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Mon, 25 Mar 2024 19:51:22 GMT
COPY file:513375723ea161120e77fe867a15962ee909f21d5ad9010e94f567e75f817d04 in /entrypoint.sh 
# Mon, 25 Mar 2024 19:51:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 25 Mar 2024 19:51:23 GMT
EXPOSE 8529
# Mon, 25 Mar 2024 19:51:23 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:3c854c8cbf469fda815b8f6183300c07cfa2fbb5703859ca79aff93ae934961b`  
		Last Modified: Sat, 27 Jan 2024 00:31:44 GMT  
		Size: 3.4 MB (3379404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ecdd28207d9bd85310dbf913e40d273fb64797a3f1333cdd213571aeff650f8`  
		Last Modified: Mon, 25 Mar 2024 19:51:55 GMT  
		Size: 204.8 MB (204848166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1841e2292362b1cf6a93ff6be80899cd59863261282ee8867197f46705a60f6`  
		Last Modified: Mon, 25 Mar 2024 19:51:37 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0ae8881e8aa2f1c444ade1abd168e516802ca7ffdab5ddf0e2007d384555cdd`  
		Last Modified: Mon, 25 Mar 2024 19:51:37 GMT  
		Size: 2.0 KB (2015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `arangodb:latest` - linux; arm64 variant v8

```console
$ docker pull arangodb@sha256:209ddde51cbb4ccf144c4fd53ebb8fd449e2713e67c317f76cf7de8d6033a418
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.0 MB (210020640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3eb15430a24d9e671b819d9c79586ad8827f98e4e041269faaa21c7c05b6308`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 26 Jan 2024 23:45:00 GMT
ADD file:c3b6b575eb741f914ec12bd4df43de0cb044a1f2bae7ff15d176e49b5986d903 in / 
# Fri, 26 Jan 2024 23:45:00 GMT
CMD ["/bin/sh"]
# Mon, 25 Mar 2024 20:07:26 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Mon, 25 Mar 2024 20:07:26 GMT
ENV ARANGO_VERSION=3.12.0
# Mon, 25 Mar 2024 20:07:46 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8003EDF6F05459984878D4A6C04AD0FD86FEC04D &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb312/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Mon, 25 Mar 2024 20:07:48 GMT
ENV GLIBCXX_FORCE_NEW=1
# Mon, 25 Mar 2024 20:07:49 GMT
RUN echo "UTC" > /etc/timezone
# Mon, 25 Mar 2024 20:07:49 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Mon, 25 Mar 2024 20:07:49 GMT
COPY file:513375723ea161120e77fe867a15962ee909f21d5ad9010e94f567e75f817d04 in /entrypoint.sh 
# Mon, 25 Mar 2024 20:07:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 25 Mar 2024 20:07:49 GMT
EXPOSE 8529
# Mon, 25 Mar 2024 20:07:49 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:5385a9a590c3e2872b3ed27554a56fb7ce544c694b41b9b95d70fa86f30b0566`  
		Last Modified: Fri, 26 Jan 2024 23:45:40 GMT  
		Size: 3.3 MB (3258283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11fb6132dc2c94d5d221a090bee94fd9e2c67ad29d3253112aa3189d14c0e7ff`  
		Last Modified: Mon, 25 Mar 2024 20:08:19 GMT  
		Size: 206.8 MB (206760203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7205ef234cbfa94927d997e215cf7f9eb1f7df6965cad485533e224133421650`  
		Last Modified: Mon, 25 Mar 2024 20:08:05 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8db282981a6d0c329fe786daca4f84bfd2455c13d5887453ed53e0de0e5a598d`  
		Last Modified: Mon, 25 Mar 2024 20:08:05 GMT  
		Size: 2.0 KB (2015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
