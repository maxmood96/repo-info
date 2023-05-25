<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `arangodb`

-	[`arangodb:3.10`](#arangodb310)
-	[`arangodb:3.10.6`](#arangodb3106)
-	[`arangodb:3.11`](#arangodb311)
-	[`arangodb:3.11.0`](#arangodb3110)
-	[`arangodb:3.9`](#arangodb39)
-	[`arangodb:3.9.10`](#arangodb3910)
-	[`arangodb:latest`](#arangodblatest)

## `arangodb:3.10`

```console
$ docker pull arangodb@sha256:a04dcd70c5b63c0e42e7895286d2aeb81e182cc3e2c5d483e14db8fc8976d116
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `arangodb:3.10` - linux; amd64

```console
$ docker pull arangodb@sha256:fff7b1b64b128fff33d075ab2a3c62e5348890e3651303d09b0e6694d656199f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.2 MB (220153430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e85ab24ec06082598abbdb3d3d0934d57f00c38eece633c1aac5892ca1b28e8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Wed, 29 Mar 2023 18:19:28 GMT
ADD file:970e6b2578ef73457ffed1189e8ba128b0211cabd3174b8c7d3afd8fb58ad614 in / 
# Wed, 29 Mar 2023 18:19:28 GMT
CMD ["/bin/sh"]
# Wed, 29 Mar 2023 19:35:19 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Thu, 04 May 2023 17:35:20 GMT
ENV ARANGO_VERSION=3.10.6
# Thu, 04 May 2023 17:35:45 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb310/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Thu, 04 May 2023 17:35:46 GMT
ENV GLIBCXX_FORCE_NEW=1
# Thu, 04 May 2023 17:35:47 GMT
RUN echo "UTC" > /etc/timezone
# Thu, 04 May 2023 17:35:47 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Thu, 04 May 2023 17:35:47 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Thu, 04 May 2023 17:35:47 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Thu, 04 May 2023 17:35:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 04 May 2023 17:35:47 GMT
EXPOSE 8529
# Thu, 04 May 2023 17:35:48 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:91d30c5bc19582de1415b18f1ec5bcbf52a558b62cf6cc201c9669df9f748c22`  
		Last Modified: Wed, 29 Mar 2023 18:20:09 GMT  
		Size: 2.8 MB (2807803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a90de0772947794f476336da1b66553c3d0953919e307b15c23b909c2db45215`  
		Last Modified: Thu, 04 May 2023 17:36:23 GMT  
		Size: 217.3 MB (217343141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d061e173c84f434e3c88e502466c4d6c33f57869a9f72da43cc4cba35a3cfb1e`  
		Last Modified: Thu, 04 May 2023 17:36:01 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ed363dd0daeca109cc313c946b7e0d29876ed34dc7700cd4e2d412aaec8f805`  
		Last Modified: Thu, 04 May 2023 17:36:01 GMT  
		Size: 2.1 KB (2086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edc1190a2ff6497eea2dfa5b90ab026ec7cf7eb5c358b2881757808b68e0b2d2`  
		Last Modified: Thu, 04 May 2023 17:36:01 GMT  
		Size: 261.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `arangodb:3.10` - linux; arm64 variant v8

```console
$ docker pull arangodb@sha256:00195880bfddb201705b222e7d72d6fc94fd002993a88d6bea4a0fe3f9d0cc75
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.9 MB (214857530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67d4dd0687cf9cfcff63defceee4c1357b834fc0db52551de10e5a6cfe44a89d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Wed, 29 Mar 2023 17:39:20 GMT
ADD file:a6a2f69b60d7d27bc6e2b9b7e9910dabdc3f5e3702c2345d26a7dc8c603ae595 in / 
# Wed, 29 Mar 2023 17:39:20 GMT
CMD ["/bin/sh"]
# Thu, 30 Mar 2023 03:53:47 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Thu, 04 May 2023 08:41:27 GMT
ENV ARANGO_VERSION=3.10.6
# Thu, 04 May 2023 08:41:51 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb310/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Thu, 04 May 2023 08:41:55 GMT
ENV GLIBCXX_FORCE_NEW=1
# Thu, 04 May 2023 08:41:55 GMT
RUN echo "UTC" > /etc/timezone
# Thu, 04 May 2023 08:41:55 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Thu, 04 May 2023 08:41:55 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Thu, 04 May 2023 08:41:55 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Thu, 04 May 2023 08:41:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 04 May 2023 08:41:55 GMT
EXPOSE 8529
# Thu, 04 May 2023 08:41:56 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:547446be3368f442c50ff95e2a2a9c85110b6b41bbb3c75b7e5ebb115f478b57`  
		Last Modified: Wed, 29 Mar 2023 17:39:56 GMT  
		Size: 2.7 MB (2709344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8854986b541b3b7fe6de76be4cac6cf004edc06cb36a08ac74d9540020bec69`  
		Last Modified: Thu, 04 May 2023 08:42:22 GMT  
		Size: 212.1 MB (212145698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0f61bb38c7d0276dbb3975069f3473117b08cb4597cffe623dc1b54935b517e`  
		Last Modified: Thu, 04 May 2023 08:42:07 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4f8628b18b9b058d1ebf269af140ec9e1919baa9793c1ff997cd0ffe15898e9`  
		Last Modified: Thu, 04 May 2023 08:42:06 GMT  
		Size: 2.1 KB (2087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce92e9544c02b8a53a5cb63b8f50ec53083a6ab616c728a785231f7ad4e0f278`  
		Last Modified: Thu, 04 May 2023 08:42:06 GMT  
		Size: 262.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:3.10.6`

```console
$ docker pull arangodb@sha256:a04dcd70c5b63c0e42e7895286d2aeb81e182cc3e2c5d483e14db8fc8976d116
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `arangodb:3.10.6` - linux; amd64

```console
$ docker pull arangodb@sha256:fff7b1b64b128fff33d075ab2a3c62e5348890e3651303d09b0e6694d656199f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.2 MB (220153430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e85ab24ec06082598abbdb3d3d0934d57f00c38eece633c1aac5892ca1b28e8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Wed, 29 Mar 2023 18:19:28 GMT
ADD file:970e6b2578ef73457ffed1189e8ba128b0211cabd3174b8c7d3afd8fb58ad614 in / 
# Wed, 29 Mar 2023 18:19:28 GMT
CMD ["/bin/sh"]
# Wed, 29 Mar 2023 19:35:19 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Thu, 04 May 2023 17:35:20 GMT
ENV ARANGO_VERSION=3.10.6
# Thu, 04 May 2023 17:35:45 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb310/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Thu, 04 May 2023 17:35:46 GMT
ENV GLIBCXX_FORCE_NEW=1
# Thu, 04 May 2023 17:35:47 GMT
RUN echo "UTC" > /etc/timezone
# Thu, 04 May 2023 17:35:47 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Thu, 04 May 2023 17:35:47 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Thu, 04 May 2023 17:35:47 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Thu, 04 May 2023 17:35:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 04 May 2023 17:35:47 GMT
EXPOSE 8529
# Thu, 04 May 2023 17:35:48 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:91d30c5bc19582de1415b18f1ec5bcbf52a558b62cf6cc201c9669df9f748c22`  
		Last Modified: Wed, 29 Mar 2023 18:20:09 GMT  
		Size: 2.8 MB (2807803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a90de0772947794f476336da1b66553c3d0953919e307b15c23b909c2db45215`  
		Last Modified: Thu, 04 May 2023 17:36:23 GMT  
		Size: 217.3 MB (217343141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d061e173c84f434e3c88e502466c4d6c33f57869a9f72da43cc4cba35a3cfb1e`  
		Last Modified: Thu, 04 May 2023 17:36:01 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ed363dd0daeca109cc313c946b7e0d29876ed34dc7700cd4e2d412aaec8f805`  
		Last Modified: Thu, 04 May 2023 17:36:01 GMT  
		Size: 2.1 KB (2086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edc1190a2ff6497eea2dfa5b90ab026ec7cf7eb5c358b2881757808b68e0b2d2`  
		Last Modified: Thu, 04 May 2023 17:36:01 GMT  
		Size: 261.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `arangodb:3.10.6` - linux; arm64 variant v8

```console
$ docker pull arangodb@sha256:00195880bfddb201705b222e7d72d6fc94fd002993a88d6bea4a0fe3f9d0cc75
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.9 MB (214857530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67d4dd0687cf9cfcff63defceee4c1357b834fc0db52551de10e5a6cfe44a89d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Wed, 29 Mar 2023 17:39:20 GMT
ADD file:a6a2f69b60d7d27bc6e2b9b7e9910dabdc3f5e3702c2345d26a7dc8c603ae595 in / 
# Wed, 29 Mar 2023 17:39:20 GMT
CMD ["/bin/sh"]
# Thu, 30 Mar 2023 03:53:47 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Thu, 04 May 2023 08:41:27 GMT
ENV ARANGO_VERSION=3.10.6
# Thu, 04 May 2023 08:41:51 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb310/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Thu, 04 May 2023 08:41:55 GMT
ENV GLIBCXX_FORCE_NEW=1
# Thu, 04 May 2023 08:41:55 GMT
RUN echo "UTC" > /etc/timezone
# Thu, 04 May 2023 08:41:55 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Thu, 04 May 2023 08:41:55 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Thu, 04 May 2023 08:41:55 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Thu, 04 May 2023 08:41:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 04 May 2023 08:41:55 GMT
EXPOSE 8529
# Thu, 04 May 2023 08:41:56 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:547446be3368f442c50ff95e2a2a9c85110b6b41bbb3c75b7e5ebb115f478b57`  
		Last Modified: Wed, 29 Mar 2023 17:39:56 GMT  
		Size: 2.7 MB (2709344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8854986b541b3b7fe6de76be4cac6cf004edc06cb36a08ac74d9540020bec69`  
		Last Modified: Thu, 04 May 2023 08:42:22 GMT  
		Size: 212.1 MB (212145698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0f61bb38c7d0276dbb3975069f3473117b08cb4597cffe623dc1b54935b517e`  
		Last Modified: Thu, 04 May 2023 08:42:07 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4f8628b18b9b058d1ebf269af140ec9e1919baa9793c1ff997cd0ffe15898e9`  
		Last Modified: Thu, 04 May 2023 08:42:06 GMT  
		Size: 2.1 KB (2087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce92e9544c02b8a53a5cb63b8f50ec53083a6ab616c728a785231f7ad4e0f278`  
		Last Modified: Thu, 04 May 2023 08:42:06 GMT  
		Size: 262.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:3.11`

**does not exist** (yet?)

## `arangodb:3.11.0`

**does not exist** (yet?)

## `arangodb:3.9`

```console
$ docker pull arangodb@sha256:a10a86ecb15317fc1b6c0f765f13de9fcd5d7e50427d1aebb60d08a634514f19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `arangodb:3.9` - linux; amd64

```console
$ docker pull arangodb@sha256:f8a65bacb58293da3291a63b8cee3191fdf48e08809cfffc71f21bf2e3da729c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.6 MB (204630799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53286ce24900f68e5da7eacf33d8f2427a28458096fc507de03b4916bf986e15`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Wed, 29 Mar 2023 18:19:33 GMT
ADD file:08ad6c1c886a26e30ae4ab103ff377ee6cfbc1be2437fa227ec28a335c63d78a in / 
# Wed, 29 Mar 2023 18:19:33 GMT
CMD ["/bin/sh"]
# Wed, 10 May 2023 17:19:25 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Wed, 10 May 2023 17:19:25 GMT
ENV ARANGO_VERSION=3.9.10
# Wed, 10 May 2023 17:19:26 GMT
ENV ARANGO_URL=https://download.arangodb.com/arangodb39/DEBIAN/amd64
# Wed, 10 May 2023 17:19:26 GMT
ENV ARANGO_PACKAGE=arangodb3_3.9.10-1_amd64.deb
# Wed, 10 May 2023 17:19:26 GMT
ENV ARANGO_PACKAGE_URL=https://download.arangodb.com/arangodb39/DEBIAN/amd64/arangodb3_3.9.10-1_amd64.deb
# Wed, 10 May 2023 17:19:26 GMT
ENV ARANGO_SIGNATURE_URL=https://download.arangodb.com/arangodb39/DEBIAN/amd64/arangodb3_3.9.10-1_amd64.deb.asc
# Wed, 10 May 2023 17:19:49 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Wed, 10 May 2023 17:19:51 GMT
ENV GLIBCXX_FORCE_NEW=1
# Wed, 10 May 2023 17:19:51 GMT
RUN echo "UTC" > /etc/timezone
# Wed, 10 May 2023 17:19:51 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Wed, 10 May 2023 17:19:51 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Wed, 10 May 2023 17:19:52 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Wed, 10 May 2023 17:19:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 May 2023 17:19:52 GMT
EXPOSE 8529
# Wed, 10 May 2023 17:19:52 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:0ce1dd7918a48990ab749aab2e805c26f691a3a8103495530e7ea5a1d168af4a`  
		Last Modified: Wed, 29 Mar 2023 18:20:17 GMT  
		Size: 2.8 MB (2826596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90d585c1930f622a4272bba8313336a35c41f822fa30120e3a69c7889020af56`  
		Last Modified: Wed, 10 May 2023 17:20:28 GMT  
		Size: 201.8 MB (201801717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b96c7762371c28beea3fd523e677c6a949a7a5bcde91a803eb30446ae1f40de`  
		Last Modified: Wed, 10 May 2023 17:20:07 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41959f1cf2c91579387c0df11d49d2ecbb949a7dd5d852195ff01c622889eef9`  
		Last Modified: Wed, 10 May 2023 17:20:07 GMT  
		Size: 2.1 KB (2086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:849bc765c140c45f788451f4df4c85baf82ce84448b50b9498c144e3a079d06d`  
		Last Modified: Wed, 10 May 2023 17:20:07 GMT  
		Size: 261.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:3.9.10`

```console
$ docker pull arangodb@sha256:a10a86ecb15317fc1b6c0f765f13de9fcd5d7e50427d1aebb60d08a634514f19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `arangodb:3.9.10` - linux; amd64

```console
$ docker pull arangodb@sha256:f8a65bacb58293da3291a63b8cee3191fdf48e08809cfffc71f21bf2e3da729c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.6 MB (204630799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53286ce24900f68e5da7eacf33d8f2427a28458096fc507de03b4916bf986e15`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Wed, 29 Mar 2023 18:19:33 GMT
ADD file:08ad6c1c886a26e30ae4ab103ff377ee6cfbc1be2437fa227ec28a335c63d78a in / 
# Wed, 29 Mar 2023 18:19:33 GMT
CMD ["/bin/sh"]
# Wed, 10 May 2023 17:19:25 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Wed, 10 May 2023 17:19:25 GMT
ENV ARANGO_VERSION=3.9.10
# Wed, 10 May 2023 17:19:26 GMT
ENV ARANGO_URL=https://download.arangodb.com/arangodb39/DEBIAN/amd64
# Wed, 10 May 2023 17:19:26 GMT
ENV ARANGO_PACKAGE=arangodb3_3.9.10-1_amd64.deb
# Wed, 10 May 2023 17:19:26 GMT
ENV ARANGO_PACKAGE_URL=https://download.arangodb.com/arangodb39/DEBIAN/amd64/arangodb3_3.9.10-1_amd64.deb
# Wed, 10 May 2023 17:19:26 GMT
ENV ARANGO_SIGNATURE_URL=https://download.arangodb.com/arangodb39/DEBIAN/amd64/arangodb3_3.9.10-1_amd64.deb.asc
# Wed, 10 May 2023 17:19:49 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Wed, 10 May 2023 17:19:51 GMT
ENV GLIBCXX_FORCE_NEW=1
# Wed, 10 May 2023 17:19:51 GMT
RUN echo "UTC" > /etc/timezone
# Wed, 10 May 2023 17:19:51 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Wed, 10 May 2023 17:19:51 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Wed, 10 May 2023 17:19:52 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Wed, 10 May 2023 17:19:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 May 2023 17:19:52 GMT
EXPOSE 8529
# Wed, 10 May 2023 17:19:52 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:0ce1dd7918a48990ab749aab2e805c26f691a3a8103495530e7ea5a1d168af4a`  
		Last Modified: Wed, 29 Mar 2023 18:20:17 GMT  
		Size: 2.8 MB (2826596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90d585c1930f622a4272bba8313336a35c41f822fa30120e3a69c7889020af56`  
		Last Modified: Wed, 10 May 2023 17:20:28 GMT  
		Size: 201.8 MB (201801717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b96c7762371c28beea3fd523e677c6a949a7a5bcde91a803eb30446ae1f40de`  
		Last Modified: Wed, 10 May 2023 17:20:07 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41959f1cf2c91579387c0df11d49d2ecbb949a7dd5d852195ff01c622889eef9`  
		Last Modified: Wed, 10 May 2023 17:20:07 GMT  
		Size: 2.1 KB (2086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:849bc765c140c45f788451f4df4c85baf82ce84448b50b9498c144e3a079d06d`  
		Last Modified: Wed, 10 May 2023 17:20:07 GMT  
		Size: 261.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:latest`

```console
$ docker pull arangodb@sha256:a04dcd70c5b63c0e42e7895286d2aeb81e182cc3e2c5d483e14db8fc8976d116
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `arangodb:latest` - linux; amd64

```console
$ docker pull arangodb@sha256:fff7b1b64b128fff33d075ab2a3c62e5348890e3651303d09b0e6694d656199f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.2 MB (220153430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e85ab24ec06082598abbdb3d3d0934d57f00c38eece633c1aac5892ca1b28e8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Wed, 29 Mar 2023 18:19:28 GMT
ADD file:970e6b2578ef73457ffed1189e8ba128b0211cabd3174b8c7d3afd8fb58ad614 in / 
# Wed, 29 Mar 2023 18:19:28 GMT
CMD ["/bin/sh"]
# Wed, 29 Mar 2023 19:35:19 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Thu, 04 May 2023 17:35:20 GMT
ENV ARANGO_VERSION=3.10.6
# Thu, 04 May 2023 17:35:45 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb310/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Thu, 04 May 2023 17:35:46 GMT
ENV GLIBCXX_FORCE_NEW=1
# Thu, 04 May 2023 17:35:47 GMT
RUN echo "UTC" > /etc/timezone
# Thu, 04 May 2023 17:35:47 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Thu, 04 May 2023 17:35:47 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Thu, 04 May 2023 17:35:47 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Thu, 04 May 2023 17:35:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 04 May 2023 17:35:47 GMT
EXPOSE 8529
# Thu, 04 May 2023 17:35:48 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:91d30c5bc19582de1415b18f1ec5bcbf52a558b62cf6cc201c9669df9f748c22`  
		Last Modified: Wed, 29 Mar 2023 18:20:09 GMT  
		Size: 2.8 MB (2807803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a90de0772947794f476336da1b66553c3d0953919e307b15c23b909c2db45215`  
		Last Modified: Thu, 04 May 2023 17:36:23 GMT  
		Size: 217.3 MB (217343141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d061e173c84f434e3c88e502466c4d6c33f57869a9f72da43cc4cba35a3cfb1e`  
		Last Modified: Thu, 04 May 2023 17:36:01 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ed363dd0daeca109cc313c946b7e0d29876ed34dc7700cd4e2d412aaec8f805`  
		Last Modified: Thu, 04 May 2023 17:36:01 GMT  
		Size: 2.1 KB (2086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edc1190a2ff6497eea2dfa5b90ab026ec7cf7eb5c358b2881757808b68e0b2d2`  
		Last Modified: Thu, 04 May 2023 17:36:01 GMT  
		Size: 261.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `arangodb:latest` - linux; arm64 variant v8

```console
$ docker pull arangodb@sha256:00195880bfddb201705b222e7d72d6fc94fd002993a88d6bea4a0fe3f9d0cc75
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.9 MB (214857530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67d4dd0687cf9cfcff63defceee4c1357b834fc0db52551de10e5a6cfe44a89d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Wed, 29 Mar 2023 17:39:20 GMT
ADD file:a6a2f69b60d7d27bc6e2b9b7e9910dabdc3f5e3702c2345d26a7dc8c603ae595 in / 
# Wed, 29 Mar 2023 17:39:20 GMT
CMD ["/bin/sh"]
# Thu, 30 Mar 2023 03:53:47 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Thu, 04 May 2023 08:41:27 GMT
ENV ARANGO_VERSION=3.10.6
# Thu, 04 May 2023 08:41:51 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb310/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Thu, 04 May 2023 08:41:55 GMT
ENV GLIBCXX_FORCE_NEW=1
# Thu, 04 May 2023 08:41:55 GMT
RUN echo "UTC" > /etc/timezone
# Thu, 04 May 2023 08:41:55 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Thu, 04 May 2023 08:41:55 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Thu, 04 May 2023 08:41:55 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Thu, 04 May 2023 08:41:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 04 May 2023 08:41:55 GMT
EXPOSE 8529
# Thu, 04 May 2023 08:41:56 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:547446be3368f442c50ff95e2a2a9c85110b6b41bbb3c75b7e5ebb115f478b57`  
		Last Modified: Wed, 29 Mar 2023 17:39:56 GMT  
		Size: 2.7 MB (2709344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8854986b541b3b7fe6de76be4cac6cf004edc06cb36a08ac74d9540020bec69`  
		Last Modified: Thu, 04 May 2023 08:42:22 GMT  
		Size: 212.1 MB (212145698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0f61bb38c7d0276dbb3975069f3473117b08cb4597cffe623dc1b54935b517e`  
		Last Modified: Thu, 04 May 2023 08:42:07 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4f8628b18b9b058d1ebf269af140ec9e1919baa9793c1ff997cd0ffe15898e9`  
		Last Modified: Thu, 04 May 2023 08:42:06 GMT  
		Size: 2.1 KB (2087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce92e9544c02b8a53a5cb63b8f50ec53083a6ab616c728a785231f7ad4e0f278`  
		Last Modified: Thu, 04 May 2023 08:42:06 GMT  
		Size: 262.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
