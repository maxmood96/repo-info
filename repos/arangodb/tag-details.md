<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `arangodb`

-	[`arangodb:3.11`](#arangodb311)
-	[`arangodb:3.11.13`](#arangodb31113)
-	[`arangodb:3.12`](#arangodb312)
-	[`arangodb:3.12.4.3`](#arangodb31243)
-	[`arangodb:latest`](#arangodblatest)

## `arangodb:3.11`

```console
$ docker pull arangodb@sha256:f8bf478c77ceb0122bb30f4f40d97f60ad2fe2fe8c64f390a64dc9f5508dd402
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `arangodb:3.11` - linux; amd64

```console
$ docker pull arangodb@sha256:14d4cf963173f6d0cb1f5df6e6c00c9f5403ffa8cf6c206b48fd5ed3fb129330
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.8 MB (207791730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fe39c991e590fb9b17db87df45d2817ce5d3dba04a0d461a946c4c57cdb7c9b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 14 Feb 2025 15:05:04 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Fri, 14 Feb 2025 15:05:04 GMT
ENV ARANGO_VERSION=3.11.13
# Fri, 14 Feb 2025 15:05:04 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8003EDF6F05459984878D4A6C04AD0FD86FEC04D &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb311/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg # buildkit
# Fri, 14 Feb 2025 15:05:04 GMT
ENV GLIBCXX_FORCE_NEW=1
# Fri, 14 Feb 2025 15:05:04 GMT
RUN echo "UTC" > /etc/timezone # buildkit
# Fri, 14 Feb 2025 15:05:04 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Fri, 14 Feb 2025 15:05:04 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 14 Feb 2025 15:05:04 GMT
COPY docker-foxx.sh /usr/bin/foxx # buildkit
# Fri, 14 Feb 2025 15:05:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 14 Feb 2025 15:05:04 GMT
EXPOSE map[8529/tcp:{}]
# Fri, 14 Feb 2025 15:05:04 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f7bd5f6389b77c24b69a9f39ef1aea79863361d0aa9f36681a1aabdec398254`  
		Last Modified: Sat, 15 Feb 2025 01:13:55 GMT  
		Size: 204.1 MB (204146999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a58fd14c9ac2e19981435b18776d552556666ec1b07e695886fa9cd4899ac0cc`  
		Last Modified: Sat, 15 Feb 2025 01:13:51 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03ab2495fb8a6cc1e9829e9561221eff60c011f3a9c05ebe5e3a201d6a5484d7`  
		Last Modified: Sat, 15 Feb 2025 01:13:50 GMT  
		Size: 2.1 KB (2087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28ebe21f9a7b14e60989be24660d4a0ce7461c76e732dd1c4dbee8f0172cb2ba`  
		Last Modified: Sat, 15 Feb 2025 01:13:51 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:3.11` - unknown; unknown

```console
$ docker pull arangodb@sha256:905d609f2c7dd7cf11fc580b06d8c0035d1208fd954b1945471a873e786a191e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1141438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be64196f7c3927d47f0964a8a5503afef9cf15da303fd5d02b99f29008c78514`

```dockerfile
```

-	Layers:
	-	`sha256:c8a8ab69e438b4e7b9570594b11aadbff1d0b78fee5c9ef8afca45afb90c524b`  
		Last Modified: Sat, 15 Feb 2025 01:13:15 GMT  
		Size: 1.1 MB (1125618 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0412bf095645ad3b18313f96b15e5997051c74a7983ff897111cbb211339776`  
		Last Modified: Sat, 15 Feb 2025 01:13:16 GMT  
		Size: 15.8 KB (15820 bytes)  
		MIME: application/vnd.in-toto+json

### `arangodb:3.11` - linux; arm64 variant v8

```console
$ docker pull arangodb@sha256:828f2854a4433aa71111859bf07dd1724c78c08b648c50948642d80629b22d1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.0 MB (211041960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de1810fe9c4f3fab56437545c85ad4e6132e8b38621d64ba626c693633710e6f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 14 Feb 2025 15:05:04 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Fri, 14 Feb 2025 15:05:04 GMT
ENV ARANGO_VERSION=3.11.13
# Fri, 14 Feb 2025 15:05:04 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8003EDF6F05459984878D4A6C04AD0FD86FEC04D &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb311/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg # buildkit
# Fri, 14 Feb 2025 15:05:04 GMT
ENV GLIBCXX_FORCE_NEW=1
# Fri, 14 Feb 2025 15:05:04 GMT
RUN echo "UTC" > /etc/timezone # buildkit
# Fri, 14 Feb 2025 15:05:04 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Fri, 14 Feb 2025 15:05:04 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 14 Feb 2025 15:05:04 GMT
COPY docker-foxx.sh /usr/bin/foxx # buildkit
# Fri, 14 Feb 2025 15:05:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 14 Feb 2025 15:05:04 GMT
EXPOSE map[8529/tcp:{}]
# Fri, 14 Feb 2025 15:05:04 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e85add573942c0332c946f388401f56b87d5cce4aed3fdd17185823f6824482e`  
		Last Modified: Sat, 15 Feb 2025 19:57:45 GMT  
		Size: 207.0 MB (207046445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea55abe764091499acf3792143258b72d566279a97e1459b6f6e9b772550c73f`  
		Last Modified: Sat, 15 Feb 2025 19:57:37 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76dbb194d2e149db6ff588f72931a66db1d0268221b7caa413c9fe16eb9e3b86`  
		Last Modified: Sat, 15 Feb 2025 19:57:37 GMT  
		Size: 2.1 KB (2088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9444deeb88d76d5cecc4e3bc770935538205197258a4aa562e7c02846cff5c62`  
		Last Modified: Sat, 15 Feb 2025 19:57:38 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:3.11` - unknown; unknown

```console
$ docker pull arangodb@sha256:2dc77f48ff7073a81780e15ea65456f211ba064aa928c2332909f5a4648a3da6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1292141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b1b70dfe23db0f16f86c6973141322fd29515938c5492fb8c4acf30e3cd521d`

```dockerfile
```

-	Layers:
	-	`sha256:56a54082483a03ccb21ea3d94d7b69ad6424730dee5607693ff364d76ef65904`  
		Last Modified: Sat, 15 Feb 2025 07:13:18 GMT  
		Size: 1.3 MB (1276226 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa1f0d606e83cc74512f1195012a3bc81be797a2373f9c3ebac3a4085f851e21`  
		Last Modified: Sat, 15 Feb 2025 07:13:18 GMT  
		Size: 15.9 KB (15915 bytes)  
		MIME: application/vnd.in-toto+json

## `arangodb:3.11.13`

```console
$ docker pull arangodb@sha256:f8bf478c77ceb0122bb30f4f40d97f60ad2fe2fe8c64f390a64dc9f5508dd402
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `arangodb:3.11.13` - linux; amd64

```console
$ docker pull arangodb@sha256:14d4cf963173f6d0cb1f5df6e6c00c9f5403ffa8cf6c206b48fd5ed3fb129330
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.8 MB (207791730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fe39c991e590fb9b17db87df45d2817ce5d3dba04a0d461a946c4c57cdb7c9b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 14 Feb 2025 15:05:04 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Fri, 14 Feb 2025 15:05:04 GMT
ENV ARANGO_VERSION=3.11.13
# Fri, 14 Feb 2025 15:05:04 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8003EDF6F05459984878D4A6C04AD0FD86FEC04D &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb311/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg # buildkit
# Fri, 14 Feb 2025 15:05:04 GMT
ENV GLIBCXX_FORCE_NEW=1
# Fri, 14 Feb 2025 15:05:04 GMT
RUN echo "UTC" > /etc/timezone # buildkit
# Fri, 14 Feb 2025 15:05:04 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Fri, 14 Feb 2025 15:05:04 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 14 Feb 2025 15:05:04 GMT
COPY docker-foxx.sh /usr/bin/foxx # buildkit
# Fri, 14 Feb 2025 15:05:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 14 Feb 2025 15:05:04 GMT
EXPOSE map[8529/tcp:{}]
# Fri, 14 Feb 2025 15:05:04 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f7bd5f6389b77c24b69a9f39ef1aea79863361d0aa9f36681a1aabdec398254`  
		Last Modified: Sat, 15 Feb 2025 01:13:55 GMT  
		Size: 204.1 MB (204146999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a58fd14c9ac2e19981435b18776d552556666ec1b07e695886fa9cd4899ac0cc`  
		Last Modified: Sat, 15 Feb 2025 01:13:51 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03ab2495fb8a6cc1e9829e9561221eff60c011f3a9c05ebe5e3a201d6a5484d7`  
		Last Modified: Sat, 15 Feb 2025 01:13:50 GMT  
		Size: 2.1 KB (2087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28ebe21f9a7b14e60989be24660d4a0ce7461c76e732dd1c4dbee8f0172cb2ba`  
		Last Modified: Sat, 15 Feb 2025 01:13:51 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:3.11.13` - unknown; unknown

```console
$ docker pull arangodb@sha256:905d609f2c7dd7cf11fc580b06d8c0035d1208fd954b1945471a873e786a191e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1141438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be64196f7c3927d47f0964a8a5503afef9cf15da303fd5d02b99f29008c78514`

```dockerfile
```

-	Layers:
	-	`sha256:c8a8ab69e438b4e7b9570594b11aadbff1d0b78fee5c9ef8afca45afb90c524b`  
		Last Modified: Sat, 15 Feb 2025 01:13:15 GMT  
		Size: 1.1 MB (1125618 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0412bf095645ad3b18313f96b15e5997051c74a7983ff897111cbb211339776`  
		Last Modified: Sat, 15 Feb 2025 01:13:16 GMT  
		Size: 15.8 KB (15820 bytes)  
		MIME: application/vnd.in-toto+json

### `arangodb:3.11.13` - linux; arm64 variant v8

```console
$ docker pull arangodb@sha256:828f2854a4433aa71111859bf07dd1724c78c08b648c50948642d80629b22d1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.0 MB (211041960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de1810fe9c4f3fab56437545c85ad4e6132e8b38621d64ba626c693633710e6f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 14 Feb 2025 15:05:04 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Fri, 14 Feb 2025 15:05:04 GMT
ENV ARANGO_VERSION=3.11.13
# Fri, 14 Feb 2025 15:05:04 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8003EDF6F05459984878D4A6C04AD0FD86FEC04D &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb311/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg # buildkit
# Fri, 14 Feb 2025 15:05:04 GMT
ENV GLIBCXX_FORCE_NEW=1
# Fri, 14 Feb 2025 15:05:04 GMT
RUN echo "UTC" > /etc/timezone # buildkit
# Fri, 14 Feb 2025 15:05:04 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Fri, 14 Feb 2025 15:05:04 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 14 Feb 2025 15:05:04 GMT
COPY docker-foxx.sh /usr/bin/foxx # buildkit
# Fri, 14 Feb 2025 15:05:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 14 Feb 2025 15:05:04 GMT
EXPOSE map[8529/tcp:{}]
# Fri, 14 Feb 2025 15:05:04 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e85add573942c0332c946f388401f56b87d5cce4aed3fdd17185823f6824482e`  
		Last Modified: Sat, 15 Feb 2025 19:57:45 GMT  
		Size: 207.0 MB (207046445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea55abe764091499acf3792143258b72d566279a97e1459b6f6e9b772550c73f`  
		Last Modified: Sat, 15 Feb 2025 19:57:37 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76dbb194d2e149db6ff588f72931a66db1d0268221b7caa413c9fe16eb9e3b86`  
		Last Modified: Sat, 15 Feb 2025 19:57:37 GMT  
		Size: 2.1 KB (2088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9444deeb88d76d5cecc4e3bc770935538205197258a4aa562e7c02846cff5c62`  
		Last Modified: Sat, 15 Feb 2025 19:57:38 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:3.11.13` - unknown; unknown

```console
$ docker pull arangodb@sha256:2dc77f48ff7073a81780e15ea65456f211ba064aa928c2332909f5a4648a3da6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1292141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b1b70dfe23db0f16f86c6973141322fd29515938c5492fb8c4acf30e3cd521d`

```dockerfile
```

-	Layers:
	-	`sha256:56a54082483a03ccb21ea3d94d7b69ad6424730dee5607693ff364d76ef65904`  
		Last Modified: Sat, 15 Feb 2025 07:13:18 GMT  
		Size: 1.3 MB (1276226 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa1f0d606e83cc74512f1195012a3bc81be797a2373f9c3ebac3a4085f851e21`  
		Last Modified: Sat, 15 Feb 2025 07:13:18 GMT  
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
