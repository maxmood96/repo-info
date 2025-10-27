<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `arangodb`

-	[`arangodb:3.12`](#arangodb312)
-	[`arangodb:3.12.6`](#arangodb3126)
-	[`arangodb:latest`](#arangodblatest)

## `arangodb:3.12`

```console
$ docker pull arangodb@sha256:f3eb07dede7ee43189aece083dccb966e756c6c339ca2852f52fd1c359af8817
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `arangodb:3.12` - linux; amd64

```console
$ docker pull arangodb@sha256:5b0d1d2911ea864ea61d7e2357789004fe912606f5980cf481739601d7cb17a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.4 MB (258375632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0015e521daf6127042fbeda199b3471da11f7ab95cf2cb6b65c3e269700d97c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Mon, 04 Aug 2025 21:34:13 GMT
ADD alpine-minirootfs-3.21.5-x86_64.tar.gz / # buildkit
# Mon, 04 Aug 2025 21:34:13 GMT
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
	-	`sha256:f637881d1138581d892d9eb942c56e0ccc7758fe3bdc0f1e6cd66059fdfd8185`  
		Last Modified: Wed, 08 Oct 2025 12:54:09 GMT  
		Size: 3.6 MB (3642569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ec4be859a0bf18bd4e707f7d4886dbc2751b6ee894141737afeca03525c22ee`  
		Last Modified: Wed, 08 Oct 2025 23:32:38 GMT  
		Size: 254.7 MB (254730908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c3446de95b4acf41e2dfcea7c651a42f4a33c88e72289780578e2be8b70c99f`  
		Last Modified: Wed, 08 Oct 2025 22:17:27 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d636acdf16c60a998d8448443824e7bcc78cb1cdf89f9002115dfd22e690db2`  
		Last Modified: Wed, 08 Oct 2025 22:17:27 GMT  
		Size: 2.0 KB (2015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:3.12` - unknown; unknown

```console
$ docker pull arangodb@sha256:f1c5a9c110c5b549c14d4c5c43d5f8827ebbdd5a764f619438e8495d06498db7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **527.4 KB (527360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc4c8d76a8f624eec0bae98ff9ebd28731416a126ebfe512cb9fff02b802a1c4`

```dockerfile
```

-	Layers:
	-	`sha256:1643c5406cf3a57e27e6c90964212bfaa4ab21b7520a1d029bfcb2d0e63ad497`  
		Last Modified: Thu, 09 Oct 2025 00:13:20 GMT  
		Size: 512.8 KB (512804 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c54aab340d8fd63d92ea4fa0db167303cbbd0ed181ebd17c6837587c507fd6a1`  
		Last Modified: Thu, 09 Oct 2025 00:13:20 GMT  
		Size: 14.6 KB (14556 bytes)  
		MIME: application/vnd.in-toto+json

### `arangodb:3.12` - linux; arm64 variant v8

```console
$ docker pull arangodb@sha256:865a119fafb88f4cc534edba10ddce1e5581a6844638661b3ef996e61c9f799c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.4 MB (257414153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3ce5759e889b2ddcc0e3d2fed2766ed5cec67b86dc37dc33c66800dd3801701`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Mon, 04 Aug 2025 21:34:13 GMT
ADD alpine-minirootfs-3.21.5-aarch64.tar.gz / # buildkit
# Mon, 04 Aug 2025 21:34:13 GMT
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
	-	`sha256:c2fe130f4aabc917e559e7eed7d37b0e21ba13b44520101696887ca892e8c63f`  
		Last Modified: Wed, 08 Oct 2025 16:24:46 GMT  
		Size: 4.0 MB (3992353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7168ec259bdbb469d751d35c45dd7b7338d5faad62974fb63f26ba44cffa989`  
		Last Modified: Wed, 08 Oct 2025 21:20:52 GMT  
		Size: 253.4 MB (253419646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f70f97053d8d8c0186a135aec68c53ca1ae7dc2640becf776c2829bf66ac8a28`  
		Last Modified: Wed, 08 Oct 2025 21:14:06 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4bedca5e5e3ad8947ce933f769f5ecf52700ca9acff272bb9305f0b26e08194`  
		Last Modified: Wed, 08 Oct 2025 21:14:06 GMT  
		Size: 2.0 KB (2014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:3.12` - unknown; unknown

```console
$ docker pull arangodb@sha256:7c1166f790ef3ebe6472d766318cf64a8d496d8f779d92405d27dd7d746aef71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **678.1 KB (678088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98668e8a734c23fe99a25898a24da6ebddcf901dd9044888575bfec844139c55`

```dockerfile
```

-	Layers:
	-	`sha256:f50e98b7bb9aad4c0fc711c060b97222dc2793fd915c870036453cf01a4fc66b`  
		Last Modified: Thu, 09 Oct 2025 00:13:24 GMT  
		Size: 663.4 KB (663424 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f48bf6f8c9fea31cd743ab525691d3c746d57e80955194a1a99ad79189aabb0e`  
		Last Modified: Thu, 09 Oct 2025 00:13:25 GMT  
		Size: 14.7 KB (14664 bytes)  
		MIME: application/vnd.in-toto+json

## `arangodb:3.12.6`

**does not exist** (yet?)

## `arangodb:latest`

```console
$ docker pull arangodb@sha256:f3eb07dede7ee43189aece083dccb966e756c6c339ca2852f52fd1c359af8817
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `arangodb:latest` - linux; amd64

```console
$ docker pull arangodb@sha256:5b0d1d2911ea864ea61d7e2357789004fe912606f5980cf481739601d7cb17a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.4 MB (258375632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0015e521daf6127042fbeda199b3471da11f7ab95cf2cb6b65c3e269700d97c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Mon, 04 Aug 2025 21:34:13 GMT
ADD alpine-minirootfs-3.21.5-x86_64.tar.gz / # buildkit
# Mon, 04 Aug 2025 21:34:13 GMT
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
	-	`sha256:f637881d1138581d892d9eb942c56e0ccc7758fe3bdc0f1e6cd66059fdfd8185`  
		Last Modified: Wed, 08 Oct 2025 12:54:09 GMT  
		Size: 3.6 MB (3642569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ec4be859a0bf18bd4e707f7d4886dbc2751b6ee894141737afeca03525c22ee`  
		Last Modified: Wed, 08 Oct 2025 23:32:38 GMT  
		Size: 254.7 MB (254730908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c3446de95b4acf41e2dfcea7c651a42f4a33c88e72289780578e2be8b70c99f`  
		Last Modified: Wed, 08 Oct 2025 22:17:27 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d636acdf16c60a998d8448443824e7bcc78cb1cdf89f9002115dfd22e690db2`  
		Last Modified: Wed, 08 Oct 2025 22:17:27 GMT  
		Size: 2.0 KB (2015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:latest` - unknown; unknown

```console
$ docker pull arangodb@sha256:f1c5a9c110c5b549c14d4c5c43d5f8827ebbdd5a764f619438e8495d06498db7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **527.4 KB (527360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc4c8d76a8f624eec0bae98ff9ebd28731416a126ebfe512cb9fff02b802a1c4`

```dockerfile
```

-	Layers:
	-	`sha256:1643c5406cf3a57e27e6c90964212bfaa4ab21b7520a1d029bfcb2d0e63ad497`  
		Last Modified: Thu, 09 Oct 2025 00:13:20 GMT  
		Size: 512.8 KB (512804 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c54aab340d8fd63d92ea4fa0db167303cbbd0ed181ebd17c6837587c507fd6a1`  
		Last Modified: Thu, 09 Oct 2025 00:13:20 GMT  
		Size: 14.6 KB (14556 bytes)  
		MIME: application/vnd.in-toto+json

### `arangodb:latest` - linux; arm64 variant v8

```console
$ docker pull arangodb@sha256:865a119fafb88f4cc534edba10ddce1e5581a6844638661b3ef996e61c9f799c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.4 MB (257414153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3ce5759e889b2ddcc0e3d2fed2766ed5cec67b86dc37dc33c66800dd3801701`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Mon, 04 Aug 2025 21:34:13 GMT
ADD alpine-minirootfs-3.21.5-aarch64.tar.gz / # buildkit
# Mon, 04 Aug 2025 21:34:13 GMT
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
	-	`sha256:c2fe130f4aabc917e559e7eed7d37b0e21ba13b44520101696887ca892e8c63f`  
		Last Modified: Wed, 08 Oct 2025 16:24:46 GMT  
		Size: 4.0 MB (3992353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7168ec259bdbb469d751d35c45dd7b7338d5faad62974fb63f26ba44cffa989`  
		Last Modified: Wed, 08 Oct 2025 21:20:52 GMT  
		Size: 253.4 MB (253419646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f70f97053d8d8c0186a135aec68c53ca1ae7dc2640becf776c2829bf66ac8a28`  
		Last Modified: Wed, 08 Oct 2025 21:14:06 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4bedca5e5e3ad8947ce933f769f5ecf52700ca9acff272bb9305f0b26e08194`  
		Last Modified: Wed, 08 Oct 2025 21:14:06 GMT  
		Size: 2.0 KB (2014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:latest` - unknown; unknown

```console
$ docker pull arangodb@sha256:7c1166f790ef3ebe6472d766318cf64a8d496d8f779d92405d27dd7d746aef71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **678.1 KB (678088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98668e8a734c23fe99a25898a24da6ebddcf901dd9044888575bfec844139c55`

```dockerfile
```

-	Layers:
	-	`sha256:f50e98b7bb9aad4c0fc711c060b97222dc2793fd915c870036453cf01a4fc66b`  
		Last Modified: Thu, 09 Oct 2025 00:13:24 GMT  
		Size: 663.4 KB (663424 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f48bf6f8c9fea31cd743ab525691d3c746d57e80955194a1a99ad79189aabb0e`  
		Last Modified: Thu, 09 Oct 2025 00:13:25 GMT  
		Size: 14.7 KB (14664 bytes)  
		MIME: application/vnd.in-toto+json
