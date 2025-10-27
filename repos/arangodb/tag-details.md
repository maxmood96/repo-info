<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `arangodb`

-	[`arangodb:3.12`](#arangodb312)
-	[`arangodb:3.12.6`](#arangodb3126)
-	[`arangodb:latest`](#arangodblatest)

## `arangodb:3.12`

```console
$ docker pull arangodb@sha256:e46594fbf0130c1f8f559e2f02d8fc7454bd60257c3a07f10a036f51c150d609
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `arangodb:3.12` - linux; amd64

```console
$ docker pull arangodb@sha256:a504624887956ca3d21f5ff7883d03aa8429ffb49c839a88c0583c2df923fe62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.8 MB (259765606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13019531f970eba464dec9bcf0c59baf32fd6dcf181cf324839a9550cd1079f3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Mon, 27 Oct 2025 10:42:22 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Mon, 27 Oct 2025 10:42:22 GMT
ENV ARANGO_VERSION=3.12.6
# Mon, 27 Oct 2025 10:42:22 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8003EDF6F05459984878D4A6C04AD0FD86FEC04D &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/9c169fe900ff79790395784287bfa82f0dc0059375a34a2881b9b745c8efd42e/arangodb312/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3e_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg # buildkit
# Mon, 27 Oct 2025 10:42:22 GMT
ENV GLIBCXX_FORCE_NEW=1
# Mon, 27 Oct 2025 10:42:22 GMT
RUN echo "UTC" > /etc/timezone # buildkit
# Mon, 27 Oct 2025 10:42:22 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Mon, 27 Oct 2025 10:42:22 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 27 Oct 2025 10:42:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 27 Oct 2025 10:42:22 GMT
EXPOSE map[8529/tcp:{}]
# Mon, 27 Oct 2025 10:42:22 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:f637881d1138581d892d9eb942c56e0ccc7758fe3bdc0f1e6cd66059fdfd8185`  
		Last Modified: Wed, 08 Oct 2025 12:54:09 GMT  
		Size: 3.6 MB (3642569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:140ab0b91e813fcf0ca9d9f9a509085267bf157e8c9cb2eaf00ae89297972746`  
		Last Modified: Mon, 27 Oct 2025 21:15:01 GMT  
		Size: 256.1 MB (256120883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81b327c14195d4435bd7b56816ccbb554a8896368c4e9de99ea37f0e6672fc73`  
		Last Modified: Mon, 27 Oct 2025 20:11:44 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cbd54f3dcb50e615f3c4474b8f269b8e0824a0b2e83dfb7c93a384e9f67c350`  
		Last Modified: Mon, 27 Oct 2025 20:11:44 GMT  
		Size: 2.0 KB (2014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:3.12` - unknown; unknown

```console
$ docker pull arangodb@sha256:3826abea713dd0aa2192cfa43b1ce0201e92a39410f250e80a1be8334aef727e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **527.3 KB (527339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a13615834f4da78f79c7db324cff767c2b1034d0ce9b753d37e8ee587feadb9`

```dockerfile
```

-	Layers:
	-	`sha256:e758ebd8c78788e1c12c7d467f76bbd99ee6f425d3811c19b36698ca38cb0e7a`  
		Last Modified: Mon, 27 Oct 2025 21:13:24 GMT  
		Size: 512.8 KB (512800 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f142224b73fd851ee2d5b6224d4a56b06b62046891515ad3f162a0249c993e26`  
		Last Modified: Mon, 27 Oct 2025 21:13:25 GMT  
		Size: 14.5 KB (14539 bytes)  
		MIME: application/vnd.in-toto+json

### `arangodb:3.12` - linux; arm64 variant v8

```console
$ docker pull arangodb@sha256:d86f485190d6478ca4469ca3efcb793f6443ac9936120fd0fda5f7efa91c97c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.9 MB (258870074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8107db04cebd5198a29ffd88693b1bfdbea55ceb0f6ec7dad65a48f719f99ec1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Mon, 27 Oct 2025 10:42:22 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Mon, 27 Oct 2025 10:42:22 GMT
ENV ARANGO_VERSION=3.12.6
# Mon, 27 Oct 2025 10:42:22 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8003EDF6F05459984878D4A6C04AD0FD86FEC04D &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/9c169fe900ff79790395784287bfa82f0dc0059375a34a2881b9b745c8efd42e/arangodb312/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3e_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg # buildkit
# Mon, 27 Oct 2025 10:42:22 GMT
ENV GLIBCXX_FORCE_NEW=1
# Mon, 27 Oct 2025 10:42:22 GMT
RUN echo "UTC" > /etc/timezone # buildkit
# Mon, 27 Oct 2025 10:42:22 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Mon, 27 Oct 2025 10:42:22 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 27 Oct 2025 10:42:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 27 Oct 2025 10:42:22 GMT
EXPOSE map[8529/tcp:{}]
# Mon, 27 Oct 2025 10:42:22 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:c2fe130f4aabc917e559e7eed7d37b0e21ba13b44520101696887ca892e8c63f`  
		Last Modified: Wed, 08 Oct 2025 16:24:46 GMT  
		Size: 4.0 MB (3992353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f31a952756cc363de0bce314cf0ed1e137e589eb00baa07f312a2222314c49b`  
		Last Modified: Mon, 27 Oct 2025 18:19:35 GMT  
		Size: 254.9 MB (254875565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea1651cf8ffb39ff3421e10dc91accfe70c853f8b39d1d0abb08726d6bbdca28`  
		Last Modified: Mon, 27 Oct 2025 17:20:19 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f335a6e8083a2e24834e1787130cf2feb2c24b1143fbd5afec28d7983c522f7b`  
		Last Modified: Mon, 27 Oct 2025 17:20:19 GMT  
		Size: 2.0 KB (2016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:3.12` - unknown; unknown

```console
$ docker pull arangodb@sha256:486d2dc263e68d1dbef621a73a576e88789e9861b0761298cebb8c84b253433f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **678.1 KB (678066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9962330844492810a7d194e6226680b377142c39a99681c8664eb602cc3052c7`

```dockerfile
```

-	Layers:
	-	`sha256:bcd2086cc7caa59c09464ea481ad05467a6514863960ec1d24f0543df3385d2f`  
		Last Modified: Mon, 27 Oct 2025 18:13:19 GMT  
		Size: 663.4 KB (663420 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d847dd755ffefa6792982722db1ff7241f33725cb2b09e27ac246d5532f5c132`  
		Last Modified: Mon, 27 Oct 2025 18:13:20 GMT  
		Size: 14.6 KB (14646 bytes)  
		MIME: application/vnd.in-toto+json

## `arangodb:3.12.6`

```console
$ docker pull arangodb@sha256:e46594fbf0130c1f8f559e2f02d8fc7454bd60257c3a07f10a036f51c150d609
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `arangodb:3.12.6` - linux; amd64

```console
$ docker pull arangodb@sha256:a504624887956ca3d21f5ff7883d03aa8429ffb49c839a88c0583c2df923fe62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.8 MB (259765606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13019531f970eba464dec9bcf0c59baf32fd6dcf181cf324839a9550cd1079f3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Mon, 27 Oct 2025 10:42:22 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Mon, 27 Oct 2025 10:42:22 GMT
ENV ARANGO_VERSION=3.12.6
# Mon, 27 Oct 2025 10:42:22 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8003EDF6F05459984878D4A6C04AD0FD86FEC04D &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/9c169fe900ff79790395784287bfa82f0dc0059375a34a2881b9b745c8efd42e/arangodb312/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3e_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg # buildkit
# Mon, 27 Oct 2025 10:42:22 GMT
ENV GLIBCXX_FORCE_NEW=1
# Mon, 27 Oct 2025 10:42:22 GMT
RUN echo "UTC" > /etc/timezone # buildkit
# Mon, 27 Oct 2025 10:42:22 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Mon, 27 Oct 2025 10:42:22 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 27 Oct 2025 10:42:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 27 Oct 2025 10:42:22 GMT
EXPOSE map[8529/tcp:{}]
# Mon, 27 Oct 2025 10:42:22 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:f637881d1138581d892d9eb942c56e0ccc7758fe3bdc0f1e6cd66059fdfd8185`  
		Last Modified: Wed, 08 Oct 2025 12:54:09 GMT  
		Size: 3.6 MB (3642569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:140ab0b91e813fcf0ca9d9f9a509085267bf157e8c9cb2eaf00ae89297972746`  
		Last Modified: Mon, 27 Oct 2025 21:15:01 GMT  
		Size: 256.1 MB (256120883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81b327c14195d4435bd7b56816ccbb554a8896368c4e9de99ea37f0e6672fc73`  
		Last Modified: Mon, 27 Oct 2025 20:11:44 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cbd54f3dcb50e615f3c4474b8f269b8e0824a0b2e83dfb7c93a384e9f67c350`  
		Last Modified: Mon, 27 Oct 2025 20:11:44 GMT  
		Size: 2.0 KB (2014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:3.12.6` - unknown; unknown

```console
$ docker pull arangodb@sha256:3826abea713dd0aa2192cfa43b1ce0201e92a39410f250e80a1be8334aef727e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **527.3 KB (527339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a13615834f4da78f79c7db324cff767c2b1034d0ce9b753d37e8ee587feadb9`

```dockerfile
```

-	Layers:
	-	`sha256:e758ebd8c78788e1c12c7d467f76bbd99ee6f425d3811c19b36698ca38cb0e7a`  
		Last Modified: Mon, 27 Oct 2025 21:13:24 GMT  
		Size: 512.8 KB (512800 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f142224b73fd851ee2d5b6224d4a56b06b62046891515ad3f162a0249c993e26`  
		Last Modified: Mon, 27 Oct 2025 21:13:25 GMT  
		Size: 14.5 KB (14539 bytes)  
		MIME: application/vnd.in-toto+json

### `arangodb:3.12.6` - linux; arm64 variant v8

```console
$ docker pull arangodb@sha256:d86f485190d6478ca4469ca3efcb793f6443ac9936120fd0fda5f7efa91c97c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.9 MB (258870074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8107db04cebd5198a29ffd88693b1bfdbea55ceb0f6ec7dad65a48f719f99ec1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Mon, 27 Oct 2025 10:42:22 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Mon, 27 Oct 2025 10:42:22 GMT
ENV ARANGO_VERSION=3.12.6
# Mon, 27 Oct 2025 10:42:22 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8003EDF6F05459984878D4A6C04AD0FD86FEC04D &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/9c169fe900ff79790395784287bfa82f0dc0059375a34a2881b9b745c8efd42e/arangodb312/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3e_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg # buildkit
# Mon, 27 Oct 2025 10:42:22 GMT
ENV GLIBCXX_FORCE_NEW=1
# Mon, 27 Oct 2025 10:42:22 GMT
RUN echo "UTC" > /etc/timezone # buildkit
# Mon, 27 Oct 2025 10:42:22 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Mon, 27 Oct 2025 10:42:22 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 27 Oct 2025 10:42:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 27 Oct 2025 10:42:22 GMT
EXPOSE map[8529/tcp:{}]
# Mon, 27 Oct 2025 10:42:22 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:c2fe130f4aabc917e559e7eed7d37b0e21ba13b44520101696887ca892e8c63f`  
		Last Modified: Wed, 08 Oct 2025 16:24:46 GMT  
		Size: 4.0 MB (3992353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f31a952756cc363de0bce314cf0ed1e137e589eb00baa07f312a2222314c49b`  
		Last Modified: Mon, 27 Oct 2025 18:19:35 GMT  
		Size: 254.9 MB (254875565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea1651cf8ffb39ff3421e10dc91accfe70c853f8b39d1d0abb08726d6bbdca28`  
		Last Modified: Mon, 27 Oct 2025 17:20:19 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f335a6e8083a2e24834e1787130cf2feb2c24b1143fbd5afec28d7983c522f7b`  
		Last Modified: Mon, 27 Oct 2025 17:20:19 GMT  
		Size: 2.0 KB (2016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:3.12.6` - unknown; unknown

```console
$ docker pull arangodb@sha256:486d2dc263e68d1dbef621a73a576e88789e9861b0761298cebb8c84b253433f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **678.1 KB (678066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9962330844492810a7d194e6226680b377142c39a99681c8664eb602cc3052c7`

```dockerfile
```

-	Layers:
	-	`sha256:bcd2086cc7caa59c09464ea481ad05467a6514863960ec1d24f0543df3385d2f`  
		Last Modified: Mon, 27 Oct 2025 18:13:19 GMT  
		Size: 663.4 KB (663420 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d847dd755ffefa6792982722db1ff7241f33725cb2b09e27ac246d5532f5c132`  
		Last Modified: Mon, 27 Oct 2025 18:13:20 GMT  
		Size: 14.6 KB (14646 bytes)  
		MIME: application/vnd.in-toto+json

## `arangodb:latest`

```console
$ docker pull arangodb@sha256:e46594fbf0130c1f8f559e2f02d8fc7454bd60257c3a07f10a036f51c150d609
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `arangodb:latest` - linux; amd64

```console
$ docker pull arangodb@sha256:a504624887956ca3d21f5ff7883d03aa8429ffb49c839a88c0583c2df923fe62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.8 MB (259765606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13019531f970eba464dec9bcf0c59baf32fd6dcf181cf324839a9550cd1079f3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Mon, 27 Oct 2025 10:42:22 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Mon, 27 Oct 2025 10:42:22 GMT
ENV ARANGO_VERSION=3.12.6
# Mon, 27 Oct 2025 10:42:22 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8003EDF6F05459984878D4A6C04AD0FD86FEC04D &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/9c169fe900ff79790395784287bfa82f0dc0059375a34a2881b9b745c8efd42e/arangodb312/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3e_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg # buildkit
# Mon, 27 Oct 2025 10:42:22 GMT
ENV GLIBCXX_FORCE_NEW=1
# Mon, 27 Oct 2025 10:42:22 GMT
RUN echo "UTC" > /etc/timezone # buildkit
# Mon, 27 Oct 2025 10:42:22 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Mon, 27 Oct 2025 10:42:22 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 27 Oct 2025 10:42:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 27 Oct 2025 10:42:22 GMT
EXPOSE map[8529/tcp:{}]
# Mon, 27 Oct 2025 10:42:22 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:f637881d1138581d892d9eb942c56e0ccc7758fe3bdc0f1e6cd66059fdfd8185`  
		Last Modified: Wed, 08 Oct 2025 12:54:09 GMT  
		Size: 3.6 MB (3642569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:140ab0b91e813fcf0ca9d9f9a509085267bf157e8c9cb2eaf00ae89297972746`  
		Last Modified: Mon, 27 Oct 2025 21:15:01 GMT  
		Size: 256.1 MB (256120883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81b327c14195d4435bd7b56816ccbb554a8896368c4e9de99ea37f0e6672fc73`  
		Last Modified: Mon, 27 Oct 2025 20:11:44 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cbd54f3dcb50e615f3c4474b8f269b8e0824a0b2e83dfb7c93a384e9f67c350`  
		Last Modified: Mon, 27 Oct 2025 20:11:44 GMT  
		Size: 2.0 KB (2014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:latest` - unknown; unknown

```console
$ docker pull arangodb@sha256:3826abea713dd0aa2192cfa43b1ce0201e92a39410f250e80a1be8334aef727e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **527.3 KB (527339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a13615834f4da78f79c7db324cff767c2b1034d0ce9b753d37e8ee587feadb9`

```dockerfile
```

-	Layers:
	-	`sha256:e758ebd8c78788e1c12c7d467f76bbd99ee6f425d3811c19b36698ca38cb0e7a`  
		Last Modified: Mon, 27 Oct 2025 21:13:24 GMT  
		Size: 512.8 KB (512800 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f142224b73fd851ee2d5b6224d4a56b06b62046891515ad3f162a0249c993e26`  
		Last Modified: Mon, 27 Oct 2025 21:13:25 GMT  
		Size: 14.5 KB (14539 bytes)  
		MIME: application/vnd.in-toto+json

### `arangodb:latest` - linux; arm64 variant v8

```console
$ docker pull arangodb@sha256:d86f485190d6478ca4469ca3efcb793f6443ac9936120fd0fda5f7efa91c97c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.9 MB (258870074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8107db04cebd5198a29ffd88693b1bfdbea55ceb0f6ec7dad65a48f719f99ec1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Mon, 27 Oct 2025 10:42:22 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Mon, 27 Oct 2025 10:42:22 GMT
ENV ARANGO_VERSION=3.12.6
# Mon, 27 Oct 2025 10:42:22 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8003EDF6F05459984878D4A6C04AD0FD86FEC04D &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/9c169fe900ff79790395784287bfa82f0dc0059375a34a2881b9b745c8efd42e/arangodb312/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3e_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg # buildkit
# Mon, 27 Oct 2025 10:42:22 GMT
ENV GLIBCXX_FORCE_NEW=1
# Mon, 27 Oct 2025 10:42:22 GMT
RUN echo "UTC" > /etc/timezone # buildkit
# Mon, 27 Oct 2025 10:42:22 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Mon, 27 Oct 2025 10:42:22 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 27 Oct 2025 10:42:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 27 Oct 2025 10:42:22 GMT
EXPOSE map[8529/tcp:{}]
# Mon, 27 Oct 2025 10:42:22 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:c2fe130f4aabc917e559e7eed7d37b0e21ba13b44520101696887ca892e8c63f`  
		Last Modified: Wed, 08 Oct 2025 16:24:46 GMT  
		Size: 4.0 MB (3992353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f31a952756cc363de0bce314cf0ed1e137e589eb00baa07f312a2222314c49b`  
		Last Modified: Mon, 27 Oct 2025 18:19:35 GMT  
		Size: 254.9 MB (254875565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea1651cf8ffb39ff3421e10dc91accfe70c853f8b39d1d0abb08726d6bbdca28`  
		Last Modified: Mon, 27 Oct 2025 17:20:19 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f335a6e8083a2e24834e1787130cf2feb2c24b1143fbd5afec28d7983c522f7b`  
		Last Modified: Mon, 27 Oct 2025 17:20:19 GMT  
		Size: 2.0 KB (2016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:latest` - unknown; unknown

```console
$ docker pull arangodb@sha256:486d2dc263e68d1dbef621a73a576e88789e9861b0761298cebb8c84b253433f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **678.1 KB (678066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9962330844492810a7d194e6226680b377142c39a99681c8664eb602cc3052c7`

```dockerfile
```

-	Layers:
	-	`sha256:bcd2086cc7caa59c09464ea481ad05467a6514863960ec1d24f0543df3385d2f`  
		Last Modified: Mon, 27 Oct 2025 18:13:19 GMT  
		Size: 663.4 KB (663420 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d847dd755ffefa6792982722db1ff7241f33725cb2b09e27ac246d5532f5c132`  
		Last Modified: Mon, 27 Oct 2025 18:13:20 GMT  
		Size: 14.6 KB (14646 bytes)  
		MIME: application/vnd.in-toto+json
