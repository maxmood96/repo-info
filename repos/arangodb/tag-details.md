<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `arangodb`

-	[`arangodb:3.11`](#arangodb311)
-	[`arangodb:3.11.12`](#arangodb31112)
-	[`arangodb:3.12`](#arangodb312)
-	[`arangodb:3.12.3`](#arangodb3123)
-	[`arangodb:latest`](#arangodblatest)

## `arangodb:3.11`

```console
$ docker pull arangodb@sha256:99af4225143db7ef78325c0b73066dffb5a83022f9e7e8b374d422a5263e55f5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `arangodb:3.11` - linux; amd64

```console
$ docker pull arangodb@sha256:f63a5173d811eea1ca060e6449e3257f79c096fe091a9a6fd6fff6da7cbaa219
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.1 MB (199149372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00907b375d3d1f25acff102d9039c0ced0d37b9bad760e715acb59b26a4f88d6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 06 Sep 2024 12:02:06 GMT
ADD alpine-minirootfs-3.17.10-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:02:06 GMT
CMD ["/bin/sh"]
# Wed, 06 Nov 2024 09:31:11 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Wed, 06 Nov 2024 09:31:11 GMT
ENV ARANGO_VERSION=3.11.12
# Wed, 06 Nov 2024 09:31:11 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8003EDF6F05459984878D4A6C04AD0FD86FEC04D &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb311/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg # buildkit
# Wed, 06 Nov 2024 09:31:11 GMT
ENV GLIBCXX_FORCE_NEW=1
# Wed, 06 Nov 2024 09:31:11 GMT
RUN echo "UTC" > /etc/timezone # buildkit
# Wed, 06 Nov 2024 09:31:11 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Wed, 06 Nov 2024 09:31:11 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 06 Nov 2024 09:31:11 GMT
COPY docker-foxx.sh /usr/bin/foxx # buildkit
# Wed, 06 Nov 2024 09:31:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 06 Nov 2024 09:31:11 GMT
EXPOSE map[8529/tcp:{}]
# Wed, 06 Nov 2024 09:31:11 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:fbcfea79c1c4819e0689385057cfd4cbd2ee9ba20e6d420b360644788a22862c`  
		Last Modified: Mon, 09 Sep 2024 07:01:59 GMT  
		Size: 3.4 MB (3392252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b6a7c612efb6701c2823d2834f2d0831f5333c4379935139cc9a84ea0b3ca2a`  
		Last Modified: Tue, 12 Nov 2024 02:02:12 GMT  
		Size: 195.8 MB (195754634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce19a496ab22cd5d857e7281b226bbcdf1ad517aaa28caa8369c7249482756ea`  
		Last Modified: Tue, 12 Nov 2024 02:02:08 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d66f518dfc0088affaa845c23e761f4fdd7c68776de64afac5ebfea537c5d491`  
		Last Modified: Tue, 12 Nov 2024 02:02:08 GMT  
		Size: 2.1 KB (2087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5331f41653e13b56185be229ba1de82fdac2dc6065ecf05ab8282060f8c57ef3`  
		Last Modified: Tue, 12 Nov 2024 02:02:08 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:3.11` - unknown; unknown

```console
$ docker pull arangodb@sha256:daf8e3ef1969d556393bc37257d66954815f261c815c8b7b11934b5ec514e597
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1038199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89ae5517630efd20858385aea4758b1111043222ebdc16486411109d912be7cc`

```dockerfile
```

-	Layers:
	-	`sha256:27b678c64a007553f187c8614e43bdfac3b0d92c2e5347694db0c592a877e8ab`  
		Last Modified: Tue, 12 Nov 2024 02:02:08 GMT  
		Size: 1.0 MB (1022379 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d3e1178684a484c8604e1f1916284ec511088ae00554a1ea669663fcc1c512e`  
		Last Modified: Tue, 12 Nov 2024 02:02:08 GMT  
		Size: 15.8 KB (15820 bytes)  
		MIME: application/vnd.in-toto+json

### `arangodb:3.11` - linux; arm64 variant v8

```console
$ docker pull arangodb@sha256:f8f65c5eaae5adcf7ea27e84862392faae1ada551a6eb8fda7c0232d37988f85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.4 MB (202445903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:089b66f5f87d93f0950cdce26a56916d390ed75614ad1d2bbd6d59dff2ed838c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 06 Sep 2024 12:02:06 GMT
ADD alpine-minirootfs-3.17.10-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:02:06 GMT
CMD ["/bin/sh"]
# Wed, 06 Nov 2024 09:31:11 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Wed, 06 Nov 2024 09:31:11 GMT
ENV ARANGO_VERSION=3.11.12
# Wed, 06 Nov 2024 09:31:11 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8003EDF6F05459984878D4A6C04AD0FD86FEC04D &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb311/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg # buildkit
# Wed, 06 Nov 2024 09:31:11 GMT
ENV GLIBCXX_FORCE_NEW=1
# Wed, 06 Nov 2024 09:31:11 GMT
RUN echo "UTC" > /etc/timezone # buildkit
# Wed, 06 Nov 2024 09:31:11 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Wed, 06 Nov 2024 09:31:11 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 06 Nov 2024 09:31:11 GMT
COPY docker-foxx.sh /usr/bin/foxx # buildkit
# Wed, 06 Nov 2024 09:31:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 06 Nov 2024 09:31:11 GMT
EXPOSE map[8529/tcp:{}]
# Wed, 06 Nov 2024 09:31:11 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:61254a502902280aa7caa832f8b3ed5c96aa04faf42ab0ba23ff17638f910f21`  
		Last Modified: Mon, 09 Sep 2024 07:02:02 GMT  
		Size: 3.3 MB (3275161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45fc6964c3ae6d64114db143169bd28871d1c59ad14f75450179d139308babbd`  
		Last Modified: Tue, 12 Nov 2024 02:02:58 GMT  
		Size: 199.2 MB (199168256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dff5c0047a7def6c79f6b74a26d6c57ae7d16d75975719660a7b0b5f372550b`  
		Last Modified: Tue, 12 Nov 2024 02:02:53 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3db0c011f2a7023f0a6ec139edfabbe1588067e8be34e8d3f7dbb8893ce33167`  
		Last Modified: Tue, 12 Nov 2024 02:02:53 GMT  
		Size: 2.1 KB (2088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ee1884288bfbf0549430f857ed78cde23e8420652b2edbb40081867319ee36e`  
		Last Modified: Tue, 12 Nov 2024 02:02:53 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:3.11` - unknown; unknown

```console
$ docker pull arangodb@sha256:d10eaef2399232a637b41dce9444ec72d2751ec1eb40d5d632041b3d7f7da9cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1143581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b0e63a80d44fd5dc1241f1b5194f507297b97a402964057e49f31796d04788f`

```dockerfile
```

-	Layers:
	-	`sha256:0d47356f67ff33b69e5067bc4ac33fef2a54098cc53950cf427564f4bed9415b`  
		Last Modified: Tue, 12 Nov 2024 02:02:53 GMT  
		Size: 1.1 MB (1127666 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8bdf296fe6d9d35a43e307aa1e55dd79c4059466babb3b19126c4b76cf1ff06e`  
		Last Modified: Tue, 12 Nov 2024 02:02:53 GMT  
		Size: 15.9 KB (15915 bytes)  
		MIME: application/vnd.in-toto+json

## `arangodb:3.11.12`

```console
$ docker pull arangodb@sha256:99af4225143db7ef78325c0b73066dffb5a83022f9e7e8b374d422a5263e55f5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `arangodb:3.11.12` - linux; amd64

```console
$ docker pull arangodb@sha256:f63a5173d811eea1ca060e6449e3257f79c096fe091a9a6fd6fff6da7cbaa219
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.1 MB (199149372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00907b375d3d1f25acff102d9039c0ced0d37b9bad760e715acb59b26a4f88d6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 06 Sep 2024 12:02:06 GMT
ADD alpine-minirootfs-3.17.10-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:02:06 GMT
CMD ["/bin/sh"]
# Wed, 06 Nov 2024 09:31:11 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Wed, 06 Nov 2024 09:31:11 GMT
ENV ARANGO_VERSION=3.11.12
# Wed, 06 Nov 2024 09:31:11 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8003EDF6F05459984878D4A6C04AD0FD86FEC04D &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb311/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg # buildkit
# Wed, 06 Nov 2024 09:31:11 GMT
ENV GLIBCXX_FORCE_NEW=1
# Wed, 06 Nov 2024 09:31:11 GMT
RUN echo "UTC" > /etc/timezone # buildkit
# Wed, 06 Nov 2024 09:31:11 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Wed, 06 Nov 2024 09:31:11 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 06 Nov 2024 09:31:11 GMT
COPY docker-foxx.sh /usr/bin/foxx # buildkit
# Wed, 06 Nov 2024 09:31:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 06 Nov 2024 09:31:11 GMT
EXPOSE map[8529/tcp:{}]
# Wed, 06 Nov 2024 09:31:11 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:fbcfea79c1c4819e0689385057cfd4cbd2ee9ba20e6d420b360644788a22862c`  
		Last Modified: Mon, 09 Sep 2024 07:01:59 GMT  
		Size: 3.4 MB (3392252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b6a7c612efb6701c2823d2834f2d0831f5333c4379935139cc9a84ea0b3ca2a`  
		Last Modified: Tue, 12 Nov 2024 02:02:12 GMT  
		Size: 195.8 MB (195754634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce19a496ab22cd5d857e7281b226bbcdf1ad517aaa28caa8369c7249482756ea`  
		Last Modified: Tue, 12 Nov 2024 02:02:08 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d66f518dfc0088affaa845c23e761f4fdd7c68776de64afac5ebfea537c5d491`  
		Last Modified: Tue, 12 Nov 2024 02:02:08 GMT  
		Size: 2.1 KB (2087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5331f41653e13b56185be229ba1de82fdac2dc6065ecf05ab8282060f8c57ef3`  
		Last Modified: Tue, 12 Nov 2024 02:02:08 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:3.11.12` - unknown; unknown

```console
$ docker pull arangodb@sha256:daf8e3ef1969d556393bc37257d66954815f261c815c8b7b11934b5ec514e597
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1038199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89ae5517630efd20858385aea4758b1111043222ebdc16486411109d912be7cc`

```dockerfile
```

-	Layers:
	-	`sha256:27b678c64a007553f187c8614e43bdfac3b0d92c2e5347694db0c592a877e8ab`  
		Last Modified: Tue, 12 Nov 2024 02:02:08 GMT  
		Size: 1.0 MB (1022379 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d3e1178684a484c8604e1f1916284ec511088ae00554a1ea669663fcc1c512e`  
		Last Modified: Tue, 12 Nov 2024 02:02:08 GMT  
		Size: 15.8 KB (15820 bytes)  
		MIME: application/vnd.in-toto+json

### `arangodb:3.11.12` - linux; arm64 variant v8

```console
$ docker pull arangodb@sha256:f8f65c5eaae5adcf7ea27e84862392faae1ada551a6eb8fda7c0232d37988f85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.4 MB (202445903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:089b66f5f87d93f0950cdce26a56916d390ed75614ad1d2bbd6d59dff2ed838c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 06 Sep 2024 12:02:06 GMT
ADD alpine-minirootfs-3.17.10-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:02:06 GMT
CMD ["/bin/sh"]
# Wed, 06 Nov 2024 09:31:11 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Wed, 06 Nov 2024 09:31:11 GMT
ENV ARANGO_VERSION=3.11.12
# Wed, 06 Nov 2024 09:31:11 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8003EDF6F05459984878D4A6C04AD0FD86FEC04D &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb311/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg # buildkit
# Wed, 06 Nov 2024 09:31:11 GMT
ENV GLIBCXX_FORCE_NEW=1
# Wed, 06 Nov 2024 09:31:11 GMT
RUN echo "UTC" > /etc/timezone # buildkit
# Wed, 06 Nov 2024 09:31:11 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Wed, 06 Nov 2024 09:31:11 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 06 Nov 2024 09:31:11 GMT
COPY docker-foxx.sh /usr/bin/foxx # buildkit
# Wed, 06 Nov 2024 09:31:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 06 Nov 2024 09:31:11 GMT
EXPOSE map[8529/tcp:{}]
# Wed, 06 Nov 2024 09:31:11 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:61254a502902280aa7caa832f8b3ed5c96aa04faf42ab0ba23ff17638f910f21`  
		Last Modified: Mon, 09 Sep 2024 07:02:02 GMT  
		Size: 3.3 MB (3275161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45fc6964c3ae6d64114db143169bd28871d1c59ad14f75450179d139308babbd`  
		Last Modified: Tue, 12 Nov 2024 02:02:58 GMT  
		Size: 199.2 MB (199168256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dff5c0047a7def6c79f6b74a26d6c57ae7d16d75975719660a7b0b5f372550b`  
		Last Modified: Tue, 12 Nov 2024 02:02:53 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3db0c011f2a7023f0a6ec139edfabbe1588067e8be34e8d3f7dbb8893ce33167`  
		Last Modified: Tue, 12 Nov 2024 02:02:53 GMT  
		Size: 2.1 KB (2088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ee1884288bfbf0549430f857ed78cde23e8420652b2edbb40081867319ee36e`  
		Last Modified: Tue, 12 Nov 2024 02:02:53 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:3.11.12` - unknown; unknown

```console
$ docker pull arangodb@sha256:d10eaef2399232a637b41dce9444ec72d2751ec1eb40d5d632041b3d7f7da9cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1143581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b0e63a80d44fd5dc1241f1b5194f507297b97a402964057e49f31796d04788f`

```dockerfile
```

-	Layers:
	-	`sha256:0d47356f67ff33b69e5067bc4ac33fef2a54098cc53950cf427564f4bed9415b`  
		Last Modified: Tue, 12 Nov 2024 02:02:53 GMT  
		Size: 1.1 MB (1127666 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8bdf296fe6d9d35a43e307aa1e55dd79c4059466babb3b19126c4b76cf1ff06e`  
		Last Modified: Tue, 12 Nov 2024 02:02:53 GMT  
		Size: 15.9 KB (15915 bytes)  
		MIME: application/vnd.in-toto+json

## `arangodb:3.12`

```console
$ docker pull arangodb@sha256:bab5f96a0cd667f3cd2ef6eb2f058bce89a94c1f9e86b7dec864254a55f52ad3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `arangodb:3.12` - linux; amd64

```console
$ docker pull arangodb@sha256:98dee3ef63853826c6b162b189ad9bc0cbd28736b8f86449949e7309553fa259
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.6 MB (304636261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61cbf573466c897f98267dae7f24e353b7a4e675fe66d5a53f80df2da2628908`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 06 Sep 2024 12:02:06 GMT
ADD alpine-minirootfs-3.17.10-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:02:06 GMT
CMD ["/bin/sh"]
# Wed, 30 Oct 2024 15:12:33 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Wed, 30 Oct 2024 15:12:33 GMT
ENV ARANGO_VERSION=3.12.3
# Wed, 30 Oct 2024 15:12:33 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8003EDF6F05459984878D4A6C04AD0FD86FEC04D &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb312/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg # buildkit
# Wed, 30 Oct 2024 15:12:33 GMT
ENV GLIBCXX_FORCE_NEW=1
# Wed, 30 Oct 2024 15:12:33 GMT
RUN echo "UTC" > /etc/timezone # buildkit
# Wed, 30 Oct 2024 15:12:33 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Wed, 30 Oct 2024 15:12:33 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 30 Oct 2024 15:12:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 30 Oct 2024 15:12:33 GMT
EXPOSE map[8529/tcp:{}]
# Wed, 30 Oct 2024 15:12:33 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:fbcfea79c1c4819e0689385057cfd4cbd2ee9ba20e6d420b360644788a22862c`  
		Last Modified: Mon, 09 Sep 2024 07:01:59 GMT  
		Size: 3.4 MB (3392252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b84a29e021b6aaeabf075ce866c32091fd8ef712fab99f9fda373a5ea636b9f6`  
		Last Modified: Tue, 12 Nov 2024 02:02:16 GMT  
		Size: 301.2 MB (301241853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c5ab759f98983a52ff63397651f5a3fae8b1a3df12ddf541a8c33c6ff136a0f`  
		Last Modified: Tue, 12 Nov 2024 02:02:06 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47eda9f35c5db5a20cdc21a94c2c33f7476801a78dd4cc5838f84a33d32a6644`  
		Last Modified: Tue, 12 Nov 2024 02:02:06 GMT  
		Size: 2.0 KB (2016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:3.12` - unknown; unknown

```console
$ docker pull arangodb@sha256:845c9dfee6094aea497c014869c699e3a9987cee93586de26ce0e18cfe342c9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **372.9 KB (372905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c110e5dc85c76c5fb3bde7d10a499557d4c419e5880b9dfbd97685fe0231b03`

```dockerfile
```

-	Layers:
	-	`sha256:e1d5a7fef24fc5803d50e90ffd05076e6e2c31dc2adee6bff6a50b27c245b7cf`  
		Last Modified: Tue, 12 Nov 2024 02:02:06 GMT  
		Size: 358.5 KB (358520 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51e15f395bd212b71c9bfa97c3fe80c1ef8a28d2c92b213aee3206a6536ba9fd`  
		Last Modified: Tue, 12 Nov 2024 02:02:06 GMT  
		Size: 14.4 KB (14385 bytes)  
		MIME: application/vnd.in-toto+json

### `arangodb:3.12` - linux; arm64 variant v8

```console
$ docker pull arangodb@sha256:5c5a9c26a373492d81244bd0e6c932631b332ac4ef86d4a5efe8c77cd6eb1d33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.5 MB (306524920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19aee834bf6ab375f9410ab8b6826994a9c9d150925ea1ac6e62b45173185ab5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 06 Sep 2024 12:02:06 GMT
ADD alpine-minirootfs-3.17.10-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:02:06 GMT
CMD ["/bin/sh"]
# Wed, 30 Oct 2024 15:12:33 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Wed, 30 Oct 2024 15:12:33 GMT
ENV ARANGO_VERSION=3.12.3
# Wed, 30 Oct 2024 15:12:33 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8003EDF6F05459984878D4A6C04AD0FD86FEC04D &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb312/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg # buildkit
# Wed, 30 Oct 2024 15:12:33 GMT
ENV GLIBCXX_FORCE_NEW=1
# Wed, 30 Oct 2024 15:12:33 GMT
RUN echo "UTC" > /etc/timezone # buildkit
# Wed, 30 Oct 2024 15:12:33 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Wed, 30 Oct 2024 15:12:33 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 30 Oct 2024 15:12:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 30 Oct 2024 15:12:33 GMT
EXPOSE map[8529/tcp:{}]
# Wed, 30 Oct 2024 15:12:33 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:61254a502902280aa7caa832f8b3ed5c96aa04faf42ab0ba23ff17638f910f21`  
		Last Modified: Mon, 09 Sep 2024 07:02:02 GMT  
		Size: 3.3 MB (3275161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9e8e9682cd434a2ff1f05b8704c94bc802b2a4676dab3d5b6f19874bf55a864`  
		Last Modified: Tue, 12 Nov 2024 02:04:12 GMT  
		Size: 303.2 MB (303247603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03f16d88fc0fd758c5db76f41930152f7a237f0963dc0697c99e75dd10f8dae8`  
		Last Modified: Tue, 12 Nov 2024 02:04:05 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6ad0d0cfd87b12f0d4f8e2e8ae21d794ab6c36e018bc84d180091112073d86b`  
		Last Modified: Tue, 12 Nov 2024 02:04:05 GMT  
		Size: 2.0 KB (2016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:3.12` - unknown; unknown

```console
$ docker pull arangodb@sha256:93368a07c6f35753b2f185178c69fe2602bbf6663edebe4f6bb8e5bd475b282f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **478.3 KB (478310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f94ce7f3dcfbf25e6cff5bcd99dd68702ba49c5ec0fef96d01954cd41fa0cbca`

```dockerfile
```

-	Layers:
	-	`sha256:8b35ce6b0edc95ead634e438ed902c32e5aa00e1075526844f2def7d6832b732`  
		Last Modified: Tue, 12 Nov 2024 02:04:05 GMT  
		Size: 463.8 KB (463819 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b99f0be5a6b1b2308800feeeff4d2e86bd588c6e7cf17661d56cd4191a118368`  
		Last Modified: Tue, 12 Nov 2024 02:04:05 GMT  
		Size: 14.5 KB (14491 bytes)  
		MIME: application/vnd.in-toto+json

## `arangodb:3.12.3`

```console
$ docker pull arangodb@sha256:bab5f96a0cd667f3cd2ef6eb2f058bce89a94c1f9e86b7dec864254a55f52ad3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `arangodb:3.12.3` - linux; amd64

```console
$ docker pull arangodb@sha256:98dee3ef63853826c6b162b189ad9bc0cbd28736b8f86449949e7309553fa259
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.6 MB (304636261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61cbf573466c897f98267dae7f24e353b7a4e675fe66d5a53f80df2da2628908`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 06 Sep 2024 12:02:06 GMT
ADD alpine-minirootfs-3.17.10-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:02:06 GMT
CMD ["/bin/sh"]
# Wed, 30 Oct 2024 15:12:33 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Wed, 30 Oct 2024 15:12:33 GMT
ENV ARANGO_VERSION=3.12.3
# Wed, 30 Oct 2024 15:12:33 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8003EDF6F05459984878D4A6C04AD0FD86FEC04D &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb312/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg # buildkit
# Wed, 30 Oct 2024 15:12:33 GMT
ENV GLIBCXX_FORCE_NEW=1
# Wed, 30 Oct 2024 15:12:33 GMT
RUN echo "UTC" > /etc/timezone # buildkit
# Wed, 30 Oct 2024 15:12:33 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Wed, 30 Oct 2024 15:12:33 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 30 Oct 2024 15:12:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 30 Oct 2024 15:12:33 GMT
EXPOSE map[8529/tcp:{}]
# Wed, 30 Oct 2024 15:12:33 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:fbcfea79c1c4819e0689385057cfd4cbd2ee9ba20e6d420b360644788a22862c`  
		Last Modified: Mon, 09 Sep 2024 07:01:59 GMT  
		Size: 3.4 MB (3392252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b84a29e021b6aaeabf075ce866c32091fd8ef712fab99f9fda373a5ea636b9f6`  
		Last Modified: Tue, 12 Nov 2024 02:02:16 GMT  
		Size: 301.2 MB (301241853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c5ab759f98983a52ff63397651f5a3fae8b1a3df12ddf541a8c33c6ff136a0f`  
		Last Modified: Tue, 12 Nov 2024 02:02:06 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47eda9f35c5db5a20cdc21a94c2c33f7476801a78dd4cc5838f84a33d32a6644`  
		Last Modified: Tue, 12 Nov 2024 02:02:06 GMT  
		Size: 2.0 KB (2016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:3.12.3` - unknown; unknown

```console
$ docker pull arangodb@sha256:845c9dfee6094aea497c014869c699e3a9987cee93586de26ce0e18cfe342c9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **372.9 KB (372905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c110e5dc85c76c5fb3bde7d10a499557d4c419e5880b9dfbd97685fe0231b03`

```dockerfile
```

-	Layers:
	-	`sha256:e1d5a7fef24fc5803d50e90ffd05076e6e2c31dc2adee6bff6a50b27c245b7cf`  
		Last Modified: Tue, 12 Nov 2024 02:02:06 GMT  
		Size: 358.5 KB (358520 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51e15f395bd212b71c9bfa97c3fe80c1ef8a28d2c92b213aee3206a6536ba9fd`  
		Last Modified: Tue, 12 Nov 2024 02:02:06 GMT  
		Size: 14.4 KB (14385 bytes)  
		MIME: application/vnd.in-toto+json

### `arangodb:3.12.3` - linux; arm64 variant v8

```console
$ docker pull arangodb@sha256:5c5a9c26a373492d81244bd0e6c932631b332ac4ef86d4a5efe8c77cd6eb1d33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.5 MB (306524920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19aee834bf6ab375f9410ab8b6826994a9c9d150925ea1ac6e62b45173185ab5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 06 Sep 2024 12:02:06 GMT
ADD alpine-minirootfs-3.17.10-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:02:06 GMT
CMD ["/bin/sh"]
# Wed, 30 Oct 2024 15:12:33 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Wed, 30 Oct 2024 15:12:33 GMT
ENV ARANGO_VERSION=3.12.3
# Wed, 30 Oct 2024 15:12:33 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8003EDF6F05459984878D4A6C04AD0FD86FEC04D &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb312/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg # buildkit
# Wed, 30 Oct 2024 15:12:33 GMT
ENV GLIBCXX_FORCE_NEW=1
# Wed, 30 Oct 2024 15:12:33 GMT
RUN echo "UTC" > /etc/timezone # buildkit
# Wed, 30 Oct 2024 15:12:33 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Wed, 30 Oct 2024 15:12:33 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 30 Oct 2024 15:12:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 30 Oct 2024 15:12:33 GMT
EXPOSE map[8529/tcp:{}]
# Wed, 30 Oct 2024 15:12:33 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:61254a502902280aa7caa832f8b3ed5c96aa04faf42ab0ba23ff17638f910f21`  
		Last Modified: Mon, 09 Sep 2024 07:02:02 GMT  
		Size: 3.3 MB (3275161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9e8e9682cd434a2ff1f05b8704c94bc802b2a4676dab3d5b6f19874bf55a864`  
		Last Modified: Tue, 12 Nov 2024 02:04:12 GMT  
		Size: 303.2 MB (303247603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03f16d88fc0fd758c5db76f41930152f7a237f0963dc0697c99e75dd10f8dae8`  
		Last Modified: Tue, 12 Nov 2024 02:04:05 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6ad0d0cfd87b12f0d4f8e2e8ae21d794ab6c36e018bc84d180091112073d86b`  
		Last Modified: Tue, 12 Nov 2024 02:04:05 GMT  
		Size: 2.0 KB (2016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:3.12.3` - unknown; unknown

```console
$ docker pull arangodb@sha256:93368a07c6f35753b2f185178c69fe2602bbf6663edebe4f6bb8e5bd475b282f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **478.3 KB (478310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f94ce7f3dcfbf25e6cff5bcd99dd68702ba49c5ec0fef96d01954cd41fa0cbca`

```dockerfile
```

-	Layers:
	-	`sha256:8b35ce6b0edc95ead634e438ed902c32e5aa00e1075526844f2def7d6832b732`  
		Last Modified: Tue, 12 Nov 2024 02:04:05 GMT  
		Size: 463.8 KB (463819 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b99f0be5a6b1b2308800feeeff4d2e86bd588c6e7cf17661d56cd4191a118368`  
		Last Modified: Tue, 12 Nov 2024 02:04:05 GMT  
		Size: 14.5 KB (14491 bytes)  
		MIME: application/vnd.in-toto+json

## `arangodb:latest`

```console
$ docker pull arangodb@sha256:bab5f96a0cd667f3cd2ef6eb2f058bce89a94c1f9e86b7dec864254a55f52ad3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `arangodb:latest` - linux; amd64

```console
$ docker pull arangodb@sha256:98dee3ef63853826c6b162b189ad9bc0cbd28736b8f86449949e7309553fa259
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.6 MB (304636261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61cbf573466c897f98267dae7f24e353b7a4e675fe66d5a53f80df2da2628908`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 06 Sep 2024 12:02:06 GMT
ADD alpine-minirootfs-3.17.10-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:02:06 GMT
CMD ["/bin/sh"]
# Wed, 30 Oct 2024 15:12:33 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Wed, 30 Oct 2024 15:12:33 GMT
ENV ARANGO_VERSION=3.12.3
# Wed, 30 Oct 2024 15:12:33 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8003EDF6F05459984878D4A6C04AD0FD86FEC04D &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb312/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg # buildkit
# Wed, 30 Oct 2024 15:12:33 GMT
ENV GLIBCXX_FORCE_NEW=1
# Wed, 30 Oct 2024 15:12:33 GMT
RUN echo "UTC" > /etc/timezone # buildkit
# Wed, 30 Oct 2024 15:12:33 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Wed, 30 Oct 2024 15:12:33 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 30 Oct 2024 15:12:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 30 Oct 2024 15:12:33 GMT
EXPOSE map[8529/tcp:{}]
# Wed, 30 Oct 2024 15:12:33 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:fbcfea79c1c4819e0689385057cfd4cbd2ee9ba20e6d420b360644788a22862c`  
		Last Modified: Mon, 09 Sep 2024 07:01:59 GMT  
		Size: 3.4 MB (3392252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b84a29e021b6aaeabf075ce866c32091fd8ef712fab99f9fda373a5ea636b9f6`  
		Last Modified: Tue, 12 Nov 2024 02:02:16 GMT  
		Size: 301.2 MB (301241853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c5ab759f98983a52ff63397651f5a3fae8b1a3df12ddf541a8c33c6ff136a0f`  
		Last Modified: Tue, 12 Nov 2024 02:02:06 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47eda9f35c5db5a20cdc21a94c2c33f7476801a78dd4cc5838f84a33d32a6644`  
		Last Modified: Tue, 12 Nov 2024 02:02:06 GMT  
		Size: 2.0 KB (2016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:latest` - unknown; unknown

```console
$ docker pull arangodb@sha256:845c9dfee6094aea497c014869c699e3a9987cee93586de26ce0e18cfe342c9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **372.9 KB (372905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c110e5dc85c76c5fb3bde7d10a499557d4c419e5880b9dfbd97685fe0231b03`

```dockerfile
```

-	Layers:
	-	`sha256:e1d5a7fef24fc5803d50e90ffd05076e6e2c31dc2adee6bff6a50b27c245b7cf`  
		Last Modified: Tue, 12 Nov 2024 02:02:06 GMT  
		Size: 358.5 KB (358520 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51e15f395bd212b71c9bfa97c3fe80c1ef8a28d2c92b213aee3206a6536ba9fd`  
		Last Modified: Tue, 12 Nov 2024 02:02:06 GMT  
		Size: 14.4 KB (14385 bytes)  
		MIME: application/vnd.in-toto+json

### `arangodb:latest` - linux; arm64 variant v8

```console
$ docker pull arangodb@sha256:5c5a9c26a373492d81244bd0e6c932631b332ac4ef86d4a5efe8c77cd6eb1d33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.5 MB (306524920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19aee834bf6ab375f9410ab8b6826994a9c9d150925ea1ac6e62b45173185ab5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 06 Sep 2024 12:02:06 GMT
ADD alpine-minirootfs-3.17.10-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:02:06 GMT
CMD ["/bin/sh"]
# Wed, 30 Oct 2024 15:12:33 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Wed, 30 Oct 2024 15:12:33 GMT
ENV ARANGO_VERSION=3.12.3
# Wed, 30 Oct 2024 15:12:33 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8003EDF6F05459984878D4A6C04AD0FD86FEC04D &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb312/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg # buildkit
# Wed, 30 Oct 2024 15:12:33 GMT
ENV GLIBCXX_FORCE_NEW=1
# Wed, 30 Oct 2024 15:12:33 GMT
RUN echo "UTC" > /etc/timezone # buildkit
# Wed, 30 Oct 2024 15:12:33 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Wed, 30 Oct 2024 15:12:33 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 30 Oct 2024 15:12:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 30 Oct 2024 15:12:33 GMT
EXPOSE map[8529/tcp:{}]
# Wed, 30 Oct 2024 15:12:33 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:61254a502902280aa7caa832f8b3ed5c96aa04faf42ab0ba23ff17638f910f21`  
		Last Modified: Mon, 09 Sep 2024 07:02:02 GMT  
		Size: 3.3 MB (3275161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9e8e9682cd434a2ff1f05b8704c94bc802b2a4676dab3d5b6f19874bf55a864`  
		Last Modified: Tue, 12 Nov 2024 02:04:12 GMT  
		Size: 303.2 MB (303247603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03f16d88fc0fd758c5db76f41930152f7a237f0963dc0697c99e75dd10f8dae8`  
		Last Modified: Tue, 12 Nov 2024 02:04:05 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6ad0d0cfd87b12f0d4f8e2e8ae21d794ab6c36e018bc84d180091112073d86b`  
		Last Modified: Tue, 12 Nov 2024 02:04:05 GMT  
		Size: 2.0 KB (2016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:latest` - unknown; unknown

```console
$ docker pull arangodb@sha256:93368a07c6f35753b2f185178c69fe2602bbf6663edebe4f6bb8e5bd475b282f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **478.3 KB (478310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f94ce7f3dcfbf25e6cff5bcd99dd68702ba49c5ec0fef96d01954cd41fa0cbca`

```dockerfile
```

-	Layers:
	-	`sha256:8b35ce6b0edc95ead634e438ed902c32e5aa00e1075526844f2def7d6832b732`  
		Last Modified: Tue, 12 Nov 2024 02:04:05 GMT  
		Size: 463.8 KB (463819 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b99f0be5a6b1b2308800feeeff4d2e86bd588c6e7cf17661d56cd4191a118368`  
		Last Modified: Tue, 12 Nov 2024 02:04:05 GMT  
		Size: 14.5 KB (14491 bytes)  
		MIME: application/vnd.in-toto+json
