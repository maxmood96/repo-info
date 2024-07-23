<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `arangodb`

-	[`arangodb:3.11`](#arangodb311)
-	[`arangodb:3.11.10.1`](#arangodb311101)
-	[`arangodb:3.12`](#arangodb312)
-	[`arangodb:3.12.0.2`](#arangodb31202)
-	[`arangodb:latest`](#arangodblatest)

## `arangodb:3.11`

```console
$ docker pull arangodb@sha256:b2d9f14b58176066341d7d7b75a1bf44c9323ca60450309e704cf1bf9bfdc7cb
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
$ docker pull arangodb@sha256:fe0670a28e482f3bb0ea9366734a94c7605a5efdd6534efe2a0267422d456ea5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.1 MB (202145677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6befa8fcdb63dc5c9ac3807fec03cec9b9c0f63965cee2af99b9c4f9945fa37b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Sat, 06 Jul 2024 14:26:56 GMT
ADD file:768e36150231c818b6707881e3060e9adfe496d4c48c00b59a05eecb16923c3d in / 
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
	-	`sha256:dba698d60556788613e51a85af8ac1331430729add60c326c10517189222232c`  
		Last Modified: Mon, 22 Jul 2024 21:45:05 GMT  
		Size: 3.3 MB (3274245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f7bf7a4dd54841e21866c5e3a13fdea4dd65619f1273a43563d9d88ebfffebb`  
		Last Modified: Tue, 23 Jul 2024 11:08:56 GMT  
		Size: 198.9 MB (198868949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9395fa1b942b937b36f6f7b48eb562be69a85227fd300e7d4fc97601fab4645b`  
		Last Modified: Tue, 23 Jul 2024 11:08:52 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a26973da5d537d955fca541f3bc5f512a4212cab565dd2d1f027ab6ca74f3f6`  
		Last Modified: Tue, 23 Jul 2024 11:08:52 GMT  
		Size: 2.1 KB (2087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4881cbdef715107bd71579d53b9f6f6906d2a8baed634338933abba10c5fbef`  
		Last Modified: Tue, 23 Jul 2024 11:08:53 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:3.11` - unknown; unknown

```console
$ docker pull arangodb@sha256:61ad12757825d93c63075c652885535c5ebefd496f48ace97a1cc49948696008
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1070157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5da985a986110cb46648d59d27dc4e02e096a6b8f02d5641d719e60ece0da60`

```dockerfile
```

-	Layers:
	-	`sha256:b1cde0d1eaf652389aa4cfcc58eb88e7c9b0c763eb05361eef69631205a5b919`  
		Last Modified: Tue, 23 Jul 2024 11:08:52 GMT  
		Size: 1.1 MB (1054270 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49f0631f127c5da25b7eae56dc5597590f3c5dcf16a29943c4f4de2058359280`  
		Last Modified: Tue, 23 Jul 2024 11:08:52 GMT  
		Size: 15.9 KB (15887 bytes)  
		MIME: application/vnd.in-toto+json

## `arangodb:3.11.10.1`

```console
$ docker pull arangodb@sha256:b2d9f14b58176066341d7d7b75a1bf44c9323ca60450309e704cf1bf9bfdc7cb
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
$ docker pull arangodb@sha256:fe0670a28e482f3bb0ea9366734a94c7605a5efdd6534efe2a0267422d456ea5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.1 MB (202145677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6befa8fcdb63dc5c9ac3807fec03cec9b9c0f63965cee2af99b9c4f9945fa37b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Sat, 06 Jul 2024 14:26:56 GMT
ADD file:768e36150231c818b6707881e3060e9adfe496d4c48c00b59a05eecb16923c3d in / 
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
	-	`sha256:dba698d60556788613e51a85af8ac1331430729add60c326c10517189222232c`  
		Last Modified: Mon, 22 Jul 2024 21:45:05 GMT  
		Size: 3.3 MB (3274245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f7bf7a4dd54841e21866c5e3a13fdea4dd65619f1273a43563d9d88ebfffebb`  
		Last Modified: Tue, 23 Jul 2024 11:08:56 GMT  
		Size: 198.9 MB (198868949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9395fa1b942b937b36f6f7b48eb562be69a85227fd300e7d4fc97601fab4645b`  
		Last Modified: Tue, 23 Jul 2024 11:08:52 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a26973da5d537d955fca541f3bc5f512a4212cab565dd2d1f027ab6ca74f3f6`  
		Last Modified: Tue, 23 Jul 2024 11:08:52 GMT  
		Size: 2.1 KB (2087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4881cbdef715107bd71579d53b9f6f6906d2a8baed634338933abba10c5fbef`  
		Last Modified: Tue, 23 Jul 2024 11:08:53 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:3.11.10.1` - unknown; unknown

```console
$ docker pull arangodb@sha256:61ad12757825d93c63075c652885535c5ebefd496f48ace97a1cc49948696008
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1070157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5da985a986110cb46648d59d27dc4e02e096a6b8f02d5641d719e60ece0da60`

```dockerfile
```

-	Layers:
	-	`sha256:b1cde0d1eaf652389aa4cfcc58eb88e7c9b0c763eb05361eef69631205a5b919`  
		Last Modified: Tue, 23 Jul 2024 11:08:52 GMT  
		Size: 1.1 MB (1054270 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49f0631f127c5da25b7eae56dc5597590f3c5dcf16a29943c4f4de2058359280`  
		Last Modified: Tue, 23 Jul 2024 11:08:52 GMT  
		Size: 15.9 KB (15887 bytes)  
		MIME: application/vnd.in-toto+json

## `arangodb:3.12`

```console
$ docker pull arangodb@sha256:e0e61d3ce857c5777664784d0279adb9c0ea6e05654bd632ef1cd286e63680e7
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
$ docker pull arangodb@sha256:c42c1cccf9a6458485a7aaa0d6567c7c6e3cbc99d359a8f1d6dc3bde305adb03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.4 MB (304402947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0a42ae1797fc9a080dda5a6ab0c7a18bd116b4f68d7eabf21c93d44b256abd7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 03 May 2024 11:13:37 GMT
ADD file:768e36150231c818b6707881e3060e9adfe496d4c48c00b59a05eecb16923c3d in / 
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
	-	`sha256:dba698d60556788613e51a85af8ac1331430729add60c326c10517189222232c`  
		Last Modified: Mon, 22 Jul 2024 21:45:05 GMT  
		Size: 3.3 MB (3274245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f89d1f2278162366fea1c7da8cad6fb784de5c955a027434efa42fa8ded3ed26`  
		Last Modified: Tue, 23 Jul 2024 11:10:11 GMT  
		Size: 301.1 MB (301126547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4322ee8f3d653e3cd63b31d5865c835cdc8d5a8e1f7460b8367c7d9407bc109a`  
		Last Modified: Tue, 23 Jul 2024 11:10:03 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:418b2a7ad1f935fb0d894a2e7a02a719b3ceb97fafd616763e1fd615839f6ef3`  
		Last Modified: Tue, 23 Jul 2024 11:10:03 GMT  
		Size: 2.0 KB (2017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:3.12` - unknown; unknown

```console
$ docker pull arangodb@sha256:a5e9a8d2576651b9ac5ff982c557533f1f363a9e7ddb3f3c3d433ffb05078256
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **465.6 KB (465585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0f5e5c64a1d3b1cc10f086bcd792dabebf2b864fc47a97f0df603c74804981b`

```dockerfile
```

-	Layers:
	-	`sha256:24ddac777b767b64f18ae8b9ac2c511ef7d922717fd2a2d2e7a20b6be9c600f8`  
		Last Modified: Tue, 23 Jul 2024 11:10:03 GMT  
		Size: 451.1 KB (451127 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f738a05db3acd0fa07b2d757450c82592e200710eeab86df37a2c971f74bf39a`  
		Last Modified: Tue, 23 Jul 2024 11:10:03 GMT  
		Size: 14.5 KB (14458 bytes)  
		MIME: application/vnd.in-toto+json

## `arangodb:3.12.0.2`

```console
$ docker pull arangodb@sha256:e0e61d3ce857c5777664784d0279adb9c0ea6e05654bd632ef1cd286e63680e7
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
$ docker pull arangodb@sha256:c42c1cccf9a6458485a7aaa0d6567c7c6e3cbc99d359a8f1d6dc3bde305adb03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.4 MB (304402947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0a42ae1797fc9a080dda5a6ab0c7a18bd116b4f68d7eabf21c93d44b256abd7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 03 May 2024 11:13:37 GMT
ADD file:768e36150231c818b6707881e3060e9adfe496d4c48c00b59a05eecb16923c3d in / 
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
	-	`sha256:dba698d60556788613e51a85af8ac1331430729add60c326c10517189222232c`  
		Last Modified: Mon, 22 Jul 2024 21:45:05 GMT  
		Size: 3.3 MB (3274245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f89d1f2278162366fea1c7da8cad6fb784de5c955a027434efa42fa8ded3ed26`  
		Last Modified: Tue, 23 Jul 2024 11:10:11 GMT  
		Size: 301.1 MB (301126547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4322ee8f3d653e3cd63b31d5865c835cdc8d5a8e1f7460b8367c7d9407bc109a`  
		Last Modified: Tue, 23 Jul 2024 11:10:03 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:418b2a7ad1f935fb0d894a2e7a02a719b3ceb97fafd616763e1fd615839f6ef3`  
		Last Modified: Tue, 23 Jul 2024 11:10:03 GMT  
		Size: 2.0 KB (2017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:3.12.0.2` - unknown; unknown

```console
$ docker pull arangodb@sha256:a5e9a8d2576651b9ac5ff982c557533f1f363a9e7ddb3f3c3d433ffb05078256
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **465.6 KB (465585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0f5e5c64a1d3b1cc10f086bcd792dabebf2b864fc47a97f0df603c74804981b`

```dockerfile
```

-	Layers:
	-	`sha256:24ddac777b767b64f18ae8b9ac2c511ef7d922717fd2a2d2e7a20b6be9c600f8`  
		Last Modified: Tue, 23 Jul 2024 11:10:03 GMT  
		Size: 451.1 KB (451127 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f738a05db3acd0fa07b2d757450c82592e200710eeab86df37a2c971f74bf39a`  
		Last Modified: Tue, 23 Jul 2024 11:10:03 GMT  
		Size: 14.5 KB (14458 bytes)  
		MIME: application/vnd.in-toto+json

## `arangodb:latest`

```console
$ docker pull arangodb@sha256:e0e61d3ce857c5777664784d0279adb9c0ea6e05654bd632ef1cd286e63680e7
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
$ docker pull arangodb@sha256:c42c1cccf9a6458485a7aaa0d6567c7c6e3cbc99d359a8f1d6dc3bde305adb03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.4 MB (304402947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0a42ae1797fc9a080dda5a6ab0c7a18bd116b4f68d7eabf21c93d44b256abd7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 03 May 2024 11:13:37 GMT
ADD file:768e36150231c818b6707881e3060e9adfe496d4c48c00b59a05eecb16923c3d in / 
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
	-	`sha256:dba698d60556788613e51a85af8ac1331430729add60c326c10517189222232c`  
		Last Modified: Mon, 22 Jul 2024 21:45:05 GMT  
		Size: 3.3 MB (3274245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f89d1f2278162366fea1c7da8cad6fb784de5c955a027434efa42fa8ded3ed26`  
		Last Modified: Tue, 23 Jul 2024 11:10:11 GMT  
		Size: 301.1 MB (301126547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4322ee8f3d653e3cd63b31d5865c835cdc8d5a8e1f7460b8367c7d9407bc109a`  
		Last Modified: Tue, 23 Jul 2024 11:10:03 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:418b2a7ad1f935fb0d894a2e7a02a719b3ceb97fafd616763e1fd615839f6ef3`  
		Last Modified: Tue, 23 Jul 2024 11:10:03 GMT  
		Size: 2.0 KB (2017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:latest` - unknown; unknown

```console
$ docker pull arangodb@sha256:a5e9a8d2576651b9ac5ff982c557533f1f363a9e7ddb3f3c3d433ffb05078256
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **465.6 KB (465585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0f5e5c64a1d3b1cc10f086bcd792dabebf2b864fc47a97f0df603c74804981b`

```dockerfile
```

-	Layers:
	-	`sha256:24ddac777b767b64f18ae8b9ac2c511ef7d922717fd2a2d2e7a20b6be9c600f8`  
		Last Modified: Tue, 23 Jul 2024 11:10:03 GMT  
		Size: 451.1 KB (451127 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f738a05db3acd0fa07b2d757450c82592e200710eeab86df37a2c971f74bf39a`  
		Last Modified: Tue, 23 Jul 2024 11:10:03 GMT  
		Size: 14.5 KB (14458 bytes)  
		MIME: application/vnd.in-toto+json
