<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `arangodb`

-	[`arangodb:3.11`](#arangodb311)
-	[`arangodb:3.11.14`](#arangodb31114)
-	[`arangodb:3.12`](#arangodb312)
-	[`arangodb:3.12.4.3`](#arangodb31243)
-	[`arangodb:latest`](#arangodblatest)

## `arangodb:3.11`

```console
$ docker pull arangodb@sha256:e83f37055170f647ebca1a09dd65ec850a578d8d4c9b90904de3359b909c1f16
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `arangodb:3.11` - linux; amd64

```console
$ docker pull arangodb@sha256:91a3454d21c004b1ccb3e5e428bdef7896249293858f9a3890c31036ef724f86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.0 MB (210038877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9889c421dae201ff9ec358c7055ed0ebe726ee821dfe29c28f3a8334d9d24279`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 23 May 2025 23:32:58 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Fri, 23 May 2025 23:32:58 GMT
ENV ARANGO_VERSION=3.11.14
# Fri, 23 May 2025 23:32:58 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8003EDF6F05459984878D4A6C04AD0FD86FEC04D &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb311/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg # buildkit
# Fri, 23 May 2025 23:32:58 GMT
ENV GLIBCXX_FORCE_NEW=1
# Fri, 23 May 2025 23:32:58 GMT
RUN echo "UTC" > /etc/timezone # buildkit
# Fri, 23 May 2025 23:32:58 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Fri, 23 May 2025 23:32:58 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 23 May 2025 23:32:58 GMT
COPY docker-foxx.sh /usr/bin/foxx # buildkit
# Fri, 23 May 2025 23:32:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 23 May 2025 23:32:58 GMT
EXPOSE map[8529/tcp:{}]
# Fri, 23 May 2025 23:32:58 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12c12dc522d82c716439154fbcdfd917aa37a951c27d12f150f733e459716941`  
		Last Modified: Tue, 03 Jun 2025 13:37:16 GMT  
		Size: 206.4 MB (206394147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ed0f6f271c5efd3cb21de74d90c91a88ec6e3f46726c2d7e4ebcceda9c597c9`  
		Last Modified: Tue, 03 Jun 2025 13:37:05 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdeca579227557695516270be3abbfd5eb543e2b85ff7696d06c79c6aa1e5e04`  
		Last Modified: Tue, 03 Jun 2025 13:37:04 GMT  
		Size: 2.1 KB (2086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c3f1d9a6bad9abb28c27c1ddf9a1a4a1538d91aff61ee58129467689790e22b`  
		Last Modified: Tue, 03 Jun 2025 13:37:05 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:3.11` - unknown; unknown

```console
$ docker pull arangodb@sha256:820fd3b07584ff77373a57d1a62e2c9fd1cf7f557ad7cb7fa2b5e26f08dabd81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1144725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bbcc7975e4fccb261a3978f747777d30bec41da33d7fc885c0a292a5e601c21`

```dockerfile
```

-	Layers:
	-	`sha256:e7f9b06c2de2ad1eed23b3f77856d20f5189eb1b9ac82673356a04fa9e3687ed`  
		Last Modified: Wed, 04 Jun 2025 03:12:26 GMT  
		Size: 1.1 MB (1128905 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f8688cc009cc0a210e3a05c1a694af26dc93eb0a14bfd788f2da2c2162a7c71`  
		Last Modified: Wed, 04 Jun 2025 03:12:27 GMT  
		Size: 15.8 KB (15820 bytes)  
		MIME: application/vnd.in-toto+json

### `arangodb:3.11` - linux; arm64 variant v8

```console
$ docker pull arangodb@sha256:895217b44eee0b20ca235374917458359547f969e2dbab634765f8633c5e32e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.1 MB (213115360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f04c0a5dc47a92e8b496ebba676c01caa23231b19de8b2b1d4270e510b398997`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 23 May 2025 23:32:58 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Fri, 23 May 2025 23:32:58 GMT
ENV ARANGO_VERSION=3.11.14
# Fri, 23 May 2025 23:32:58 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8003EDF6F05459984878D4A6C04AD0FD86FEC04D &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb311/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg # buildkit
# Fri, 23 May 2025 23:32:58 GMT
ENV GLIBCXX_FORCE_NEW=1
# Fri, 23 May 2025 23:32:58 GMT
RUN echo "UTC" > /etc/timezone # buildkit
# Fri, 23 May 2025 23:32:58 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Fri, 23 May 2025 23:32:58 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 23 May 2025 23:32:58 GMT
COPY docker-foxx.sh /usr/bin/foxx # buildkit
# Fri, 23 May 2025 23:32:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 23 May 2025 23:32:58 GMT
EXPOSE map[8529/tcp:{}]
# Fri, 23 May 2025 23:32:58 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:462f9616f39f2e2483cce2f1d1a65193e57af7dba0b30ba6f067d88ec231f4e7`  
		Last Modified: Tue, 03 Jun 2025 13:40:32 GMT  
		Size: 209.1 MB (209119846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a20141cd646b913d3e08495f0fae723edeab5103904af9e09284eb72e53e570a`  
		Last Modified: Tue, 03 Jun 2025 13:40:05 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d44870ed5b238027ef468c3debc8ef3886d5decc8a7cee4dc358451140d823d`  
		Last Modified: Tue, 03 Jun 2025 13:40:05 GMT  
		Size: 2.1 KB (2087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:901ec1d19a6cf6059ed3093ad26727b1662fe54525245a80aa180edec1e87aba`  
		Last Modified: Tue, 03 Jun 2025 13:40:07 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:3.11` - unknown; unknown

```console
$ docker pull arangodb@sha256:6edbef5f29144d446fd93ade4dd0d416332ec7dca43be8b42f944fe793be92b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1295428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8697e1dd269b53115f5121a4d75104a5c64c1c10e140a5a0246f3adbfa0c92b7`

```dockerfile
```

-	Layers:
	-	`sha256:c17cf9b1d365875aaaf55cdeede9a246a007cd51b1e8d5cb13753848539d2297`  
		Last Modified: Fri, 23 May 2025 23:47:59 GMT  
		Size: 1.3 MB (1279513 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb144ab1ee1d0646d3709e92e8d416fd1303171dd1fccaf81967490da20b4240`  
		Last Modified: Fri, 23 May 2025 23:47:59 GMT  
		Size: 15.9 KB (15915 bytes)  
		MIME: application/vnd.in-toto+json

## `arangodb:3.11.14`

```console
$ docker pull arangodb@sha256:e83f37055170f647ebca1a09dd65ec850a578d8d4c9b90904de3359b909c1f16
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `arangodb:3.11.14` - linux; amd64

```console
$ docker pull arangodb@sha256:91a3454d21c004b1ccb3e5e428bdef7896249293858f9a3890c31036ef724f86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.0 MB (210038877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9889c421dae201ff9ec358c7055ed0ebe726ee821dfe29c28f3a8334d9d24279`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 23 May 2025 23:32:58 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Fri, 23 May 2025 23:32:58 GMT
ENV ARANGO_VERSION=3.11.14
# Fri, 23 May 2025 23:32:58 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8003EDF6F05459984878D4A6C04AD0FD86FEC04D &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb311/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg # buildkit
# Fri, 23 May 2025 23:32:58 GMT
ENV GLIBCXX_FORCE_NEW=1
# Fri, 23 May 2025 23:32:58 GMT
RUN echo "UTC" > /etc/timezone # buildkit
# Fri, 23 May 2025 23:32:58 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Fri, 23 May 2025 23:32:58 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 23 May 2025 23:32:58 GMT
COPY docker-foxx.sh /usr/bin/foxx # buildkit
# Fri, 23 May 2025 23:32:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 23 May 2025 23:32:58 GMT
EXPOSE map[8529/tcp:{}]
# Fri, 23 May 2025 23:32:58 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12c12dc522d82c716439154fbcdfd917aa37a951c27d12f150f733e459716941`  
		Last Modified: Tue, 03 Jun 2025 13:37:16 GMT  
		Size: 206.4 MB (206394147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ed0f6f271c5efd3cb21de74d90c91a88ec6e3f46726c2d7e4ebcceda9c597c9`  
		Last Modified: Tue, 03 Jun 2025 13:37:05 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdeca579227557695516270be3abbfd5eb543e2b85ff7696d06c79c6aa1e5e04`  
		Last Modified: Tue, 03 Jun 2025 13:37:04 GMT  
		Size: 2.1 KB (2086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c3f1d9a6bad9abb28c27c1ddf9a1a4a1538d91aff61ee58129467689790e22b`  
		Last Modified: Tue, 03 Jun 2025 13:37:05 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:3.11.14` - unknown; unknown

```console
$ docker pull arangodb@sha256:820fd3b07584ff77373a57d1a62e2c9fd1cf7f557ad7cb7fa2b5e26f08dabd81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1144725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bbcc7975e4fccb261a3978f747777d30bec41da33d7fc885c0a292a5e601c21`

```dockerfile
```

-	Layers:
	-	`sha256:e7f9b06c2de2ad1eed23b3f77856d20f5189eb1b9ac82673356a04fa9e3687ed`  
		Last Modified: Wed, 04 Jun 2025 03:12:26 GMT  
		Size: 1.1 MB (1128905 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f8688cc009cc0a210e3a05c1a694af26dc93eb0a14bfd788f2da2c2162a7c71`  
		Last Modified: Wed, 04 Jun 2025 03:12:27 GMT  
		Size: 15.8 KB (15820 bytes)  
		MIME: application/vnd.in-toto+json

### `arangodb:3.11.14` - linux; arm64 variant v8

```console
$ docker pull arangodb@sha256:895217b44eee0b20ca235374917458359547f969e2dbab634765f8633c5e32e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.1 MB (213115360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f04c0a5dc47a92e8b496ebba676c01caa23231b19de8b2b1d4270e510b398997`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 23 May 2025 23:32:58 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Fri, 23 May 2025 23:32:58 GMT
ENV ARANGO_VERSION=3.11.14
# Fri, 23 May 2025 23:32:58 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8003EDF6F05459984878D4A6C04AD0FD86FEC04D &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb311/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg # buildkit
# Fri, 23 May 2025 23:32:58 GMT
ENV GLIBCXX_FORCE_NEW=1
# Fri, 23 May 2025 23:32:58 GMT
RUN echo "UTC" > /etc/timezone # buildkit
# Fri, 23 May 2025 23:32:58 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Fri, 23 May 2025 23:32:58 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 23 May 2025 23:32:58 GMT
COPY docker-foxx.sh /usr/bin/foxx # buildkit
# Fri, 23 May 2025 23:32:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 23 May 2025 23:32:58 GMT
EXPOSE map[8529/tcp:{}]
# Fri, 23 May 2025 23:32:58 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:462f9616f39f2e2483cce2f1d1a65193e57af7dba0b30ba6f067d88ec231f4e7`  
		Last Modified: Tue, 03 Jun 2025 13:40:32 GMT  
		Size: 209.1 MB (209119846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a20141cd646b913d3e08495f0fae723edeab5103904af9e09284eb72e53e570a`  
		Last Modified: Tue, 03 Jun 2025 13:40:05 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d44870ed5b238027ef468c3debc8ef3886d5decc8a7cee4dc358451140d823d`  
		Last Modified: Tue, 03 Jun 2025 13:40:05 GMT  
		Size: 2.1 KB (2087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:901ec1d19a6cf6059ed3093ad26727b1662fe54525245a80aa180edec1e87aba`  
		Last Modified: Tue, 03 Jun 2025 13:40:07 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:3.11.14` - unknown; unknown

```console
$ docker pull arangodb@sha256:6edbef5f29144d446fd93ade4dd0d416332ec7dca43be8b42f944fe793be92b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1295428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8697e1dd269b53115f5121a4d75104a5c64c1c10e140a5a0246f3adbfa0c92b7`

```dockerfile
```

-	Layers:
	-	`sha256:c17cf9b1d365875aaaf55cdeede9a246a007cd51b1e8d5cb13753848539d2297`  
		Last Modified: Fri, 23 May 2025 23:47:59 GMT  
		Size: 1.3 MB (1279513 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb144ab1ee1d0646d3709e92e8d416fd1303171dd1fccaf81967490da20b4240`  
		Last Modified: Fri, 23 May 2025 23:47:59 GMT  
		Size: 15.9 KB (15915 bytes)  
		MIME: application/vnd.in-toto+json

## `arangodb:3.12`

```console
$ docker pull arangodb@sha256:527c66aa819d8530150981b0968357901b2f335062c132b6b8b667f59def8ec2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `arangodb:3.12` - linux; amd64

```console
$ docker pull arangodb@sha256:ac38852c8c0f873f56b1a72b55b9afd7900d6c2430b2324ef3a67c2d596952e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.8 MB (226818330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d23b75a8acc07edd34a980000d0b2cc4841a4f8def89b09fce982234eb7d47bf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 02 May 2025 14:22:22 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Fri, 02 May 2025 14:22:22 GMT
ENV ARANGO_VERSION=3.12.4.3
# Fri, 02 May 2025 14:22:22 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8003EDF6F05459984878D4A6C04AD0FD86FEC04D &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb312/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg # buildkit
# Fri, 02 May 2025 14:22:22 GMT
ENV GLIBCXX_FORCE_NEW=1
# Fri, 02 May 2025 14:22:22 GMT
RUN echo "UTC" > /etc/timezone # buildkit
# Fri, 02 May 2025 14:22:22 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Fri, 02 May 2025 14:22:22 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 02 May 2025 14:22:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 02 May 2025 14:22:22 GMT
EXPOSE map[8529/tcp:{}]
# Fri, 02 May 2025 14:22:22 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c6b126090c0b0953702d824929e7e26c07b8f4b5ff6727aaff17400652177b1`  
		Last Modified: Thu, 08 May 2025 17:09:31 GMT  
		Size: 223.2 MB (223173928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca0876fbb1b434c6fe684e458e9e1f92daead9031379b8fdc61422e61c13a4fb`  
		Last Modified: Thu, 08 May 2025 17:05:04 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3edfcb6266cca46852db3e1ca102b4a71d381a7e924422f1b0b623b666f93e6`  
		Last Modified: Thu, 08 May 2025 17:05:04 GMT  
		Size: 2.0 KB (2015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:3.12` - unknown; unknown

```console
$ docker pull arangodb@sha256:936891622600e5199094bc79c5f1ad231208b088841e2de2077f4910a3df7bd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **404.7 KB (404670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa731d19cf7cfa7ae28b2222a7c163e68b6c38b2ed8e6fd4e7e27ec1051a7b48`

```dockerfile
```

-	Layers:
	-	`sha256:c4118246a94c9fd5ff666932bbd101df5e0e4c73e6faa04aff0aac35ce8a116b`  
		Last Modified: Sun, 18 May 2025 11:44:32 GMT  
		Size: 390.3 KB (390267 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1854e9d2b1ed12662ae0b0995d604a37ea80e9dddcede2888282c5c02d2a04a`  
		Last Modified: Sun, 18 May 2025 11:44:32 GMT  
		Size: 14.4 KB (14403 bytes)  
		MIME: application/vnd.in-toto+json

### `arangodb:3.12` - linux; arm64 variant v8

```console
$ docker pull arangodb@sha256:73f7152888962b4836ea41a76815b51238be827dd0f3e9c9f04a104e776af57d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.3 MB (227308594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8a3619bf7969550dc08a0002a610eab9ccb00fb98bbcb16e2be7e9a7ad7486a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 02 May 2025 14:22:22 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Fri, 02 May 2025 14:22:22 GMT
ENV ARANGO_VERSION=3.12.4.3
# Fri, 02 May 2025 14:22:22 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8003EDF6F05459984878D4A6C04AD0FD86FEC04D &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb312/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg # buildkit
# Fri, 02 May 2025 14:22:22 GMT
ENV GLIBCXX_FORCE_NEW=1
# Fri, 02 May 2025 14:22:22 GMT
RUN echo "UTC" > /etc/timezone # buildkit
# Fri, 02 May 2025 14:22:22 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Fri, 02 May 2025 14:22:22 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 02 May 2025 14:22:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 02 May 2025 14:22:22 GMT
EXPOSE map[8529/tcp:{}]
# Fri, 02 May 2025 14:22:22 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1fa68dc9d5277e7329bed3f9e2c9f668ff281391725983e1f7f781324f2d24b`  
		Last Modified: Thu, 08 May 2025 17:50:07 GMT  
		Size: 223.3 MB (223313410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5920b3e505934712fb5114a974798ba2511ded809e337630cc053e7b1132027e`  
		Last Modified: Thu, 08 May 2025 17:46:11 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5830d7fba7025455ac732f90886a5a612fda1c8f2060505e1591a15db9b38311`  
		Last Modified: Thu, 08 May 2025 17:46:12 GMT  
		Size: 2.0 KB (2015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:3.12` - unknown; unknown

```console
$ docker pull arangodb@sha256:c141a9c936ad3ed3bd0eabc2b86e748189cfdff5bec5d35dee0b167242362820
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **555.4 KB (555397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e3612520f827a2b929ac02c0cb161607e0c2c7ce86610ea6ae8e77dc8671cc5`

```dockerfile
```

-	Layers:
	-	`sha256:4de02ac9a05bc09355efaf201c6c0197842d285cee910dd6d99edc5f0c61fa3f`  
		Last Modified: Sun, 18 May 2025 11:44:35 GMT  
		Size: 540.9 KB (540887 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98265fa0c5715d537b36217ed315b6b68ac3753a89a117a82b16593c5a6edd3b`  
		Last Modified: Sun, 18 May 2025 11:44:35 GMT  
		Size: 14.5 KB (14510 bytes)  
		MIME: application/vnd.in-toto+json

## `arangodb:3.12.4.3`

```console
$ docker pull arangodb@sha256:527c66aa819d8530150981b0968357901b2f335062c132b6b8b667f59def8ec2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `arangodb:3.12.4.3` - linux; amd64

```console
$ docker pull arangodb@sha256:ac38852c8c0f873f56b1a72b55b9afd7900d6c2430b2324ef3a67c2d596952e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.8 MB (226818330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d23b75a8acc07edd34a980000d0b2cc4841a4f8def89b09fce982234eb7d47bf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 02 May 2025 14:22:22 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Fri, 02 May 2025 14:22:22 GMT
ENV ARANGO_VERSION=3.12.4.3
# Fri, 02 May 2025 14:22:22 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8003EDF6F05459984878D4A6C04AD0FD86FEC04D &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb312/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg # buildkit
# Fri, 02 May 2025 14:22:22 GMT
ENV GLIBCXX_FORCE_NEW=1
# Fri, 02 May 2025 14:22:22 GMT
RUN echo "UTC" > /etc/timezone # buildkit
# Fri, 02 May 2025 14:22:22 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Fri, 02 May 2025 14:22:22 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 02 May 2025 14:22:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 02 May 2025 14:22:22 GMT
EXPOSE map[8529/tcp:{}]
# Fri, 02 May 2025 14:22:22 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c6b126090c0b0953702d824929e7e26c07b8f4b5ff6727aaff17400652177b1`  
		Last Modified: Thu, 08 May 2025 17:09:31 GMT  
		Size: 223.2 MB (223173928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca0876fbb1b434c6fe684e458e9e1f92daead9031379b8fdc61422e61c13a4fb`  
		Last Modified: Thu, 08 May 2025 17:05:04 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3edfcb6266cca46852db3e1ca102b4a71d381a7e924422f1b0b623b666f93e6`  
		Last Modified: Thu, 08 May 2025 17:05:04 GMT  
		Size: 2.0 KB (2015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:3.12.4.3` - unknown; unknown

```console
$ docker pull arangodb@sha256:936891622600e5199094bc79c5f1ad231208b088841e2de2077f4910a3df7bd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **404.7 KB (404670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa731d19cf7cfa7ae28b2222a7c163e68b6c38b2ed8e6fd4e7e27ec1051a7b48`

```dockerfile
```

-	Layers:
	-	`sha256:c4118246a94c9fd5ff666932bbd101df5e0e4c73e6faa04aff0aac35ce8a116b`  
		Last Modified: Sun, 18 May 2025 11:44:32 GMT  
		Size: 390.3 KB (390267 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1854e9d2b1ed12662ae0b0995d604a37ea80e9dddcede2888282c5c02d2a04a`  
		Last Modified: Sun, 18 May 2025 11:44:32 GMT  
		Size: 14.4 KB (14403 bytes)  
		MIME: application/vnd.in-toto+json

### `arangodb:3.12.4.3` - linux; arm64 variant v8

```console
$ docker pull arangodb@sha256:73f7152888962b4836ea41a76815b51238be827dd0f3e9c9f04a104e776af57d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.3 MB (227308594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8a3619bf7969550dc08a0002a610eab9ccb00fb98bbcb16e2be7e9a7ad7486a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 02 May 2025 14:22:22 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Fri, 02 May 2025 14:22:22 GMT
ENV ARANGO_VERSION=3.12.4.3
# Fri, 02 May 2025 14:22:22 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8003EDF6F05459984878D4A6C04AD0FD86FEC04D &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb312/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg # buildkit
# Fri, 02 May 2025 14:22:22 GMT
ENV GLIBCXX_FORCE_NEW=1
# Fri, 02 May 2025 14:22:22 GMT
RUN echo "UTC" > /etc/timezone # buildkit
# Fri, 02 May 2025 14:22:22 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Fri, 02 May 2025 14:22:22 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 02 May 2025 14:22:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 02 May 2025 14:22:22 GMT
EXPOSE map[8529/tcp:{}]
# Fri, 02 May 2025 14:22:22 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1fa68dc9d5277e7329bed3f9e2c9f668ff281391725983e1f7f781324f2d24b`  
		Last Modified: Thu, 08 May 2025 17:50:07 GMT  
		Size: 223.3 MB (223313410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5920b3e505934712fb5114a974798ba2511ded809e337630cc053e7b1132027e`  
		Last Modified: Thu, 08 May 2025 17:46:11 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5830d7fba7025455ac732f90886a5a612fda1c8f2060505e1591a15db9b38311`  
		Last Modified: Thu, 08 May 2025 17:46:12 GMT  
		Size: 2.0 KB (2015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:3.12.4.3` - unknown; unknown

```console
$ docker pull arangodb@sha256:c141a9c936ad3ed3bd0eabc2b86e748189cfdff5bec5d35dee0b167242362820
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **555.4 KB (555397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e3612520f827a2b929ac02c0cb161607e0c2c7ce86610ea6ae8e77dc8671cc5`

```dockerfile
```

-	Layers:
	-	`sha256:4de02ac9a05bc09355efaf201c6c0197842d285cee910dd6d99edc5f0c61fa3f`  
		Last Modified: Sun, 18 May 2025 11:44:35 GMT  
		Size: 540.9 KB (540887 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98265fa0c5715d537b36217ed315b6b68ac3753a89a117a82b16593c5a6edd3b`  
		Last Modified: Sun, 18 May 2025 11:44:35 GMT  
		Size: 14.5 KB (14510 bytes)  
		MIME: application/vnd.in-toto+json

## `arangodb:latest`

```console
$ docker pull arangodb@sha256:527c66aa819d8530150981b0968357901b2f335062c132b6b8b667f59def8ec2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `arangodb:latest` - linux; amd64

```console
$ docker pull arangodb@sha256:ac38852c8c0f873f56b1a72b55b9afd7900d6c2430b2324ef3a67c2d596952e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.8 MB (226818330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d23b75a8acc07edd34a980000d0b2cc4841a4f8def89b09fce982234eb7d47bf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 02 May 2025 14:22:22 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Fri, 02 May 2025 14:22:22 GMT
ENV ARANGO_VERSION=3.12.4.3
# Fri, 02 May 2025 14:22:22 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8003EDF6F05459984878D4A6C04AD0FD86FEC04D &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb312/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg # buildkit
# Fri, 02 May 2025 14:22:22 GMT
ENV GLIBCXX_FORCE_NEW=1
# Fri, 02 May 2025 14:22:22 GMT
RUN echo "UTC" > /etc/timezone # buildkit
# Fri, 02 May 2025 14:22:22 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Fri, 02 May 2025 14:22:22 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 02 May 2025 14:22:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 02 May 2025 14:22:22 GMT
EXPOSE map[8529/tcp:{}]
# Fri, 02 May 2025 14:22:22 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c6b126090c0b0953702d824929e7e26c07b8f4b5ff6727aaff17400652177b1`  
		Last Modified: Thu, 08 May 2025 17:09:31 GMT  
		Size: 223.2 MB (223173928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca0876fbb1b434c6fe684e458e9e1f92daead9031379b8fdc61422e61c13a4fb`  
		Last Modified: Thu, 08 May 2025 17:05:04 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3edfcb6266cca46852db3e1ca102b4a71d381a7e924422f1b0b623b666f93e6`  
		Last Modified: Thu, 08 May 2025 17:05:04 GMT  
		Size: 2.0 KB (2015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:latest` - unknown; unknown

```console
$ docker pull arangodb@sha256:936891622600e5199094bc79c5f1ad231208b088841e2de2077f4910a3df7bd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **404.7 KB (404670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa731d19cf7cfa7ae28b2222a7c163e68b6c38b2ed8e6fd4e7e27ec1051a7b48`

```dockerfile
```

-	Layers:
	-	`sha256:c4118246a94c9fd5ff666932bbd101df5e0e4c73e6faa04aff0aac35ce8a116b`  
		Last Modified: Sun, 18 May 2025 11:44:32 GMT  
		Size: 390.3 KB (390267 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1854e9d2b1ed12662ae0b0995d604a37ea80e9dddcede2888282c5c02d2a04a`  
		Last Modified: Sun, 18 May 2025 11:44:32 GMT  
		Size: 14.4 KB (14403 bytes)  
		MIME: application/vnd.in-toto+json

### `arangodb:latest` - linux; arm64 variant v8

```console
$ docker pull arangodb@sha256:73f7152888962b4836ea41a76815b51238be827dd0f3e9c9f04a104e776af57d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.3 MB (227308594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8a3619bf7969550dc08a0002a610eab9ccb00fb98bbcb16e2be7e9a7ad7486a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 02 May 2025 14:22:22 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Fri, 02 May 2025 14:22:22 GMT
ENV ARANGO_VERSION=3.12.4.3
# Fri, 02 May 2025 14:22:22 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8003EDF6F05459984878D4A6C04AD0FD86FEC04D &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb312/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg # buildkit
# Fri, 02 May 2025 14:22:22 GMT
ENV GLIBCXX_FORCE_NEW=1
# Fri, 02 May 2025 14:22:22 GMT
RUN echo "UTC" > /etc/timezone # buildkit
# Fri, 02 May 2025 14:22:22 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Fri, 02 May 2025 14:22:22 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 02 May 2025 14:22:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 02 May 2025 14:22:22 GMT
EXPOSE map[8529/tcp:{}]
# Fri, 02 May 2025 14:22:22 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1fa68dc9d5277e7329bed3f9e2c9f668ff281391725983e1f7f781324f2d24b`  
		Last Modified: Thu, 08 May 2025 17:50:07 GMT  
		Size: 223.3 MB (223313410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5920b3e505934712fb5114a974798ba2511ded809e337630cc053e7b1132027e`  
		Last Modified: Thu, 08 May 2025 17:46:11 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5830d7fba7025455ac732f90886a5a612fda1c8f2060505e1591a15db9b38311`  
		Last Modified: Thu, 08 May 2025 17:46:12 GMT  
		Size: 2.0 KB (2015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:latest` - unknown; unknown

```console
$ docker pull arangodb@sha256:c141a9c936ad3ed3bd0eabc2b86e748189cfdff5bec5d35dee0b167242362820
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **555.4 KB (555397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e3612520f827a2b929ac02c0cb161607e0c2c7ce86610ea6ae8e77dc8671cc5`

```dockerfile
```

-	Layers:
	-	`sha256:4de02ac9a05bc09355efaf201c6c0197842d285cee910dd6d99edc5f0c61fa3f`  
		Last Modified: Sun, 18 May 2025 11:44:35 GMT  
		Size: 540.9 KB (540887 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98265fa0c5715d537b36217ed315b6b68ac3753a89a117a82b16593c5a6edd3b`  
		Last Modified: Sun, 18 May 2025 11:44:35 GMT  
		Size: 14.5 KB (14510 bytes)  
		MIME: application/vnd.in-toto+json
