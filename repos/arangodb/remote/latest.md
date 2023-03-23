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
