<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `arangodb`

-	[`arangodb:3.10`](#arangodb310)
-	[`arangodb:3.10.1`](#arangodb3101)
-	[`arangodb:3.8`](#arangodb38)
-	[`arangodb:3.8.8`](#arangodb388)
-	[`arangodb:3.9`](#arangodb39)
-	[`arangodb:3.9.4`](#arangodb394)
-	[`arangodb:latest`](#arangodblatest)

## `arangodb:3.10`

```console
$ docker pull arangodb@sha256:8fd9123f7ce6f75efc62b8e94edb06f7a8b738c94996d94b8fd27de0fa965150
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `arangodb:3.10` - linux; amd64

```console
$ docker pull arangodb@sha256:999b44ca9d70b7beae9b51aec9da16c4c9daf77283d8c3f291fc6c850321a741
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.9 MB (218887650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b7c720d994f4adf1a4287db33da9e9a83918c86dc41154af3f4fedc7edd83a6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Wed, 12 Oct 2022 19:19:28 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Thu, 10 Nov 2022 20:20:48 GMT
ENV ARANGO_VERSION=3.10.1
# Thu, 10 Nov 2022 20:21:14 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.0 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb310/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Thu, 10 Nov 2022 20:21:15 GMT
ENV GLIBCXX_FORCE_NEW=1
# Thu, 10 Nov 2022 20:21:16 GMT
RUN echo "UTC" > /etc/timezone
# Thu, 10 Nov 2022 20:21:16 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Thu, 10 Nov 2022 20:21:16 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Thu, 10 Nov 2022 20:21:16 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Thu, 10 Nov 2022 20:21:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 10 Nov 2022 20:21:17 GMT
EXPOSE 8529
# Thu, 10 Nov 2022 20:21:17 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23f8096fce9f3584b0e9fcea1c87d294760695ae7b52926a81b2723656a1c0ca`  
		Last Modified: Thu, 10 Nov 2022 20:21:58 GMT  
		Size: 216.1 MB (216079109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5044b000c08463ffd9330c0fa80421c6b48588fc95496a2213db4043af2037e`  
		Last Modified: Thu, 10 Nov 2022 20:21:34 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb722b98beeec30fbdcd94f32cbfecb53bb1c73ded621fee2bd0d67980a2af8f`  
		Last Modified: Thu, 10 Nov 2022 20:21:34 GMT  
		Size: 2.1 KB (2087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cd387c6e50f5af0ee466e0219ab7db7e2989e271c3a6b509574bb7550535dbf`  
		Last Modified: Thu, 10 Nov 2022 20:21:34 GMT  
		Size: 261.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `arangodb:3.10` - linux; arm64 variant v8

```console
$ docker pull arangodb@sha256:bfe2bad277d6194cd6582fd161566ba6a98f7803b15a9001cdd1fc2839c5d46e
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.6 MB (213568318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4884ff439d28dc68edec3a8163ca6041b10ff8423ba67f3a3483a42d16947696`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Thu, 10 Nov 2022 20:39:41 GMT
ADD file:960fd469d48cf79ba14bbda71f3192074ed860c112e30e0bc92bff3440cb45ab in / 
# Thu, 10 Nov 2022 20:39:41 GMT
CMD ["/bin/sh"]
# Thu, 10 Nov 2022 20:40:58 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Thu, 10 Nov 2022 20:40:58 GMT
ENV ARANGO_VERSION=3.10.1
# Thu, 10 Nov 2022 20:41:20 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.0 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb310/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Thu, 10 Nov 2022 20:41:24 GMT
ENV GLIBCXX_FORCE_NEW=1
# Thu, 10 Nov 2022 20:41:24 GMT
RUN echo "UTC" > /etc/timezone
# Thu, 10 Nov 2022 20:41:24 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Thu, 10 Nov 2022 20:41:24 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Thu, 10 Nov 2022 20:41:24 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Thu, 10 Nov 2022 20:41:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 10 Nov 2022 20:41:24 GMT
EXPOSE 8529
# Thu, 10 Nov 2022 20:41:25 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:9b18e9b68314027565b90ff6189d65942c0f7986da80df008b8431276885218e`  
		Last Modified: Tue, 09 Aug 2022 17:40:38 GMT  
		Size: 2.7 MB (2707663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abfb7eac48ceea29733e97df0512693e4c05262fc011d9b6b3211af125aa80ea`  
		Last Modified: Thu, 10 Nov 2022 20:41:55 GMT  
		Size: 210.9 MB (210858170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:851154154cfb3d094e323035795d15f09ff139c8ee998bfaba4549bcaf180ea4`  
		Last Modified: Thu, 10 Nov 2022 20:41:38 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96cbab6db577b2b8a94027d1286ffb2858c8df3114226aec44b0a4ae1d2aa50f`  
		Last Modified: Thu, 10 Nov 2022 20:41:38 GMT  
		Size: 2.1 KB (2086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38b46638b706329a23745fbdfb4d4330bc911a0dfb8143467a9be9f56cffaa76`  
		Last Modified: Thu, 10 Nov 2022 20:41:37 GMT  
		Size: 260.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:3.10.1`

```console
$ docker pull arangodb@sha256:8fd9123f7ce6f75efc62b8e94edb06f7a8b738c94996d94b8fd27de0fa965150
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `arangodb:3.10.1` - linux; amd64

```console
$ docker pull arangodb@sha256:999b44ca9d70b7beae9b51aec9da16c4c9daf77283d8c3f291fc6c850321a741
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.9 MB (218887650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b7c720d994f4adf1a4287db33da9e9a83918c86dc41154af3f4fedc7edd83a6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Wed, 12 Oct 2022 19:19:28 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Thu, 10 Nov 2022 20:20:48 GMT
ENV ARANGO_VERSION=3.10.1
# Thu, 10 Nov 2022 20:21:14 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.0 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb310/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Thu, 10 Nov 2022 20:21:15 GMT
ENV GLIBCXX_FORCE_NEW=1
# Thu, 10 Nov 2022 20:21:16 GMT
RUN echo "UTC" > /etc/timezone
# Thu, 10 Nov 2022 20:21:16 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Thu, 10 Nov 2022 20:21:16 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Thu, 10 Nov 2022 20:21:16 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Thu, 10 Nov 2022 20:21:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 10 Nov 2022 20:21:17 GMT
EXPOSE 8529
# Thu, 10 Nov 2022 20:21:17 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23f8096fce9f3584b0e9fcea1c87d294760695ae7b52926a81b2723656a1c0ca`  
		Last Modified: Thu, 10 Nov 2022 20:21:58 GMT  
		Size: 216.1 MB (216079109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5044b000c08463ffd9330c0fa80421c6b48588fc95496a2213db4043af2037e`  
		Last Modified: Thu, 10 Nov 2022 20:21:34 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb722b98beeec30fbdcd94f32cbfecb53bb1c73ded621fee2bd0d67980a2af8f`  
		Last Modified: Thu, 10 Nov 2022 20:21:34 GMT  
		Size: 2.1 KB (2087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cd387c6e50f5af0ee466e0219ab7db7e2989e271c3a6b509574bb7550535dbf`  
		Last Modified: Thu, 10 Nov 2022 20:21:34 GMT  
		Size: 261.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `arangodb:3.10.1` - linux; arm64 variant v8

```console
$ docker pull arangodb@sha256:bfe2bad277d6194cd6582fd161566ba6a98f7803b15a9001cdd1fc2839c5d46e
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.6 MB (213568318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4884ff439d28dc68edec3a8163ca6041b10ff8423ba67f3a3483a42d16947696`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Thu, 10 Nov 2022 20:39:41 GMT
ADD file:960fd469d48cf79ba14bbda71f3192074ed860c112e30e0bc92bff3440cb45ab in / 
# Thu, 10 Nov 2022 20:39:41 GMT
CMD ["/bin/sh"]
# Thu, 10 Nov 2022 20:40:58 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Thu, 10 Nov 2022 20:40:58 GMT
ENV ARANGO_VERSION=3.10.1
# Thu, 10 Nov 2022 20:41:20 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.0 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb310/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Thu, 10 Nov 2022 20:41:24 GMT
ENV GLIBCXX_FORCE_NEW=1
# Thu, 10 Nov 2022 20:41:24 GMT
RUN echo "UTC" > /etc/timezone
# Thu, 10 Nov 2022 20:41:24 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Thu, 10 Nov 2022 20:41:24 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Thu, 10 Nov 2022 20:41:24 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Thu, 10 Nov 2022 20:41:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 10 Nov 2022 20:41:24 GMT
EXPOSE 8529
# Thu, 10 Nov 2022 20:41:25 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:9b18e9b68314027565b90ff6189d65942c0f7986da80df008b8431276885218e`  
		Last Modified: Tue, 09 Aug 2022 17:40:38 GMT  
		Size: 2.7 MB (2707663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abfb7eac48ceea29733e97df0512693e4c05262fc011d9b6b3211af125aa80ea`  
		Last Modified: Thu, 10 Nov 2022 20:41:55 GMT  
		Size: 210.9 MB (210858170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:851154154cfb3d094e323035795d15f09ff139c8ee998bfaba4549bcaf180ea4`  
		Last Modified: Thu, 10 Nov 2022 20:41:38 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96cbab6db577b2b8a94027d1286ffb2858c8df3114226aec44b0a4ae1d2aa50f`  
		Last Modified: Thu, 10 Nov 2022 20:41:38 GMT  
		Size: 2.1 KB (2086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38b46638b706329a23745fbdfb4d4330bc911a0dfb8143467a9be9f56cffaa76`  
		Last Modified: Thu, 10 Nov 2022 20:41:37 GMT  
		Size: 260.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:3.8`

```console
$ docker pull arangodb@sha256:2a87ce7fd3bfb80fb57d802d533b960ed91c69df92ede6f3834550c9311a93d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `arangodb:3.8` - linux; amd64

```console
$ docker pull arangodb@sha256:82ccaafd5b9c219349bdafd666ee800bc00908d700af2962cc08d163e11de7fe
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.3 MB (195268712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e80ef161d591ff18c52eca3538ec44e42819183e354f709278962b14025a118`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:07 GMT
ADD file:b9bd10cf83356cb7281baa0fbaca5186cf27491f59eda87abe57f83a5aaf5ec1 in / 
# Tue, 09 Aug 2022 17:20:08 GMT
CMD ["/bin/sh"]
# Thu, 06 Oct 2022 19:51:41 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Thu, 27 Oct 2022 00:44:25 GMT
ENV ARANGO_VERSION=3.8.8
# Thu, 27 Oct 2022 00:44:25 GMT
ENV ARANGO_URL=https://download.arangodb.com/arangodb38/DEBIAN/amd64
# Thu, 27 Oct 2022 00:44:25 GMT
ENV ARANGO_PACKAGE=arangodb3_3.8.8-1_amd64.deb
# Thu, 27 Oct 2022 00:44:25 GMT
ENV ARANGO_PACKAGE_URL=https://download.arangodb.com/arangodb38/DEBIAN/amd64/arangodb3_3.8.8-1_amd64.deb
# Thu, 27 Oct 2022 00:44:25 GMT
ENV ARANGO_SIGNATURE_URL=https://download.arangodb.com/arangodb38/DEBIAN/amd64/arangodb3_3.8.8-1_amd64.deb.asc
# Thu, 27 Oct 2022 00:44:51 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.0.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Thu, 27 Oct 2022 00:44:53 GMT
ENV GLIBCXX_FORCE_NEW=1
# Thu, 27 Oct 2022 00:44:54 GMT
RUN echo "UTC" > /etc/timezone
# Thu, 27 Oct 2022 00:44:54 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Thu, 27 Oct 2022 00:44:54 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Thu, 27 Oct 2022 00:44:54 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Thu, 27 Oct 2022 00:44:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 27 Oct 2022 00:44:54 GMT
EXPOSE 8529
# Thu, 27 Oct 2022 00:44:54 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:c7ed990a2339ee598662849de4f56e2241399f5a32340c8c4a7bbd5378a12b5f`  
		Last Modified: Tue, 09 Aug 2022 17:21:06 GMT  
		Size: 2.8 MB (2827489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:487a9ea0d1ee31646f1db6eed2b72422eec6050cabde55ea9242e08219565270`  
		Last Modified: Thu, 27 Oct 2022 00:46:08 GMT  
		Size: 192.4 MB (192438735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7f0c4d39107a370e74ba90537142345ca825ce6adeb7b6b8cbf0935cbad919`  
		Last Modified: Thu, 27 Oct 2022 00:45:45 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3f2bc8d483668b3099208c86d5ebab704d1a990a2d6f9a657f5e9b520c20d92`  
		Last Modified: Thu, 27 Oct 2022 00:45:45 GMT  
		Size: 2.1 KB (2087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b1975f6734b8a781ef62fe7666ce113b642303738fc119f1c99887943511c03`  
		Last Modified: Thu, 27 Oct 2022 00:45:45 GMT  
		Size: 262.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:3.8.8`

```console
$ docker pull arangodb@sha256:2a87ce7fd3bfb80fb57d802d533b960ed91c69df92ede6f3834550c9311a93d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `arangodb:3.8.8` - linux; amd64

```console
$ docker pull arangodb@sha256:82ccaafd5b9c219349bdafd666ee800bc00908d700af2962cc08d163e11de7fe
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.3 MB (195268712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e80ef161d591ff18c52eca3538ec44e42819183e354f709278962b14025a118`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:07 GMT
ADD file:b9bd10cf83356cb7281baa0fbaca5186cf27491f59eda87abe57f83a5aaf5ec1 in / 
# Tue, 09 Aug 2022 17:20:08 GMT
CMD ["/bin/sh"]
# Thu, 06 Oct 2022 19:51:41 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Thu, 27 Oct 2022 00:44:25 GMT
ENV ARANGO_VERSION=3.8.8
# Thu, 27 Oct 2022 00:44:25 GMT
ENV ARANGO_URL=https://download.arangodb.com/arangodb38/DEBIAN/amd64
# Thu, 27 Oct 2022 00:44:25 GMT
ENV ARANGO_PACKAGE=arangodb3_3.8.8-1_amd64.deb
# Thu, 27 Oct 2022 00:44:25 GMT
ENV ARANGO_PACKAGE_URL=https://download.arangodb.com/arangodb38/DEBIAN/amd64/arangodb3_3.8.8-1_amd64.deb
# Thu, 27 Oct 2022 00:44:25 GMT
ENV ARANGO_SIGNATURE_URL=https://download.arangodb.com/arangodb38/DEBIAN/amd64/arangodb3_3.8.8-1_amd64.deb.asc
# Thu, 27 Oct 2022 00:44:51 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.0.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Thu, 27 Oct 2022 00:44:53 GMT
ENV GLIBCXX_FORCE_NEW=1
# Thu, 27 Oct 2022 00:44:54 GMT
RUN echo "UTC" > /etc/timezone
# Thu, 27 Oct 2022 00:44:54 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Thu, 27 Oct 2022 00:44:54 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Thu, 27 Oct 2022 00:44:54 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Thu, 27 Oct 2022 00:44:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 27 Oct 2022 00:44:54 GMT
EXPOSE 8529
# Thu, 27 Oct 2022 00:44:54 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:c7ed990a2339ee598662849de4f56e2241399f5a32340c8c4a7bbd5378a12b5f`  
		Last Modified: Tue, 09 Aug 2022 17:21:06 GMT  
		Size: 2.8 MB (2827489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:487a9ea0d1ee31646f1db6eed2b72422eec6050cabde55ea9242e08219565270`  
		Last Modified: Thu, 27 Oct 2022 00:46:08 GMT  
		Size: 192.4 MB (192438735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7f0c4d39107a370e74ba90537142345ca825ce6adeb7b6b8cbf0935cbad919`  
		Last Modified: Thu, 27 Oct 2022 00:45:45 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3f2bc8d483668b3099208c86d5ebab704d1a990a2d6f9a657f5e9b520c20d92`  
		Last Modified: Thu, 27 Oct 2022 00:45:45 GMT  
		Size: 2.1 KB (2087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b1975f6734b8a781ef62fe7666ce113b642303738fc119f1c99887943511c03`  
		Last Modified: Thu, 27 Oct 2022 00:45:45 GMT  
		Size: 262.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:3.9`

```console
$ docker pull arangodb@sha256:bb3b3d377c2cb653e46dafa8a3742d9a8697d2b2ce664c15278aee5753288216
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `arangodb:3.9` - linux; amd64

```console
$ docker pull arangodb@sha256:612a3084d7fadeb1a22639918846d9f498ea44dec3601ea910dfb86dffbc84cd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.0 MB (201030479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfbf93d1fc2f432469d2aee1cc7560a6ab6d434a5a9c95b5fd1f0e3d643367c1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:07 GMT
ADD file:b9bd10cf83356cb7281baa0fbaca5186cf27491f59eda87abe57f83a5aaf5ec1 in / 
# Tue, 09 Aug 2022 17:20:08 GMT
CMD ["/bin/sh"]
# Thu, 06 Oct 2022 19:51:41 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Thu, 27 Oct 2022 00:44:59 GMT
ENV ARANGO_VERSION=3.9.4
# Thu, 27 Oct 2022 00:44:59 GMT
ENV ARANGO_URL=https://download.arangodb.com/arangodb39/DEBIAN/amd64
# Thu, 27 Oct 2022 00:44:59 GMT
ENV ARANGO_PACKAGE=arangodb3_3.9.4-1_amd64.deb
# Thu, 27 Oct 2022 00:44:59 GMT
ENV ARANGO_PACKAGE_URL=https://download.arangodb.com/arangodb39/DEBIAN/amd64/arangodb3_3.9.4-1_amd64.deb
# Thu, 27 Oct 2022 00:44:59 GMT
ENV ARANGO_SIGNATURE_URL=https://download.arangodb.com/arangodb39/DEBIAN/amd64/arangodb3_3.9.4-1_amd64.deb.asc
# Thu, 27 Oct 2022 00:45:26 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.0.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Thu, 27 Oct 2022 00:45:27 GMT
ENV GLIBCXX_FORCE_NEW=1
# Thu, 27 Oct 2022 00:45:28 GMT
RUN echo "UTC" > /etc/timezone
# Thu, 27 Oct 2022 00:45:28 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Thu, 27 Oct 2022 00:45:28 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Thu, 27 Oct 2022 00:45:28 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Thu, 27 Oct 2022 00:45:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 27 Oct 2022 00:45:29 GMT
EXPOSE 8529
# Thu, 27 Oct 2022 00:45:29 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:c7ed990a2339ee598662849de4f56e2241399f5a32340c8c4a7bbd5378a12b5f`  
		Last Modified: Tue, 09 Aug 2022 17:21:06 GMT  
		Size: 2.8 MB (2827489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:263b804ffb991879c0dc084587bc70a4be6fc5fe77e9f74ab504dde6d0139576`  
		Last Modified: Thu, 27 Oct 2022 00:46:41 GMT  
		Size: 198.2 MB (198200504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1910669dedc5e424d53e636b85757c76b5a61a39d728b5d028c9446fc4495e81`  
		Last Modified: Thu, 27 Oct 2022 00:46:18 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8192ad34b83c45e67fcbb5ac8329e9e7f4375c88162aa53d4e09d2ef447adf11`  
		Last Modified: Thu, 27 Oct 2022 00:46:18 GMT  
		Size: 2.1 KB (2085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6f89c44c76352cbdfc9df6382bcd4f1b8a5f8e1f4c4d2069e32840a2b186554`  
		Last Modified: Thu, 27 Oct 2022 00:46:18 GMT  
		Size: 262.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:3.9.4`

```console
$ docker pull arangodb@sha256:bb3b3d377c2cb653e46dafa8a3742d9a8697d2b2ce664c15278aee5753288216
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `arangodb:3.9.4` - linux; amd64

```console
$ docker pull arangodb@sha256:612a3084d7fadeb1a22639918846d9f498ea44dec3601ea910dfb86dffbc84cd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.0 MB (201030479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfbf93d1fc2f432469d2aee1cc7560a6ab6d434a5a9c95b5fd1f0e3d643367c1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:07 GMT
ADD file:b9bd10cf83356cb7281baa0fbaca5186cf27491f59eda87abe57f83a5aaf5ec1 in / 
# Tue, 09 Aug 2022 17:20:08 GMT
CMD ["/bin/sh"]
# Thu, 06 Oct 2022 19:51:41 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Thu, 27 Oct 2022 00:44:59 GMT
ENV ARANGO_VERSION=3.9.4
# Thu, 27 Oct 2022 00:44:59 GMT
ENV ARANGO_URL=https://download.arangodb.com/arangodb39/DEBIAN/amd64
# Thu, 27 Oct 2022 00:44:59 GMT
ENV ARANGO_PACKAGE=arangodb3_3.9.4-1_amd64.deb
# Thu, 27 Oct 2022 00:44:59 GMT
ENV ARANGO_PACKAGE_URL=https://download.arangodb.com/arangodb39/DEBIAN/amd64/arangodb3_3.9.4-1_amd64.deb
# Thu, 27 Oct 2022 00:44:59 GMT
ENV ARANGO_SIGNATURE_URL=https://download.arangodb.com/arangodb39/DEBIAN/amd64/arangodb3_3.9.4-1_amd64.deb.asc
# Thu, 27 Oct 2022 00:45:26 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.0.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Thu, 27 Oct 2022 00:45:27 GMT
ENV GLIBCXX_FORCE_NEW=1
# Thu, 27 Oct 2022 00:45:28 GMT
RUN echo "UTC" > /etc/timezone
# Thu, 27 Oct 2022 00:45:28 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Thu, 27 Oct 2022 00:45:28 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Thu, 27 Oct 2022 00:45:28 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Thu, 27 Oct 2022 00:45:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 27 Oct 2022 00:45:29 GMT
EXPOSE 8529
# Thu, 27 Oct 2022 00:45:29 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:c7ed990a2339ee598662849de4f56e2241399f5a32340c8c4a7bbd5378a12b5f`  
		Last Modified: Tue, 09 Aug 2022 17:21:06 GMT  
		Size: 2.8 MB (2827489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:263b804ffb991879c0dc084587bc70a4be6fc5fe77e9f74ab504dde6d0139576`  
		Last Modified: Thu, 27 Oct 2022 00:46:41 GMT  
		Size: 198.2 MB (198200504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1910669dedc5e424d53e636b85757c76b5a61a39d728b5d028c9446fc4495e81`  
		Last Modified: Thu, 27 Oct 2022 00:46:18 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8192ad34b83c45e67fcbb5ac8329e9e7f4375c88162aa53d4e09d2ef447adf11`  
		Last Modified: Thu, 27 Oct 2022 00:46:18 GMT  
		Size: 2.1 KB (2085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6f89c44c76352cbdfc9df6382bcd4f1b8a5f8e1f4c4d2069e32840a2b186554`  
		Last Modified: Thu, 27 Oct 2022 00:46:18 GMT  
		Size: 262.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:latest`

```console
$ docker pull arangodb@sha256:8fd9123f7ce6f75efc62b8e94edb06f7a8b738c94996d94b8fd27de0fa965150
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `arangodb:latest` - linux; amd64

```console
$ docker pull arangodb@sha256:999b44ca9d70b7beae9b51aec9da16c4c9daf77283d8c3f291fc6c850321a741
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.9 MB (218887650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b7c720d994f4adf1a4287db33da9e9a83918c86dc41154af3f4fedc7edd83a6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Wed, 12 Oct 2022 19:19:28 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Thu, 10 Nov 2022 20:20:48 GMT
ENV ARANGO_VERSION=3.10.1
# Thu, 10 Nov 2022 20:21:14 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.0 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb310/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Thu, 10 Nov 2022 20:21:15 GMT
ENV GLIBCXX_FORCE_NEW=1
# Thu, 10 Nov 2022 20:21:16 GMT
RUN echo "UTC" > /etc/timezone
# Thu, 10 Nov 2022 20:21:16 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Thu, 10 Nov 2022 20:21:16 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Thu, 10 Nov 2022 20:21:16 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Thu, 10 Nov 2022 20:21:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 10 Nov 2022 20:21:17 GMT
EXPOSE 8529
# Thu, 10 Nov 2022 20:21:17 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23f8096fce9f3584b0e9fcea1c87d294760695ae7b52926a81b2723656a1c0ca`  
		Last Modified: Thu, 10 Nov 2022 20:21:58 GMT  
		Size: 216.1 MB (216079109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5044b000c08463ffd9330c0fa80421c6b48588fc95496a2213db4043af2037e`  
		Last Modified: Thu, 10 Nov 2022 20:21:34 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb722b98beeec30fbdcd94f32cbfecb53bb1c73ded621fee2bd0d67980a2af8f`  
		Last Modified: Thu, 10 Nov 2022 20:21:34 GMT  
		Size: 2.1 KB (2087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cd387c6e50f5af0ee466e0219ab7db7e2989e271c3a6b509574bb7550535dbf`  
		Last Modified: Thu, 10 Nov 2022 20:21:34 GMT  
		Size: 261.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `arangodb:latest` - linux; arm64 variant v8

```console
$ docker pull arangodb@sha256:bfe2bad277d6194cd6582fd161566ba6a98f7803b15a9001cdd1fc2839c5d46e
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.6 MB (213568318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4884ff439d28dc68edec3a8163ca6041b10ff8423ba67f3a3483a42d16947696`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Thu, 10 Nov 2022 20:39:41 GMT
ADD file:960fd469d48cf79ba14bbda71f3192074ed860c112e30e0bc92bff3440cb45ab in / 
# Thu, 10 Nov 2022 20:39:41 GMT
CMD ["/bin/sh"]
# Thu, 10 Nov 2022 20:40:58 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Thu, 10 Nov 2022 20:40:58 GMT
ENV ARANGO_VERSION=3.10.1
# Thu, 10 Nov 2022 20:41:20 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.0 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb310/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Thu, 10 Nov 2022 20:41:24 GMT
ENV GLIBCXX_FORCE_NEW=1
# Thu, 10 Nov 2022 20:41:24 GMT
RUN echo "UTC" > /etc/timezone
# Thu, 10 Nov 2022 20:41:24 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Thu, 10 Nov 2022 20:41:24 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Thu, 10 Nov 2022 20:41:24 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Thu, 10 Nov 2022 20:41:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 10 Nov 2022 20:41:24 GMT
EXPOSE 8529
# Thu, 10 Nov 2022 20:41:25 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:9b18e9b68314027565b90ff6189d65942c0f7986da80df008b8431276885218e`  
		Last Modified: Tue, 09 Aug 2022 17:40:38 GMT  
		Size: 2.7 MB (2707663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abfb7eac48ceea29733e97df0512693e4c05262fc011d9b6b3211af125aa80ea`  
		Last Modified: Thu, 10 Nov 2022 20:41:55 GMT  
		Size: 210.9 MB (210858170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:851154154cfb3d094e323035795d15f09ff139c8ee998bfaba4549bcaf180ea4`  
		Last Modified: Thu, 10 Nov 2022 20:41:38 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96cbab6db577b2b8a94027d1286ffb2858c8df3114226aec44b0a4ae1d2aa50f`  
		Last Modified: Thu, 10 Nov 2022 20:41:38 GMT  
		Size: 2.1 KB (2086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38b46638b706329a23745fbdfb4d4330bc911a0dfb8143467a9be9f56cffaa76`  
		Last Modified: Thu, 10 Nov 2022 20:41:37 GMT  
		Size: 260.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
