<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `arangodb`

-	[`arangodb:3.11`](#arangodb311)
-	[`arangodb:3.11.10.1`](#arangodb311101)
-	[`arangodb:3.12`](#arangodb312)
-	[`arangodb:3.12.2`](#arangodb3122)
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
$ docker pull arangodb@sha256:a5d45f281ce008520fa44e14cd7f44432319ee5d769751ae9d7b5f83b5bb5be7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `arangodb:3.12` - linux; amd64

```console
$ docker pull arangodb@sha256:afae45c0fb49ba2cfb79382f1395f24b3dfaee5316d6b48145e2bbaa1e9d1e5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.8 MB (303798916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06d38d6f2284cdc1ae969d286485a764297d4d7707659fb335805ad2440e0380`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Mon, 22 Jul 2024 22:27:00 GMT
ADD file:ec892b6986dac395477ae6947272ea0913b711cda60bbd7d575b374ecfc4cee2 in / 
# Mon, 22 Jul 2024 22:27:00 GMT
CMD ["/bin/sh"]
# Fri, 26 Jul 2024 09:57:49 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Fri, 26 Jul 2024 09:57:49 GMT
ENV ARANGO_VERSION=3.12.1
# Fri, 26 Jul 2024 09:57:49 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8003EDF6F05459984878D4A6C04AD0FD86FEC04D &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb312/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg # buildkit
# Fri, 26 Jul 2024 09:57:49 GMT
ENV GLIBCXX_FORCE_NEW=1
# Fri, 26 Jul 2024 09:57:49 GMT
RUN echo "UTC" > /etc/timezone # buildkit
# Fri, 26 Jul 2024 09:57:49 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Fri, 26 Jul 2024 09:57:49 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 26 Jul 2024 09:57:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Jul 2024 09:57:49 GMT
EXPOSE map[8529/tcp:{}]
# Fri, 26 Jul 2024 09:57:49 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:b99da37831f37d3f77de0ac7a864f9b69f1dbb4461e5ddfe5a3c2b7e2a3586c5`  
		Last Modified: Mon, 22 Jul 2024 22:27:42 GMT  
		Size: 3.4 MB (3391983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:165dd34e21479ad84f8334e5c1e4b6d52640ba1f571158d32dedd91e4b958457`  
		Last Modified: Fri, 26 Jul 2024 17:56:35 GMT  
		Size: 300.4 MB (300404777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e44f4149f91bbc27aa2d46b12c0943fa3c3d846be4dc750a29e40bddba115caf`  
		Last Modified: Fri, 26 Jul 2024 17:56:28 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d78e72446afbf0ae96d750c1126b056d3928e6231b98ddee55c00d56ec8dd2c`  
		Last Modified: Fri, 26 Jul 2024 17:56:28 GMT  
		Size: 2.0 KB (2016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:3.12` - unknown; unknown

```console
$ docker pull arangodb@sha256:ea5b4c50fafa1c4ba77e1c747c9f95d331c784bafaf150567b1227975a37b206
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **360.0 KB (359972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1123264fac96739337a606f08c4ad5c4653769174790bd04a1a8c4a669c12c95`

```dockerfile
```

-	Layers:
	-	`sha256:68c98fd7c1334e63c6addecaafdaa5310b0d6a1aa368a8b9deb77e1752d78981`  
		Last Modified: Fri, 26 Jul 2024 17:56:28 GMT  
		Size: 345.8 KB (345820 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2bf28d848a07e97a3849e695f486c7c9b057a5e52c35dcc60748ba881ccaae4`  
		Last Modified: Fri, 26 Jul 2024 17:56:28 GMT  
		Size: 14.2 KB (14152 bytes)  
		MIME: application/vnd.in-toto+json

### `arangodb:3.12` - linux; arm64 variant v8

```console
$ docker pull arangodb@sha256:d1d0426b7cb02ed078a0a8816f5433dc2d0c8c4efd144a34f4726aca6cf26adc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.6 MB (305641487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ea8bc79469fa1b5f65bde3ac2f3c2c29c253e84112067e6c869c707a73acbfb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:25 GMT
ADD file:768e36150231c818b6707881e3060e9adfe496d4c48c00b59a05eecb16923c3d in / 
# Mon, 22 Jul 2024 21:44:25 GMT
CMD ["/bin/sh"]
# Fri, 26 Jul 2024 09:57:49 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Fri, 26 Jul 2024 09:57:49 GMT
ENV ARANGO_VERSION=3.12.1
# Fri, 26 Jul 2024 09:57:49 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8003EDF6F05459984878D4A6C04AD0FD86FEC04D &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb312/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg # buildkit
# Fri, 26 Jul 2024 09:57:49 GMT
ENV GLIBCXX_FORCE_NEW=1
# Fri, 26 Jul 2024 09:57:49 GMT
RUN echo "UTC" > /etc/timezone # buildkit
# Fri, 26 Jul 2024 09:57:49 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Fri, 26 Jul 2024 09:57:49 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 26 Jul 2024 09:57:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Jul 2024 09:57:49 GMT
EXPOSE map[8529/tcp:{}]
# Fri, 26 Jul 2024 09:57:49 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:dba698d60556788613e51a85af8ac1331430729add60c326c10517189222232c`  
		Last Modified: Mon, 22 Jul 2024 21:45:05 GMT  
		Size: 3.3 MB (3274245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e24c79362d91b40dc30e22020875b1b10336cf8c464cfef8bfbf2dcbf27d7c1f`  
		Last Modified: Fri, 26 Jul 2024 17:56:12 GMT  
		Size: 302.4 MB (302365086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:411b22215226c32da6c822867f1894a161e2e9bf7fe2ffa964079114c768573e`  
		Last Modified: Fri, 26 Jul 2024 17:56:05 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7683158292df2871be2d82e9b714659092c0521a1f84975fd52a9af8ba3041bc`  
		Last Modified: Fri, 26 Jul 2024 17:56:05 GMT  
		Size: 2.0 KB (2016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:3.12` - unknown; unknown

```console
$ docker pull arangodb@sha256:0d9f7dca946d9d6358ac5ab690ccef38bd3dae72bd9df65134d15885ba0299f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **465.6 KB (465559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:934a07d2866322d006a64cb259c18fbf0d0fb8df3047ff7e648a829eca907bcf`

```dockerfile
```

-	Layers:
	-	`sha256:13dc36b30d7f9af277cd7b36bb6e896d4e596b6944e613117a985a695aa632f4`  
		Last Modified: Fri, 26 Jul 2024 17:56:05 GMT  
		Size: 451.1 KB (451119 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:637606f4a0e8ddd5376bf0bb1b194f3ea0bd089e55589a13fca8a18d2ee3e016`  
		Last Modified: Fri, 26 Jul 2024 17:56:05 GMT  
		Size: 14.4 KB (14440 bytes)  
		MIME: application/vnd.in-toto+json

## `arangodb:3.12.2`

```console
$ docker pull arangodb@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `arangodb:latest`

```console
$ docker pull arangodb@sha256:a5d45f281ce008520fa44e14cd7f44432319ee5d769751ae9d7b5f83b5bb5be7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `arangodb:latest` - linux; amd64

```console
$ docker pull arangodb@sha256:afae45c0fb49ba2cfb79382f1395f24b3dfaee5316d6b48145e2bbaa1e9d1e5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.8 MB (303798916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06d38d6f2284cdc1ae969d286485a764297d4d7707659fb335805ad2440e0380`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Mon, 22 Jul 2024 22:27:00 GMT
ADD file:ec892b6986dac395477ae6947272ea0913b711cda60bbd7d575b374ecfc4cee2 in / 
# Mon, 22 Jul 2024 22:27:00 GMT
CMD ["/bin/sh"]
# Fri, 26 Jul 2024 09:57:49 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Fri, 26 Jul 2024 09:57:49 GMT
ENV ARANGO_VERSION=3.12.1
# Fri, 26 Jul 2024 09:57:49 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8003EDF6F05459984878D4A6C04AD0FD86FEC04D &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb312/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg # buildkit
# Fri, 26 Jul 2024 09:57:49 GMT
ENV GLIBCXX_FORCE_NEW=1
# Fri, 26 Jul 2024 09:57:49 GMT
RUN echo "UTC" > /etc/timezone # buildkit
# Fri, 26 Jul 2024 09:57:49 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Fri, 26 Jul 2024 09:57:49 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 26 Jul 2024 09:57:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Jul 2024 09:57:49 GMT
EXPOSE map[8529/tcp:{}]
# Fri, 26 Jul 2024 09:57:49 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:b99da37831f37d3f77de0ac7a864f9b69f1dbb4461e5ddfe5a3c2b7e2a3586c5`  
		Last Modified: Mon, 22 Jul 2024 22:27:42 GMT  
		Size: 3.4 MB (3391983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:165dd34e21479ad84f8334e5c1e4b6d52640ba1f571158d32dedd91e4b958457`  
		Last Modified: Fri, 26 Jul 2024 17:56:35 GMT  
		Size: 300.4 MB (300404777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e44f4149f91bbc27aa2d46b12c0943fa3c3d846be4dc750a29e40bddba115caf`  
		Last Modified: Fri, 26 Jul 2024 17:56:28 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d78e72446afbf0ae96d750c1126b056d3928e6231b98ddee55c00d56ec8dd2c`  
		Last Modified: Fri, 26 Jul 2024 17:56:28 GMT  
		Size: 2.0 KB (2016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:latest` - unknown; unknown

```console
$ docker pull arangodb@sha256:ea5b4c50fafa1c4ba77e1c747c9f95d331c784bafaf150567b1227975a37b206
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **360.0 KB (359972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1123264fac96739337a606f08c4ad5c4653769174790bd04a1a8c4a669c12c95`

```dockerfile
```

-	Layers:
	-	`sha256:68c98fd7c1334e63c6addecaafdaa5310b0d6a1aa368a8b9deb77e1752d78981`  
		Last Modified: Fri, 26 Jul 2024 17:56:28 GMT  
		Size: 345.8 KB (345820 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2bf28d848a07e97a3849e695f486c7c9b057a5e52c35dcc60748ba881ccaae4`  
		Last Modified: Fri, 26 Jul 2024 17:56:28 GMT  
		Size: 14.2 KB (14152 bytes)  
		MIME: application/vnd.in-toto+json

### `arangodb:latest` - linux; arm64 variant v8

```console
$ docker pull arangodb@sha256:d1d0426b7cb02ed078a0a8816f5433dc2d0c8c4efd144a34f4726aca6cf26adc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.6 MB (305641487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ea8bc79469fa1b5f65bde3ac2f3c2c29c253e84112067e6c869c707a73acbfb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:25 GMT
ADD file:768e36150231c818b6707881e3060e9adfe496d4c48c00b59a05eecb16923c3d in / 
# Mon, 22 Jul 2024 21:44:25 GMT
CMD ["/bin/sh"]
# Fri, 26 Jul 2024 09:57:49 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Fri, 26 Jul 2024 09:57:49 GMT
ENV ARANGO_VERSION=3.12.1
# Fri, 26 Jul 2024 09:57:49 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8003EDF6F05459984878D4A6C04AD0FD86FEC04D &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb312/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg # buildkit
# Fri, 26 Jul 2024 09:57:49 GMT
ENV GLIBCXX_FORCE_NEW=1
# Fri, 26 Jul 2024 09:57:49 GMT
RUN echo "UTC" > /etc/timezone # buildkit
# Fri, 26 Jul 2024 09:57:49 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Fri, 26 Jul 2024 09:57:49 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 26 Jul 2024 09:57:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Jul 2024 09:57:49 GMT
EXPOSE map[8529/tcp:{}]
# Fri, 26 Jul 2024 09:57:49 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:dba698d60556788613e51a85af8ac1331430729add60c326c10517189222232c`  
		Last Modified: Mon, 22 Jul 2024 21:45:05 GMT  
		Size: 3.3 MB (3274245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e24c79362d91b40dc30e22020875b1b10336cf8c464cfef8bfbf2dcbf27d7c1f`  
		Last Modified: Fri, 26 Jul 2024 17:56:12 GMT  
		Size: 302.4 MB (302365086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:411b22215226c32da6c822867f1894a161e2e9bf7fe2ffa964079114c768573e`  
		Last Modified: Fri, 26 Jul 2024 17:56:05 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7683158292df2871be2d82e9b714659092c0521a1f84975fd52a9af8ba3041bc`  
		Last Modified: Fri, 26 Jul 2024 17:56:05 GMT  
		Size: 2.0 KB (2016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:latest` - unknown; unknown

```console
$ docker pull arangodb@sha256:0d9f7dca946d9d6358ac5ab690ccef38bd3dae72bd9df65134d15885ba0299f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **465.6 KB (465559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:934a07d2866322d006a64cb259c18fbf0d0fb8df3047ff7e648a829eca907bcf`

```dockerfile
```

-	Layers:
	-	`sha256:13dc36b30d7f9af277cd7b36bb6e896d4e596b6944e613117a985a695aa632f4`  
		Last Modified: Fri, 26 Jul 2024 17:56:05 GMT  
		Size: 451.1 KB (451119 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:637606f4a0e8ddd5376bf0bb1b194f3ea0bd089e55589a13fca8a18d2ee3e016`  
		Last Modified: Fri, 26 Jul 2024 17:56:05 GMT  
		Size: 14.4 KB (14440 bytes)  
		MIME: application/vnd.in-toto+json
