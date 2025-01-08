## `arangodb:latest`

```console
$ docker pull arangodb@sha256:c33fdeaba92afdf00223190c99ad2145bef5ac0ca750d14d364cf0681ef82778
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `arangodb:latest` - linux; amd64

```console
$ docker pull arangodb@sha256:4e628e0f7f6207f61cea4403e4d3f4bd13d56fe1269d43841aa6470b5e284e47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.0 MB (304972016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16f1bc16513cc57b2c1917ca50f8bfc8c858390f0071d1ba24a1e698994424a2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 13 Dec 2024 15:32:12 GMT
ADD alpine-minirootfs-3.18.10-x86_64.tar.gz / # buildkit
# Fri, 13 Dec 2024 15:32:12 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 15:32:12 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Fri, 13 Dec 2024 15:32:12 GMT
ENV ARANGO_VERSION=3.12.3
# Fri, 13 Dec 2024 15:32:12 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8003EDF6F05459984878D4A6C04AD0FD86FEC04D &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb312/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg # buildkit
# Fri, 13 Dec 2024 15:32:12 GMT
ENV GLIBCXX_FORCE_NEW=1
# Fri, 13 Dec 2024 15:32:12 GMT
RUN echo "UTC" > /etc/timezone # buildkit
# Fri, 13 Dec 2024 15:32:12 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Fri, 13 Dec 2024 15:32:12 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 13 Dec 2024 15:32:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 13 Dec 2024 15:32:12 GMT
EXPOSE map[8529/tcp:{}]
# Fri, 13 Dec 2024 15:32:12 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:5fa62e1bbddf13eb6443e20aa8ed938bec91a8a5d5d0a26e58e8eafb3ada9a1c`  
		Last Modified: Tue, 07 Jan 2025 02:28:37 GMT  
		Size: 3.4 MB (3407632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afbf11229f90d63e134ecbba3c7ae2cca5ac5999024c047fee6c57165aab9c24`  
		Last Modified: Tue, 07 Jan 2025 03:14:40 GMT  
		Size: 301.6 MB (301562228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e04f7e25502cc7d4e11aa930e7ea544213c22c7ba8aadec7127d41beb6ae2b2`  
		Last Modified: Tue, 07 Jan 2025 03:14:36 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec376324cb0972efed8b6f9183e6f78ba4f3c069c46d448466c95a672f5319e9`  
		Last Modified: Tue, 07 Jan 2025 03:14:36 GMT  
		Size: 2.0 KB (2016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:latest` - unknown; unknown

```console
$ docker pull arangodb@sha256:7743a6731316c56510e09981baef0ef09042e7fbcb315e3630806b467cb6b6e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **376.7 KB (376740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ff6780334b88ef7de3dd06bee4ce614f5313057111cc5c70c0425e8d731c722`

```dockerfile
```

-	Layers:
	-	`sha256:269bab6665f1b334c1f34c22e3d6363bd8bf0cd24e55b7d69591df0c8e75494b`  
		Last Modified: Tue, 07 Jan 2025 03:14:36 GMT  
		Size: 362.3 KB (362320 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ccd09f6814ef304a72499307a47a1590ccb224300202e5b95d7a10944ff97431`  
		Last Modified: Tue, 07 Jan 2025 03:14:36 GMT  
		Size: 14.4 KB (14420 bytes)  
		MIME: application/vnd.in-toto+json

### `arangodb:latest` - linux; arm64 variant v8

```console
$ docker pull arangodb@sha256:a0c43b73388d67302ee275e753d25735b1b9d44c9365d6c8c1cfae25d8358c53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.0 MB (307023576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45c9a50b96e96c1fcd79e0c940651295d2ec92f605b44edb1d4ef5a45584e3a4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 13 Dec 2024 15:32:12 GMT
ADD alpine-minirootfs-3.18.11-aarch64.tar.gz / # buildkit
# Fri, 13 Dec 2024 15:32:12 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 15:32:12 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Fri, 13 Dec 2024 15:32:12 GMT
ENV ARANGO_VERSION=3.12.3
# Fri, 13 Dec 2024 15:32:12 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8003EDF6F05459984878D4A6C04AD0FD86FEC04D &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb312/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg # buildkit
# Fri, 13 Dec 2024 15:32:12 GMT
ENV GLIBCXX_FORCE_NEW=1
# Fri, 13 Dec 2024 15:32:12 GMT
RUN echo "UTC" > /etc/timezone # buildkit
# Fri, 13 Dec 2024 15:32:12 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Fri, 13 Dec 2024 15:32:12 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 13 Dec 2024 15:32:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 13 Dec 2024 15:32:12 GMT
EXPOSE map[8529/tcp:{}]
# Fri, 13 Dec 2024 15:32:12 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:f6b431426dd566e612639f03cd46e521b3133a043bb6b60edeeeef80d513e870`  
		Last Modified: Wed, 08 Jan 2025 17:24:31 GMT  
		Size: 3.3 MB (3341861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:399e87667dbf8485916ec5591df0028fe095f3edce1549049cec4edb0278a760`  
		Last Modified: Wed, 08 Jan 2025 18:08:07 GMT  
		Size: 303.7 MB (303679559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63ded694ad352635c791018a1bd16112c9acb0474761bea48533a257db2bb816`  
		Last Modified: Wed, 08 Jan 2025 18:07:57 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1118b145252942dca477375962823451a7c5bc835f80dcb14321bfdf21076646`  
		Last Modified: Wed, 08 Jan 2025 18:07:57 GMT  
		Size: 2.0 KB (2016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:latest` - unknown; unknown

```console
$ docker pull arangodb@sha256:e6cf5739648df446404e1db3dbf8dba54d592163517b484f3eebcda92c08e07e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **482.0 KB (481985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44d2398c20dab7b0858935f6f72b52956888e65098f22e230f78fee23d6f7b54`

```dockerfile
```

-	Layers:
	-	`sha256:7f4780997539bed07671ab41ce8e7a4bcfda7a128f44495742acbc79456c4b28`  
		Last Modified: Wed, 08 Jan 2025 18:07:58 GMT  
		Size: 467.5 KB (467457 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be56b6c3547e9febbc69d02a80c63feac44d63c328ba7e5d9948880c3c0ad756`  
		Last Modified: Wed, 08 Jan 2025 18:07:57 GMT  
		Size: 14.5 KB (14528 bytes)  
		MIME: application/vnd.in-toto+json
