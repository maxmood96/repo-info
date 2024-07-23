<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `arangodb`

-	[`arangodb:3.11`](#arangodb311)
-	[`arangodb:3.11.10.1`](#arangodb311101)
-	[`arangodb:3.12`](#arangodb312)
-	[`arangodb:3.12.0.2`](#arangodb31202)
-	[`arangodb:latest`](#arangodblatest)

## `arangodb:3.11`

```console
$ docker pull arangodb@sha256:be5c19e9596d8f0dc7b9f06236e89430d08fa617dd6b0efdbb55880c9ffa44b5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `arangodb:3.11` - linux; amd64

```console
$ docker pull arangodb@sha256:9187aa45ca959ed25b71ab8fb754edbc25b7d7a45e5c20ff2f10089e90479923
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.8 MB (198849533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dabc0b692d5577e3904ff21b667024f166c6c477d701d5f4303c80d402a9868`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Sat, 06 Jul 2024 14:26:56 GMT
ADD file:ec892b6986dac395477ae6947272ea0913b711cda60bbd7d575b374ecfc4cee2 in / 
# Sat, 06 Jul 2024 14:26:56 GMT
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
	-	`sha256:b99da37831f37d3f77de0ac7a864f9b69f1dbb4461e5ddfe5a3c2b7e2a3586c5`  
		Last Modified: Mon, 22 Jul 2024 22:27:42 GMT  
		Size: 3.4 MB (3391983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:028d68e3c62ca81a47a3070ece7a8e971810cd0b1216782d0feaa7a41bcc7a49`  
		Last Modified: Mon, 22 Jul 2024 23:03:47 GMT  
		Size: 195.5 MB (195455066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebb3c26f3cef8c90ca233d3703bc7a373668c655180548898480363c937dc2c7`  
		Last Modified: Mon, 22 Jul 2024 23:03:44 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29689fa26695b3fdfaef85e773eaf14f9ec22736d6e6f908c3ed0232e4016259`  
		Last Modified: Mon, 22 Jul 2024 23:03:44 GMT  
		Size: 2.1 KB (2087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a645d5e787c7d11362504ee2c1b94bba171ed7952f9837e7e1794a08b3116f2`  
		Last Modified: Mon, 22 Jul 2024 23:03:44 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:3.11` - unknown; unknown

```console
$ docker pull arangodb@sha256:4324ca1e74e8866561b694a03cc005916f40e1d5bfa23987a337d9df9cb6b09e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **964.6 KB (964594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b1abe90f3e21f1c53513d7e82abfcee5ef98458f0310f06cd3b98a9defa4e8f`

```dockerfile
```

-	Layers:
	-	`sha256:7349d9e1e2c896aa9110312b6b4788e68ded94b7c66aa465071fd802c536072c`  
		Last Modified: Mon, 22 Jul 2024 23:03:44 GMT  
		Size: 949.0 KB (948983 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71e7ebe2fcb12fbdfafe7616da4a497a5411453c373cb5f4082f545feab77aa6`  
		Last Modified: Mon, 22 Jul 2024 23:03:44 GMT  
		Size: 15.6 KB (15611 bytes)  
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
$ docker pull arangodb@sha256:be5c19e9596d8f0dc7b9f06236e89430d08fa617dd6b0efdbb55880c9ffa44b5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `arangodb:3.11.10.1` - linux; amd64

```console
$ docker pull arangodb@sha256:9187aa45ca959ed25b71ab8fb754edbc25b7d7a45e5c20ff2f10089e90479923
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.8 MB (198849533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dabc0b692d5577e3904ff21b667024f166c6c477d701d5f4303c80d402a9868`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Sat, 06 Jul 2024 14:26:56 GMT
ADD file:ec892b6986dac395477ae6947272ea0913b711cda60bbd7d575b374ecfc4cee2 in / 
# Sat, 06 Jul 2024 14:26:56 GMT
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
	-	`sha256:b99da37831f37d3f77de0ac7a864f9b69f1dbb4461e5ddfe5a3c2b7e2a3586c5`  
		Last Modified: Mon, 22 Jul 2024 22:27:42 GMT  
		Size: 3.4 MB (3391983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:028d68e3c62ca81a47a3070ece7a8e971810cd0b1216782d0feaa7a41bcc7a49`  
		Last Modified: Mon, 22 Jul 2024 23:03:47 GMT  
		Size: 195.5 MB (195455066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebb3c26f3cef8c90ca233d3703bc7a373668c655180548898480363c937dc2c7`  
		Last Modified: Mon, 22 Jul 2024 23:03:44 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29689fa26695b3fdfaef85e773eaf14f9ec22736d6e6f908c3ed0232e4016259`  
		Last Modified: Mon, 22 Jul 2024 23:03:44 GMT  
		Size: 2.1 KB (2087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a645d5e787c7d11362504ee2c1b94bba171ed7952f9837e7e1794a08b3116f2`  
		Last Modified: Mon, 22 Jul 2024 23:03:44 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:3.11.10.1` - unknown; unknown

```console
$ docker pull arangodb@sha256:4324ca1e74e8866561b694a03cc005916f40e1d5bfa23987a337d9df9cb6b09e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **964.6 KB (964594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b1abe90f3e21f1c53513d7e82abfcee5ef98458f0310f06cd3b98a9defa4e8f`

```dockerfile
```

-	Layers:
	-	`sha256:7349d9e1e2c896aa9110312b6b4788e68ded94b7c66aa465071fd802c536072c`  
		Last Modified: Mon, 22 Jul 2024 23:03:44 GMT  
		Size: 949.0 KB (948983 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71e7ebe2fcb12fbdfafe7616da4a497a5411453c373cb5f4082f545feab77aa6`  
		Last Modified: Mon, 22 Jul 2024 23:03:44 GMT  
		Size: 15.6 KB (15611 bytes)  
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
$ docker pull arangodb@sha256:d0494ad974c8b51a7dcc79aa55241c1a9db3d6f2318d1beb0d46e2355dd02259
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `arangodb:3.12` - linux; amd64

```console
$ docker pull arangodb@sha256:57b6499556701cde8843b6a4963a7c4e8297a7f78b58ca29abae2f702f588535
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.2 MB (302165083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df2746e862f2101f0d420183fe46d4aef8e22f5fed8a9fb187d89ef7435a67d5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 03 May 2024 11:13:37 GMT
ADD file:ec892b6986dac395477ae6947272ea0913b711cda60bbd7d575b374ecfc4cee2 in / 
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
	-	`sha256:b99da37831f37d3f77de0ac7a864f9b69f1dbb4461e5ddfe5a3c2b7e2a3586c5`  
		Last Modified: Mon, 22 Jul 2024 22:27:42 GMT  
		Size: 3.4 MB (3391983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a032fed7998b90100868e0873b72451e0e8a34d3beff464d1a7130e12d603142`  
		Last Modified: Mon, 22 Jul 2024 23:03:46 GMT  
		Size: 298.8 MB (298770945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26e2621baa529b5d6b96fd7261a96180bd48760f881eae64f8ea24c5f4600ae8`  
		Last Modified: Mon, 22 Jul 2024 23:03:42 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:930c59ef369a7fcaa60a57900ca9b8a34ecfb7172e49a210f30c0e5d1db7da10`  
		Last Modified: Mon, 22 Jul 2024 23:03:42 GMT  
		Size: 2.0 KB (2017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:3.12` - unknown; unknown

```console
$ docker pull arangodb@sha256:d4265f257eb57fcbb4432964051aad27bee61c759c8d9b7e78760c508d7f523c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **360.0 KB (359997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45579d73cdb7da08262bd09f8e0ef346d359d42515003374a293fa18c2ef2a82`

```dockerfile
```

-	Layers:
	-	`sha256:831d42012d8a0ecf29cc721360c583865df5786d43f2e5ad328639c7aedb9e69`  
		Last Modified: Mon, 22 Jul 2024 23:03:43 GMT  
		Size: 345.8 KB (345828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1f035ff8273633eb87f30808ff68ea238cd9891261d577882e83b8e786ba267`  
		Last Modified: Mon, 22 Jul 2024 23:03:42 GMT  
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
$ docker pull arangodb@sha256:d0494ad974c8b51a7dcc79aa55241c1a9db3d6f2318d1beb0d46e2355dd02259
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `arangodb:3.12.0.2` - linux; amd64

```console
$ docker pull arangodb@sha256:57b6499556701cde8843b6a4963a7c4e8297a7f78b58ca29abae2f702f588535
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.2 MB (302165083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df2746e862f2101f0d420183fe46d4aef8e22f5fed8a9fb187d89ef7435a67d5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 03 May 2024 11:13:37 GMT
ADD file:ec892b6986dac395477ae6947272ea0913b711cda60bbd7d575b374ecfc4cee2 in / 
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
	-	`sha256:b99da37831f37d3f77de0ac7a864f9b69f1dbb4461e5ddfe5a3c2b7e2a3586c5`  
		Last Modified: Mon, 22 Jul 2024 22:27:42 GMT  
		Size: 3.4 MB (3391983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a032fed7998b90100868e0873b72451e0e8a34d3beff464d1a7130e12d603142`  
		Last Modified: Mon, 22 Jul 2024 23:03:46 GMT  
		Size: 298.8 MB (298770945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26e2621baa529b5d6b96fd7261a96180bd48760f881eae64f8ea24c5f4600ae8`  
		Last Modified: Mon, 22 Jul 2024 23:03:42 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:930c59ef369a7fcaa60a57900ca9b8a34ecfb7172e49a210f30c0e5d1db7da10`  
		Last Modified: Mon, 22 Jul 2024 23:03:42 GMT  
		Size: 2.0 KB (2017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:3.12.0.2` - unknown; unknown

```console
$ docker pull arangodb@sha256:d4265f257eb57fcbb4432964051aad27bee61c759c8d9b7e78760c508d7f523c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **360.0 KB (359997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45579d73cdb7da08262bd09f8e0ef346d359d42515003374a293fa18c2ef2a82`

```dockerfile
```

-	Layers:
	-	`sha256:831d42012d8a0ecf29cc721360c583865df5786d43f2e5ad328639c7aedb9e69`  
		Last Modified: Mon, 22 Jul 2024 23:03:43 GMT  
		Size: 345.8 KB (345828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1f035ff8273633eb87f30808ff68ea238cd9891261d577882e83b8e786ba267`  
		Last Modified: Mon, 22 Jul 2024 23:03:42 GMT  
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
$ docker pull arangodb@sha256:d0494ad974c8b51a7dcc79aa55241c1a9db3d6f2318d1beb0d46e2355dd02259
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `arangodb:latest` - linux; amd64

```console
$ docker pull arangodb@sha256:57b6499556701cde8843b6a4963a7c4e8297a7f78b58ca29abae2f702f588535
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.2 MB (302165083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df2746e862f2101f0d420183fe46d4aef8e22f5fed8a9fb187d89ef7435a67d5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 03 May 2024 11:13:37 GMT
ADD file:ec892b6986dac395477ae6947272ea0913b711cda60bbd7d575b374ecfc4cee2 in / 
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
	-	`sha256:b99da37831f37d3f77de0ac7a864f9b69f1dbb4461e5ddfe5a3c2b7e2a3586c5`  
		Last Modified: Mon, 22 Jul 2024 22:27:42 GMT  
		Size: 3.4 MB (3391983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a032fed7998b90100868e0873b72451e0e8a34d3beff464d1a7130e12d603142`  
		Last Modified: Mon, 22 Jul 2024 23:03:46 GMT  
		Size: 298.8 MB (298770945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26e2621baa529b5d6b96fd7261a96180bd48760f881eae64f8ea24c5f4600ae8`  
		Last Modified: Mon, 22 Jul 2024 23:03:42 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:930c59ef369a7fcaa60a57900ca9b8a34ecfb7172e49a210f30c0e5d1db7da10`  
		Last Modified: Mon, 22 Jul 2024 23:03:42 GMT  
		Size: 2.0 KB (2017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:latest` - unknown; unknown

```console
$ docker pull arangodb@sha256:d4265f257eb57fcbb4432964051aad27bee61c759c8d9b7e78760c508d7f523c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **360.0 KB (359997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45579d73cdb7da08262bd09f8e0ef346d359d42515003374a293fa18c2ef2a82`

```dockerfile
```

-	Layers:
	-	`sha256:831d42012d8a0ecf29cc721360c583865df5786d43f2e5ad328639c7aedb9e69`  
		Last Modified: Mon, 22 Jul 2024 23:03:43 GMT  
		Size: 345.8 KB (345828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1f035ff8273633eb87f30808ff68ea238cd9891261d577882e83b8e786ba267`  
		Last Modified: Mon, 22 Jul 2024 23:03:42 GMT  
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
