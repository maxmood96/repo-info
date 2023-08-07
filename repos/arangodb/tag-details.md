<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `arangodb`

-	[`arangodb:3.10`](#arangodb310)
-	[`arangodb:3.10.9`](#arangodb3109)
-	[`arangodb:3.11`](#arangodb311)
-	[`arangodb:3.11.2`](#arangodb3112)
-	[`arangodb:3.9`](#arangodb39)
-	[`arangodb:3.9.11`](#arangodb3911)
-	[`arangodb:latest`](#arangodblatest)

## `arangodb:3.10`

```console
$ docker pull arangodb@sha256:6471bd9b7e89a8aa35bb7760f11bf28061529bfd208a2408502d21109016e29c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `arangodb:3.10` - linux; amd64

```console
$ docker pull arangodb@sha256:310b6d8268fadc6557c46b266437f2e7496cb44a79fc4cf0faf1d99da7819fbc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.9 MB (222904344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e4e56c0b89097fe9595310ac7119844cb927e4f76fcd524db953d42b7876ce4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Mon, 07 Aug 2023 19:20:31 GMT
ADD file:76d829bbce3dd420a8419919b0916c0fda917011d1e6752ca5b9e53d5ca890a6 in / 
# Mon, 07 Aug 2023 19:20:31 GMT
CMD ["/bin/sh"]
# Mon, 07 Aug 2023 20:01:27 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Mon, 07 Aug 2023 20:01:27 GMT
ENV ARANGO_VERSION=3.10.9
# Mon, 07 Aug 2023 20:01:53 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb310/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Mon, 07 Aug 2023 20:01:55 GMT
ENV GLIBCXX_FORCE_NEW=1
# Mon, 07 Aug 2023 20:01:55 GMT
RUN echo "UTC" > /etc/timezone
# Mon, 07 Aug 2023 20:01:55 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Mon, 07 Aug 2023 20:01:55 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Mon, 07 Aug 2023 20:01:55 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Mon, 07 Aug 2023 20:01:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 07 Aug 2023 20:01:56 GMT
EXPOSE 8529
# Mon, 07 Aug 2023 20:01:56 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:659d66d51139e8abad819d17e5d3c45eb82e88b9fc588c4de7711f251309b9d2`  
		Last Modified: Mon, 07 Aug 2023 19:21:19 GMT  
		Size: 2.8 MB (2807683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dfb353c2d433d13c258b1a4ad24b6ce16694443fbd594328da0131822ecdc35`  
		Last Modified: Mon, 07 Aug 2023 20:03:45 GMT  
		Size: 220.1 MB (220094174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fe1b4b844b88b7e7731d5deac2a85779daee0d8b76944568f090ec1bb7ff277`  
		Last Modified: Mon, 07 Aug 2023 20:03:21 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43e98312f4b0d01c451524b8916a36988db15bfebec2e31f992b420e6ffc219b`  
		Last Modified: Mon, 07 Aug 2023 20:03:21 GMT  
		Size: 2.1 KB (2086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c712065c4acd1d8a2f34e4e44e40e49daacabaeb5fb47bd8fdbea4fd6f7c066`  
		Last Modified: Mon, 07 Aug 2023 20:03:21 GMT  
		Size: 262.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `arangodb:3.10` - linux; arm64 variant v8

```console
$ docker pull arangodb@sha256:34ed00f611e81e594002ed1ab15871a38947c34beb0af1e90aabddebe2b645c3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.2 MB (218173090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ae0ab0dd5234378362bde2a51b73ee8455450485006336f3dd7a34a81452efa`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Mon, 07 Aug 2023 19:39:26 GMT
ADD file:cf85500a1f5b87a88587b279c8b8018eebeb3092f402b7e2cc4ad3873e078580 in / 
# Mon, 07 Aug 2023 19:39:26 GMT
CMD ["/bin/sh"]
# Mon, 07 Aug 2023 20:49:17 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Mon, 07 Aug 2023 20:49:18 GMT
ENV ARANGO_VERSION=3.10.9
# Mon, 07 Aug 2023 20:49:45 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb310/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Mon, 07 Aug 2023 20:49:49 GMT
ENV GLIBCXX_FORCE_NEW=1
# Mon, 07 Aug 2023 20:49:49 GMT
RUN echo "UTC" > /etc/timezone
# Mon, 07 Aug 2023 20:49:49 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Mon, 07 Aug 2023 20:49:49 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Mon, 07 Aug 2023 20:49:50 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Mon, 07 Aug 2023 20:49:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 07 Aug 2023 20:49:50 GMT
EXPOSE 8529
# Mon, 07 Aug 2023 20:49:50 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:bdb2de7ba06c3a4e10b98f439a8c70afd63eee492c2ddc32342331a8e9ef4ff7`  
		Last Modified: Mon, 07 Aug 2023 19:40:08 GMT  
		Size: 2.7 MB (2708023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81fc24b23dc69b14ba399d53d38679a9f66ff15b1c71ecc19029fba410390f8f`  
		Last Modified: Mon, 07 Aug 2023 20:50:56 GMT  
		Size: 215.5 MB (215462582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6077f160d9601f57ec04a5d285933ee9c53bbe9af180d6eacd5a88f9672abc52`  
		Last Modified: Mon, 07 Aug 2023 20:50:38 GMT  
		Size: 137.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22a0d65e7cab2edecd453572c0c2e9c9dda2f891b45d95990179e3463eb1d7f2`  
		Last Modified: Mon, 07 Aug 2023 20:50:38 GMT  
		Size: 2.1 KB (2087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfcbf5bce88242af6c545a77f0949a2c60b6b829161fc92eae8637d7c00f6606`  
		Last Modified: Mon, 07 Aug 2023 20:50:38 GMT  
		Size: 261.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:3.10.9`

```console
$ docker pull arangodb@sha256:6471bd9b7e89a8aa35bb7760f11bf28061529bfd208a2408502d21109016e29c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `arangodb:3.10.9` - linux; amd64

```console
$ docker pull arangodb@sha256:310b6d8268fadc6557c46b266437f2e7496cb44a79fc4cf0faf1d99da7819fbc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.9 MB (222904344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e4e56c0b89097fe9595310ac7119844cb927e4f76fcd524db953d42b7876ce4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Mon, 07 Aug 2023 19:20:31 GMT
ADD file:76d829bbce3dd420a8419919b0916c0fda917011d1e6752ca5b9e53d5ca890a6 in / 
# Mon, 07 Aug 2023 19:20:31 GMT
CMD ["/bin/sh"]
# Mon, 07 Aug 2023 20:01:27 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Mon, 07 Aug 2023 20:01:27 GMT
ENV ARANGO_VERSION=3.10.9
# Mon, 07 Aug 2023 20:01:53 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb310/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Mon, 07 Aug 2023 20:01:55 GMT
ENV GLIBCXX_FORCE_NEW=1
# Mon, 07 Aug 2023 20:01:55 GMT
RUN echo "UTC" > /etc/timezone
# Mon, 07 Aug 2023 20:01:55 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Mon, 07 Aug 2023 20:01:55 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Mon, 07 Aug 2023 20:01:55 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Mon, 07 Aug 2023 20:01:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 07 Aug 2023 20:01:56 GMT
EXPOSE 8529
# Mon, 07 Aug 2023 20:01:56 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:659d66d51139e8abad819d17e5d3c45eb82e88b9fc588c4de7711f251309b9d2`  
		Last Modified: Mon, 07 Aug 2023 19:21:19 GMT  
		Size: 2.8 MB (2807683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dfb353c2d433d13c258b1a4ad24b6ce16694443fbd594328da0131822ecdc35`  
		Last Modified: Mon, 07 Aug 2023 20:03:45 GMT  
		Size: 220.1 MB (220094174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fe1b4b844b88b7e7731d5deac2a85779daee0d8b76944568f090ec1bb7ff277`  
		Last Modified: Mon, 07 Aug 2023 20:03:21 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43e98312f4b0d01c451524b8916a36988db15bfebec2e31f992b420e6ffc219b`  
		Last Modified: Mon, 07 Aug 2023 20:03:21 GMT  
		Size: 2.1 KB (2086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c712065c4acd1d8a2f34e4e44e40e49daacabaeb5fb47bd8fdbea4fd6f7c066`  
		Last Modified: Mon, 07 Aug 2023 20:03:21 GMT  
		Size: 262.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `arangodb:3.10.9` - linux; arm64 variant v8

```console
$ docker pull arangodb@sha256:34ed00f611e81e594002ed1ab15871a38947c34beb0af1e90aabddebe2b645c3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.2 MB (218173090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ae0ab0dd5234378362bde2a51b73ee8455450485006336f3dd7a34a81452efa`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Mon, 07 Aug 2023 19:39:26 GMT
ADD file:cf85500a1f5b87a88587b279c8b8018eebeb3092f402b7e2cc4ad3873e078580 in / 
# Mon, 07 Aug 2023 19:39:26 GMT
CMD ["/bin/sh"]
# Mon, 07 Aug 2023 20:49:17 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Mon, 07 Aug 2023 20:49:18 GMT
ENV ARANGO_VERSION=3.10.9
# Mon, 07 Aug 2023 20:49:45 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb310/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Mon, 07 Aug 2023 20:49:49 GMT
ENV GLIBCXX_FORCE_NEW=1
# Mon, 07 Aug 2023 20:49:49 GMT
RUN echo "UTC" > /etc/timezone
# Mon, 07 Aug 2023 20:49:49 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Mon, 07 Aug 2023 20:49:49 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Mon, 07 Aug 2023 20:49:50 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Mon, 07 Aug 2023 20:49:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 07 Aug 2023 20:49:50 GMT
EXPOSE 8529
# Mon, 07 Aug 2023 20:49:50 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:bdb2de7ba06c3a4e10b98f439a8c70afd63eee492c2ddc32342331a8e9ef4ff7`  
		Last Modified: Mon, 07 Aug 2023 19:40:08 GMT  
		Size: 2.7 MB (2708023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81fc24b23dc69b14ba399d53d38679a9f66ff15b1c71ecc19029fba410390f8f`  
		Last Modified: Mon, 07 Aug 2023 20:50:56 GMT  
		Size: 215.5 MB (215462582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6077f160d9601f57ec04a5d285933ee9c53bbe9af180d6eacd5a88f9672abc52`  
		Last Modified: Mon, 07 Aug 2023 20:50:38 GMT  
		Size: 137.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22a0d65e7cab2edecd453572c0c2e9c9dda2f891b45d95990179e3463eb1d7f2`  
		Last Modified: Mon, 07 Aug 2023 20:50:38 GMT  
		Size: 2.1 KB (2087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfcbf5bce88242af6c545a77f0949a2c60b6b829161fc92eae8637d7c00f6606`  
		Last Modified: Mon, 07 Aug 2023 20:50:38 GMT  
		Size: 261.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:3.11`

```console
$ docker pull arangodb@sha256:8556a0b65ea1402eb9e57325c4bdb3d104712fea7cc5d2f3731e0fec2d1cbd93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `arangodb:3.11` - linux; amd64

```console
$ docker pull arangodb@sha256:812a1206d67f66168693fc5e4fb1399435794313813b87591c678aee905ee06d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.7 MB (246722206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0daa5d5f1b8579c3574571e6b485e98799d84183f57a281a33d7f11c763e133a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Mon, 07 Aug 2023 19:20:31 GMT
ADD file:76d829bbce3dd420a8419919b0916c0fda917011d1e6752ca5b9e53d5ca890a6 in / 
# Mon, 07 Aug 2023 19:20:31 GMT
CMD ["/bin/sh"]
# Mon, 07 Aug 2023 20:01:27 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Mon, 07 Aug 2023 20:02:01 GMT
ENV ARANGO_VERSION=3.11.2
# Mon, 07 Aug 2023 20:02:27 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb311/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Mon, 07 Aug 2023 20:02:29 GMT
ENV GLIBCXX_FORCE_NEW=1
# Mon, 07 Aug 2023 20:02:29 GMT
RUN echo "UTC" > /etc/timezone
# Mon, 07 Aug 2023 20:02:30 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Mon, 07 Aug 2023 20:02:30 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Mon, 07 Aug 2023 20:02:30 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Mon, 07 Aug 2023 20:02:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 07 Aug 2023 20:02:30 GMT
EXPOSE 8529
# Mon, 07 Aug 2023 20:02:30 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:659d66d51139e8abad819d17e5d3c45eb82e88b9fc588c4de7711f251309b9d2`  
		Last Modified: Mon, 07 Aug 2023 19:21:19 GMT  
		Size: 2.8 MB (2807683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:952cc4946923e5d7adbb0fe4fff8085210bb5f6c986dacde641a23e1cc014fed`  
		Last Modified: Mon, 07 Aug 2023 20:04:20 GMT  
		Size: 243.9 MB (243912038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47975cfa4e68060e2784b6ce179913a193de0831e78bc1cc9a8303f9c8cc4f6a`  
		Last Modified: Mon, 07 Aug 2023 20:03:54 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb44872a0add811d36f568676fe17c641abb9cfba7f4661700002d9f84d958fa`  
		Last Modified: Mon, 07 Aug 2023 20:03:54 GMT  
		Size: 2.1 KB (2086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:576a3b295402a9f35f5d633d7f0d720e9e97d7284a36eed08a7f29f4df6e93af`  
		Last Modified: Mon, 07 Aug 2023 20:03:54 GMT  
		Size: 260.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `arangodb:3.11` - linux; arm64 variant v8

```console
$ docker pull arangodb@sha256:aa9e5f1235648f8197c06535af74714c7648a37bd5dbcdab331a451118ca00d7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.2 MB (241158126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b80d65cf75694d6800c402a101166c79a52468b336d8a11163f79acadf2d053a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Mon, 07 Aug 2023 19:39:26 GMT
ADD file:cf85500a1f5b87a88587b279c8b8018eebeb3092f402b7e2cc4ad3873e078580 in / 
# Mon, 07 Aug 2023 19:39:26 GMT
CMD ["/bin/sh"]
# Mon, 07 Aug 2023 20:49:17 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Mon, 07 Aug 2023 20:49:58 GMT
ENV ARANGO_VERSION=3.11.2
# Mon, 07 Aug 2023 20:50:22 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb311/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Mon, 07 Aug 2023 20:50:26 GMT
ENV GLIBCXX_FORCE_NEW=1
# Mon, 07 Aug 2023 20:50:26 GMT
RUN echo "UTC" > /etc/timezone
# Mon, 07 Aug 2023 20:50:26 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Mon, 07 Aug 2023 20:50:26 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Mon, 07 Aug 2023 20:50:26 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Mon, 07 Aug 2023 20:50:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 07 Aug 2023 20:50:26 GMT
EXPOSE 8529
# Mon, 07 Aug 2023 20:50:26 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:bdb2de7ba06c3a4e10b98f439a8c70afd63eee492c2ddc32342331a8e9ef4ff7`  
		Last Modified: Mon, 07 Aug 2023 19:40:08 GMT  
		Size: 2.7 MB (2708023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56e0e75a4088aa897df041f66e2716004eef7280bff4ecf9bba08ed9a8f9725c`  
		Last Modified: Mon, 07 Aug 2023 20:51:25 GMT  
		Size: 238.4 MB (238447616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:982760a315fe722eae8644c7a3fe523db4dacafa0d381c3706aef40c13c4b74a`  
		Last Modified: Mon, 07 Aug 2023 20:51:06 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e908d0b1f1685f319d1d00252bd2c1da69cce6f2908cb6cc5717af1b385c86a`  
		Last Modified: Mon, 07 Aug 2023 20:51:06 GMT  
		Size: 2.1 KB (2086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1467932f7da233a7efa2a50a172e4451f628c8fdb573713ce56f5d6e5405b3f`  
		Last Modified: Mon, 07 Aug 2023 20:51:06 GMT  
		Size: 262.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:3.11.2`

```console
$ docker pull arangodb@sha256:8556a0b65ea1402eb9e57325c4bdb3d104712fea7cc5d2f3731e0fec2d1cbd93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `arangodb:3.11.2` - linux; amd64

```console
$ docker pull arangodb@sha256:812a1206d67f66168693fc5e4fb1399435794313813b87591c678aee905ee06d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.7 MB (246722206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0daa5d5f1b8579c3574571e6b485e98799d84183f57a281a33d7f11c763e133a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Mon, 07 Aug 2023 19:20:31 GMT
ADD file:76d829bbce3dd420a8419919b0916c0fda917011d1e6752ca5b9e53d5ca890a6 in / 
# Mon, 07 Aug 2023 19:20:31 GMT
CMD ["/bin/sh"]
# Mon, 07 Aug 2023 20:01:27 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Mon, 07 Aug 2023 20:02:01 GMT
ENV ARANGO_VERSION=3.11.2
# Mon, 07 Aug 2023 20:02:27 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb311/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Mon, 07 Aug 2023 20:02:29 GMT
ENV GLIBCXX_FORCE_NEW=1
# Mon, 07 Aug 2023 20:02:29 GMT
RUN echo "UTC" > /etc/timezone
# Mon, 07 Aug 2023 20:02:30 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Mon, 07 Aug 2023 20:02:30 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Mon, 07 Aug 2023 20:02:30 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Mon, 07 Aug 2023 20:02:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 07 Aug 2023 20:02:30 GMT
EXPOSE 8529
# Mon, 07 Aug 2023 20:02:30 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:659d66d51139e8abad819d17e5d3c45eb82e88b9fc588c4de7711f251309b9d2`  
		Last Modified: Mon, 07 Aug 2023 19:21:19 GMT  
		Size: 2.8 MB (2807683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:952cc4946923e5d7adbb0fe4fff8085210bb5f6c986dacde641a23e1cc014fed`  
		Last Modified: Mon, 07 Aug 2023 20:04:20 GMT  
		Size: 243.9 MB (243912038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47975cfa4e68060e2784b6ce179913a193de0831e78bc1cc9a8303f9c8cc4f6a`  
		Last Modified: Mon, 07 Aug 2023 20:03:54 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb44872a0add811d36f568676fe17c641abb9cfba7f4661700002d9f84d958fa`  
		Last Modified: Mon, 07 Aug 2023 20:03:54 GMT  
		Size: 2.1 KB (2086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:576a3b295402a9f35f5d633d7f0d720e9e97d7284a36eed08a7f29f4df6e93af`  
		Last Modified: Mon, 07 Aug 2023 20:03:54 GMT  
		Size: 260.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `arangodb:3.11.2` - linux; arm64 variant v8

```console
$ docker pull arangodb@sha256:aa9e5f1235648f8197c06535af74714c7648a37bd5dbcdab331a451118ca00d7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.2 MB (241158126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b80d65cf75694d6800c402a101166c79a52468b336d8a11163f79acadf2d053a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Mon, 07 Aug 2023 19:39:26 GMT
ADD file:cf85500a1f5b87a88587b279c8b8018eebeb3092f402b7e2cc4ad3873e078580 in / 
# Mon, 07 Aug 2023 19:39:26 GMT
CMD ["/bin/sh"]
# Mon, 07 Aug 2023 20:49:17 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Mon, 07 Aug 2023 20:49:58 GMT
ENV ARANGO_VERSION=3.11.2
# Mon, 07 Aug 2023 20:50:22 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb311/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Mon, 07 Aug 2023 20:50:26 GMT
ENV GLIBCXX_FORCE_NEW=1
# Mon, 07 Aug 2023 20:50:26 GMT
RUN echo "UTC" > /etc/timezone
# Mon, 07 Aug 2023 20:50:26 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Mon, 07 Aug 2023 20:50:26 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Mon, 07 Aug 2023 20:50:26 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Mon, 07 Aug 2023 20:50:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 07 Aug 2023 20:50:26 GMT
EXPOSE 8529
# Mon, 07 Aug 2023 20:50:26 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:bdb2de7ba06c3a4e10b98f439a8c70afd63eee492c2ddc32342331a8e9ef4ff7`  
		Last Modified: Mon, 07 Aug 2023 19:40:08 GMT  
		Size: 2.7 MB (2708023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56e0e75a4088aa897df041f66e2716004eef7280bff4ecf9bba08ed9a8f9725c`  
		Last Modified: Mon, 07 Aug 2023 20:51:25 GMT  
		Size: 238.4 MB (238447616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:982760a315fe722eae8644c7a3fe523db4dacafa0d381c3706aef40c13c4b74a`  
		Last Modified: Mon, 07 Aug 2023 20:51:06 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e908d0b1f1685f319d1d00252bd2c1da69cce6f2908cb6cc5717af1b385c86a`  
		Last Modified: Mon, 07 Aug 2023 20:51:06 GMT  
		Size: 2.1 KB (2086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1467932f7da233a7efa2a50a172e4451f628c8fdb573713ce56f5d6e5405b3f`  
		Last Modified: Mon, 07 Aug 2023 20:51:06 GMT  
		Size: 262.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:3.9`

```console
$ docker pull arangodb@sha256:48444fecfbd47c46b39273e285eabfd0d4bc38c0e663cf290f9859fb1258dd7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `arangodb:3.9` - linux; amd64

```console
$ docker pull arangodb@sha256:b684ee4696aaa277213b729dbfc97523c069b30adb27d6f3c083f3362715ff13
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.3 MB (205259056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a828c1780a3534212e7e84822bda377579c8c05f4aaaebf925a95074089f5809`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Mon, 07 Aug 2023 19:20:37 GMT
ADD file:4faae297b6caba92e1791a5ff667be0fcb4de6a4de2df155395957ef9d8ad5e5 in / 
# Mon, 07 Aug 2023 19:20:37 GMT
CMD ["/bin/sh"]
# Mon, 07 Aug 2023 20:00:53 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Mon, 07 Aug 2023 20:00:53 GMT
ENV ARANGO_VERSION=3.9.11
# Mon, 07 Aug 2023 20:00:53 GMT
ENV ARANGO_URL=https://download.arangodb.com/arangodb39/DEBIAN/amd64
# Mon, 07 Aug 2023 20:00:53 GMT
ENV ARANGO_PACKAGE=arangodb3_3.9.11-1_amd64.deb
# Mon, 07 Aug 2023 20:00:53 GMT
ENV ARANGO_PACKAGE_URL=https://download.arangodb.com/arangodb39/DEBIAN/amd64/arangodb3_3.9.11-1_amd64.deb
# Mon, 07 Aug 2023 20:00:53 GMT
ENV ARANGO_SIGNATURE_URL=https://download.arangodb.com/arangodb39/DEBIAN/amd64/arangodb3_3.9.11-1_amd64.deb.asc
# Mon, 07 Aug 2023 20:01:21 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Mon, 07 Aug 2023 20:01:22 GMT
ENV GLIBCXX_FORCE_NEW=1
# Mon, 07 Aug 2023 20:01:23 GMT
RUN echo "UTC" > /etc/timezone
# Mon, 07 Aug 2023 20:01:23 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Mon, 07 Aug 2023 20:01:23 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Mon, 07 Aug 2023 20:01:23 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Mon, 07 Aug 2023 20:01:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 07 Aug 2023 20:01:23 GMT
EXPOSE 8529
# Mon, 07 Aug 2023 20:01:23 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:3695f6c099b80e503148dbb435d044c35147f81d34b9d6fbb27b3dcf1fd7ecaf`  
		Last Modified: Mon, 07 Aug 2023 19:21:27 GMT  
		Size: 2.8 MB (2826006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82c566ea949470dfa5a39d8cbab7a2eeaac8bcea317ac08e61baab3ab187f0d7`  
		Last Modified: Mon, 07 Aug 2023 20:03:11 GMT  
		Size: 202.4 MB (202430564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96d76fe7b5c0012d15f8beb4f1bb4e1f8e8e6b84c6b380586a6692649ce4f84b`  
		Last Modified: Mon, 07 Aug 2023 20:02:45 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:056e2ece5d15da38fd51256f56856f25ff1fd57932f14ee1ab28d79fbab87fdd`  
		Last Modified: Mon, 07 Aug 2023 20:02:45 GMT  
		Size: 2.1 KB (2086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04056651227117636854c720f1abe7d7b7a1e360324af9e192bed188a33cbc40`  
		Last Modified: Mon, 07 Aug 2023 20:02:45 GMT  
		Size: 261.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:3.9.11`

```console
$ docker pull arangodb@sha256:48444fecfbd47c46b39273e285eabfd0d4bc38c0e663cf290f9859fb1258dd7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `arangodb:3.9.11` - linux; amd64

```console
$ docker pull arangodb@sha256:b684ee4696aaa277213b729dbfc97523c069b30adb27d6f3c083f3362715ff13
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.3 MB (205259056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a828c1780a3534212e7e84822bda377579c8c05f4aaaebf925a95074089f5809`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Mon, 07 Aug 2023 19:20:37 GMT
ADD file:4faae297b6caba92e1791a5ff667be0fcb4de6a4de2df155395957ef9d8ad5e5 in / 
# Mon, 07 Aug 2023 19:20:37 GMT
CMD ["/bin/sh"]
# Mon, 07 Aug 2023 20:00:53 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Mon, 07 Aug 2023 20:00:53 GMT
ENV ARANGO_VERSION=3.9.11
# Mon, 07 Aug 2023 20:00:53 GMT
ENV ARANGO_URL=https://download.arangodb.com/arangodb39/DEBIAN/amd64
# Mon, 07 Aug 2023 20:00:53 GMT
ENV ARANGO_PACKAGE=arangodb3_3.9.11-1_amd64.deb
# Mon, 07 Aug 2023 20:00:53 GMT
ENV ARANGO_PACKAGE_URL=https://download.arangodb.com/arangodb39/DEBIAN/amd64/arangodb3_3.9.11-1_amd64.deb
# Mon, 07 Aug 2023 20:00:53 GMT
ENV ARANGO_SIGNATURE_URL=https://download.arangodb.com/arangodb39/DEBIAN/amd64/arangodb3_3.9.11-1_amd64.deb.asc
# Mon, 07 Aug 2023 20:01:21 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Mon, 07 Aug 2023 20:01:22 GMT
ENV GLIBCXX_FORCE_NEW=1
# Mon, 07 Aug 2023 20:01:23 GMT
RUN echo "UTC" > /etc/timezone
# Mon, 07 Aug 2023 20:01:23 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Mon, 07 Aug 2023 20:01:23 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Mon, 07 Aug 2023 20:01:23 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Mon, 07 Aug 2023 20:01:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 07 Aug 2023 20:01:23 GMT
EXPOSE 8529
# Mon, 07 Aug 2023 20:01:23 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:3695f6c099b80e503148dbb435d044c35147f81d34b9d6fbb27b3dcf1fd7ecaf`  
		Last Modified: Mon, 07 Aug 2023 19:21:27 GMT  
		Size: 2.8 MB (2826006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82c566ea949470dfa5a39d8cbab7a2eeaac8bcea317ac08e61baab3ab187f0d7`  
		Last Modified: Mon, 07 Aug 2023 20:03:11 GMT  
		Size: 202.4 MB (202430564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96d76fe7b5c0012d15f8beb4f1bb4e1f8e8e6b84c6b380586a6692649ce4f84b`  
		Last Modified: Mon, 07 Aug 2023 20:02:45 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:056e2ece5d15da38fd51256f56856f25ff1fd57932f14ee1ab28d79fbab87fdd`  
		Last Modified: Mon, 07 Aug 2023 20:02:45 GMT  
		Size: 2.1 KB (2086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04056651227117636854c720f1abe7d7b7a1e360324af9e192bed188a33cbc40`  
		Last Modified: Mon, 07 Aug 2023 20:02:45 GMT  
		Size: 261.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:latest`

```console
$ docker pull arangodb@sha256:8556a0b65ea1402eb9e57325c4bdb3d104712fea7cc5d2f3731e0fec2d1cbd93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `arangodb:latest` - linux; amd64

```console
$ docker pull arangodb@sha256:812a1206d67f66168693fc5e4fb1399435794313813b87591c678aee905ee06d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.7 MB (246722206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0daa5d5f1b8579c3574571e6b485e98799d84183f57a281a33d7f11c763e133a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Mon, 07 Aug 2023 19:20:31 GMT
ADD file:76d829bbce3dd420a8419919b0916c0fda917011d1e6752ca5b9e53d5ca890a6 in / 
# Mon, 07 Aug 2023 19:20:31 GMT
CMD ["/bin/sh"]
# Mon, 07 Aug 2023 20:01:27 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Mon, 07 Aug 2023 20:02:01 GMT
ENV ARANGO_VERSION=3.11.2
# Mon, 07 Aug 2023 20:02:27 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb311/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Mon, 07 Aug 2023 20:02:29 GMT
ENV GLIBCXX_FORCE_NEW=1
# Mon, 07 Aug 2023 20:02:29 GMT
RUN echo "UTC" > /etc/timezone
# Mon, 07 Aug 2023 20:02:30 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Mon, 07 Aug 2023 20:02:30 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Mon, 07 Aug 2023 20:02:30 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Mon, 07 Aug 2023 20:02:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 07 Aug 2023 20:02:30 GMT
EXPOSE 8529
# Mon, 07 Aug 2023 20:02:30 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:659d66d51139e8abad819d17e5d3c45eb82e88b9fc588c4de7711f251309b9d2`  
		Last Modified: Mon, 07 Aug 2023 19:21:19 GMT  
		Size: 2.8 MB (2807683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:952cc4946923e5d7adbb0fe4fff8085210bb5f6c986dacde641a23e1cc014fed`  
		Last Modified: Mon, 07 Aug 2023 20:04:20 GMT  
		Size: 243.9 MB (243912038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47975cfa4e68060e2784b6ce179913a193de0831e78bc1cc9a8303f9c8cc4f6a`  
		Last Modified: Mon, 07 Aug 2023 20:03:54 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb44872a0add811d36f568676fe17c641abb9cfba7f4661700002d9f84d958fa`  
		Last Modified: Mon, 07 Aug 2023 20:03:54 GMT  
		Size: 2.1 KB (2086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:576a3b295402a9f35f5d633d7f0d720e9e97d7284a36eed08a7f29f4df6e93af`  
		Last Modified: Mon, 07 Aug 2023 20:03:54 GMT  
		Size: 260.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `arangodb:latest` - linux; arm64 variant v8

```console
$ docker pull arangodb@sha256:aa9e5f1235648f8197c06535af74714c7648a37bd5dbcdab331a451118ca00d7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.2 MB (241158126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b80d65cf75694d6800c402a101166c79a52468b336d8a11163f79acadf2d053a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Mon, 07 Aug 2023 19:39:26 GMT
ADD file:cf85500a1f5b87a88587b279c8b8018eebeb3092f402b7e2cc4ad3873e078580 in / 
# Mon, 07 Aug 2023 19:39:26 GMT
CMD ["/bin/sh"]
# Mon, 07 Aug 2023 20:49:17 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Mon, 07 Aug 2023 20:49:58 GMT
ENV ARANGO_VERSION=3.11.2
# Mon, 07 Aug 2023 20:50:22 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb311/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Mon, 07 Aug 2023 20:50:26 GMT
ENV GLIBCXX_FORCE_NEW=1
# Mon, 07 Aug 2023 20:50:26 GMT
RUN echo "UTC" > /etc/timezone
# Mon, 07 Aug 2023 20:50:26 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Mon, 07 Aug 2023 20:50:26 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Mon, 07 Aug 2023 20:50:26 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Mon, 07 Aug 2023 20:50:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 07 Aug 2023 20:50:26 GMT
EXPOSE 8529
# Mon, 07 Aug 2023 20:50:26 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:bdb2de7ba06c3a4e10b98f439a8c70afd63eee492c2ddc32342331a8e9ef4ff7`  
		Last Modified: Mon, 07 Aug 2023 19:40:08 GMT  
		Size: 2.7 MB (2708023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56e0e75a4088aa897df041f66e2716004eef7280bff4ecf9bba08ed9a8f9725c`  
		Last Modified: Mon, 07 Aug 2023 20:51:25 GMT  
		Size: 238.4 MB (238447616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:982760a315fe722eae8644c7a3fe523db4dacafa0d381c3706aef40c13c4b74a`  
		Last Modified: Mon, 07 Aug 2023 20:51:06 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e908d0b1f1685f319d1d00252bd2c1da69cce6f2908cb6cc5717af1b385c86a`  
		Last Modified: Mon, 07 Aug 2023 20:51:06 GMT  
		Size: 2.1 KB (2086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1467932f7da233a7efa2a50a172e4451f628c8fdb573713ce56f5d6e5405b3f`  
		Last Modified: Mon, 07 Aug 2023 20:51:06 GMT  
		Size: 262.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
