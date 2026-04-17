<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `arangodb`

-	[`arangodb:3.12`](#arangodb312)
-	[`arangodb:3.12.9`](#arangodb3129)
-	[`arangodb:latest`](#arangodblatest)

## `arangodb:3.12`

```console
$ docker pull arangodb@sha256:15608ffa3663473e1321ac1fb2ad03fe648e728d311295cbe267a627ba6031a7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `arangodb:3.12` - linux; amd64

```console
$ docker pull arangodb@sha256:683f6f526e687095f45ee664447c21e3a843d3822b820e9e83f431396a36b6b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.3 MB (260261861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:546bd2887a27c5f0f749efb9866a0753f0d4a7d3c82c498259c52fbd5061f704`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:15 GMT
ADD alpine-minirootfs-3.21.7-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:15 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:12:07 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Fri, 17 Apr 2026 00:12:07 GMT
ENV ARANGO_VERSION=3.12.9
# Fri, 17 Apr 2026 00:12:07 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8003EDF6F05459984878D4A6C04AD0FD86FEC04D &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/9c169fe900ff79790395784287bfa82f0dc0059375a34a2881b9b745c8efd42e/arangodb312/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3e_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg # buildkit
# Fri, 17 Apr 2026 00:12:07 GMT
ENV GLIBCXX_FORCE_NEW=1
# Fri, 17 Apr 2026 00:12:07 GMT
RUN echo "UTC" > /etc/timezone # buildkit
# Fri, 17 Apr 2026 00:12:07 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Fri, 17 Apr 2026 00:12:07 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 17 Apr 2026 00:12:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 17 Apr 2026 00:12:07 GMT
EXPOSE map[8529/tcp:{}]
# Fri, 17 Apr 2026 00:12:07 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:897d797d2723cf0e318402f4d6f37d51b011517e5cf09246b22155f0fa90dc81`  
		Last Modified: Thu, 16 Apr 2026 05:32:55 GMT  
		Size: 3.6 MB (3646875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1813845f167da2b3b63b9284b59387b4ef75a37b0c1ecd759ac280bba0222814`  
		Last Modified: Fri, 17 Apr 2026 00:12:38 GMT  
		Size: 256.6 MB (256612832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9bedd3ebcf3a83d6131c91b3c63d6f61a2a45fa7bb61ac68a179b78904d8057`  
		Last Modified: Fri, 17 Apr 2026 00:12:33 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d05b5049b085ea94832b9a7712aae5eb2f67727724f4c2dccfb040a1a71acbd`  
		Last Modified: Fri, 17 Apr 2026 00:12:33 GMT  
		Size: 2.0 KB (2014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:3.12` - unknown; unknown

```console
$ docker pull arangodb@sha256:6d7e4fba81070e45c6440ff99c3eab131cb87b4830d41162ff3aa9eac13db46d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **522.1 KB (522128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0aa7479a54a3e4ab55fcae11bf6efcef9b093d1f144b65d60afdae46061d84d`

```dockerfile
```

-	Layers:
	-	`sha256:264a22d90beb141d057116e1ec69d8b7cddb43adca5ee6bf64eb378d590ef330`  
		Last Modified: Fri, 17 Apr 2026 00:12:33 GMT  
		Size: 507.6 KB (507616 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27e6941ec2f5bf2efc242d772a6e63a3eab3c13b8bcee925982c83aaa6755a1e`  
		Last Modified: Fri, 17 Apr 2026 00:12:33 GMT  
		Size: 14.5 KB (14512 bytes)  
		MIME: application/vnd.in-toto+json

### `arangodb:3.12` - linux; arm64 variant v8

```console
$ docker pull arangodb@sha256:1627de154d9f591f6de8a2f1d18fcee6c658439928bf8a75c9fa8e636b709793
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.7 MB (258733948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:885f510c6714a7af6ef1cfa1c3a4043e88d8b92ea18cae1fb6103015482c0c0b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:13 GMT
ADD alpine-minirootfs-3.21.7-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:13 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:11:39 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Fri, 17 Apr 2026 00:11:39 GMT
ENV ARANGO_VERSION=3.12.9
# Fri, 17 Apr 2026 00:11:39 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8003EDF6F05459984878D4A6C04AD0FD86FEC04D &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/9c169fe900ff79790395784287bfa82f0dc0059375a34a2881b9b745c8efd42e/arangodb312/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3e_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg # buildkit
# Fri, 17 Apr 2026 00:11:39 GMT
ENV GLIBCXX_FORCE_NEW=1
# Fri, 17 Apr 2026 00:11:39 GMT
RUN echo "UTC" > /etc/timezone # buildkit
# Fri, 17 Apr 2026 00:11:39 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Fri, 17 Apr 2026 00:11:39 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 17 Apr 2026 00:11:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 17 Apr 2026 00:11:39 GMT
EXPOSE map[8529/tcp:{}]
# Fri, 17 Apr 2026 00:11:39 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:2dd7199cff98a7400e801cbfad6de906972a4e3dd0a749d4c1b80f5a1e3e4108`  
		Last Modified: Thu, 16 Apr 2026 05:32:50 GMT  
		Size: 4.0 MB (3994465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23b098577a830e0fe8563ae9fbbb774d77ac36ea65ab1354be2970efe9dfb26f`  
		Last Modified: Fri, 17 Apr 2026 00:12:13 GMT  
		Size: 254.7 MB (254737329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a57604cb474461de9b83a41e060e566aec7cda9f97b13b8a863389fdb9e8d1e0`  
		Last Modified: Fri, 17 Apr 2026 00:12:07 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e6dbc4f00df61f7b993b5989d1ae85b34120c7254dc48a39b7554a4e2d5f30a`  
		Last Modified: Fri, 17 Apr 2026 00:12:07 GMT  
		Size: 2.0 KB (2014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:3.12` - unknown; unknown

```console
$ docker pull arangodb@sha256:a86a513ef87e49fd6a45dc7bff6246ee53e5519bdf9dce03c8941f236e52d4d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **672.9 KB (672855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd2494114fede371c5b57028443fe30e2dad2783f0fe76efcdbf94d217834822`

```dockerfile
```

-	Layers:
	-	`sha256:66ed6a0f798ede4057ce584d1138a57f91a7dd9cd259339f2d5795c44d44719f`  
		Last Modified: Fri, 17 Apr 2026 00:12:07 GMT  
		Size: 658.2 KB (658236 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7036dd98875b1bc2cc293585f1e61e44709bbd3ad684ad4335ec82ba4d7fe55`  
		Last Modified: Fri, 17 Apr 2026 00:12:07 GMT  
		Size: 14.6 KB (14619 bytes)  
		MIME: application/vnd.in-toto+json

## `arangodb:3.12.9`

```console
$ docker pull arangodb@sha256:15608ffa3663473e1321ac1fb2ad03fe648e728d311295cbe267a627ba6031a7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `arangodb:3.12.9` - linux; amd64

```console
$ docker pull arangodb@sha256:683f6f526e687095f45ee664447c21e3a843d3822b820e9e83f431396a36b6b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.3 MB (260261861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:546bd2887a27c5f0f749efb9866a0753f0d4a7d3c82c498259c52fbd5061f704`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:15 GMT
ADD alpine-minirootfs-3.21.7-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:15 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:12:07 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Fri, 17 Apr 2026 00:12:07 GMT
ENV ARANGO_VERSION=3.12.9
# Fri, 17 Apr 2026 00:12:07 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8003EDF6F05459984878D4A6C04AD0FD86FEC04D &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/9c169fe900ff79790395784287bfa82f0dc0059375a34a2881b9b745c8efd42e/arangodb312/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3e_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg # buildkit
# Fri, 17 Apr 2026 00:12:07 GMT
ENV GLIBCXX_FORCE_NEW=1
# Fri, 17 Apr 2026 00:12:07 GMT
RUN echo "UTC" > /etc/timezone # buildkit
# Fri, 17 Apr 2026 00:12:07 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Fri, 17 Apr 2026 00:12:07 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 17 Apr 2026 00:12:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 17 Apr 2026 00:12:07 GMT
EXPOSE map[8529/tcp:{}]
# Fri, 17 Apr 2026 00:12:07 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:897d797d2723cf0e318402f4d6f37d51b011517e5cf09246b22155f0fa90dc81`  
		Last Modified: Thu, 16 Apr 2026 05:32:55 GMT  
		Size: 3.6 MB (3646875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1813845f167da2b3b63b9284b59387b4ef75a37b0c1ecd759ac280bba0222814`  
		Last Modified: Fri, 17 Apr 2026 00:12:38 GMT  
		Size: 256.6 MB (256612832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9bedd3ebcf3a83d6131c91b3c63d6f61a2a45fa7bb61ac68a179b78904d8057`  
		Last Modified: Fri, 17 Apr 2026 00:12:33 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d05b5049b085ea94832b9a7712aae5eb2f67727724f4c2dccfb040a1a71acbd`  
		Last Modified: Fri, 17 Apr 2026 00:12:33 GMT  
		Size: 2.0 KB (2014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:3.12.9` - unknown; unknown

```console
$ docker pull arangodb@sha256:6d7e4fba81070e45c6440ff99c3eab131cb87b4830d41162ff3aa9eac13db46d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **522.1 KB (522128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0aa7479a54a3e4ab55fcae11bf6efcef9b093d1f144b65d60afdae46061d84d`

```dockerfile
```

-	Layers:
	-	`sha256:264a22d90beb141d057116e1ec69d8b7cddb43adca5ee6bf64eb378d590ef330`  
		Last Modified: Fri, 17 Apr 2026 00:12:33 GMT  
		Size: 507.6 KB (507616 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27e6941ec2f5bf2efc242d772a6e63a3eab3c13b8bcee925982c83aaa6755a1e`  
		Last Modified: Fri, 17 Apr 2026 00:12:33 GMT  
		Size: 14.5 KB (14512 bytes)  
		MIME: application/vnd.in-toto+json

### `arangodb:3.12.9` - linux; arm64 variant v8

```console
$ docker pull arangodb@sha256:1627de154d9f591f6de8a2f1d18fcee6c658439928bf8a75c9fa8e636b709793
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.7 MB (258733948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:885f510c6714a7af6ef1cfa1c3a4043e88d8b92ea18cae1fb6103015482c0c0b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:13 GMT
ADD alpine-minirootfs-3.21.7-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:13 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:11:39 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Fri, 17 Apr 2026 00:11:39 GMT
ENV ARANGO_VERSION=3.12.9
# Fri, 17 Apr 2026 00:11:39 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8003EDF6F05459984878D4A6C04AD0FD86FEC04D &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/9c169fe900ff79790395784287bfa82f0dc0059375a34a2881b9b745c8efd42e/arangodb312/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3e_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg # buildkit
# Fri, 17 Apr 2026 00:11:39 GMT
ENV GLIBCXX_FORCE_NEW=1
# Fri, 17 Apr 2026 00:11:39 GMT
RUN echo "UTC" > /etc/timezone # buildkit
# Fri, 17 Apr 2026 00:11:39 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Fri, 17 Apr 2026 00:11:39 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 17 Apr 2026 00:11:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 17 Apr 2026 00:11:39 GMT
EXPOSE map[8529/tcp:{}]
# Fri, 17 Apr 2026 00:11:39 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:2dd7199cff98a7400e801cbfad6de906972a4e3dd0a749d4c1b80f5a1e3e4108`  
		Last Modified: Thu, 16 Apr 2026 05:32:50 GMT  
		Size: 4.0 MB (3994465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23b098577a830e0fe8563ae9fbbb774d77ac36ea65ab1354be2970efe9dfb26f`  
		Last Modified: Fri, 17 Apr 2026 00:12:13 GMT  
		Size: 254.7 MB (254737329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a57604cb474461de9b83a41e060e566aec7cda9f97b13b8a863389fdb9e8d1e0`  
		Last Modified: Fri, 17 Apr 2026 00:12:07 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e6dbc4f00df61f7b993b5989d1ae85b34120c7254dc48a39b7554a4e2d5f30a`  
		Last Modified: Fri, 17 Apr 2026 00:12:07 GMT  
		Size: 2.0 KB (2014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:3.12.9` - unknown; unknown

```console
$ docker pull arangodb@sha256:a86a513ef87e49fd6a45dc7bff6246ee53e5519bdf9dce03c8941f236e52d4d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **672.9 KB (672855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd2494114fede371c5b57028443fe30e2dad2783f0fe76efcdbf94d217834822`

```dockerfile
```

-	Layers:
	-	`sha256:66ed6a0f798ede4057ce584d1138a57f91a7dd9cd259339f2d5795c44d44719f`  
		Last Modified: Fri, 17 Apr 2026 00:12:07 GMT  
		Size: 658.2 KB (658236 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7036dd98875b1bc2cc293585f1e61e44709bbd3ad684ad4335ec82ba4d7fe55`  
		Last Modified: Fri, 17 Apr 2026 00:12:07 GMT  
		Size: 14.6 KB (14619 bytes)  
		MIME: application/vnd.in-toto+json

## `arangodb:latest`

```console
$ docker pull arangodb@sha256:15608ffa3663473e1321ac1fb2ad03fe648e728d311295cbe267a627ba6031a7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `arangodb:latest` - linux; amd64

```console
$ docker pull arangodb@sha256:683f6f526e687095f45ee664447c21e3a843d3822b820e9e83f431396a36b6b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.3 MB (260261861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:546bd2887a27c5f0f749efb9866a0753f0d4a7d3c82c498259c52fbd5061f704`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:15 GMT
ADD alpine-minirootfs-3.21.7-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:15 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:12:07 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Fri, 17 Apr 2026 00:12:07 GMT
ENV ARANGO_VERSION=3.12.9
# Fri, 17 Apr 2026 00:12:07 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8003EDF6F05459984878D4A6C04AD0FD86FEC04D &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/9c169fe900ff79790395784287bfa82f0dc0059375a34a2881b9b745c8efd42e/arangodb312/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3e_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg # buildkit
# Fri, 17 Apr 2026 00:12:07 GMT
ENV GLIBCXX_FORCE_NEW=1
# Fri, 17 Apr 2026 00:12:07 GMT
RUN echo "UTC" > /etc/timezone # buildkit
# Fri, 17 Apr 2026 00:12:07 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Fri, 17 Apr 2026 00:12:07 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 17 Apr 2026 00:12:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 17 Apr 2026 00:12:07 GMT
EXPOSE map[8529/tcp:{}]
# Fri, 17 Apr 2026 00:12:07 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:897d797d2723cf0e318402f4d6f37d51b011517e5cf09246b22155f0fa90dc81`  
		Last Modified: Thu, 16 Apr 2026 05:32:55 GMT  
		Size: 3.6 MB (3646875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1813845f167da2b3b63b9284b59387b4ef75a37b0c1ecd759ac280bba0222814`  
		Last Modified: Fri, 17 Apr 2026 00:12:38 GMT  
		Size: 256.6 MB (256612832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9bedd3ebcf3a83d6131c91b3c63d6f61a2a45fa7bb61ac68a179b78904d8057`  
		Last Modified: Fri, 17 Apr 2026 00:12:33 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d05b5049b085ea94832b9a7712aae5eb2f67727724f4c2dccfb040a1a71acbd`  
		Last Modified: Fri, 17 Apr 2026 00:12:33 GMT  
		Size: 2.0 KB (2014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:latest` - unknown; unknown

```console
$ docker pull arangodb@sha256:6d7e4fba81070e45c6440ff99c3eab131cb87b4830d41162ff3aa9eac13db46d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **522.1 KB (522128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0aa7479a54a3e4ab55fcae11bf6efcef9b093d1f144b65d60afdae46061d84d`

```dockerfile
```

-	Layers:
	-	`sha256:264a22d90beb141d057116e1ec69d8b7cddb43adca5ee6bf64eb378d590ef330`  
		Last Modified: Fri, 17 Apr 2026 00:12:33 GMT  
		Size: 507.6 KB (507616 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27e6941ec2f5bf2efc242d772a6e63a3eab3c13b8bcee925982c83aaa6755a1e`  
		Last Modified: Fri, 17 Apr 2026 00:12:33 GMT  
		Size: 14.5 KB (14512 bytes)  
		MIME: application/vnd.in-toto+json

### `arangodb:latest` - linux; arm64 variant v8

```console
$ docker pull arangodb@sha256:1627de154d9f591f6de8a2f1d18fcee6c658439928bf8a75c9fa8e636b709793
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.7 MB (258733948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:885f510c6714a7af6ef1cfa1c3a4043e88d8b92ea18cae1fb6103015482c0c0b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:13 GMT
ADD alpine-minirootfs-3.21.7-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:13 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:11:39 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Fri, 17 Apr 2026 00:11:39 GMT
ENV ARANGO_VERSION=3.12.9
# Fri, 17 Apr 2026 00:11:39 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8003EDF6F05459984878D4A6C04AD0FD86FEC04D &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/9c169fe900ff79790395784287bfa82f0dc0059375a34a2881b9b745c8efd42e/arangodb312/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3e_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg # buildkit
# Fri, 17 Apr 2026 00:11:39 GMT
ENV GLIBCXX_FORCE_NEW=1
# Fri, 17 Apr 2026 00:11:39 GMT
RUN echo "UTC" > /etc/timezone # buildkit
# Fri, 17 Apr 2026 00:11:39 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Fri, 17 Apr 2026 00:11:39 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 17 Apr 2026 00:11:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 17 Apr 2026 00:11:39 GMT
EXPOSE map[8529/tcp:{}]
# Fri, 17 Apr 2026 00:11:39 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:2dd7199cff98a7400e801cbfad6de906972a4e3dd0a749d4c1b80f5a1e3e4108`  
		Last Modified: Thu, 16 Apr 2026 05:32:50 GMT  
		Size: 4.0 MB (3994465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23b098577a830e0fe8563ae9fbbb774d77ac36ea65ab1354be2970efe9dfb26f`  
		Last Modified: Fri, 17 Apr 2026 00:12:13 GMT  
		Size: 254.7 MB (254737329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a57604cb474461de9b83a41e060e566aec7cda9f97b13b8a863389fdb9e8d1e0`  
		Last Modified: Fri, 17 Apr 2026 00:12:07 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e6dbc4f00df61f7b993b5989d1ae85b34120c7254dc48a39b7554a4e2d5f30a`  
		Last Modified: Fri, 17 Apr 2026 00:12:07 GMT  
		Size: 2.0 KB (2014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:latest` - unknown; unknown

```console
$ docker pull arangodb@sha256:a86a513ef87e49fd6a45dc7bff6246ee53e5519bdf9dce03c8941f236e52d4d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **672.9 KB (672855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd2494114fede371c5b57028443fe30e2dad2783f0fe76efcdbf94d217834822`

```dockerfile
```

-	Layers:
	-	`sha256:66ed6a0f798ede4057ce584d1138a57f91a7dd9cd259339f2d5795c44d44719f`  
		Last Modified: Fri, 17 Apr 2026 00:12:07 GMT  
		Size: 658.2 KB (658236 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7036dd98875b1bc2cc293585f1e61e44709bbd3ad684ad4335ec82ba4d7fe55`  
		Last Modified: Fri, 17 Apr 2026 00:12:07 GMT  
		Size: 14.6 KB (14619 bytes)  
		MIME: application/vnd.in-toto+json
