<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `arangodb`

-	[`arangodb:3.10`](#arangodb310)
-	[`arangodb:3.10.7`](#arangodb3107)
-	[`arangodb:3.11`](#arangodb311)
-	[`arangodb:3.11.1`](#arangodb3111)
-	[`arangodb:3.9`](#arangodb39)
-	[`arangodb:3.9.11`](#arangodb3911)
-	[`arangodb:latest`](#arangodblatest)

## `arangodb:3.10`

```console
$ docker pull arangodb@sha256:1d3c0e315e232e69dc937646c6103d641bd8a1ca4536c76b516440699c5314f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `arangodb:3.10` - linux; amd64

```console
$ docker pull arangodb@sha256:10f15ac78b57e04e9c2656a49e237555d2be36a818ae80d5ce09e559fc61633b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.2 MB (220245693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0bd8a9514e260bc8574ce492c852254fdd5f88809dd3ebe9e46c9fe29006e59`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Wed, 14 Jun 2023 20:42:09 GMT
ADD file:4af69326e088b3c0f82320e9cd97b60c28bf019b984787c6f1c22489e6221f29 in / 
# Wed, 14 Jun 2023 20:42:09 GMT
CMD ["/bin/sh"]
# Thu, 15 Jun 2023 04:31:43 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Thu, 15 Jun 2023 04:31:43 GMT
ENV ARANGO_VERSION=3.10.6
# Thu, 15 Jun 2023 04:32:10 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb310/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Thu, 15 Jun 2023 04:32:11 GMT
ENV GLIBCXX_FORCE_NEW=1
# Thu, 15 Jun 2023 04:32:12 GMT
RUN echo "UTC" > /etc/timezone
# Thu, 15 Jun 2023 04:32:12 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Thu, 15 Jun 2023 04:32:12 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Thu, 15 Jun 2023 04:32:12 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Thu, 15 Jun 2023 04:32:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 15 Jun 2023 04:32:12 GMT
EXPOSE 8529
# Thu, 15 Jun 2023 04:32:13 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:c1d6d1b2d5a367259e6e51a7f4d1ccd66a28cc9940d6599d8a8ea9544dd4b4a8`  
		Last Modified: Wed, 14 Jun 2023 20:42:45 GMT  
		Size: 2.8 MB (2807669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1834269bfae091fda17fda3b54899f666d74cc0fc2185a205047f185386b66f7`  
		Last Modified: Thu, 15 Jun 2023 04:33:50 GMT  
		Size: 217.4 MB (217435537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74f130895aa65e54b24bb448efd517574689bcb9cc5674154cd59ac34ab70852`  
		Last Modified: Thu, 15 Jun 2023 04:33:28 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:577e2a912c41256da67dca7494d2a9fe7793170650abcbb4e8624e11352cfd1f`  
		Last Modified: Thu, 15 Jun 2023 04:33:29 GMT  
		Size: 2.1 KB (2087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5069711d5e8288bc984327d69b30ac4c9ed35fdac8ea6719e4a2f2b320e0c5e5`  
		Last Modified: Thu, 15 Jun 2023 04:33:28 GMT  
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

## `arangodb:3.10.7`

**does not exist** (yet?)

## `arangodb:3.11`

```console
$ docker pull arangodb@sha256:60efcef1ed89ae452176bfc46a959778a51aa9ce737884ddd83e3e0d0da93bcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `arangodb:3.11` - linux; amd64

```console
$ docker pull arangodb@sha256:a83da1ac7f63cffa81aa6529c36d2a4402e0f17f97983b63532ea33da989853d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.0 MB (243985856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1cac5e714df7b1923942a77c2834c5724bb7800ec267c4e16eff5b348cb05a2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Wed, 14 Jun 2023 20:42:09 GMT
ADD file:4af69326e088b3c0f82320e9cd97b60c28bf019b984787c6f1c22489e6221f29 in / 
# Wed, 14 Jun 2023 20:42:09 GMT
CMD ["/bin/sh"]
# Thu, 15 Jun 2023 04:31:43 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Thu, 15 Jun 2023 04:32:18 GMT
ENV ARANGO_VERSION=3.11.0
# Thu, 15 Jun 2023 04:32:45 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb311/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Thu, 15 Jun 2023 04:32:47 GMT
ENV GLIBCXX_FORCE_NEW=1
# Thu, 15 Jun 2023 04:32:47 GMT
RUN echo "UTC" > /etc/timezone
# Thu, 15 Jun 2023 04:32:47 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Thu, 15 Jun 2023 04:32:47 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Thu, 15 Jun 2023 04:32:47 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Thu, 15 Jun 2023 04:32:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 15 Jun 2023 04:32:48 GMT
EXPOSE 8529
# Thu, 15 Jun 2023 04:32:48 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:c1d6d1b2d5a367259e6e51a7f4d1ccd66a28cc9940d6599d8a8ea9544dd4b4a8`  
		Last Modified: Wed, 14 Jun 2023 20:42:45 GMT  
		Size: 2.8 MB (2807669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6431a4bf43d6122ad701a1f0504d9e8d44c5b1aa9ba16f864e171593cb601778`  
		Last Modified: Thu, 15 Jun 2023 04:34:22 GMT  
		Size: 241.2 MB (241175701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e309c7910e7b7cfab219d67ac05be6b0fcc7cb59f943a97e83354271b61b1cb`  
		Last Modified: Thu, 15 Jun 2023 04:33:59 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b42a4e0589400bc3ec60b097b11f3d6cff2c09502643111f20ad57d101f4bee5`  
		Last Modified: Thu, 15 Jun 2023 04:33:59 GMT  
		Size: 2.1 KB (2086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24c69c0b73703db4aae77cea275f919aae5cb654ad5cd2aaf43d627cb8e68057`  
		Last Modified: Thu, 15 Jun 2023 04:33:59 GMT  
		Size: 261.0 B  
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

## `arangodb:3.11.1`

**does not exist** (yet?)

## `arangodb:3.9`

```console
$ docker pull arangodb@sha256:ccf0b7efd9fdec9bee4d9be7146a5de6ac31f9f81fc6af3f117c69f3fae8a6fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `arangodb:3.9` - linux; amd64

```console
$ docker pull arangodb@sha256:ab0472c6a34396b6ee935ff2d20e728e7cee47c1185aa4c2e87ad5e5e5be7071
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.9 MB (204918983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b57af32609c3ba32aed5579df23b0bcdd83cc24cf847e6e8e9ce09087203469e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Wed, 14 Jun 2023 20:42:13 GMT
ADD file:4fa8e307f595ecff485113fb0ec6e2320979eaa6fb3eb467d2433771a6f016e6 in / 
# Wed, 14 Jun 2023 20:42:13 GMT
CMD ["/bin/sh"]
# Thu, 15 Jun 2023 04:31:09 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Thu, 15 Jun 2023 04:31:09 GMT
ENV ARANGO_VERSION=3.9.11
# Thu, 15 Jun 2023 04:31:09 GMT
ENV ARANGO_URL=https://download.arangodb.com/arangodb39/DEBIAN/amd64
# Thu, 15 Jun 2023 04:31:09 GMT
ENV ARANGO_PACKAGE=arangodb3_3.9.11-1_amd64.deb
# Thu, 15 Jun 2023 04:31:09 GMT
ENV ARANGO_PACKAGE_URL=https://download.arangodb.com/arangodb39/DEBIAN/amd64/arangodb3_3.9.11-1_amd64.deb
# Thu, 15 Jun 2023 04:31:09 GMT
ENV ARANGO_SIGNATURE_URL=https://download.arangodb.com/arangodb39/DEBIAN/amd64/arangodb3_3.9.11-1_amd64.deb.asc
# Thu, 15 Jun 2023 04:31:33 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Thu, 15 Jun 2023 04:31:35 GMT
ENV GLIBCXX_FORCE_NEW=1
# Thu, 15 Jun 2023 04:31:35 GMT
RUN echo "UTC" > /etc/timezone
# Thu, 15 Jun 2023 04:31:36 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Thu, 15 Jun 2023 04:31:36 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Thu, 15 Jun 2023 04:31:36 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Thu, 15 Jun 2023 04:31:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 15 Jun 2023 04:31:36 GMT
EXPOSE 8529
# Thu, 15 Jun 2023 04:31:36 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:0cdfa0c98ed79707cd91c5dd7ebd282aa2b976d86a9e699d7fc188cdb6be390e`  
		Last Modified: Wed, 14 Jun 2023 20:42:58 GMT  
		Size: 2.8 MB (2825916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7c16a1d2ea9ec99f711bc1f059e3453f6aef7ed8a715c89fc6641bbfeaae75a`  
		Last Modified: Thu, 15 Jun 2023 04:33:20 GMT  
		Size: 202.1 MB (202090582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d51cd75103f25338f7755dd747750cdfce1fc4ce93f6574938d8a09eb5038ace`  
		Last Modified: Thu, 15 Jun 2023 04:32:59 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d618805dae2b46f80669fc843875aee0478255cb03b54b1900549877120ea31e`  
		Last Modified: Thu, 15 Jun 2023 04:32:59 GMT  
		Size: 2.1 KB (2085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fabe4d9a822ca5fd9154a10fc60698da3125d474633150cd5010745963b7ce2`  
		Last Modified: Thu, 15 Jun 2023 04:33:00 GMT  
		Size: 261.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:3.9.11`

```console
$ docker pull arangodb@sha256:ccf0b7efd9fdec9bee4d9be7146a5de6ac31f9f81fc6af3f117c69f3fae8a6fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `arangodb:3.9.11` - linux; amd64

```console
$ docker pull arangodb@sha256:ab0472c6a34396b6ee935ff2d20e728e7cee47c1185aa4c2e87ad5e5e5be7071
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.9 MB (204918983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b57af32609c3ba32aed5579df23b0bcdd83cc24cf847e6e8e9ce09087203469e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Wed, 14 Jun 2023 20:42:13 GMT
ADD file:4fa8e307f595ecff485113fb0ec6e2320979eaa6fb3eb467d2433771a6f016e6 in / 
# Wed, 14 Jun 2023 20:42:13 GMT
CMD ["/bin/sh"]
# Thu, 15 Jun 2023 04:31:09 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Thu, 15 Jun 2023 04:31:09 GMT
ENV ARANGO_VERSION=3.9.11
# Thu, 15 Jun 2023 04:31:09 GMT
ENV ARANGO_URL=https://download.arangodb.com/arangodb39/DEBIAN/amd64
# Thu, 15 Jun 2023 04:31:09 GMT
ENV ARANGO_PACKAGE=arangodb3_3.9.11-1_amd64.deb
# Thu, 15 Jun 2023 04:31:09 GMT
ENV ARANGO_PACKAGE_URL=https://download.arangodb.com/arangodb39/DEBIAN/amd64/arangodb3_3.9.11-1_amd64.deb
# Thu, 15 Jun 2023 04:31:09 GMT
ENV ARANGO_SIGNATURE_URL=https://download.arangodb.com/arangodb39/DEBIAN/amd64/arangodb3_3.9.11-1_amd64.deb.asc
# Thu, 15 Jun 2023 04:31:33 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Thu, 15 Jun 2023 04:31:35 GMT
ENV GLIBCXX_FORCE_NEW=1
# Thu, 15 Jun 2023 04:31:35 GMT
RUN echo "UTC" > /etc/timezone
# Thu, 15 Jun 2023 04:31:36 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Thu, 15 Jun 2023 04:31:36 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Thu, 15 Jun 2023 04:31:36 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Thu, 15 Jun 2023 04:31:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 15 Jun 2023 04:31:36 GMT
EXPOSE 8529
# Thu, 15 Jun 2023 04:31:36 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:0cdfa0c98ed79707cd91c5dd7ebd282aa2b976d86a9e699d7fc188cdb6be390e`  
		Last Modified: Wed, 14 Jun 2023 20:42:58 GMT  
		Size: 2.8 MB (2825916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7c16a1d2ea9ec99f711bc1f059e3453f6aef7ed8a715c89fc6641bbfeaae75a`  
		Last Modified: Thu, 15 Jun 2023 04:33:20 GMT  
		Size: 202.1 MB (202090582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d51cd75103f25338f7755dd747750cdfce1fc4ce93f6574938d8a09eb5038ace`  
		Last Modified: Thu, 15 Jun 2023 04:32:59 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d618805dae2b46f80669fc843875aee0478255cb03b54b1900549877120ea31e`  
		Last Modified: Thu, 15 Jun 2023 04:32:59 GMT  
		Size: 2.1 KB (2085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fabe4d9a822ca5fd9154a10fc60698da3125d474633150cd5010745963b7ce2`  
		Last Modified: Thu, 15 Jun 2023 04:33:00 GMT  
		Size: 261.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:latest`

```console
$ docker pull arangodb@sha256:60efcef1ed89ae452176bfc46a959778a51aa9ce737884ddd83e3e0d0da93bcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `arangodb:latest` - linux; amd64

```console
$ docker pull arangodb@sha256:a83da1ac7f63cffa81aa6529c36d2a4402e0f17f97983b63532ea33da989853d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.0 MB (243985856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1cac5e714df7b1923942a77c2834c5724bb7800ec267c4e16eff5b348cb05a2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Wed, 14 Jun 2023 20:42:09 GMT
ADD file:4af69326e088b3c0f82320e9cd97b60c28bf019b984787c6f1c22489e6221f29 in / 
# Wed, 14 Jun 2023 20:42:09 GMT
CMD ["/bin/sh"]
# Thu, 15 Jun 2023 04:31:43 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Thu, 15 Jun 2023 04:32:18 GMT
ENV ARANGO_VERSION=3.11.0
# Thu, 15 Jun 2023 04:32:45 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb311/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Thu, 15 Jun 2023 04:32:47 GMT
ENV GLIBCXX_FORCE_NEW=1
# Thu, 15 Jun 2023 04:32:47 GMT
RUN echo "UTC" > /etc/timezone
# Thu, 15 Jun 2023 04:32:47 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Thu, 15 Jun 2023 04:32:47 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Thu, 15 Jun 2023 04:32:47 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Thu, 15 Jun 2023 04:32:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 15 Jun 2023 04:32:48 GMT
EXPOSE 8529
# Thu, 15 Jun 2023 04:32:48 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:c1d6d1b2d5a367259e6e51a7f4d1ccd66a28cc9940d6599d8a8ea9544dd4b4a8`  
		Last Modified: Wed, 14 Jun 2023 20:42:45 GMT  
		Size: 2.8 MB (2807669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6431a4bf43d6122ad701a1f0504d9e8d44c5b1aa9ba16f864e171593cb601778`  
		Last Modified: Thu, 15 Jun 2023 04:34:22 GMT  
		Size: 241.2 MB (241175701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e309c7910e7b7cfab219d67ac05be6b0fcc7cb59f943a97e83354271b61b1cb`  
		Last Modified: Thu, 15 Jun 2023 04:33:59 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b42a4e0589400bc3ec60b097b11f3d6cff2c09502643111f20ad57d101f4bee5`  
		Last Modified: Thu, 15 Jun 2023 04:33:59 GMT  
		Size: 2.1 KB (2086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24c69c0b73703db4aae77cea275f919aae5cb654ad5cd2aaf43d627cb8e68057`  
		Last Modified: Thu, 15 Jun 2023 04:33:59 GMT  
		Size: 261.0 B  
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
