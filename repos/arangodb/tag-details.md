<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `arangodb`

-	[`arangodb:3.12`](#arangodb312)
-	[`arangodb:3.12.5.2`](#arangodb31252)
-	[`arangodb:latest`](#arangodblatest)

## `arangodb:3.12`

```console
$ docker pull arangodb@sha256:06a97bdc51a98f714634d620ea46e9a02c5daf3925342f6332af2e598c9ae7aa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `arangodb:3.12` - linux; amd64

```console
$ docker pull arangodb@sha256:09dda000c512e102c4e5d397194e714a31e884135e9f47ab0bc2ceacc6d63a49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.4 MB (258370716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4f094201e1027d397f737394d2182fedd26a848b6b95a340dc954fddae1922d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Mon, 04 Aug 2025 21:34:13 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Mon, 04 Aug 2025 21:34:13 GMT
ENV ARANGO_VERSION=3.12.5.2
# Mon, 04 Aug 2025 21:34:13 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8003EDF6F05459984878D4A6C04AD0FD86FEC04D &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/9c169fe900ff79790395784287bfa82f0dc0059375a34a2881b9b745c8efd42e/arangodb312/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3e_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg # buildkit
# Mon, 04 Aug 2025 21:34:13 GMT
ENV GLIBCXX_FORCE_NEW=1
# Mon, 04 Aug 2025 21:34:13 GMT
RUN echo "UTC" > /etc/timezone # buildkit
# Mon, 04 Aug 2025 21:34:13 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Mon, 04 Aug 2025 21:34:13 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 04 Aug 2025 21:34:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 04 Aug 2025 21:34:13 GMT
EXPOSE map[8529/tcp:{}]
# Mon, 04 Aug 2025 21:34:13 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:0368fd46e3c6d237d81390ff086f93aee216df5cfa814041a491453fb0932a12`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3637570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a245da2ceafe74f3750cdecde280ecc0c18581d559f122b813056722793e025b`  
		Last Modified: Tue, 05 Aug 2025 00:13:56 GMT  
		Size: 254.7 MB (254730994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:148fb316f6887150b44cfd0e0793af9b5d03b52c2fb62951d9b2ff487b5d9a56`  
		Last Modified: Mon, 04 Aug 2025 22:02:20 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df7c0a937d34f347166d9a0507c9775b7c79baf2c8929e8fe2c79883135025eb`  
		Last Modified: Mon, 04 Aug 2025 22:02:20 GMT  
		Size: 2.0 KB (2012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:3.12` - unknown; unknown

```console
$ docker pull arangodb@sha256:c8ed776540b1ae69d00b5a3028009a64bb44cbdb9e97fafce335d92c0f264b39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **527.4 KB (527361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de981c65fab33ef56b262afd7237db219178c139102d9f13e57b130ac1af8bd2`

```dockerfile
```

-	Layers:
	-	`sha256:55a3de47287c8ad3e87843c8514a21ebdf9e40497626ddde76e57aa3c8e29649`  
		Last Modified: Tue, 05 Aug 2025 00:13:16 GMT  
		Size: 512.8 KB (512804 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab8d11d49ee956463ffde3d06e883d19d0e3b3bc552243e20f2276c05e80a65a`  
		Last Modified: Tue, 05 Aug 2025 00:13:17 GMT  
		Size: 14.6 KB (14557 bytes)  
		MIME: application/vnd.in-toto+json

### `arangodb:3.12` - linux; arm64 variant v8

```console
$ docker pull arangodb@sha256:c0109cc6d5322cb02dc2519e5c371e65671d699d67084b056b0b10b2faf827c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.4 MB (257408697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c428de49ea52a71057170af66beb19217f63bdb9aba93ef1c3d40304e31eb397`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Mon, 04 Aug 2025 21:34:13 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Mon, 04 Aug 2025 21:34:13 GMT
ENV ARANGO_VERSION=3.12.5.2
# Mon, 04 Aug 2025 21:34:13 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8003EDF6F05459984878D4A6C04AD0FD86FEC04D &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/9c169fe900ff79790395784287bfa82f0dc0059375a34a2881b9b745c8efd42e/arangodb312/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3e_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg # buildkit
# Mon, 04 Aug 2025 21:34:13 GMT
ENV GLIBCXX_FORCE_NEW=1
# Mon, 04 Aug 2025 21:34:13 GMT
RUN echo "UTC" > /etc/timezone # buildkit
# Mon, 04 Aug 2025 21:34:13 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Mon, 04 Aug 2025 21:34:13 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 04 Aug 2025 21:34:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 04 Aug 2025 21:34:13 GMT
EXPOSE map[8529/tcp:{}]
# Mon, 04 Aug 2025 21:34:13 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:d06c6b665c9b4c183a2e300b290a6b4b7db03f803122fe93d91e9178f425e488`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 4.0 MB (3986937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1538c54af64609a3fa8cac621a809bb0671f34457f7d416bce87608d1ec366a9`  
		Last Modified: Tue, 05 Aug 2025 05:57:12 GMT  
		Size: 253.4 MB (253419605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1048648318bb81986eca787865cb6a96a3514e856dae2b97ea0ae7652cd54e7`  
		Last Modified: Tue, 05 Aug 2025 00:13:22 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6885a573bb6187aa0d73e7fd6847a885d741a4b57df407d09cc64d51c43ede74`  
		Last Modified: Tue, 05 Aug 2025 00:13:25 GMT  
		Size: 2.0 KB (2015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:3.12` - unknown; unknown

```console
$ docker pull arangodb@sha256:d95a16f544e75aa5fe94a2b3d39859c0848d9272d3e55d46a806f9eb19273d9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **678.1 KB (678088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbfb9b729b5940163dddc770457b3b901550ab41fa83d1d65be617ed3eb062c2`

```dockerfile
```

-	Layers:
	-	`sha256:5f4d05669eaaeb7f8766ffd49601c0d343f5374d467572942242c112ad83429a`  
		Last Modified: Tue, 05 Aug 2025 03:13:21 GMT  
		Size: 663.4 KB (663424 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:860d4beadede2af6a6234a848a6720c6c1c4e869c57ae281994b423b193534e0`  
		Last Modified: Tue, 05 Aug 2025 03:13:22 GMT  
		Size: 14.7 KB (14664 bytes)  
		MIME: application/vnd.in-toto+json

## `arangodb:3.12.5.2`

```console
$ docker pull arangodb@sha256:06a97bdc51a98f714634d620ea46e9a02c5daf3925342f6332af2e598c9ae7aa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `arangodb:3.12.5.2` - linux; amd64

```console
$ docker pull arangodb@sha256:09dda000c512e102c4e5d397194e714a31e884135e9f47ab0bc2ceacc6d63a49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.4 MB (258370716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4f094201e1027d397f737394d2182fedd26a848b6b95a340dc954fddae1922d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Mon, 04 Aug 2025 21:34:13 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Mon, 04 Aug 2025 21:34:13 GMT
ENV ARANGO_VERSION=3.12.5.2
# Mon, 04 Aug 2025 21:34:13 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8003EDF6F05459984878D4A6C04AD0FD86FEC04D &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/9c169fe900ff79790395784287bfa82f0dc0059375a34a2881b9b745c8efd42e/arangodb312/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3e_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg # buildkit
# Mon, 04 Aug 2025 21:34:13 GMT
ENV GLIBCXX_FORCE_NEW=1
# Mon, 04 Aug 2025 21:34:13 GMT
RUN echo "UTC" > /etc/timezone # buildkit
# Mon, 04 Aug 2025 21:34:13 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Mon, 04 Aug 2025 21:34:13 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 04 Aug 2025 21:34:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 04 Aug 2025 21:34:13 GMT
EXPOSE map[8529/tcp:{}]
# Mon, 04 Aug 2025 21:34:13 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:0368fd46e3c6d237d81390ff086f93aee216df5cfa814041a491453fb0932a12`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3637570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a245da2ceafe74f3750cdecde280ecc0c18581d559f122b813056722793e025b`  
		Last Modified: Tue, 05 Aug 2025 00:13:56 GMT  
		Size: 254.7 MB (254730994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:148fb316f6887150b44cfd0e0793af9b5d03b52c2fb62951d9b2ff487b5d9a56`  
		Last Modified: Mon, 04 Aug 2025 22:02:20 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df7c0a937d34f347166d9a0507c9775b7c79baf2c8929e8fe2c79883135025eb`  
		Last Modified: Mon, 04 Aug 2025 22:02:20 GMT  
		Size: 2.0 KB (2012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:3.12.5.2` - unknown; unknown

```console
$ docker pull arangodb@sha256:c8ed776540b1ae69d00b5a3028009a64bb44cbdb9e97fafce335d92c0f264b39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **527.4 KB (527361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de981c65fab33ef56b262afd7237db219178c139102d9f13e57b130ac1af8bd2`

```dockerfile
```

-	Layers:
	-	`sha256:55a3de47287c8ad3e87843c8514a21ebdf9e40497626ddde76e57aa3c8e29649`  
		Last Modified: Tue, 05 Aug 2025 00:13:16 GMT  
		Size: 512.8 KB (512804 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab8d11d49ee956463ffde3d06e883d19d0e3b3bc552243e20f2276c05e80a65a`  
		Last Modified: Tue, 05 Aug 2025 00:13:17 GMT  
		Size: 14.6 KB (14557 bytes)  
		MIME: application/vnd.in-toto+json

### `arangodb:3.12.5.2` - linux; arm64 variant v8

```console
$ docker pull arangodb@sha256:c0109cc6d5322cb02dc2519e5c371e65671d699d67084b056b0b10b2faf827c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.4 MB (257408697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c428de49ea52a71057170af66beb19217f63bdb9aba93ef1c3d40304e31eb397`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Mon, 04 Aug 2025 21:34:13 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Mon, 04 Aug 2025 21:34:13 GMT
ENV ARANGO_VERSION=3.12.5.2
# Mon, 04 Aug 2025 21:34:13 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8003EDF6F05459984878D4A6C04AD0FD86FEC04D &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/9c169fe900ff79790395784287bfa82f0dc0059375a34a2881b9b745c8efd42e/arangodb312/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3e_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg # buildkit
# Mon, 04 Aug 2025 21:34:13 GMT
ENV GLIBCXX_FORCE_NEW=1
# Mon, 04 Aug 2025 21:34:13 GMT
RUN echo "UTC" > /etc/timezone # buildkit
# Mon, 04 Aug 2025 21:34:13 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Mon, 04 Aug 2025 21:34:13 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 04 Aug 2025 21:34:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 04 Aug 2025 21:34:13 GMT
EXPOSE map[8529/tcp:{}]
# Mon, 04 Aug 2025 21:34:13 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:d06c6b665c9b4c183a2e300b290a6b4b7db03f803122fe93d91e9178f425e488`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 4.0 MB (3986937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1538c54af64609a3fa8cac621a809bb0671f34457f7d416bce87608d1ec366a9`  
		Last Modified: Tue, 05 Aug 2025 05:57:12 GMT  
		Size: 253.4 MB (253419605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1048648318bb81986eca787865cb6a96a3514e856dae2b97ea0ae7652cd54e7`  
		Last Modified: Tue, 05 Aug 2025 00:13:22 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6885a573bb6187aa0d73e7fd6847a885d741a4b57df407d09cc64d51c43ede74`  
		Last Modified: Tue, 05 Aug 2025 00:13:25 GMT  
		Size: 2.0 KB (2015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:3.12.5.2` - unknown; unknown

```console
$ docker pull arangodb@sha256:d95a16f544e75aa5fe94a2b3d39859c0848d9272d3e55d46a806f9eb19273d9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **678.1 KB (678088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbfb9b729b5940163dddc770457b3b901550ab41fa83d1d65be617ed3eb062c2`

```dockerfile
```

-	Layers:
	-	`sha256:5f4d05669eaaeb7f8766ffd49601c0d343f5374d467572942242c112ad83429a`  
		Last Modified: Tue, 05 Aug 2025 03:13:21 GMT  
		Size: 663.4 KB (663424 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:860d4beadede2af6a6234a848a6720c6c1c4e869c57ae281994b423b193534e0`  
		Last Modified: Tue, 05 Aug 2025 03:13:22 GMT  
		Size: 14.7 KB (14664 bytes)  
		MIME: application/vnd.in-toto+json

## `arangodb:latest`

```console
$ docker pull arangodb@sha256:06a97bdc51a98f714634d620ea46e9a02c5daf3925342f6332af2e598c9ae7aa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `arangodb:latest` - linux; amd64

```console
$ docker pull arangodb@sha256:09dda000c512e102c4e5d397194e714a31e884135e9f47ab0bc2ceacc6d63a49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.4 MB (258370716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4f094201e1027d397f737394d2182fedd26a848b6b95a340dc954fddae1922d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Mon, 04 Aug 2025 21:34:13 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Mon, 04 Aug 2025 21:34:13 GMT
ENV ARANGO_VERSION=3.12.5.2
# Mon, 04 Aug 2025 21:34:13 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8003EDF6F05459984878D4A6C04AD0FD86FEC04D &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/9c169fe900ff79790395784287bfa82f0dc0059375a34a2881b9b745c8efd42e/arangodb312/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3e_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg # buildkit
# Mon, 04 Aug 2025 21:34:13 GMT
ENV GLIBCXX_FORCE_NEW=1
# Mon, 04 Aug 2025 21:34:13 GMT
RUN echo "UTC" > /etc/timezone # buildkit
# Mon, 04 Aug 2025 21:34:13 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Mon, 04 Aug 2025 21:34:13 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 04 Aug 2025 21:34:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 04 Aug 2025 21:34:13 GMT
EXPOSE map[8529/tcp:{}]
# Mon, 04 Aug 2025 21:34:13 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:0368fd46e3c6d237d81390ff086f93aee216df5cfa814041a491453fb0932a12`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3637570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a245da2ceafe74f3750cdecde280ecc0c18581d559f122b813056722793e025b`  
		Last Modified: Tue, 05 Aug 2025 00:13:56 GMT  
		Size: 254.7 MB (254730994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:148fb316f6887150b44cfd0e0793af9b5d03b52c2fb62951d9b2ff487b5d9a56`  
		Last Modified: Mon, 04 Aug 2025 22:02:20 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df7c0a937d34f347166d9a0507c9775b7c79baf2c8929e8fe2c79883135025eb`  
		Last Modified: Mon, 04 Aug 2025 22:02:20 GMT  
		Size: 2.0 KB (2012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:latest` - unknown; unknown

```console
$ docker pull arangodb@sha256:c8ed776540b1ae69d00b5a3028009a64bb44cbdb9e97fafce335d92c0f264b39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **527.4 KB (527361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de981c65fab33ef56b262afd7237db219178c139102d9f13e57b130ac1af8bd2`

```dockerfile
```

-	Layers:
	-	`sha256:55a3de47287c8ad3e87843c8514a21ebdf9e40497626ddde76e57aa3c8e29649`  
		Last Modified: Tue, 05 Aug 2025 00:13:16 GMT  
		Size: 512.8 KB (512804 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab8d11d49ee956463ffde3d06e883d19d0e3b3bc552243e20f2276c05e80a65a`  
		Last Modified: Tue, 05 Aug 2025 00:13:17 GMT  
		Size: 14.6 KB (14557 bytes)  
		MIME: application/vnd.in-toto+json

### `arangodb:latest` - linux; arm64 variant v8

```console
$ docker pull arangodb@sha256:c0109cc6d5322cb02dc2519e5c371e65671d699d67084b056b0b10b2faf827c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.4 MB (257408697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c428de49ea52a71057170af66beb19217f63bdb9aba93ef1c3d40304e31eb397`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Mon, 04 Aug 2025 21:34:13 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Mon, 04 Aug 2025 21:34:13 GMT
ENV ARANGO_VERSION=3.12.5.2
# Mon, 04 Aug 2025 21:34:13 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8003EDF6F05459984878D4A6C04AD0FD86FEC04D &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/9c169fe900ff79790395784287bfa82f0dc0059375a34a2881b9b745c8efd42e/arangodb312/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3e_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg # buildkit
# Mon, 04 Aug 2025 21:34:13 GMT
ENV GLIBCXX_FORCE_NEW=1
# Mon, 04 Aug 2025 21:34:13 GMT
RUN echo "UTC" > /etc/timezone # buildkit
# Mon, 04 Aug 2025 21:34:13 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Mon, 04 Aug 2025 21:34:13 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 04 Aug 2025 21:34:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 04 Aug 2025 21:34:13 GMT
EXPOSE map[8529/tcp:{}]
# Mon, 04 Aug 2025 21:34:13 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:d06c6b665c9b4c183a2e300b290a6b4b7db03f803122fe93d91e9178f425e488`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 4.0 MB (3986937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1538c54af64609a3fa8cac621a809bb0671f34457f7d416bce87608d1ec366a9`  
		Last Modified: Tue, 05 Aug 2025 05:57:12 GMT  
		Size: 253.4 MB (253419605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1048648318bb81986eca787865cb6a96a3514e856dae2b97ea0ae7652cd54e7`  
		Last Modified: Tue, 05 Aug 2025 00:13:22 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6885a573bb6187aa0d73e7fd6847a885d741a4b57df407d09cc64d51c43ede74`  
		Last Modified: Tue, 05 Aug 2025 00:13:25 GMT  
		Size: 2.0 KB (2015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:latest` - unknown; unknown

```console
$ docker pull arangodb@sha256:d95a16f544e75aa5fe94a2b3d39859c0848d9272d3e55d46a806f9eb19273d9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **678.1 KB (678088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbfb9b729b5940163dddc770457b3b901550ab41fa83d1d65be617ed3eb062c2`

```dockerfile
```

-	Layers:
	-	`sha256:5f4d05669eaaeb7f8766ffd49601c0d343f5374d467572942242c112ad83429a`  
		Last Modified: Tue, 05 Aug 2025 03:13:21 GMT  
		Size: 663.4 KB (663424 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:860d4beadede2af6a6234a848a6720c6c1c4e869c57ae281994b423b193534e0`  
		Last Modified: Tue, 05 Aug 2025 03:13:22 GMT  
		Size: 14.7 KB (14664 bytes)  
		MIME: application/vnd.in-toto+json
