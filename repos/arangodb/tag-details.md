<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `arangodb`

-	[`arangodb:3.10`](#arangodb310)
-	[`arangodb:3.10.6`](#arangodb3106)
-	[`arangodb:3.11`](#arangodb311)
-	[`arangodb:3.11.0`](#arangodb3110)
-	[`arangodb:3.9`](#arangodb39)
-	[`arangodb:3.9.11`](#arangodb3911)
-	[`arangodb:latest`](#arangodblatest)

## `arangodb:3.10`

```console
$ docker pull arangodb@sha256:db1b031952c08e0ca9034e4b748101e3613165c75aa41bdae5a0f9f9c79cfbcc
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
$ docker pull arangodb@sha256:cace3377a4a931248ef08d1d78aac3b6599d3cc1ec68a9a1f1f8b3742aa49f24
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.9 MB (214945690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a66ac2f4fad9ed0f456c2bab20068d299071e534bc8bf27b561051ba8aa70081`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Wed, 14 Jun 2023 20:49:07 GMT
ADD file:e80eabe59d1f87ef41634428d9f8fdeb633c2128ac97564f96f5495ef6bf2c72 in / 
# Wed, 14 Jun 2023 20:49:07 GMT
CMD ["/bin/sh"]
# Wed, 14 Jun 2023 22:45:26 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Wed, 14 Jun 2023 22:45:26 GMT
ENV ARANGO_VERSION=3.10.6
# Wed, 14 Jun 2023 22:45:51 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb310/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Wed, 14 Jun 2023 22:45:55 GMT
ENV GLIBCXX_FORCE_NEW=1
# Wed, 14 Jun 2023 22:45:56 GMT
RUN echo "UTC" > /etc/timezone
# Wed, 14 Jun 2023 22:45:56 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Wed, 14 Jun 2023 22:45:56 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Wed, 14 Jun 2023 22:45:56 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Wed, 14 Jun 2023 22:45:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 14 Jun 2023 22:45:56 GMT
EXPOSE 8529
# Wed, 14 Jun 2023 22:45:56 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:a880266d3b77f75696023df2da1ef66c3c565e0f70596242395c9e68de955c7c`  
		Last Modified: Wed, 14 Jun 2023 20:49:43 GMT  
		Size: 2.7 MB (2707906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba74b1b82b388746f7ae718c248d35026157e1181985f98bf6d472117c50a97f`  
		Last Modified: Wed, 14 Jun 2023 22:46:55 GMT  
		Size: 212.2 MB (212235298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3651d7cd2f983c440bd666e4c8fe83b4dc1f125f567f452209fc309a68050bab`  
		Last Modified: Wed, 14 Jun 2023 22:46:39 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:728532038f5c9220c7edcb2fc3d78b70275c144a04259b9e13ddad9aac3fe229`  
		Last Modified: Wed, 14 Jun 2023 22:46:39 GMT  
		Size: 2.1 KB (2085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6be6b36686de24f2860356e102516661b3121a8a330998463f7f4a78c812a34d`  
		Last Modified: Wed, 14 Jun 2023 22:46:39 GMT  
		Size: 262.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:3.10.6`

```console
$ docker pull arangodb@sha256:db1b031952c08e0ca9034e4b748101e3613165c75aa41bdae5a0f9f9c79cfbcc
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
$ docker pull arangodb@sha256:cace3377a4a931248ef08d1d78aac3b6599d3cc1ec68a9a1f1f8b3742aa49f24
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.9 MB (214945690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a66ac2f4fad9ed0f456c2bab20068d299071e534bc8bf27b561051ba8aa70081`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Wed, 14 Jun 2023 20:49:07 GMT
ADD file:e80eabe59d1f87ef41634428d9f8fdeb633c2128ac97564f96f5495ef6bf2c72 in / 
# Wed, 14 Jun 2023 20:49:07 GMT
CMD ["/bin/sh"]
# Wed, 14 Jun 2023 22:45:26 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Wed, 14 Jun 2023 22:45:26 GMT
ENV ARANGO_VERSION=3.10.6
# Wed, 14 Jun 2023 22:45:51 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb310/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Wed, 14 Jun 2023 22:45:55 GMT
ENV GLIBCXX_FORCE_NEW=1
# Wed, 14 Jun 2023 22:45:56 GMT
RUN echo "UTC" > /etc/timezone
# Wed, 14 Jun 2023 22:45:56 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Wed, 14 Jun 2023 22:45:56 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Wed, 14 Jun 2023 22:45:56 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Wed, 14 Jun 2023 22:45:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 14 Jun 2023 22:45:56 GMT
EXPOSE 8529
# Wed, 14 Jun 2023 22:45:56 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:a880266d3b77f75696023df2da1ef66c3c565e0f70596242395c9e68de955c7c`  
		Last Modified: Wed, 14 Jun 2023 20:49:43 GMT  
		Size: 2.7 MB (2707906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba74b1b82b388746f7ae718c248d35026157e1181985f98bf6d472117c50a97f`  
		Last Modified: Wed, 14 Jun 2023 22:46:55 GMT  
		Size: 212.2 MB (212235298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3651d7cd2f983c440bd666e4c8fe83b4dc1f125f567f452209fc309a68050bab`  
		Last Modified: Wed, 14 Jun 2023 22:46:39 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:728532038f5c9220c7edcb2fc3d78b70275c144a04259b9e13ddad9aac3fe229`  
		Last Modified: Wed, 14 Jun 2023 22:46:39 GMT  
		Size: 2.1 KB (2085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6be6b36686de24f2860356e102516661b3121a8a330998463f7f4a78c812a34d`  
		Last Modified: Wed, 14 Jun 2023 22:46:39 GMT  
		Size: 262.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:3.11`

```console
$ docker pull arangodb@sha256:ee1b8182f168a8c2742dc122cd8a3af6cabaed425eb21c84a81f1b239208b02a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `arangodb:3.11` - linux; amd64

```console
$ docker pull arangodb@sha256:b6b9e69bc433655ec3a04f41b0dde212d4080babc0316b3029897dfbe1e54750
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.0 MB (243964371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90184ccfdeb2eabf0e0e6019b7745574b4ae36380a9f8e13e9bfeb5618fa426c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Wed, 29 Mar 2023 18:19:28 GMT
ADD file:970e6b2578ef73457ffed1189e8ba128b0211cabd3174b8c7d3afd8fb58ad614 in / 
# Wed, 29 Mar 2023 18:19:28 GMT
CMD ["/bin/sh"]
# Wed, 29 Mar 2023 19:35:19 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Fri, 26 May 2023 22:48:01 GMT
ENV ARANGO_VERSION=3.11.0
# Fri, 26 May 2023 22:48:30 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb311/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Fri, 26 May 2023 22:48:31 GMT
ENV GLIBCXX_FORCE_NEW=1
# Fri, 26 May 2023 22:48:32 GMT
RUN echo "UTC" > /etc/timezone
# Fri, 26 May 2023 22:48:32 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Fri, 26 May 2023 22:48:32 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Fri, 26 May 2023 22:48:32 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Fri, 26 May 2023 22:48:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 May 2023 22:48:32 GMT
EXPOSE 8529
# Fri, 26 May 2023 22:48:32 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:91d30c5bc19582de1415b18f1ec5bcbf52a558b62cf6cc201c9669df9f748c22`  
		Last Modified: Wed, 29 Mar 2023 18:20:09 GMT  
		Size: 2.8 MB (2807803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04b5248d92652fb9e51ec0e23dcb31a174ee1a3d8e55a093f43067aa799cf0f4`  
		Last Modified: Fri, 26 May 2023 22:49:07 GMT  
		Size: 241.2 MB (241154082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:337b4d1efaae1f2582f39582e14c09d379068f55ab1a9a112475b3dbffd08838`  
		Last Modified: Fri, 26 May 2023 22:48:44 GMT  
		Size: 137.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01a1ddc19c647fd79e5abf0a8ba11d17a29976cddeec8cff5a0a1906994d6aa5`  
		Last Modified: Fri, 26 May 2023 22:48:44 GMT  
		Size: 2.1 KB (2086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4508e0738e7d2dce04d6048661b811852ee754388c7f054024dcdb82ae4a908`  
		Last Modified: Fri, 26 May 2023 22:48:44 GMT  
		Size: 263.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `arangodb:3.11` - linux; arm64 variant v8

```console
$ docker pull arangodb@sha256:a91dada434e4be42b0a5345e822bd882fb8e4b2214a8e66c2183b84c1b801bd9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.3 MB (238338461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2264bd13f4357f422d5b166946b50c38cb495df6ea073f3cbd9e23d2b88a4072`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Wed, 14 Jun 2023 20:49:07 GMT
ADD file:e80eabe59d1f87ef41634428d9f8fdeb633c2128ac97564f96f5495ef6bf2c72 in / 
# Wed, 14 Jun 2023 20:49:07 GMT
CMD ["/bin/sh"]
# Wed, 14 Jun 2023 22:45:26 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Wed, 14 Jun 2023 22:46:00 GMT
ENV ARANGO_VERSION=3.11.0
# Wed, 14 Jun 2023 22:46:24 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb311/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Wed, 14 Jun 2023 22:46:27 GMT
ENV GLIBCXX_FORCE_NEW=1
# Wed, 14 Jun 2023 22:46:28 GMT
RUN echo "UTC" > /etc/timezone
# Wed, 14 Jun 2023 22:46:28 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Wed, 14 Jun 2023 22:46:28 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Wed, 14 Jun 2023 22:46:28 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Wed, 14 Jun 2023 22:46:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 14 Jun 2023 22:46:28 GMT
EXPOSE 8529
# Wed, 14 Jun 2023 22:46:28 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:a880266d3b77f75696023df2da1ef66c3c565e0f70596242395c9e68de955c7c`  
		Last Modified: Wed, 14 Jun 2023 20:49:43 GMT  
		Size: 2.7 MB (2707906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5da19c8f6a1edbfd55d983afeea9d58150da07a58824672f1a02e885267d0412`  
		Last Modified: Wed, 14 Jun 2023 22:47:25 GMT  
		Size: 235.6 MB (235628068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b39cc356770a9f35dfcf88166308eb81917cf0f9268aeb1a6615e18bd914f6`  
		Last Modified: Wed, 14 Jun 2023 22:47:08 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07ee3329ebc66f51f7e2757cd64d9ad46257008561ae95805b9cbb9f1e30622a`  
		Last Modified: Wed, 14 Jun 2023 22:47:08 GMT  
		Size: 2.1 KB (2086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:743957648b762a7dce68adabf44903ad76d669bddd9081ccf26887519a8ac0c3`  
		Last Modified: Wed, 14 Jun 2023 22:47:09 GMT  
		Size: 262.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:3.11.0`

```console
$ docker pull arangodb@sha256:ee1b8182f168a8c2742dc122cd8a3af6cabaed425eb21c84a81f1b239208b02a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `arangodb:3.11.0` - linux; amd64

```console
$ docker pull arangodb@sha256:b6b9e69bc433655ec3a04f41b0dde212d4080babc0316b3029897dfbe1e54750
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.0 MB (243964371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90184ccfdeb2eabf0e0e6019b7745574b4ae36380a9f8e13e9bfeb5618fa426c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Wed, 29 Mar 2023 18:19:28 GMT
ADD file:970e6b2578ef73457ffed1189e8ba128b0211cabd3174b8c7d3afd8fb58ad614 in / 
# Wed, 29 Mar 2023 18:19:28 GMT
CMD ["/bin/sh"]
# Wed, 29 Mar 2023 19:35:19 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Fri, 26 May 2023 22:48:01 GMT
ENV ARANGO_VERSION=3.11.0
# Fri, 26 May 2023 22:48:30 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb311/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Fri, 26 May 2023 22:48:31 GMT
ENV GLIBCXX_FORCE_NEW=1
# Fri, 26 May 2023 22:48:32 GMT
RUN echo "UTC" > /etc/timezone
# Fri, 26 May 2023 22:48:32 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Fri, 26 May 2023 22:48:32 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Fri, 26 May 2023 22:48:32 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Fri, 26 May 2023 22:48:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 May 2023 22:48:32 GMT
EXPOSE 8529
# Fri, 26 May 2023 22:48:32 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:91d30c5bc19582de1415b18f1ec5bcbf52a558b62cf6cc201c9669df9f748c22`  
		Last Modified: Wed, 29 Mar 2023 18:20:09 GMT  
		Size: 2.8 MB (2807803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04b5248d92652fb9e51ec0e23dcb31a174ee1a3d8e55a093f43067aa799cf0f4`  
		Last Modified: Fri, 26 May 2023 22:49:07 GMT  
		Size: 241.2 MB (241154082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:337b4d1efaae1f2582f39582e14c09d379068f55ab1a9a112475b3dbffd08838`  
		Last Modified: Fri, 26 May 2023 22:48:44 GMT  
		Size: 137.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01a1ddc19c647fd79e5abf0a8ba11d17a29976cddeec8cff5a0a1906994d6aa5`  
		Last Modified: Fri, 26 May 2023 22:48:44 GMT  
		Size: 2.1 KB (2086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4508e0738e7d2dce04d6048661b811852ee754388c7f054024dcdb82ae4a908`  
		Last Modified: Fri, 26 May 2023 22:48:44 GMT  
		Size: 263.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `arangodb:3.11.0` - linux; arm64 variant v8

```console
$ docker pull arangodb@sha256:a91dada434e4be42b0a5345e822bd882fb8e4b2214a8e66c2183b84c1b801bd9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.3 MB (238338461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2264bd13f4357f422d5b166946b50c38cb495df6ea073f3cbd9e23d2b88a4072`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Wed, 14 Jun 2023 20:49:07 GMT
ADD file:e80eabe59d1f87ef41634428d9f8fdeb633c2128ac97564f96f5495ef6bf2c72 in / 
# Wed, 14 Jun 2023 20:49:07 GMT
CMD ["/bin/sh"]
# Wed, 14 Jun 2023 22:45:26 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Wed, 14 Jun 2023 22:46:00 GMT
ENV ARANGO_VERSION=3.11.0
# Wed, 14 Jun 2023 22:46:24 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb311/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Wed, 14 Jun 2023 22:46:27 GMT
ENV GLIBCXX_FORCE_NEW=1
# Wed, 14 Jun 2023 22:46:28 GMT
RUN echo "UTC" > /etc/timezone
# Wed, 14 Jun 2023 22:46:28 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Wed, 14 Jun 2023 22:46:28 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Wed, 14 Jun 2023 22:46:28 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Wed, 14 Jun 2023 22:46:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 14 Jun 2023 22:46:28 GMT
EXPOSE 8529
# Wed, 14 Jun 2023 22:46:28 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:a880266d3b77f75696023df2da1ef66c3c565e0f70596242395c9e68de955c7c`  
		Last Modified: Wed, 14 Jun 2023 20:49:43 GMT  
		Size: 2.7 MB (2707906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5da19c8f6a1edbfd55d983afeea9d58150da07a58824672f1a02e885267d0412`  
		Last Modified: Wed, 14 Jun 2023 22:47:25 GMT  
		Size: 235.6 MB (235628068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b39cc356770a9f35dfcf88166308eb81917cf0f9268aeb1a6615e18bd914f6`  
		Last Modified: Wed, 14 Jun 2023 22:47:08 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07ee3329ebc66f51f7e2757cd64d9ad46257008561ae95805b9cbb9f1e30622a`  
		Last Modified: Wed, 14 Jun 2023 22:47:08 GMT  
		Size: 2.1 KB (2086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:743957648b762a7dce68adabf44903ad76d669bddd9081ccf26887519a8ac0c3`  
		Last Modified: Wed, 14 Jun 2023 22:47:09 GMT  
		Size: 262.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:3.9`

```console
$ docker pull arangodb@sha256:b665a5dfe26c813382ddd5615710d801d6706bc43b61819a1a0c7fd26918dd2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `arangodb:3.9` - linux; amd64

```console
$ docker pull arangodb@sha256:a39d825d505802496779364f0ec9c9e84fb6034fdc6fa9a07d975e22b8d19871
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.9 MB (204913424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:881d2ee3e0aa30d22b1226fe7eee45923cf958cffe8b8690e13ec62de4ebb7e1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Wed, 29 Mar 2023 18:19:33 GMT
ADD file:08ad6c1c886a26e30ae4ab103ff377ee6cfbc1be2437fa227ec28a335c63d78a in / 
# Wed, 29 Mar 2023 18:19:33 GMT
CMD ["/bin/sh"]
# Wed, 10 May 2023 17:19:25 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Thu, 08 Jun 2023 21:42:22 GMT
ENV ARANGO_VERSION=3.9.11
# Thu, 08 Jun 2023 21:42:22 GMT
ENV ARANGO_URL=https://download.arangodb.com/arangodb39/DEBIAN/amd64
# Thu, 08 Jun 2023 21:42:22 GMT
ENV ARANGO_PACKAGE=arangodb3_3.9.11-1_amd64.deb
# Thu, 08 Jun 2023 21:42:22 GMT
ENV ARANGO_PACKAGE_URL=https://download.arangodb.com/arangodb39/DEBIAN/amd64/arangodb3_3.9.11-1_amd64.deb
# Thu, 08 Jun 2023 21:42:22 GMT
ENV ARANGO_SIGNATURE_URL=https://download.arangodb.com/arangodb39/DEBIAN/amd64/arangodb3_3.9.11-1_amd64.deb.asc
# Thu, 08 Jun 2023 21:42:51 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Thu, 08 Jun 2023 21:42:52 GMT
ENV GLIBCXX_FORCE_NEW=1
# Thu, 08 Jun 2023 21:42:53 GMT
RUN echo "UTC" > /etc/timezone
# Thu, 08 Jun 2023 21:42:53 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Thu, 08 Jun 2023 21:42:53 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Thu, 08 Jun 2023 21:42:53 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Thu, 08 Jun 2023 21:42:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 08 Jun 2023 21:42:53 GMT
EXPOSE 8529
# Thu, 08 Jun 2023 21:42:53 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:0ce1dd7918a48990ab749aab2e805c26f691a3a8103495530e7ea5a1d168af4a`  
		Last Modified: Wed, 29 Mar 2023 18:20:17 GMT  
		Size: 2.8 MB (2826596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28980ee9c20e0b8e8bec8cc358ab3d28401d751e437890e07a482335524ac633`  
		Last Modified: Thu, 08 Jun 2023 21:43:28 GMT  
		Size: 202.1 MB (202084342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:349a02bf5350f0d5814fbb55843fec40109498c0322944d19a47e0d33ad8241e`  
		Last Modified: Thu, 08 Jun 2023 21:43:07 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84a8c4e0b39b011ad5b408666a294e8247ea65a283a57015d72f7c9a6b4ef4e1`  
		Last Modified: Thu, 08 Jun 2023 21:43:07 GMT  
		Size: 2.1 KB (2086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bd355e5cab59d6d20a22fa1738dd3329fe7f01ff32d5c2aa39ba1e9b72e8bc3`  
		Last Modified: Thu, 08 Jun 2023 21:43:07 GMT  
		Size: 261.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:3.9.11`

```console
$ docker pull arangodb@sha256:b665a5dfe26c813382ddd5615710d801d6706bc43b61819a1a0c7fd26918dd2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `arangodb:3.9.11` - linux; amd64

```console
$ docker pull arangodb@sha256:a39d825d505802496779364f0ec9c9e84fb6034fdc6fa9a07d975e22b8d19871
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.9 MB (204913424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:881d2ee3e0aa30d22b1226fe7eee45923cf958cffe8b8690e13ec62de4ebb7e1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Wed, 29 Mar 2023 18:19:33 GMT
ADD file:08ad6c1c886a26e30ae4ab103ff377ee6cfbc1be2437fa227ec28a335c63d78a in / 
# Wed, 29 Mar 2023 18:19:33 GMT
CMD ["/bin/sh"]
# Wed, 10 May 2023 17:19:25 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Thu, 08 Jun 2023 21:42:22 GMT
ENV ARANGO_VERSION=3.9.11
# Thu, 08 Jun 2023 21:42:22 GMT
ENV ARANGO_URL=https://download.arangodb.com/arangodb39/DEBIAN/amd64
# Thu, 08 Jun 2023 21:42:22 GMT
ENV ARANGO_PACKAGE=arangodb3_3.9.11-1_amd64.deb
# Thu, 08 Jun 2023 21:42:22 GMT
ENV ARANGO_PACKAGE_URL=https://download.arangodb.com/arangodb39/DEBIAN/amd64/arangodb3_3.9.11-1_amd64.deb
# Thu, 08 Jun 2023 21:42:22 GMT
ENV ARANGO_SIGNATURE_URL=https://download.arangodb.com/arangodb39/DEBIAN/amd64/arangodb3_3.9.11-1_amd64.deb.asc
# Thu, 08 Jun 2023 21:42:51 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Thu, 08 Jun 2023 21:42:52 GMT
ENV GLIBCXX_FORCE_NEW=1
# Thu, 08 Jun 2023 21:42:53 GMT
RUN echo "UTC" > /etc/timezone
# Thu, 08 Jun 2023 21:42:53 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Thu, 08 Jun 2023 21:42:53 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Thu, 08 Jun 2023 21:42:53 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Thu, 08 Jun 2023 21:42:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 08 Jun 2023 21:42:53 GMT
EXPOSE 8529
# Thu, 08 Jun 2023 21:42:53 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:0ce1dd7918a48990ab749aab2e805c26f691a3a8103495530e7ea5a1d168af4a`  
		Last Modified: Wed, 29 Mar 2023 18:20:17 GMT  
		Size: 2.8 MB (2826596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28980ee9c20e0b8e8bec8cc358ab3d28401d751e437890e07a482335524ac633`  
		Last Modified: Thu, 08 Jun 2023 21:43:28 GMT  
		Size: 202.1 MB (202084342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:349a02bf5350f0d5814fbb55843fec40109498c0322944d19a47e0d33ad8241e`  
		Last Modified: Thu, 08 Jun 2023 21:43:07 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84a8c4e0b39b011ad5b408666a294e8247ea65a283a57015d72f7c9a6b4ef4e1`  
		Last Modified: Thu, 08 Jun 2023 21:43:07 GMT  
		Size: 2.1 KB (2086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bd355e5cab59d6d20a22fa1738dd3329fe7f01ff32d5c2aa39ba1e9b72e8bc3`  
		Last Modified: Thu, 08 Jun 2023 21:43:07 GMT  
		Size: 261.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:latest`

```console
$ docker pull arangodb@sha256:ee1b8182f168a8c2742dc122cd8a3af6cabaed425eb21c84a81f1b239208b02a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `arangodb:latest` - linux; amd64

```console
$ docker pull arangodb@sha256:b6b9e69bc433655ec3a04f41b0dde212d4080babc0316b3029897dfbe1e54750
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.0 MB (243964371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90184ccfdeb2eabf0e0e6019b7745574b4ae36380a9f8e13e9bfeb5618fa426c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Wed, 29 Mar 2023 18:19:28 GMT
ADD file:970e6b2578ef73457ffed1189e8ba128b0211cabd3174b8c7d3afd8fb58ad614 in / 
# Wed, 29 Mar 2023 18:19:28 GMT
CMD ["/bin/sh"]
# Wed, 29 Mar 2023 19:35:19 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Fri, 26 May 2023 22:48:01 GMT
ENV ARANGO_VERSION=3.11.0
# Fri, 26 May 2023 22:48:30 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb311/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Fri, 26 May 2023 22:48:31 GMT
ENV GLIBCXX_FORCE_NEW=1
# Fri, 26 May 2023 22:48:32 GMT
RUN echo "UTC" > /etc/timezone
# Fri, 26 May 2023 22:48:32 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Fri, 26 May 2023 22:48:32 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Fri, 26 May 2023 22:48:32 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Fri, 26 May 2023 22:48:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 May 2023 22:48:32 GMT
EXPOSE 8529
# Fri, 26 May 2023 22:48:32 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:91d30c5bc19582de1415b18f1ec5bcbf52a558b62cf6cc201c9669df9f748c22`  
		Last Modified: Wed, 29 Mar 2023 18:20:09 GMT  
		Size: 2.8 MB (2807803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04b5248d92652fb9e51ec0e23dcb31a174ee1a3d8e55a093f43067aa799cf0f4`  
		Last Modified: Fri, 26 May 2023 22:49:07 GMT  
		Size: 241.2 MB (241154082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:337b4d1efaae1f2582f39582e14c09d379068f55ab1a9a112475b3dbffd08838`  
		Last Modified: Fri, 26 May 2023 22:48:44 GMT  
		Size: 137.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01a1ddc19c647fd79e5abf0a8ba11d17a29976cddeec8cff5a0a1906994d6aa5`  
		Last Modified: Fri, 26 May 2023 22:48:44 GMT  
		Size: 2.1 KB (2086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4508e0738e7d2dce04d6048661b811852ee754388c7f054024dcdb82ae4a908`  
		Last Modified: Fri, 26 May 2023 22:48:44 GMT  
		Size: 263.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `arangodb:latest` - linux; arm64 variant v8

```console
$ docker pull arangodb@sha256:a91dada434e4be42b0a5345e822bd882fb8e4b2214a8e66c2183b84c1b801bd9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.3 MB (238338461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2264bd13f4357f422d5b166946b50c38cb495df6ea073f3cbd9e23d2b88a4072`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Wed, 14 Jun 2023 20:49:07 GMT
ADD file:e80eabe59d1f87ef41634428d9f8fdeb633c2128ac97564f96f5495ef6bf2c72 in / 
# Wed, 14 Jun 2023 20:49:07 GMT
CMD ["/bin/sh"]
# Wed, 14 Jun 2023 22:45:26 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Wed, 14 Jun 2023 22:46:00 GMT
ENV ARANGO_VERSION=3.11.0
# Wed, 14 Jun 2023 22:46:24 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb311/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Wed, 14 Jun 2023 22:46:27 GMT
ENV GLIBCXX_FORCE_NEW=1
# Wed, 14 Jun 2023 22:46:28 GMT
RUN echo "UTC" > /etc/timezone
# Wed, 14 Jun 2023 22:46:28 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Wed, 14 Jun 2023 22:46:28 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Wed, 14 Jun 2023 22:46:28 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Wed, 14 Jun 2023 22:46:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 14 Jun 2023 22:46:28 GMT
EXPOSE 8529
# Wed, 14 Jun 2023 22:46:28 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:a880266d3b77f75696023df2da1ef66c3c565e0f70596242395c9e68de955c7c`  
		Last Modified: Wed, 14 Jun 2023 20:49:43 GMT  
		Size: 2.7 MB (2707906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5da19c8f6a1edbfd55d983afeea9d58150da07a58824672f1a02e885267d0412`  
		Last Modified: Wed, 14 Jun 2023 22:47:25 GMT  
		Size: 235.6 MB (235628068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b39cc356770a9f35dfcf88166308eb81917cf0f9268aeb1a6615e18bd914f6`  
		Last Modified: Wed, 14 Jun 2023 22:47:08 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07ee3329ebc66f51f7e2757cd64d9ad46257008561ae95805b9cbb9f1e30622a`  
		Last Modified: Wed, 14 Jun 2023 22:47:08 GMT  
		Size: 2.1 KB (2086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:743957648b762a7dce68adabf44903ad76d669bddd9081ccf26887519a8ac0c3`  
		Last Modified: Wed, 14 Jun 2023 22:47:09 GMT  
		Size: 262.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
