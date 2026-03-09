## `arangodb:latest`

```console
$ docker pull arangodb@sha256:c7c73e4f2694d70dffcf4cea779ba60355e6563018550ea70bcb77ce8e35fb97
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `arangodb:latest` - linux; amd64

```console
$ docker pull arangodb@sha256:d92629226f63d208d86bd6911538262b0ace7916bd977e5e9ef8a0a357090b43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.0 MB (259957970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b76ff4c299a723011197590e03c537ee955c77b76f553a0e5524a6348a65275e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:43 GMT
ADD alpine-minirootfs-3.21.6-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:43 GMT
CMD ["/bin/sh"]
# Mon, 09 Mar 2026 18:04:25 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Mon, 09 Mar 2026 18:04:25 GMT
ENV ARANGO_VERSION=3.12.8
# Mon, 09 Mar 2026 18:04:25 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8003EDF6F05459984878D4A6C04AD0FD86FEC04D &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/9c169fe900ff79790395784287bfa82f0dc0059375a34a2881b9b745c8efd42e/arangodb312/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3e_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg # buildkit
# Mon, 09 Mar 2026 18:04:25 GMT
ENV GLIBCXX_FORCE_NEW=1
# Mon, 09 Mar 2026 18:04:25 GMT
RUN echo "UTC" > /etc/timezone # buildkit
# Mon, 09 Mar 2026 18:04:25 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Mon, 09 Mar 2026 18:04:25 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 09 Mar 2026 18:04:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Mar 2026 18:04:25 GMT
EXPOSE map[8529/tcp:{}]
# Mon, 09 Mar 2026 18:04:25 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:bc1da058f299723f8258c5a82dd007d1dd72e275087b726d5e1be5ef6198f286`  
		Last Modified: Wed, 28 Jan 2026 01:18:49 GMT  
		Size: 3.6 MB (3643742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b5c5ee847de394f0379cb6b1426f73ab315fa4d6db8bb7c354613b5ead4cf20`  
		Last Modified: Mon, 09 Mar 2026 18:04:58 GMT  
		Size: 256.3 MB (256312074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba77b1e8914ccf0ec023665ec4b30e17a6b2345662f2d3dd656e07d1cb3d793d`  
		Last Modified: Mon, 09 Mar 2026 18:04:52 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87db348bbb11cff8de0be398281942570fafee3aa996e285976c9e8a08aec6be`  
		Last Modified: Mon, 09 Mar 2026 18:04:52 GMT  
		Size: 2.0 KB (2014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:latest` - unknown; unknown

```console
$ docker pull arangodb@sha256:a6481c2ffaeb8376f9ce0e06f5eb3c91e88e837af9203579fd52af0124e09134
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **521.8 KB (521813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e17c9439390bb208f88e9f23e0d05376583716f0b087f55e68dc6fe9e5f0b0c6`

```dockerfile
```

-	Layers:
	-	`sha256:6ec92167b0792f6d4bda820ca66ec4c241e81a586802ffda97819318e4b5a2e3`  
		Last Modified: Mon, 09 Mar 2026 18:04:52 GMT  
		Size: 507.3 KB (507301 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4965b2b3ea57f2a6069fb3b7d755cacd7e3afa744e0aadfc4ed58ef37253a058`  
		Last Modified: Mon, 09 Mar 2026 18:04:52 GMT  
		Size: 14.5 KB (14512 bytes)  
		MIME: application/vnd.in-toto+json

### `arangodb:latest` - linux; arm64 variant v8

```console
$ docker pull arangodb@sha256:34ea0b13e4da69a60090820ea5b0f1ebc3fc52ec9488619b5b8e12afff8488e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.9 MB (258850994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bcbc364a5f8442a23c48fc1f8c680b135b65d1a86b2365b284f32049a1f3202`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:07 GMT
ADD alpine-minirootfs-3.21.6-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:07 GMT
CMD ["/bin/sh"]
# Mon, 09 Mar 2026 18:03:44 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Mon, 09 Mar 2026 18:03:44 GMT
ENV ARANGO_VERSION=3.12.8
# Mon, 09 Mar 2026 18:03:44 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8003EDF6F05459984878D4A6C04AD0FD86FEC04D &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/9c169fe900ff79790395784287bfa82f0dc0059375a34a2881b9b745c8efd42e/arangodb312/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3e_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg # buildkit
# Mon, 09 Mar 2026 18:03:44 GMT
ENV GLIBCXX_FORCE_NEW=1
# Mon, 09 Mar 2026 18:03:44 GMT
RUN echo "UTC" > /etc/timezone # buildkit
# Mon, 09 Mar 2026 18:03:44 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Mon, 09 Mar 2026 18:03:44 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 09 Mar 2026 18:03:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Mar 2026 18:03:44 GMT
EXPOSE map[8529/tcp:{}]
# Mon, 09 Mar 2026 18:03:44 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:a447a5de8f4eb4a987d81c0afa14d459cc714599c020c08f45fafa9c6c904b30`  
		Last Modified: Wed, 28 Jan 2026 01:18:13 GMT  
		Size: 4.0 MB (3992880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d415eb5c9a67f92c2fd749016df71c44d0380e72f41f8860b79d9ab442dd731`  
		Last Modified: Mon, 09 Mar 2026 18:04:18 GMT  
		Size: 254.9 MB (254855962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7df68f20680237d2abdd3421206f8ef681b04df75c9013cd71ea826da424737`  
		Last Modified: Mon, 09 Mar 2026 18:04:12 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f08164b3a600f9a09191eacc3a4a1f98ed080fcf1444a67392bdd8a851dbed43`  
		Last Modified: Mon, 09 Mar 2026 18:04:12 GMT  
		Size: 2.0 KB (2014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:latest` - unknown; unknown

```console
$ docker pull arangodb@sha256:fc33cb947695ff1b059d84b6d972f97ecfcbd5212a5b8ebba5dd9901eaf78ff5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **672.5 KB (672540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:244403daf1e70565d0fad88244d231f6419fa79a9474993c26acdb3a5f5c75b8`

```dockerfile
```

-	Layers:
	-	`sha256:b5c00608fb2ec255e3cf56e3f902853b2b6c711262123cf63d7bf6a7f985ea45`  
		Last Modified: Mon, 09 Mar 2026 18:04:12 GMT  
		Size: 657.9 KB (657921 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8793bb4ddb06b99fe11f79f5fffd9b18133c6ca7a30a2c22d810873e7fdde373`  
		Last Modified: Mon, 09 Mar 2026 18:04:12 GMT  
		Size: 14.6 KB (14619 bytes)  
		MIME: application/vnd.in-toto+json
