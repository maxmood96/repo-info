<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `arangodb`

-	[`arangodb:3.11`](#arangodb311)
-	[`arangodb:3.11.11`](#arangodb31111)
-	[`arangodb:3.12`](#arangodb312)
-	[`arangodb:3.12.2`](#arangodb3122)
-	[`arangodb:latest`](#arangodblatest)

## `arangodb:3.11`

```console
$ docker pull arangodb@sha256:f2466832640014a4667c146f3ce2cdbb78d0c3bc55460a87d4bb281ef70c777e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `arangodb:3.11` - linux; amd64

```console
$ docker pull arangodb@sha256:9a8033e19640ae75307fae5bd58cfb00faefbe2c2a09937b5a4bc6bce7f9220c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.9 MB (198901593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c39bb727646011985dfc2ce5222ee07dd7db87c18f4a2a475b19e4b6aa305e9c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Sat, 06 Jul 2024 14:26:56 GMT
ADD file:8bf458f5fbed9f27c897506538c02fb5810b70aba850bb883d2120985fa15bac in / 
# Sat, 06 Jul 2024 14:26:56 GMT
CMD ["/bin/sh"]
# Sat, 06 Jul 2024 14:26:56 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Sat, 06 Jul 2024 14:26:56 GMT
ENV ARANGO_VERSION=3.11.10.1
# Sat, 06 Jul 2024 14:26:56 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb311/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg # buildkit
# Sat, 06 Jul 2024 14:26:56 GMT
ENV GLIBCXX_FORCE_NEW=1
# Sat, 06 Jul 2024 14:26:56 GMT
RUN echo "UTC" > /etc/timezone # buildkit
# Sat, 06 Jul 2024 14:26:56 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Sat, 06 Jul 2024 14:26:56 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Sat, 06 Jul 2024 14:26:56 GMT
COPY docker-foxx.sh /usr/bin/foxx # buildkit
# Sat, 06 Jul 2024 14:26:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 06 Jul 2024 14:26:56 GMT
EXPOSE map[8529/tcp:{}]
# Sat, 06 Jul 2024 14:26:56 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:a0f4cbe03b6df9e61ce02b3c41bbc05481842858bd48d9687614abe719303b47`  
		Last Modified: Fri, 06 Sep 2024 22:21:07 GMT  
		Size: 3.4 MB (3392194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28a8d1cec32315e07f21b2b2baea56745aba9448908b184b6e76907852ea00c5`  
		Last Modified: Fri, 06 Sep 2024 23:15:33 GMT  
		Size: 195.5 MB (195506914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f5024e3590883f76714846de34b994b8fc2ec7cfca0a313c6830ee50eaf790c`  
		Last Modified: Fri, 06 Sep 2024 23:15:30 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a47b34a27c7e3270270ece469185932dedb602b33572de5ca83541852134250`  
		Last Modified: Fri, 06 Sep 2024 23:15:30 GMT  
		Size: 2.1 KB (2088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9168eae5d3d5390a64d3b3e45cfa29a325e743641fa954ea08bf877e337ddb74`  
		Last Modified: Fri, 06 Sep 2024 23:15:31 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:3.11` - unknown; unknown

```console
$ docker pull arangodb@sha256:4cc17f3a0e14db924535ff4be825134c81586b03927c9a3eff125ccd68b9fe48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **964.0 KB (964017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e3c4c283b5cdac46f0263b3cebfb3da3af0d657a40627f5a4c0dcb206948f8e`

```dockerfile
```

-	Layers:
	-	`sha256:956a9c705ef311a9f3b6a5a3fc7504fbc7e39024f582081eb6812b1ea82149b5`  
		Last Modified: Fri, 06 Sep 2024 23:15:30 GMT  
		Size: 948.4 KB (948406 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf13d2e2e04909763d86c1cd4b820b64417f1897f834a4b0df2ec50e857c3845`  
		Last Modified: Fri, 06 Sep 2024 23:15:30 GMT  
		Size: 15.6 KB (15611 bytes)  
		MIME: application/vnd.in-toto+json

### `arangodb:3.11` - linux; arm64 variant v8

```console
$ docker pull arangodb@sha256:cce62d79b752f298a4b099f4cf2e89f773cd493139065c6e3a6c925c499a690a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.2 MB (202199351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c94359c491a02791bc998cf046a0dc15c93bcedd7cc7a380e2dc1fcdfc0bf4c7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Sat, 06 Jul 2024 14:26:56 GMT
ADD file:e3f989df31d7e2d820078058c5d0ed7d98695c5b86bd172276270ebb59d75ee6 in / 
# Sat, 06 Jul 2024 14:26:56 GMT
CMD ["/bin/sh"]
# Sat, 06 Jul 2024 14:26:56 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Sat, 06 Jul 2024 14:26:56 GMT
ENV ARANGO_VERSION=3.11.10.1
# Sat, 06 Jul 2024 14:26:56 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb311/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg # buildkit
# Sat, 06 Jul 2024 14:26:56 GMT
ENV GLIBCXX_FORCE_NEW=1
# Sat, 06 Jul 2024 14:26:56 GMT
RUN echo "UTC" > /etc/timezone # buildkit
# Sat, 06 Jul 2024 14:26:56 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Sat, 06 Jul 2024 14:26:56 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Sat, 06 Jul 2024 14:26:56 GMT
COPY docker-foxx.sh /usr/bin/foxx # buildkit
# Sat, 06 Jul 2024 14:26:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 06 Jul 2024 14:26:56 GMT
EXPOSE map[8529/tcp:{}]
# Sat, 06 Jul 2024 14:26:56 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:4a3d188841b4b0359cda0d73dc5f89f8bc569f3bcb178cfd0507b4ead0db7bf4`  
		Last Modified: Fri, 06 Sep 2024 22:45:06 GMT  
		Size: 3.3 MB (3275072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:357bd4e9eb4ddc89889ab9190907a04af60c98cfe8e07e6c9c8c3d706cfaa622`  
		Last Modified: Sat, 07 Sep 2024 02:45:55 GMT  
		Size: 198.9 MB (198921795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22eae1d1bebef8f72380fab255a32b7207ad28c9a437e6cbf4c9245dd43fbb35`  
		Last Modified: Sat, 07 Sep 2024 02:45:50 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0df2594419b9434e8626dcedc569eaac80245d7aa2a9df877bb1189ccfcd7cb3`  
		Last Modified: Sat, 07 Sep 2024 02:45:50 GMT  
		Size: 2.1 KB (2087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d141e4561e093c49f373fa8e73c6d62ad498e9c5e8afa099a1de1a0e0699068a`  
		Last Modified: Sat, 07 Sep 2024 02:45:51 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:3.11` - unknown; unknown

```console
$ docker pull arangodb@sha256:0d34d8218630eb1817ae07b59ab160a568aef7d23feba7601f716129e2ea1e43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1069580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa92748ef9487fb13ddd13269ea2e516d6f1a44aeb185721d2f1093483ffaa97`

```dockerfile
```

-	Layers:
	-	`sha256:ff28cd46a15d71f685b852b605538ea7db202393b84c2096c7ff6f57e78f57de`  
		Last Modified: Sat, 07 Sep 2024 02:45:50 GMT  
		Size: 1.1 MB (1053693 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0e19e7a9131c2a9042759f33665487b5ac9c4568f10d233fbb348a6c1a710f4`  
		Last Modified: Sat, 07 Sep 2024 02:45:50 GMT  
		Size: 15.9 KB (15887 bytes)  
		MIME: application/vnd.in-toto+json

## `arangodb:3.11.11`

**does not exist** (yet?)

## `arangodb:3.12`

```console
$ docker pull arangodb@sha256:86900a367435d28e68c5ea023f074887f446a2a0c31d4eae3d7812ef9bc4f6aa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `arangodb:3.12` - linux; amd64

```console
$ docker pull arangodb@sha256:1116070d437ec3d4bc57691d52ce1bfee8496a8bb34d0c73c19896bed0fbc3d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.9 MB (302882938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b065f7e6170743361c0924f465c62f3ab5a536eed80b27ed0ce07dd4deeebd2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Tue, 27 Aug 2024 15:12:16 GMT
ADD file:8bf458f5fbed9f27c897506538c02fb5810b70aba850bb883d2120985fa15bac in / 
# Tue, 27 Aug 2024 15:12:16 GMT
CMD ["/bin/sh"]
# Tue, 27 Aug 2024 15:12:16 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Tue, 27 Aug 2024 15:12:16 GMT
ENV ARANGO_VERSION=3.12.2
# Tue, 27 Aug 2024 15:12:16 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8003EDF6F05459984878D4A6C04AD0FD86FEC04D &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb312/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg # buildkit
# Tue, 27 Aug 2024 15:12:16 GMT
ENV GLIBCXX_FORCE_NEW=1
# Tue, 27 Aug 2024 15:12:16 GMT
RUN echo "UTC" > /etc/timezone # buildkit
# Tue, 27 Aug 2024 15:12:16 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Tue, 27 Aug 2024 15:12:16 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 27 Aug 2024 15:12:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 27 Aug 2024 15:12:16 GMT
EXPOSE map[8529/tcp:{}]
# Tue, 27 Aug 2024 15:12:16 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:a0f4cbe03b6df9e61ce02b3c41bbc05481842858bd48d9687614abe719303b47`  
		Last Modified: Fri, 06 Sep 2024 22:21:07 GMT  
		Size: 3.4 MB (3392194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49a1f452304f4c30119e5711de9c5cde32028436b3418d3fdac26994d21194b7`  
		Last Modified: Fri, 06 Sep 2024 23:15:34 GMT  
		Size: 299.5 MB (299488588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cf357aa9fa450477bae167fd108ff01273d3c63731898bf1d79ffdd23aec29e`  
		Last Modified: Fri, 06 Sep 2024 23:15:30 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cbf4ac60298128ae88a19a2838044a9bedc05191c90540ca3112ac02b44d6e9`  
		Last Modified: Fri, 06 Sep 2024 23:15:30 GMT  
		Size: 2.0 KB (2016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:3.12` - unknown; unknown

```console
$ docker pull arangodb@sha256:6e8cb3815727ccb200f4f86f85fca645479e7071f469a9bcb2f5e6933b79d57d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **361.5 KB (361542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8b49375ad3fd2b5c90a7b49f4fd7c148e5ca0810ebad955d54d8e16cd83a340`

```dockerfile
```

-	Layers:
	-	`sha256:48331eb50787bc4daa1e60cc3a5e848a12b33de2a440e3de6228a8a4f58f9040`  
		Last Modified: Fri, 06 Sep 2024 23:15:31 GMT  
		Size: 347.4 KB (347390 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa77f4a14b212ced8573b6fa04b43f9c086d0fb680f06bb38177a859c4b40150`  
		Last Modified: Fri, 06 Sep 2024 23:15:30 GMT  
		Size: 14.2 KB (14152 bytes)  
		MIME: application/vnd.in-toto+json

### `arangodb:3.12` - linux; arm64 variant v8

```console
$ docker pull arangodb@sha256:0dc3cc2632158e7292309629cf33b0401c6901b53f8c633c06133f0cc8a0c3eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.7 MB (304675738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d42fd3351c3ef519fbec5a4ec501809ba8e52dea42b4f728222bf8e1c096b6a6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Tue, 27 Aug 2024 15:12:16 GMT
ADD file:e3f989df31d7e2d820078058c5d0ed7d98695c5b86bd172276270ebb59d75ee6 in / 
# Tue, 27 Aug 2024 15:12:16 GMT
CMD ["/bin/sh"]
# Tue, 27 Aug 2024 15:12:16 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Tue, 27 Aug 2024 15:12:16 GMT
ENV ARANGO_VERSION=3.12.2
# Tue, 27 Aug 2024 15:12:16 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8003EDF6F05459984878D4A6C04AD0FD86FEC04D &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb312/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg # buildkit
# Tue, 27 Aug 2024 15:12:16 GMT
ENV GLIBCXX_FORCE_NEW=1
# Tue, 27 Aug 2024 15:12:16 GMT
RUN echo "UTC" > /etc/timezone # buildkit
# Tue, 27 Aug 2024 15:12:16 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Tue, 27 Aug 2024 15:12:16 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 27 Aug 2024 15:12:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 27 Aug 2024 15:12:16 GMT
EXPOSE map[8529/tcp:{}]
# Tue, 27 Aug 2024 15:12:16 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:4a3d188841b4b0359cda0d73dc5f89f8bc569f3bcb178cfd0507b4ead0db7bf4`  
		Last Modified: Fri, 06 Sep 2024 22:45:06 GMT  
		Size: 3.3 MB (3275072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cf7966d79f14a85391123be39cca32586ba4f7500728c5daeca5fdb623b0e8d`  
		Last Modified: Sat, 07 Sep 2024 04:18:35 GMT  
		Size: 301.4 MB (301398510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84f8fcaf4551340a01b8982880a08d0cbde8e6e66b15ba167b26543a9c697445`  
		Last Modified: Sat, 07 Sep 2024 04:18:29 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5249cc2ab632e58d18be46e53425e146cfe0d2ad0ef378241ee586f5552f64d`  
		Last Modified: Sat, 07 Sep 2024 04:18:29 GMT  
		Size: 2.0 KB (2016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:3.12` - unknown; unknown

```console
$ docker pull arangodb@sha256:195e356b696c821ab8e39b50c622f7c1be703b4ce8efa13bf578555c6362c534
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **467.1 KB (467129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:714bbca94d370022c14f72fde61686228c0839192ff117db2e654be54787271a`

```dockerfile
```

-	Layers:
	-	`sha256:32dea479efdcee2e8752a57510dcd823c08ad9889dade0e9d7f1e9d249ce82ab`  
		Last Modified: Sat, 07 Sep 2024 04:18:29 GMT  
		Size: 452.7 KB (452689 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65765fe83c5b07f248b8cd5b8daa3876c3b97584729483428f2a3b819e5eab54`  
		Last Modified: Sat, 07 Sep 2024 04:18:29 GMT  
		Size: 14.4 KB (14440 bytes)  
		MIME: application/vnd.in-toto+json

## `arangodb:3.12.2`

```console
$ docker pull arangodb@sha256:86900a367435d28e68c5ea023f074887f446a2a0c31d4eae3d7812ef9bc4f6aa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `arangodb:3.12.2` - linux; amd64

```console
$ docker pull arangodb@sha256:1116070d437ec3d4bc57691d52ce1bfee8496a8bb34d0c73c19896bed0fbc3d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.9 MB (302882938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b065f7e6170743361c0924f465c62f3ab5a536eed80b27ed0ce07dd4deeebd2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Tue, 27 Aug 2024 15:12:16 GMT
ADD file:8bf458f5fbed9f27c897506538c02fb5810b70aba850bb883d2120985fa15bac in / 
# Tue, 27 Aug 2024 15:12:16 GMT
CMD ["/bin/sh"]
# Tue, 27 Aug 2024 15:12:16 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Tue, 27 Aug 2024 15:12:16 GMT
ENV ARANGO_VERSION=3.12.2
# Tue, 27 Aug 2024 15:12:16 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8003EDF6F05459984878D4A6C04AD0FD86FEC04D &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb312/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg # buildkit
# Tue, 27 Aug 2024 15:12:16 GMT
ENV GLIBCXX_FORCE_NEW=1
# Tue, 27 Aug 2024 15:12:16 GMT
RUN echo "UTC" > /etc/timezone # buildkit
# Tue, 27 Aug 2024 15:12:16 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Tue, 27 Aug 2024 15:12:16 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 27 Aug 2024 15:12:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 27 Aug 2024 15:12:16 GMT
EXPOSE map[8529/tcp:{}]
# Tue, 27 Aug 2024 15:12:16 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:a0f4cbe03b6df9e61ce02b3c41bbc05481842858bd48d9687614abe719303b47`  
		Last Modified: Fri, 06 Sep 2024 22:21:07 GMT  
		Size: 3.4 MB (3392194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49a1f452304f4c30119e5711de9c5cde32028436b3418d3fdac26994d21194b7`  
		Last Modified: Fri, 06 Sep 2024 23:15:34 GMT  
		Size: 299.5 MB (299488588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cf357aa9fa450477bae167fd108ff01273d3c63731898bf1d79ffdd23aec29e`  
		Last Modified: Fri, 06 Sep 2024 23:15:30 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cbf4ac60298128ae88a19a2838044a9bedc05191c90540ca3112ac02b44d6e9`  
		Last Modified: Fri, 06 Sep 2024 23:15:30 GMT  
		Size: 2.0 KB (2016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:3.12.2` - unknown; unknown

```console
$ docker pull arangodb@sha256:6e8cb3815727ccb200f4f86f85fca645479e7071f469a9bcb2f5e6933b79d57d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **361.5 KB (361542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8b49375ad3fd2b5c90a7b49f4fd7c148e5ca0810ebad955d54d8e16cd83a340`

```dockerfile
```

-	Layers:
	-	`sha256:48331eb50787bc4daa1e60cc3a5e848a12b33de2a440e3de6228a8a4f58f9040`  
		Last Modified: Fri, 06 Sep 2024 23:15:31 GMT  
		Size: 347.4 KB (347390 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa77f4a14b212ced8573b6fa04b43f9c086d0fb680f06bb38177a859c4b40150`  
		Last Modified: Fri, 06 Sep 2024 23:15:30 GMT  
		Size: 14.2 KB (14152 bytes)  
		MIME: application/vnd.in-toto+json

### `arangodb:3.12.2` - linux; arm64 variant v8

```console
$ docker pull arangodb@sha256:0dc3cc2632158e7292309629cf33b0401c6901b53f8c633c06133f0cc8a0c3eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.7 MB (304675738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d42fd3351c3ef519fbec5a4ec501809ba8e52dea42b4f728222bf8e1c096b6a6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Tue, 27 Aug 2024 15:12:16 GMT
ADD file:e3f989df31d7e2d820078058c5d0ed7d98695c5b86bd172276270ebb59d75ee6 in / 
# Tue, 27 Aug 2024 15:12:16 GMT
CMD ["/bin/sh"]
# Tue, 27 Aug 2024 15:12:16 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Tue, 27 Aug 2024 15:12:16 GMT
ENV ARANGO_VERSION=3.12.2
# Tue, 27 Aug 2024 15:12:16 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8003EDF6F05459984878D4A6C04AD0FD86FEC04D &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb312/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg # buildkit
# Tue, 27 Aug 2024 15:12:16 GMT
ENV GLIBCXX_FORCE_NEW=1
# Tue, 27 Aug 2024 15:12:16 GMT
RUN echo "UTC" > /etc/timezone # buildkit
# Tue, 27 Aug 2024 15:12:16 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Tue, 27 Aug 2024 15:12:16 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 27 Aug 2024 15:12:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 27 Aug 2024 15:12:16 GMT
EXPOSE map[8529/tcp:{}]
# Tue, 27 Aug 2024 15:12:16 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:4a3d188841b4b0359cda0d73dc5f89f8bc569f3bcb178cfd0507b4ead0db7bf4`  
		Last Modified: Fri, 06 Sep 2024 22:45:06 GMT  
		Size: 3.3 MB (3275072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cf7966d79f14a85391123be39cca32586ba4f7500728c5daeca5fdb623b0e8d`  
		Last Modified: Sat, 07 Sep 2024 04:18:35 GMT  
		Size: 301.4 MB (301398510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84f8fcaf4551340a01b8982880a08d0cbde8e6e66b15ba167b26543a9c697445`  
		Last Modified: Sat, 07 Sep 2024 04:18:29 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5249cc2ab632e58d18be46e53425e146cfe0d2ad0ef378241ee586f5552f64d`  
		Last Modified: Sat, 07 Sep 2024 04:18:29 GMT  
		Size: 2.0 KB (2016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:3.12.2` - unknown; unknown

```console
$ docker pull arangodb@sha256:195e356b696c821ab8e39b50c622f7c1be703b4ce8efa13bf578555c6362c534
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **467.1 KB (467129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:714bbca94d370022c14f72fde61686228c0839192ff117db2e654be54787271a`

```dockerfile
```

-	Layers:
	-	`sha256:32dea479efdcee2e8752a57510dcd823c08ad9889dade0e9d7f1e9d249ce82ab`  
		Last Modified: Sat, 07 Sep 2024 04:18:29 GMT  
		Size: 452.7 KB (452689 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65765fe83c5b07f248b8cd5b8daa3876c3b97584729483428f2a3b819e5eab54`  
		Last Modified: Sat, 07 Sep 2024 04:18:29 GMT  
		Size: 14.4 KB (14440 bytes)  
		MIME: application/vnd.in-toto+json

## `arangodb:latest`

```console
$ docker pull arangodb@sha256:86900a367435d28e68c5ea023f074887f446a2a0c31d4eae3d7812ef9bc4f6aa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `arangodb:latest` - linux; amd64

```console
$ docker pull arangodb@sha256:1116070d437ec3d4bc57691d52ce1bfee8496a8bb34d0c73c19896bed0fbc3d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.9 MB (302882938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b065f7e6170743361c0924f465c62f3ab5a536eed80b27ed0ce07dd4deeebd2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Tue, 27 Aug 2024 15:12:16 GMT
ADD file:8bf458f5fbed9f27c897506538c02fb5810b70aba850bb883d2120985fa15bac in / 
# Tue, 27 Aug 2024 15:12:16 GMT
CMD ["/bin/sh"]
# Tue, 27 Aug 2024 15:12:16 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Tue, 27 Aug 2024 15:12:16 GMT
ENV ARANGO_VERSION=3.12.2
# Tue, 27 Aug 2024 15:12:16 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8003EDF6F05459984878D4A6C04AD0FD86FEC04D &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb312/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg # buildkit
# Tue, 27 Aug 2024 15:12:16 GMT
ENV GLIBCXX_FORCE_NEW=1
# Tue, 27 Aug 2024 15:12:16 GMT
RUN echo "UTC" > /etc/timezone # buildkit
# Tue, 27 Aug 2024 15:12:16 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Tue, 27 Aug 2024 15:12:16 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 27 Aug 2024 15:12:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 27 Aug 2024 15:12:16 GMT
EXPOSE map[8529/tcp:{}]
# Tue, 27 Aug 2024 15:12:16 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:a0f4cbe03b6df9e61ce02b3c41bbc05481842858bd48d9687614abe719303b47`  
		Last Modified: Fri, 06 Sep 2024 22:21:07 GMT  
		Size: 3.4 MB (3392194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49a1f452304f4c30119e5711de9c5cde32028436b3418d3fdac26994d21194b7`  
		Last Modified: Fri, 06 Sep 2024 23:15:34 GMT  
		Size: 299.5 MB (299488588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cf357aa9fa450477bae167fd108ff01273d3c63731898bf1d79ffdd23aec29e`  
		Last Modified: Fri, 06 Sep 2024 23:15:30 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cbf4ac60298128ae88a19a2838044a9bedc05191c90540ca3112ac02b44d6e9`  
		Last Modified: Fri, 06 Sep 2024 23:15:30 GMT  
		Size: 2.0 KB (2016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:latest` - unknown; unknown

```console
$ docker pull arangodb@sha256:6e8cb3815727ccb200f4f86f85fca645479e7071f469a9bcb2f5e6933b79d57d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **361.5 KB (361542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8b49375ad3fd2b5c90a7b49f4fd7c148e5ca0810ebad955d54d8e16cd83a340`

```dockerfile
```

-	Layers:
	-	`sha256:48331eb50787bc4daa1e60cc3a5e848a12b33de2a440e3de6228a8a4f58f9040`  
		Last Modified: Fri, 06 Sep 2024 23:15:31 GMT  
		Size: 347.4 KB (347390 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa77f4a14b212ced8573b6fa04b43f9c086d0fb680f06bb38177a859c4b40150`  
		Last Modified: Fri, 06 Sep 2024 23:15:30 GMT  
		Size: 14.2 KB (14152 bytes)  
		MIME: application/vnd.in-toto+json

### `arangodb:latest` - linux; arm64 variant v8

```console
$ docker pull arangodb@sha256:0dc3cc2632158e7292309629cf33b0401c6901b53f8c633c06133f0cc8a0c3eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.7 MB (304675738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d42fd3351c3ef519fbec5a4ec501809ba8e52dea42b4f728222bf8e1c096b6a6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Tue, 27 Aug 2024 15:12:16 GMT
ADD file:e3f989df31d7e2d820078058c5d0ed7d98695c5b86bd172276270ebb59d75ee6 in / 
# Tue, 27 Aug 2024 15:12:16 GMT
CMD ["/bin/sh"]
# Tue, 27 Aug 2024 15:12:16 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Tue, 27 Aug 2024 15:12:16 GMT
ENV ARANGO_VERSION=3.12.2
# Tue, 27 Aug 2024 15:12:16 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8003EDF6F05459984878D4A6C04AD0FD86FEC04D &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb312/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg # buildkit
# Tue, 27 Aug 2024 15:12:16 GMT
ENV GLIBCXX_FORCE_NEW=1
# Tue, 27 Aug 2024 15:12:16 GMT
RUN echo "UTC" > /etc/timezone # buildkit
# Tue, 27 Aug 2024 15:12:16 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Tue, 27 Aug 2024 15:12:16 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 27 Aug 2024 15:12:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 27 Aug 2024 15:12:16 GMT
EXPOSE map[8529/tcp:{}]
# Tue, 27 Aug 2024 15:12:16 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:4a3d188841b4b0359cda0d73dc5f89f8bc569f3bcb178cfd0507b4ead0db7bf4`  
		Last Modified: Fri, 06 Sep 2024 22:45:06 GMT  
		Size: 3.3 MB (3275072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cf7966d79f14a85391123be39cca32586ba4f7500728c5daeca5fdb623b0e8d`  
		Last Modified: Sat, 07 Sep 2024 04:18:35 GMT  
		Size: 301.4 MB (301398510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84f8fcaf4551340a01b8982880a08d0cbde8e6e66b15ba167b26543a9c697445`  
		Last Modified: Sat, 07 Sep 2024 04:18:29 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5249cc2ab632e58d18be46e53425e146cfe0d2ad0ef378241ee586f5552f64d`  
		Last Modified: Sat, 07 Sep 2024 04:18:29 GMT  
		Size: 2.0 KB (2016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:latest` - unknown; unknown

```console
$ docker pull arangodb@sha256:195e356b696c821ab8e39b50c622f7c1be703b4ce8efa13bf578555c6362c534
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **467.1 KB (467129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:714bbca94d370022c14f72fde61686228c0839192ff117db2e654be54787271a`

```dockerfile
```

-	Layers:
	-	`sha256:32dea479efdcee2e8752a57510dcd823c08ad9889dade0e9d7f1e9d249ce82ab`  
		Last Modified: Sat, 07 Sep 2024 04:18:29 GMT  
		Size: 452.7 KB (452689 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65765fe83c5b07f248b8cd5b8daa3876c3b97584729483428f2a3b819e5eab54`  
		Last Modified: Sat, 07 Sep 2024 04:18:29 GMT  
		Size: 14.4 KB (14440 bytes)  
		MIME: application/vnd.in-toto+json
