## `arangodb:latest`

```console
$ docker pull arangodb@sha256:843b99d2c5db44502ec058b67bb69b30c9ba2a009bfddff3555844d9f9c1050a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `arangodb:latest` - linux; amd64

```console
$ docker pull arangodb@sha256:bc8d975c5c4d623ecfda6e99740948ea2bd3654ac6002489d46e8670a7d30536
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.8 MB (232804164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad19c4d889a5e9fae8663371719623a7ec39c3b2ac5c5c4f9bc7cd1928577394`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
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
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Tue, 14 Jan 2025 20:33:02 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21cbbaa4ffe75c1fa2ee581499014cda04af03762d814c019aeb5b057409ced5`  
		Last Modified: Mon, 03 Feb 2025 22:38:50 GMT  
		Size: 229.2 MB (229160293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1789fa35d31f5466d129c9f53cf6f9de32eb3de7b5a091e83ca808027759bec4`  
		Last Modified: Mon, 03 Feb 2025 20:35:18 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dff4beaebc6f3bd7bb258dd5dc4fa13d97341ae2804d59cf7b98a67b8247443d`  
		Last Modified: Mon, 03 Feb 2025 20:40:00 GMT  
		Size: 2.0 KB (2016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:latest` - unknown; unknown

```console
$ docker pull arangodb@sha256:1abc0ae3b9df4e253aff5ba8279514aec44c84df075ef5364c01366e444a714a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **405.4 KB (405438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3285e266c7f04af6a3a9a2305561f812d5e877ea4c1a643d41207187efd7dac`

```dockerfile
```

-	Layers:
	-	`sha256:b3ae0bf81aa0773991934640dbe8c8158f77b65489552355fd3afd131bcda7cb`  
		Last Modified: Thu, 13 Feb 2025 08:58:20 GMT  
		Size: 391.1 KB (391053 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c30e0e20a8ec3e41d05d70284f5111f304bd866a6be83b7d2fcefe60b7badf44`  
		Last Modified: Thu, 13 Feb 2025 08:58:20 GMT  
		Size: 14.4 KB (14385 bytes)  
		MIME: application/vnd.in-toto+json

### `arangodb:latest` - linux; arm64 variant v8

```console
$ docker pull arangodb@sha256:8e9292e26f360ae00244947ff7ddef294dd243c2a7e24ac50f4f072935c96fb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.5 MB (231494150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9db9559a27854b251ff9d328df983e3d76bf7c39d6782d5b767a39abb79e48a2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
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
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Tue, 14 Jan 2025 20:33:00 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:515a952c8c2ffd929bafe060d52b05e0dca8460c73105534f31e6d3c7fb5e706`  
		Last Modified: Tue, 04 Feb 2025 08:10:27 GMT  
		Size: 227.5 MB (227499636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6729615bb223164967441285bba1fc52be7a38cc152de417e459852d45b5450`  
		Last Modified: Mon, 03 Feb 2025 21:13:17 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f18d1e1ea093090fbc2f2828633e471bb1a2e15ddbdd820532d22956c9b08b00`  
		Last Modified: Tue, 04 Feb 2025 12:01:03 GMT  
		Size: 2.0 KB (2015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:latest` - unknown; unknown

```console
$ docker pull arangodb@sha256:af3c1d27e6d6c9dda484441a81d392209534988a0ea8c5aae7077de75fd789ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **556.2 KB (556165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c35a419ae7cce3478c1dd4520ec669de4dfca66f075c04e5e2d6cba13e3e7227`

```dockerfile
```

-	Layers:
	-	`sha256:25c6838add58351336f00a30f6634cec375168646d40fc44d4cb93d097ca925c`  
		Last Modified: Thu, 13 Feb 2025 08:58:39 GMT  
		Size: 541.7 KB (541673 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:123f0abbca3a954c871c66c9ef1c9eb76231ec8ccd250aaf63479a3579d10128`  
		Last Modified: Thu, 13 Feb 2025 08:58:38 GMT  
		Size: 14.5 KB (14492 bytes)  
		MIME: application/vnd.in-toto+json
