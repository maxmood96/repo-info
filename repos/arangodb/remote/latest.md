## `arangodb:latest`

```console
$ docker pull arangodb@sha256:b7cc8dbf5f24c0fe235b6e50a26dbcfaebaf9abe0d322acefcf3dab63b5a0102
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `arangodb:latest` - linux; amd64

```console
$ docker pull arangodb@sha256:8ec63e60fcb954e7108a308795f562dafd285552aaf0d4f9824782b8be6d48b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.8 MB (232804659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c91f56b449ee93e28fb334072fb8b1d23a6baacdf73a7285467265899a878fdd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Wed, 29 Jan 2025 11:48:08 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Wed, 29 Jan 2025 11:48:08 GMT
CMD ["/bin/sh"]
# Wed, 29 Jan 2025 11:48:08 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Wed, 29 Jan 2025 11:48:08 GMT
ENV ARANGO_VERSION=3.12.4
# Wed, 29 Jan 2025 11:48:08 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8003EDF6F05459984878D4A6C04AD0FD86FEC04D &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb312/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg # buildkit
# Wed, 29 Jan 2025 11:48:08 GMT
ENV GLIBCXX_FORCE_NEW=1
# Wed, 29 Jan 2025 11:48:08 GMT
RUN echo "UTC" > /etc/timezone # buildkit
# Wed, 29 Jan 2025 11:48:08 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Wed, 29 Jan 2025 11:48:08 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 29 Jan 2025 11:48:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 29 Jan 2025 11:48:08 GMT
EXPOSE map[8529/tcp:{}]
# Wed, 29 Jan 2025 11:48:08 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6c74b8fc358e5cd758a39a8cb609904e55b1fc5f7fa5831fb157886e5599e47`  
		Last Modified: Fri, 14 Feb 2025 22:14:01 GMT  
		Size: 229.2 MB (229160256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05a93864b83fa1e50e6679ffd3ad565a60e92a6ed51e33d4f97667acffa48834`  
		Last Modified: Fri, 14 Feb 2025 22:13:53 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a82bed114865afd11ccf2719c7cca1f6e79c860b76f327275324d060bf7f6f1`  
		Last Modified: Fri, 14 Feb 2025 22:13:53 GMT  
		Size: 2.0 KB (2016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:latest` - unknown; unknown

```console
$ docker pull arangodb@sha256:796bd3496b11301bed127244ec2f4cb75f998fdfcc7e981826f25d4951d76d8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **405.4 KB (405444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1d1012c5cef89ed733f225e7dab0c7e42e53d770f4f9861e05964ae3cf438b6`

```dockerfile
```

-	Layers:
	-	`sha256:76ae3dd6fddf6a30bdc1192b7249277400a0fe27ad5c6158f64fbfed5d26a80d`  
		Last Modified: Fri, 14 Feb 2025 22:13:18 GMT  
		Size: 391.1 KB (391059 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:041b9a4b47fdc7120dafb59c96a339c2165eb20a6893b6915b4b98f94c9fe9c1`  
		Last Modified: Fri, 14 Feb 2025 22:13:18 GMT  
		Size: 14.4 KB (14385 bytes)  
		MIME: application/vnd.in-toto+json

### `arangodb:latest` - linux; arm64 variant v8

```console
$ docker pull arangodb@sha256:eb4a6a29676756240e3cdce070139b2e3155f8a816c27003def644fbb95f482f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.5 MB (231494960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee653d3b531327ae13507d3ddc31087149e283ea91975c05fe8eca7d6a3d8cba`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Wed, 29 Jan 2025 11:48:08 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Wed, 29 Jan 2025 11:48:08 GMT
CMD ["/bin/sh"]
# Wed, 29 Jan 2025 11:48:08 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Wed, 29 Jan 2025 11:48:08 GMT
ENV ARANGO_VERSION=3.12.4
# Wed, 29 Jan 2025 11:48:08 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8003EDF6F05459984878D4A6C04AD0FD86FEC04D &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb312/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg # buildkit
# Wed, 29 Jan 2025 11:48:08 GMT
ENV GLIBCXX_FORCE_NEW=1
# Wed, 29 Jan 2025 11:48:08 GMT
RUN echo "UTC" > /etc/timezone # buildkit
# Wed, 29 Jan 2025 11:48:08 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Wed, 29 Jan 2025 11:48:08 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 29 Jan 2025 11:48:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 29 Jan 2025 11:48:08 GMT
EXPOSE map[8529/tcp:{}]
# Wed, 29 Jan 2025 11:48:08 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:200038a661537fcff0a106bde53fd78550efad67a7943fb5b6cbc76e592187c9`  
		Last Modified: Sat, 15 Feb 2025 02:48:13 GMT  
		Size: 227.5 MB (227499775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fd41fcf3c0c1828661abc790d0bab8793bb4e0ea394065dfd7381511992bc19`  
		Last Modified: Sat, 15 Feb 2025 02:47:58 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01e675dad5f2faa04d96bd057f106ac8ac5a80c5a751331e2cd44ad62d68cc38`  
		Last Modified: Sat, 15 Feb 2025 02:47:57 GMT  
		Size: 2.0 KB (2016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:latest` - unknown; unknown

```console
$ docker pull arangodb@sha256:e857d3c5c582fe3d1b9e3e20b35cefe52d002a216addcdccacf5dfe5a8c487d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **556.2 KB (556171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:897976928a4a0fd826ed46b0e3f1f679e8777939ecaa1e29bdf47bfbe024ecfa`

```dockerfile
```

-	Layers:
	-	`sha256:6bd6932583253630ac0c585e0f75db374b5ed452702f8b6a65c2c82f9e4e9680`  
		Last Modified: Sat, 15 Feb 2025 01:13:22 GMT  
		Size: 541.7 KB (541679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1dd2c8a40fbee90edcae77ffd82986510207e2b9ba75ea65b8fc637cdcbca5f6`  
		Last Modified: Sat, 15 Feb 2025 01:13:22 GMT  
		Size: 14.5 KB (14492 bytes)  
		MIME: application/vnd.in-toto+json
