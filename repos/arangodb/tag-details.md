<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `arangodb`

-	[`arangodb:3.10`](#arangodb310)
-	[`arangodb:3.10.5`](#arangodb3105)
-	[`arangodb:3.8`](#arangodb38)
-	[`arangodb:3.8.8`](#arangodb388)
-	[`arangodb:3.9`](#arangodb39)
-	[`arangodb:3.9.10`](#arangodb3910)
-	[`arangodb:latest`](#arangodblatest)

## `arangodb:3.10`

```console
$ docker pull arangodb@sha256:62d047ff5a3d3c4ed587e19810beb88697bce6f4fc8210f1f2f7ed6b95c9a0db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `arangodb:3.10` - linux; amd64

```console
$ docker pull arangodb@sha256:06f6e77e2218aa2df240b2af6c9d4373e11f0bb3218e396df1f8f630c39da2cf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.0 MB (220044042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91c5c8e9ebae1fa1a6434778510f5d3c5164745f8c0afa5ddcc2ca2ae3606b85`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:50 GMT
ADD file:ac5fb7eb0d68040d948989f0a50914d0d4a6b631cfe76b508eecd82eb7d46953 in / 
# Sat, 11 Feb 2023 04:46:50 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 07:14:04 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Wed, 22 Mar 2023 23:21:52 GMT
ENV ARANGO_VERSION=3.10.5
# Wed, 22 Mar 2023 23:22:16 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb310/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Wed, 22 Mar 2023 23:22:18 GMT
ENV GLIBCXX_FORCE_NEW=1
# Wed, 22 Mar 2023 23:22:18 GMT
RUN echo "UTC" > /etc/timezone
# Wed, 22 Mar 2023 23:22:18 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Wed, 22 Mar 2023 23:22:19 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Wed, 22 Mar 2023 23:22:19 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Wed, 22 Mar 2023 23:22:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Mar 2023 23:22:19 GMT
EXPOSE 8529
# Wed, 22 Mar 2023 23:22:19 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:ef5531b6e74e7865f5d142926b572d742ad47c153211de707903b4f5dd8d9e77`  
		Last Modified: Sat, 11 Feb 2023 04:47:32 GMT  
		Size: 2.8 MB (2807762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b954adda27a7bb2ea3c1d1765316afc66e4e38a9fe335f9de753328be9d243c1`  
		Last Modified: Wed, 22 Mar 2023 23:23:26 GMT  
		Size: 217.2 MB (217233795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96acfdb6a01cd3a47b070c45433ba136c1812ca36186751265c6ed81efdfa219`  
		Last Modified: Wed, 22 Mar 2023 23:23:04 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fdb9cc36dbb5d77c8b684c74ed908f39e51532363f8040a4ec0c3d805f7194a`  
		Last Modified: Wed, 22 Mar 2023 23:23:04 GMT  
		Size: 2.1 KB (2085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61cfec1118a50430656ad0e7dc2a72f400ba1c90d17d41e759de9c16c52f0dd0`  
		Last Modified: Wed, 22 Mar 2023 23:23:05 GMT  
		Size: 261.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `arangodb:3.10` - linux; arm64 variant v8

```console
$ docker pull arangodb@sha256:3cae9e8aacac2c50661b9ee8b21abae1148549a1d30d2e884073512fe2aac75d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.8 MB (214752771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd9a975e8db55f5c0af5d6fd664ca7b33ea1c3dca2fd2a336185c9decb4e7c5f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:13 GMT
ADD file:738e640812bf6089767190a2976ceffc11f3e809be3e2b1ebb43c85ad3199fba in / 
# Fri, 10 Feb 2023 21:24:13 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 21:40:53 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Wed, 22 Mar 2023 23:42:44 GMT
ENV ARANGO_VERSION=3.10.5
# Wed, 22 Mar 2023 23:43:08 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb310/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Wed, 22 Mar 2023 23:43:11 GMT
ENV GLIBCXX_FORCE_NEW=1
# Wed, 22 Mar 2023 23:43:12 GMT
RUN echo "UTC" > /etc/timezone
# Wed, 22 Mar 2023 23:43:12 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Wed, 22 Mar 2023 23:43:12 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Wed, 22 Mar 2023 23:43:12 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Wed, 22 Mar 2023 23:43:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Mar 2023 23:43:12 GMT
EXPOSE 8529
# Wed, 22 Mar 2023 23:43:12 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:3760b48202b3e349986edb6fe5dd93cd003726b7c345d51f6fc4ace1b46fc2ba`  
		Last Modified: Fri, 10 Feb 2023 21:24:52 GMT  
		Size: 2.7 MB (2709502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2aa0dd90b1dc1bff7bfc5c28e1a2497b2e4facb97592f3e961c56f8f641893c`  
		Last Modified: Wed, 22 Mar 2023 23:43:38 GMT  
		Size: 212.0 MB (212040783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f145ec7697dbd98446906b91acfafd51dfa3d4841c2a3bbd1b9258228d924ddf`  
		Last Modified: Wed, 22 Mar 2023 23:43:22 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44374400d50e3b7a17a84cbbd6181d56ad3ff282fae72d3a9d25c7cabd2772dd`  
		Last Modified: Wed, 22 Mar 2023 23:43:22 GMT  
		Size: 2.1 KB (2085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6a031c0079436fe91e4d55ced9446bed63816a8234188cb2a4b9df018c628a2`  
		Last Modified: Wed, 22 Mar 2023 23:43:22 GMT  
		Size: 262.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:3.10.5`

```console
$ docker pull arangodb@sha256:62d047ff5a3d3c4ed587e19810beb88697bce6f4fc8210f1f2f7ed6b95c9a0db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `arangodb:3.10.5` - linux; amd64

```console
$ docker pull arangodb@sha256:06f6e77e2218aa2df240b2af6c9d4373e11f0bb3218e396df1f8f630c39da2cf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.0 MB (220044042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91c5c8e9ebae1fa1a6434778510f5d3c5164745f8c0afa5ddcc2ca2ae3606b85`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:50 GMT
ADD file:ac5fb7eb0d68040d948989f0a50914d0d4a6b631cfe76b508eecd82eb7d46953 in / 
# Sat, 11 Feb 2023 04:46:50 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 07:14:04 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Wed, 22 Mar 2023 23:21:52 GMT
ENV ARANGO_VERSION=3.10.5
# Wed, 22 Mar 2023 23:22:16 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb310/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Wed, 22 Mar 2023 23:22:18 GMT
ENV GLIBCXX_FORCE_NEW=1
# Wed, 22 Mar 2023 23:22:18 GMT
RUN echo "UTC" > /etc/timezone
# Wed, 22 Mar 2023 23:22:18 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Wed, 22 Mar 2023 23:22:19 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Wed, 22 Mar 2023 23:22:19 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Wed, 22 Mar 2023 23:22:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Mar 2023 23:22:19 GMT
EXPOSE 8529
# Wed, 22 Mar 2023 23:22:19 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:ef5531b6e74e7865f5d142926b572d742ad47c153211de707903b4f5dd8d9e77`  
		Last Modified: Sat, 11 Feb 2023 04:47:32 GMT  
		Size: 2.8 MB (2807762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b954adda27a7bb2ea3c1d1765316afc66e4e38a9fe335f9de753328be9d243c1`  
		Last Modified: Wed, 22 Mar 2023 23:23:26 GMT  
		Size: 217.2 MB (217233795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96acfdb6a01cd3a47b070c45433ba136c1812ca36186751265c6ed81efdfa219`  
		Last Modified: Wed, 22 Mar 2023 23:23:04 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fdb9cc36dbb5d77c8b684c74ed908f39e51532363f8040a4ec0c3d805f7194a`  
		Last Modified: Wed, 22 Mar 2023 23:23:04 GMT  
		Size: 2.1 KB (2085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61cfec1118a50430656ad0e7dc2a72f400ba1c90d17d41e759de9c16c52f0dd0`  
		Last Modified: Wed, 22 Mar 2023 23:23:05 GMT  
		Size: 261.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `arangodb:3.10.5` - linux; arm64 variant v8

```console
$ docker pull arangodb@sha256:3cae9e8aacac2c50661b9ee8b21abae1148549a1d30d2e884073512fe2aac75d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.8 MB (214752771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd9a975e8db55f5c0af5d6fd664ca7b33ea1c3dca2fd2a336185c9decb4e7c5f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:13 GMT
ADD file:738e640812bf6089767190a2976ceffc11f3e809be3e2b1ebb43c85ad3199fba in / 
# Fri, 10 Feb 2023 21:24:13 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 21:40:53 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Wed, 22 Mar 2023 23:42:44 GMT
ENV ARANGO_VERSION=3.10.5
# Wed, 22 Mar 2023 23:43:08 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb310/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Wed, 22 Mar 2023 23:43:11 GMT
ENV GLIBCXX_FORCE_NEW=1
# Wed, 22 Mar 2023 23:43:12 GMT
RUN echo "UTC" > /etc/timezone
# Wed, 22 Mar 2023 23:43:12 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Wed, 22 Mar 2023 23:43:12 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Wed, 22 Mar 2023 23:43:12 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Wed, 22 Mar 2023 23:43:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Mar 2023 23:43:12 GMT
EXPOSE 8529
# Wed, 22 Mar 2023 23:43:12 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:3760b48202b3e349986edb6fe5dd93cd003726b7c345d51f6fc4ace1b46fc2ba`  
		Last Modified: Fri, 10 Feb 2023 21:24:52 GMT  
		Size: 2.7 MB (2709502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2aa0dd90b1dc1bff7bfc5c28e1a2497b2e4facb97592f3e961c56f8f641893c`  
		Last Modified: Wed, 22 Mar 2023 23:43:38 GMT  
		Size: 212.0 MB (212040783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f145ec7697dbd98446906b91acfafd51dfa3d4841c2a3bbd1b9258228d924ddf`  
		Last Modified: Wed, 22 Mar 2023 23:43:22 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44374400d50e3b7a17a84cbbd6181d56ad3ff282fae72d3a9d25c7cabd2772dd`  
		Last Modified: Wed, 22 Mar 2023 23:43:22 GMT  
		Size: 2.1 KB (2085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6a031c0079436fe91e4d55ced9446bed63816a8234188cb2a4b9df018c628a2`  
		Last Modified: Wed, 22 Mar 2023 23:43:22 GMT  
		Size: 262.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:3.8`

```console
$ docker pull arangodb@sha256:8875dd096a2bf77e0b4e09ccb22eecc62194ff97e3676d76a119072381d8232a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `arangodb:3.8` - linux; amd64

```console
$ docker pull arangodb@sha256:5e9491426371da85a3f76964df73af2bee2b2fd1f2afc2bb37ec6d27399e1321
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.6 MB (195563968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a69ee5f4a17e15afb32ca08346a1d3735b40dd04a0e1114815c95ce7d3df229f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:59 GMT
ADD file:a41bb436701fd0adf99a3157d19f172b3e54ea033f5c617009e2d1bdeac206d7 in / 
# Sat, 11 Feb 2023 04:46:59 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 07:12:56 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Sat, 11 Feb 2023 07:12:56 GMT
ENV ARANGO_VERSION=3.8.8
# Sat, 11 Feb 2023 07:12:56 GMT
ENV ARANGO_URL=https://download.arangodb.com/arangodb38/DEBIAN/amd64
# Sat, 11 Feb 2023 07:12:56 GMT
ENV ARANGO_PACKAGE=arangodb3_3.8.8-1_amd64.deb
# Sat, 11 Feb 2023 07:12:56 GMT
ENV ARANGO_PACKAGE_URL=https://download.arangodb.com/arangodb38/DEBIAN/amd64/arangodb3_3.8.8-1_amd64.deb
# Sat, 11 Feb 2023 07:12:57 GMT
ENV ARANGO_SIGNATURE_URL=https://download.arangodb.com/arangodb38/DEBIAN/amd64/arangodb3_3.8.8-1_amd64.deb.asc
# Sat, 11 Feb 2023 07:13:22 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.0.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Sat, 11 Feb 2023 07:13:24 GMT
ENV GLIBCXX_FORCE_NEW=1
# Sat, 11 Feb 2023 07:13:24 GMT
RUN echo "UTC" > /etc/timezone
# Sat, 11 Feb 2023 07:13:24 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Sat, 11 Feb 2023 07:13:24 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Sat, 11 Feb 2023 07:13:25 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Sat, 11 Feb 2023 07:13:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 11 Feb 2023 07:13:25 GMT
EXPOSE 8529
# Sat, 11 Feb 2023 07:13:25 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:d261077062b2aebb9ca8dc61f2b00e7e2b4e44179d3cfbe526c4ee0c5e41b26f`  
		Last Modified: Sat, 11 Feb 2023 04:47:49 GMT  
		Size: 2.8 MB (2829633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b52f97a875524282e52658d0cebb1aea3d76cdb9d92896c0af291ccc4c5fd45a`  
		Last Modified: Sat, 11 Feb 2023 07:15:09 GMT  
		Size: 192.7 MB (192731851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbca32a09d4b2233aaf87eb68dd9d99ff43903a1bedf0db1209bf01ba0a01e51`  
		Last Modified: Sat, 11 Feb 2023 07:14:47 GMT  
		Size: 136.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63f77081e4f0927ab4c1d0968996a8c52e9d6c6582f16dd9034623b62f7242d7`  
		Last Modified: Sat, 11 Feb 2023 07:14:47 GMT  
		Size: 2.1 KB (2085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10a35dade599ba08dfe1b3eff1eed291c8e245457e46f26ca672739180e40f16`  
		Last Modified: Sat, 11 Feb 2023 07:14:47 GMT  
		Size: 263.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:3.8.8`

```console
$ docker pull arangodb@sha256:8875dd096a2bf77e0b4e09ccb22eecc62194ff97e3676d76a119072381d8232a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `arangodb:3.8.8` - linux; amd64

```console
$ docker pull arangodb@sha256:5e9491426371da85a3f76964df73af2bee2b2fd1f2afc2bb37ec6d27399e1321
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.6 MB (195563968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a69ee5f4a17e15afb32ca08346a1d3735b40dd04a0e1114815c95ce7d3df229f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:59 GMT
ADD file:a41bb436701fd0adf99a3157d19f172b3e54ea033f5c617009e2d1bdeac206d7 in / 
# Sat, 11 Feb 2023 04:46:59 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 07:12:56 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Sat, 11 Feb 2023 07:12:56 GMT
ENV ARANGO_VERSION=3.8.8
# Sat, 11 Feb 2023 07:12:56 GMT
ENV ARANGO_URL=https://download.arangodb.com/arangodb38/DEBIAN/amd64
# Sat, 11 Feb 2023 07:12:56 GMT
ENV ARANGO_PACKAGE=arangodb3_3.8.8-1_amd64.deb
# Sat, 11 Feb 2023 07:12:56 GMT
ENV ARANGO_PACKAGE_URL=https://download.arangodb.com/arangodb38/DEBIAN/amd64/arangodb3_3.8.8-1_amd64.deb
# Sat, 11 Feb 2023 07:12:57 GMT
ENV ARANGO_SIGNATURE_URL=https://download.arangodb.com/arangodb38/DEBIAN/amd64/arangodb3_3.8.8-1_amd64.deb.asc
# Sat, 11 Feb 2023 07:13:22 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.0.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Sat, 11 Feb 2023 07:13:24 GMT
ENV GLIBCXX_FORCE_NEW=1
# Sat, 11 Feb 2023 07:13:24 GMT
RUN echo "UTC" > /etc/timezone
# Sat, 11 Feb 2023 07:13:24 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Sat, 11 Feb 2023 07:13:24 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Sat, 11 Feb 2023 07:13:25 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Sat, 11 Feb 2023 07:13:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 11 Feb 2023 07:13:25 GMT
EXPOSE 8529
# Sat, 11 Feb 2023 07:13:25 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:d261077062b2aebb9ca8dc61f2b00e7e2b4e44179d3cfbe526c4ee0c5e41b26f`  
		Last Modified: Sat, 11 Feb 2023 04:47:49 GMT  
		Size: 2.8 MB (2829633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b52f97a875524282e52658d0cebb1aea3d76cdb9d92896c0af291ccc4c5fd45a`  
		Last Modified: Sat, 11 Feb 2023 07:15:09 GMT  
		Size: 192.7 MB (192731851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbca32a09d4b2233aaf87eb68dd9d99ff43903a1bedf0db1209bf01ba0a01e51`  
		Last Modified: Sat, 11 Feb 2023 07:14:47 GMT  
		Size: 136.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63f77081e4f0927ab4c1d0968996a8c52e9d6c6582f16dd9034623b62f7242d7`  
		Last Modified: Sat, 11 Feb 2023 07:14:47 GMT  
		Size: 2.1 KB (2085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10a35dade599ba08dfe1b3eff1eed291c8e245457e46f26ca672739180e40f16`  
		Last Modified: Sat, 11 Feb 2023 07:14:47 GMT  
		Size: 263.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:3.9`

```console
$ docker pull arangodb@sha256:77cdbc1b4635f4805b4c236ef58102d706ad9bd52b2951fa6f798215409572b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `arangodb:3.9` - linux; amd64

```console
$ docker pull arangodb@sha256:212c95329400fe732d4ed5538979059937ce3033df79d997ed62ede9ff328f30
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.7 MB (202717784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae5cf16ed7acd2c0324d7a39bcfb9461c9b94647e25ee391e0a4f6521557c57b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:59 GMT
ADD file:a41bb436701fd0adf99a3157d19f172b3e54ea033f5c617009e2d1bdeac206d7 in / 
# Sat, 11 Feb 2023 04:46:59 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 07:12:56 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Wed, 22 Mar 2023 23:21:18 GMT
ENV ARANGO_VERSION=3.9.10
# Wed, 22 Mar 2023 23:21:18 GMT
ENV ARANGO_URL=https://download.arangodb.com/arangodb39/DEBIAN/amd64
# Wed, 22 Mar 2023 23:21:18 GMT
ENV ARANGO_PACKAGE=arangodb3_3.9.10-1_amd64.deb
# Wed, 22 Mar 2023 23:21:18 GMT
ENV ARANGO_PACKAGE_URL=https://download.arangodb.com/arangodb39/DEBIAN/amd64/arangodb3_3.9.10-1_amd64.deb
# Wed, 22 Mar 2023 23:21:19 GMT
ENV ARANGO_SIGNATURE_URL=https://download.arangodb.com/arangodb39/DEBIAN/amd64/arangodb3_3.9.10-1_amd64.deb.asc
# Wed, 22 Mar 2023 23:21:43 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Wed, 22 Mar 2023 23:21:44 GMT
ENV GLIBCXX_FORCE_NEW=1
# Wed, 22 Mar 2023 23:21:45 GMT
RUN echo "UTC" > /etc/timezone
# Wed, 22 Mar 2023 23:21:45 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Wed, 22 Mar 2023 23:21:45 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Wed, 22 Mar 2023 23:21:45 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Wed, 22 Mar 2023 23:21:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Mar 2023 23:21:45 GMT
EXPOSE 8529
# Wed, 22 Mar 2023 23:21:45 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:d261077062b2aebb9ca8dc61f2b00e7e2b4e44179d3cfbe526c4ee0c5e41b26f`  
		Last Modified: Sat, 11 Feb 2023 04:47:49 GMT  
		Size: 2.8 MB (2829633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdc41df59d48247183e8b79238967e7513b1f273bf2e2cd9c6b10264ec1608aa`  
		Last Modified: Wed, 22 Mar 2023 23:22:55 GMT  
		Size: 199.9 MB (199885664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:938529aa3de9f020d2c2a3f640d703433c957189d0b403e3556a91db8a6806f5`  
		Last Modified: Wed, 22 Mar 2023 23:22:34 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0331699df4f626ccdc0ec4c93c0c3b022d54d3d3719dfed2ded9603aef3d5dde`  
		Last Modified: Wed, 22 Mar 2023 23:22:34 GMT  
		Size: 2.1 KB (2086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8255c07ffa9d37779f7c8045c5f37d0f89014aadcc6d59dceadf9cf7bb69aa29`  
		Last Modified: Wed, 22 Mar 2023 23:22:34 GMT  
		Size: 262.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:3.9.10`

```console
$ docker pull arangodb@sha256:77cdbc1b4635f4805b4c236ef58102d706ad9bd52b2951fa6f798215409572b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `arangodb:3.9.10` - linux; amd64

```console
$ docker pull arangodb@sha256:212c95329400fe732d4ed5538979059937ce3033df79d997ed62ede9ff328f30
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.7 MB (202717784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae5cf16ed7acd2c0324d7a39bcfb9461c9b94647e25ee391e0a4f6521557c57b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:59 GMT
ADD file:a41bb436701fd0adf99a3157d19f172b3e54ea033f5c617009e2d1bdeac206d7 in / 
# Sat, 11 Feb 2023 04:46:59 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 07:12:56 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Wed, 22 Mar 2023 23:21:18 GMT
ENV ARANGO_VERSION=3.9.10
# Wed, 22 Mar 2023 23:21:18 GMT
ENV ARANGO_URL=https://download.arangodb.com/arangodb39/DEBIAN/amd64
# Wed, 22 Mar 2023 23:21:18 GMT
ENV ARANGO_PACKAGE=arangodb3_3.9.10-1_amd64.deb
# Wed, 22 Mar 2023 23:21:18 GMT
ENV ARANGO_PACKAGE_URL=https://download.arangodb.com/arangodb39/DEBIAN/amd64/arangodb3_3.9.10-1_amd64.deb
# Wed, 22 Mar 2023 23:21:19 GMT
ENV ARANGO_SIGNATURE_URL=https://download.arangodb.com/arangodb39/DEBIAN/amd64/arangodb3_3.9.10-1_amd64.deb.asc
# Wed, 22 Mar 2023 23:21:43 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Wed, 22 Mar 2023 23:21:44 GMT
ENV GLIBCXX_FORCE_NEW=1
# Wed, 22 Mar 2023 23:21:45 GMT
RUN echo "UTC" > /etc/timezone
# Wed, 22 Mar 2023 23:21:45 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Wed, 22 Mar 2023 23:21:45 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Wed, 22 Mar 2023 23:21:45 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Wed, 22 Mar 2023 23:21:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Mar 2023 23:21:45 GMT
EXPOSE 8529
# Wed, 22 Mar 2023 23:21:45 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:d261077062b2aebb9ca8dc61f2b00e7e2b4e44179d3cfbe526c4ee0c5e41b26f`  
		Last Modified: Sat, 11 Feb 2023 04:47:49 GMT  
		Size: 2.8 MB (2829633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdc41df59d48247183e8b79238967e7513b1f273bf2e2cd9c6b10264ec1608aa`  
		Last Modified: Wed, 22 Mar 2023 23:22:55 GMT  
		Size: 199.9 MB (199885664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:938529aa3de9f020d2c2a3f640d703433c957189d0b403e3556a91db8a6806f5`  
		Last Modified: Wed, 22 Mar 2023 23:22:34 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0331699df4f626ccdc0ec4c93c0c3b022d54d3d3719dfed2ded9603aef3d5dde`  
		Last Modified: Wed, 22 Mar 2023 23:22:34 GMT  
		Size: 2.1 KB (2086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8255c07ffa9d37779f7c8045c5f37d0f89014aadcc6d59dceadf9cf7bb69aa29`  
		Last Modified: Wed, 22 Mar 2023 23:22:34 GMT  
		Size: 262.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:latest`

```console
$ docker pull arangodb@sha256:62d047ff5a3d3c4ed587e19810beb88697bce6f4fc8210f1f2f7ed6b95c9a0db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `arangodb:latest` - linux; amd64

```console
$ docker pull arangodb@sha256:06f6e77e2218aa2df240b2af6c9d4373e11f0bb3218e396df1f8f630c39da2cf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.0 MB (220044042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91c5c8e9ebae1fa1a6434778510f5d3c5164745f8c0afa5ddcc2ca2ae3606b85`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:50 GMT
ADD file:ac5fb7eb0d68040d948989f0a50914d0d4a6b631cfe76b508eecd82eb7d46953 in / 
# Sat, 11 Feb 2023 04:46:50 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 07:14:04 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Wed, 22 Mar 2023 23:21:52 GMT
ENV ARANGO_VERSION=3.10.5
# Wed, 22 Mar 2023 23:22:16 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb310/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Wed, 22 Mar 2023 23:22:18 GMT
ENV GLIBCXX_FORCE_NEW=1
# Wed, 22 Mar 2023 23:22:18 GMT
RUN echo "UTC" > /etc/timezone
# Wed, 22 Mar 2023 23:22:18 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Wed, 22 Mar 2023 23:22:19 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Wed, 22 Mar 2023 23:22:19 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Wed, 22 Mar 2023 23:22:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Mar 2023 23:22:19 GMT
EXPOSE 8529
# Wed, 22 Mar 2023 23:22:19 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:ef5531b6e74e7865f5d142926b572d742ad47c153211de707903b4f5dd8d9e77`  
		Last Modified: Sat, 11 Feb 2023 04:47:32 GMT  
		Size: 2.8 MB (2807762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b954adda27a7bb2ea3c1d1765316afc66e4e38a9fe335f9de753328be9d243c1`  
		Last Modified: Wed, 22 Mar 2023 23:23:26 GMT  
		Size: 217.2 MB (217233795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96acfdb6a01cd3a47b070c45433ba136c1812ca36186751265c6ed81efdfa219`  
		Last Modified: Wed, 22 Mar 2023 23:23:04 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fdb9cc36dbb5d77c8b684c74ed908f39e51532363f8040a4ec0c3d805f7194a`  
		Last Modified: Wed, 22 Mar 2023 23:23:04 GMT  
		Size: 2.1 KB (2085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61cfec1118a50430656ad0e7dc2a72f400ba1c90d17d41e759de9c16c52f0dd0`  
		Last Modified: Wed, 22 Mar 2023 23:23:05 GMT  
		Size: 261.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `arangodb:latest` - linux; arm64 variant v8

```console
$ docker pull arangodb@sha256:3cae9e8aacac2c50661b9ee8b21abae1148549a1d30d2e884073512fe2aac75d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.8 MB (214752771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd9a975e8db55f5c0af5d6fd664ca7b33ea1c3dca2fd2a336185c9decb4e7c5f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:13 GMT
ADD file:738e640812bf6089767190a2976ceffc11f3e809be3e2b1ebb43c85ad3199fba in / 
# Fri, 10 Feb 2023 21:24:13 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 21:40:53 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Wed, 22 Mar 2023 23:42:44 GMT
ENV ARANGO_VERSION=3.10.5
# Wed, 22 Mar 2023 23:43:08 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb310/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Wed, 22 Mar 2023 23:43:11 GMT
ENV GLIBCXX_FORCE_NEW=1
# Wed, 22 Mar 2023 23:43:12 GMT
RUN echo "UTC" > /etc/timezone
# Wed, 22 Mar 2023 23:43:12 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Wed, 22 Mar 2023 23:43:12 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Wed, 22 Mar 2023 23:43:12 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Wed, 22 Mar 2023 23:43:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Mar 2023 23:43:12 GMT
EXPOSE 8529
# Wed, 22 Mar 2023 23:43:12 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:3760b48202b3e349986edb6fe5dd93cd003726b7c345d51f6fc4ace1b46fc2ba`  
		Last Modified: Fri, 10 Feb 2023 21:24:52 GMT  
		Size: 2.7 MB (2709502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2aa0dd90b1dc1bff7bfc5c28e1a2497b2e4facb97592f3e961c56f8f641893c`  
		Last Modified: Wed, 22 Mar 2023 23:43:38 GMT  
		Size: 212.0 MB (212040783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f145ec7697dbd98446906b91acfafd51dfa3d4841c2a3bbd1b9258228d924ddf`  
		Last Modified: Wed, 22 Mar 2023 23:43:22 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44374400d50e3b7a17a84cbbd6181d56ad3ff282fae72d3a9d25c7cabd2772dd`  
		Last Modified: Wed, 22 Mar 2023 23:43:22 GMT  
		Size: 2.1 KB (2085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6a031c0079436fe91e4d55ced9446bed63816a8234188cb2a4b9df018c628a2`  
		Last Modified: Wed, 22 Mar 2023 23:43:22 GMT  
		Size: 262.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
