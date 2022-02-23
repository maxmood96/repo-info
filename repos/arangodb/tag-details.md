<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `arangodb`

-	[`arangodb:3.7`](#arangodb37)
-	[`arangodb:3.7.17`](#arangodb3717)
-	[`arangodb:3.8`](#arangodb38)
-	[`arangodb:3.8.6`](#arangodb386)
-	[`arangodb:3.9`](#arangodb39)
-	[`arangodb:3.9.0`](#arangodb390)
-	[`arangodb:latest`](#arangodblatest)

## `arangodb:3.7`

```console
$ docker pull arangodb@sha256:d9f434f9b2beded54b6666bcd69b529ff59d4745706d31ba9d58a17c686a962a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `arangodb:3.7` - linux; amd64

```console
$ docker pull arangodb@sha256:a2a42938899b297f04633b9a9085d6f8fcdb09fe793abbf41f75200eca62862b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.1 MB (133138324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8524338ba668cf6d2cdc8e69fe2cf24abff301392a572657b1a88a258f4b1e8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Mon, 24 Jan 2022 23:19:42 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Tue, 01 Feb 2022 22:19:15 GMT
ENV ARANGO_VERSION=3.7.17
# Tue, 01 Feb 2022 22:19:15 GMT
ENV ARANGO_URL=https://download.arangodb.com/arangodb37/DEBIAN/amd64
# Tue, 01 Feb 2022 22:19:16 GMT
ENV ARANGO_PACKAGE=arangodb3_3.7.17-1_amd64.deb
# Tue, 01 Feb 2022 22:19:16 GMT
ENV ARANGO_PACKAGE_URL=https://download.arangodb.com/arangodb37/DEBIAN/amd64/arangodb3_3.7.17-1_amd64.deb
# Tue, 01 Feb 2022 22:19:16 GMT
ENV ARANGO_SIGNATURE_URL=https://download.arangodb.com/arangodb37/DEBIAN/amd64/arangodb3_3.7.17-1_amd64.deb.asc
# Tue, 01 Feb 2022 22:19:44 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Tue, 01 Feb 2022 22:19:46 GMT
ENV GLIBCXX_FORCE_NEW=1
# Tue, 01 Feb 2022 22:19:46 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Tue, 01 Feb 2022 22:19:46 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Tue, 01 Feb 2022 22:19:46 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Tue, 01 Feb 2022 22:19:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 01 Feb 2022 22:19:47 GMT
EXPOSE 8529
# Tue, 01 Feb 2022 22:19:47 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63502ac4eff1694e8166142355a152fbda17f0313931796b554e21abb1b08016`  
		Last Modified: Tue, 01 Feb 2022 22:20:26 GMT  
		Size: 130.3 MB (130312996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e46aa055d725b997c61d353d85d90cbef2a3503e20aaa6bcb793e40f855ab604`  
		Last Modified: Tue, 01 Feb 2022 22:20:07 GMT  
		Size: 2.1 KB (2085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5388e2c8efed23f36ea92a659a624b99199d9d433c6da21193c20bf01b0ed7f8`  
		Last Modified: Tue, 01 Feb 2022 22:20:07 GMT  
		Size: 262.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:3.7.17`

```console
$ docker pull arangodb@sha256:d9f434f9b2beded54b6666bcd69b529ff59d4745706d31ba9d58a17c686a962a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `arangodb:3.7.17` - linux; amd64

```console
$ docker pull arangodb@sha256:a2a42938899b297f04633b9a9085d6f8fcdb09fe793abbf41f75200eca62862b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.1 MB (133138324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8524338ba668cf6d2cdc8e69fe2cf24abff301392a572657b1a88a258f4b1e8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Mon, 24 Jan 2022 23:19:42 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Tue, 01 Feb 2022 22:19:15 GMT
ENV ARANGO_VERSION=3.7.17
# Tue, 01 Feb 2022 22:19:15 GMT
ENV ARANGO_URL=https://download.arangodb.com/arangodb37/DEBIAN/amd64
# Tue, 01 Feb 2022 22:19:16 GMT
ENV ARANGO_PACKAGE=arangodb3_3.7.17-1_amd64.deb
# Tue, 01 Feb 2022 22:19:16 GMT
ENV ARANGO_PACKAGE_URL=https://download.arangodb.com/arangodb37/DEBIAN/amd64/arangodb3_3.7.17-1_amd64.deb
# Tue, 01 Feb 2022 22:19:16 GMT
ENV ARANGO_SIGNATURE_URL=https://download.arangodb.com/arangodb37/DEBIAN/amd64/arangodb3_3.7.17-1_amd64.deb.asc
# Tue, 01 Feb 2022 22:19:44 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Tue, 01 Feb 2022 22:19:46 GMT
ENV GLIBCXX_FORCE_NEW=1
# Tue, 01 Feb 2022 22:19:46 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Tue, 01 Feb 2022 22:19:46 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Tue, 01 Feb 2022 22:19:46 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Tue, 01 Feb 2022 22:19:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 01 Feb 2022 22:19:47 GMT
EXPOSE 8529
# Tue, 01 Feb 2022 22:19:47 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63502ac4eff1694e8166142355a152fbda17f0313931796b554e21abb1b08016`  
		Last Modified: Tue, 01 Feb 2022 22:20:26 GMT  
		Size: 130.3 MB (130312996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e46aa055d725b997c61d353d85d90cbef2a3503e20aaa6bcb793e40f855ab604`  
		Last Modified: Tue, 01 Feb 2022 22:20:07 GMT  
		Size: 2.1 KB (2085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5388e2c8efed23f36ea92a659a624b99199d9d433c6da21193c20bf01b0ed7f8`  
		Last Modified: Tue, 01 Feb 2022 22:20:07 GMT  
		Size: 262.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:3.8`

```console
$ docker pull arangodb@sha256:ff55cda4b7adf76b321504e65cd03fe7679fd7fa325b88dea54b25f86a36bd3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `arangodb:3.8` - linux; amd64

```console
$ docker pull arangodb@sha256:83bc9e8695aa6b7ad84d45df380e96875df9c5358513c6bf656326ece5359195
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.2 MB (191181407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b1edc188caa25539d7a2977c968119b65229059038ea6eaef6d313ff16137cd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Mon, 24 Jan 2022 23:19:42 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Wed, 23 Feb 2022 21:19:23 GMT
ENV ARANGO_VERSION=3.8.6
# Wed, 23 Feb 2022 21:19:23 GMT
ENV ARANGO_URL=https://download.arangodb.com/arangodb38/DEBIAN/amd64
# Wed, 23 Feb 2022 21:19:23 GMT
ENV ARANGO_PACKAGE=arangodb3_3.8.6-1_amd64.deb
# Wed, 23 Feb 2022 21:19:24 GMT
ENV ARANGO_PACKAGE_URL=https://download.arangodb.com/arangodb38/DEBIAN/amd64/arangodb3_3.8.6-1_amd64.deb
# Wed, 23 Feb 2022 21:19:24 GMT
ENV ARANGO_SIGNATURE_URL=https://download.arangodb.com/arangodb38/DEBIAN/amd64/arangodb3_3.8.6-1_amd64.deb.asc
# Wed, 23 Feb 2022 21:19:50 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.0.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Wed, 23 Feb 2022 21:19:51 GMT
ENV GLIBCXX_FORCE_NEW=1
# Wed, 23 Feb 2022 21:19:51 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Wed, 23 Feb 2022 21:19:52 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Wed, 23 Feb 2022 21:19:52 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Wed, 23 Feb 2022 21:19:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 23 Feb 2022 21:19:52 GMT
EXPOSE 8529
# Wed, 23 Feb 2022 21:19:52 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:773e8fb6c7eee1801bee5d91ecafe02d69e3f2e71684483e862bc5a30d552b36`  
		Last Modified: Wed, 23 Feb 2022 21:20:33 GMT  
		Size: 188.4 MB (188356080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fec3d4a5736752d1e2cffe4b418182235d4676380c35bd48651c1e6e43d91da9`  
		Last Modified: Wed, 23 Feb 2022 21:20:11 GMT  
		Size: 2.1 KB (2085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd62ac8afe0ac621c740aeb6ed5477ac428591be2dde65e86516f898ebf57f8a`  
		Last Modified: Wed, 23 Feb 2022 21:20:11 GMT  
		Size: 261.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:3.8.6`

```console
$ docker pull arangodb@sha256:ff55cda4b7adf76b321504e65cd03fe7679fd7fa325b88dea54b25f86a36bd3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `arangodb:3.8.6` - linux; amd64

```console
$ docker pull arangodb@sha256:83bc9e8695aa6b7ad84d45df380e96875df9c5358513c6bf656326ece5359195
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.2 MB (191181407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b1edc188caa25539d7a2977c968119b65229059038ea6eaef6d313ff16137cd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Mon, 24 Jan 2022 23:19:42 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Wed, 23 Feb 2022 21:19:23 GMT
ENV ARANGO_VERSION=3.8.6
# Wed, 23 Feb 2022 21:19:23 GMT
ENV ARANGO_URL=https://download.arangodb.com/arangodb38/DEBIAN/amd64
# Wed, 23 Feb 2022 21:19:23 GMT
ENV ARANGO_PACKAGE=arangodb3_3.8.6-1_amd64.deb
# Wed, 23 Feb 2022 21:19:24 GMT
ENV ARANGO_PACKAGE_URL=https://download.arangodb.com/arangodb38/DEBIAN/amd64/arangodb3_3.8.6-1_amd64.deb
# Wed, 23 Feb 2022 21:19:24 GMT
ENV ARANGO_SIGNATURE_URL=https://download.arangodb.com/arangodb38/DEBIAN/amd64/arangodb3_3.8.6-1_amd64.deb.asc
# Wed, 23 Feb 2022 21:19:50 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.0.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Wed, 23 Feb 2022 21:19:51 GMT
ENV GLIBCXX_FORCE_NEW=1
# Wed, 23 Feb 2022 21:19:51 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Wed, 23 Feb 2022 21:19:52 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Wed, 23 Feb 2022 21:19:52 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Wed, 23 Feb 2022 21:19:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 23 Feb 2022 21:19:52 GMT
EXPOSE 8529
# Wed, 23 Feb 2022 21:19:52 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:773e8fb6c7eee1801bee5d91ecafe02d69e3f2e71684483e862bc5a30d552b36`  
		Last Modified: Wed, 23 Feb 2022 21:20:33 GMT  
		Size: 188.4 MB (188356080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fec3d4a5736752d1e2cffe4b418182235d4676380c35bd48651c1e6e43d91da9`  
		Last Modified: Wed, 23 Feb 2022 21:20:11 GMT  
		Size: 2.1 KB (2085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd62ac8afe0ac621c740aeb6ed5477ac428591be2dde65e86516f898ebf57f8a`  
		Last Modified: Wed, 23 Feb 2022 21:20:11 GMT  
		Size: 261.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:3.9`

```console
$ docker pull arangodb@sha256:9fba4f596cefc32f8886c6a15de699185ec486b8b7e24b60b76db6170133f59d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `arangodb:3.9` - linux; amd64

```console
$ docker pull arangodb@sha256:0f469bbcb43f0c21f0d18580334444e0220225d687d8e4ec8e4e7288db58abad
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.9 MB (197863337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e501430d3240ce0de619698fd06175826e5f5a7716f065e5872cc2c24cf79c4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Mon, 24 Jan 2022 23:19:42 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Wed, 09 Feb 2022 20:19:17 GMT
ENV ARANGO_VERSION=3.9.0
# Wed, 09 Feb 2022 20:19:18 GMT
ENV ARANGO_URL=https://download.arangodb.com/arangodb39/DEBIAN/amd64
# Wed, 09 Feb 2022 20:19:18 GMT
ENV ARANGO_PACKAGE=arangodb3_3.9.0-1_amd64.deb
# Wed, 09 Feb 2022 20:19:18 GMT
ENV ARANGO_PACKAGE_URL=https://download.arangodb.com/arangodb39/DEBIAN/amd64/arangodb3_3.9.0-1_amd64.deb
# Wed, 09 Feb 2022 20:19:18 GMT
ENV ARANGO_SIGNATURE_URL=https://download.arangodb.com/arangodb39/DEBIAN/amd64/arangodb3_3.9.0-1_amd64.deb.asc
# Wed, 09 Feb 2022 20:19:44 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.0.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Wed, 09 Feb 2022 20:19:46 GMT
ENV GLIBCXX_FORCE_NEW=1
# Wed, 09 Feb 2022 20:19:46 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Wed, 09 Feb 2022 20:19:46 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Wed, 09 Feb 2022 20:19:46 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Wed, 09 Feb 2022 20:19:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 09 Feb 2022 20:19:47 GMT
EXPOSE 8529
# Wed, 09 Feb 2022 20:19:47 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f02a853c7927a577dfc0ac95ac85249d61600035e0f5cbaaa06c6c4eb946582c`  
		Last Modified: Wed, 09 Feb 2022 20:20:25 GMT  
		Size: 195.0 MB (195038012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8d34c0c7faf0c8c16dbf6629b3a2202f3dc4c43008811d594b86833a729ed65`  
		Last Modified: Wed, 09 Feb 2022 20:20:03 GMT  
		Size: 2.1 KB (2084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:706c235208c4c929f663f80c4edaf478530749a2c26e2b1d4290d68fe4e2e36a`  
		Last Modified: Wed, 09 Feb 2022 20:20:03 GMT  
		Size: 260.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:3.9.0`

```console
$ docker pull arangodb@sha256:9fba4f596cefc32f8886c6a15de699185ec486b8b7e24b60b76db6170133f59d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `arangodb:3.9.0` - linux; amd64

```console
$ docker pull arangodb@sha256:0f469bbcb43f0c21f0d18580334444e0220225d687d8e4ec8e4e7288db58abad
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.9 MB (197863337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e501430d3240ce0de619698fd06175826e5f5a7716f065e5872cc2c24cf79c4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Mon, 24 Jan 2022 23:19:42 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Wed, 09 Feb 2022 20:19:17 GMT
ENV ARANGO_VERSION=3.9.0
# Wed, 09 Feb 2022 20:19:18 GMT
ENV ARANGO_URL=https://download.arangodb.com/arangodb39/DEBIAN/amd64
# Wed, 09 Feb 2022 20:19:18 GMT
ENV ARANGO_PACKAGE=arangodb3_3.9.0-1_amd64.deb
# Wed, 09 Feb 2022 20:19:18 GMT
ENV ARANGO_PACKAGE_URL=https://download.arangodb.com/arangodb39/DEBIAN/amd64/arangodb3_3.9.0-1_amd64.deb
# Wed, 09 Feb 2022 20:19:18 GMT
ENV ARANGO_SIGNATURE_URL=https://download.arangodb.com/arangodb39/DEBIAN/amd64/arangodb3_3.9.0-1_amd64.deb.asc
# Wed, 09 Feb 2022 20:19:44 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.0.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Wed, 09 Feb 2022 20:19:46 GMT
ENV GLIBCXX_FORCE_NEW=1
# Wed, 09 Feb 2022 20:19:46 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Wed, 09 Feb 2022 20:19:46 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Wed, 09 Feb 2022 20:19:46 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Wed, 09 Feb 2022 20:19:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 09 Feb 2022 20:19:47 GMT
EXPOSE 8529
# Wed, 09 Feb 2022 20:19:47 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f02a853c7927a577dfc0ac95ac85249d61600035e0f5cbaaa06c6c4eb946582c`  
		Last Modified: Wed, 09 Feb 2022 20:20:25 GMT  
		Size: 195.0 MB (195038012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8d34c0c7faf0c8c16dbf6629b3a2202f3dc4c43008811d594b86833a729ed65`  
		Last Modified: Wed, 09 Feb 2022 20:20:03 GMT  
		Size: 2.1 KB (2084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:706c235208c4c929f663f80c4edaf478530749a2c26e2b1d4290d68fe4e2e36a`  
		Last Modified: Wed, 09 Feb 2022 20:20:03 GMT  
		Size: 260.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:latest`

```console
$ docker pull arangodb@sha256:9fba4f596cefc32f8886c6a15de699185ec486b8b7e24b60b76db6170133f59d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `arangodb:latest` - linux; amd64

```console
$ docker pull arangodb@sha256:0f469bbcb43f0c21f0d18580334444e0220225d687d8e4ec8e4e7288db58abad
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.9 MB (197863337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e501430d3240ce0de619698fd06175826e5f5a7716f065e5872cc2c24cf79c4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Mon, 24 Jan 2022 23:19:42 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Wed, 09 Feb 2022 20:19:17 GMT
ENV ARANGO_VERSION=3.9.0
# Wed, 09 Feb 2022 20:19:18 GMT
ENV ARANGO_URL=https://download.arangodb.com/arangodb39/DEBIAN/amd64
# Wed, 09 Feb 2022 20:19:18 GMT
ENV ARANGO_PACKAGE=arangodb3_3.9.0-1_amd64.deb
# Wed, 09 Feb 2022 20:19:18 GMT
ENV ARANGO_PACKAGE_URL=https://download.arangodb.com/arangodb39/DEBIAN/amd64/arangodb3_3.9.0-1_amd64.deb
# Wed, 09 Feb 2022 20:19:18 GMT
ENV ARANGO_SIGNATURE_URL=https://download.arangodb.com/arangodb39/DEBIAN/amd64/arangodb3_3.9.0-1_amd64.deb.asc
# Wed, 09 Feb 2022 20:19:44 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.0.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Wed, 09 Feb 2022 20:19:46 GMT
ENV GLIBCXX_FORCE_NEW=1
# Wed, 09 Feb 2022 20:19:46 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Wed, 09 Feb 2022 20:19:46 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Wed, 09 Feb 2022 20:19:46 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Wed, 09 Feb 2022 20:19:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 09 Feb 2022 20:19:47 GMT
EXPOSE 8529
# Wed, 09 Feb 2022 20:19:47 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f02a853c7927a577dfc0ac95ac85249d61600035e0f5cbaaa06c6c4eb946582c`  
		Last Modified: Wed, 09 Feb 2022 20:20:25 GMT  
		Size: 195.0 MB (195038012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8d34c0c7faf0c8c16dbf6629b3a2202f3dc4c43008811d594b86833a729ed65`  
		Last Modified: Wed, 09 Feb 2022 20:20:03 GMT  
		Size: 2.1 KB (2084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:706c235208c4c929f663f80c4edaf478530749a2c26e2b1d4290d68fe4e2e36a`  
		Last Modified: Wed, 09 Feb 2022 20:20:03 GMT  
		Size: 260.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
