<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `arangodb`

-	[`arangodb:3.6`](#arangodb36)
-	[`arangodb:3.6.12`](#arangodb3612)
-	[`arangodb:3.7`](#arangodb37)
-	[`arangodb:3.7.8`](#arangodb378)
-	[`arangodb:latest`](#arangodblatest)

## `arangodb:3.6`

```console
$ docker pull arangodb@sha256:020516c4a87fcadbbab11c53e3104f51c69b0451f3f0c7becfe99cc4e3e20e39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `arangodb:3.6` - linux; amd64

```console
$ docker pull arangodb@sha256:b752984634ed9281fe1ab375d57080184f6a2bd805ef3195355c879a5644aedf
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.3 MB (119341253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17560854b565b86712c04ca27cf8ac6e54a0b887441886294d075bdedea2f6d5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Wed, 24 Feb 2021 20:20:11 GMT
ADD file:7eeea546ecde7a036bf634c08719879d32c7ec6ae599708cd91dc1b830735223 in / 
# Wed, 24 Feb 2021 20:20:12 GMT
CMD ["/bin/sh"]
# Wed, 24 Feb 2021 20:36:06 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Wed, 24 Feb 2021 20:36:07 GMT
ENV ARANGO_VERSION=3.6.11
# Wed, 24 Feb 2021 20:36:07 GMT
ENV ARANGO_URL=https://download.arangodb.com/arangodb36/DEBIAN/amd64
# Wed, 24 Feb 2021 20:36:07 GMT
ENV ARANGO_PACKAGE=arangodb3_3.6.11-1_amd64.deb
# Wed, 24 Feb 2021 20:36:07 GMT
ENV ARANGO_PACKAGE_URL=https://download.arangodb.com/arangodb36/DEBIAN/amd64/arangodb3_3.6.11-1_amd64.deb
# Wed, 24 Feb 2021 20:36:07 GMT
ENV ARANGO_SIGNATURE_URL=https://download.arangodb.com/arangodb36/DEBIAN/amd64/arangodb3_3.6.11-1_amd64.deb.asc
# Wed, 24 Feb 2021 20:36:35 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli &&     apk del yarn &&     gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     echo chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     echo chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Wed, 24 Feb 2021 20:36:35 GMT
ENV GLIBCXX_FORCE_NEW=1
# Wed, 24 Feb 2021 20:36:35 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Wed, 24 Feb 2021 20:36:36 GMT
COPY file:3a0ad717437ce87e5e260280982f3288fcfff74b46a1f17e5cd07f64d64ee5fa in /entrypoint.sh 
# Wed, 24 Feb 2021 20:36:36 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Wed, 24 Feb 2021 20:36:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Feb 2021 20:36:36 GMT
EXPOSE 8529
# Wed, 24 Feb 2021 20:36:36 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:e95f33c60a645d6d31f52fdc334aecec0d79a1b410789eae37fbf69efcd587ab`  
		Last Modified: Wed, 24 Feb 2021 20:20:43 GMT  
		Size: 2.8 MB (2815313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a3f32a215aaa6bc1e56624ca07075013ad410e92f66d6c19100bf76034ed55b`  
		Last Modified: Wed, 24 Feb 2021 20:37:44 GMT  
		Size: 116.5 MB (116523499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32785247e6c6403df62ed57228cd14b31dc48cf68ae85bddc877929438e96f99`  
		Last Modified: Wed, 24 Feb 2021 20:37:25 GMT  
		Size: 2.2 KB (2179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26664c7c4e9ea38c03436a5036c1ba3653c685e5ba9352ffdd2c438c230d1452`  
		Last Modified: Wed, 24 Feb 2021 20:37:25 GMT  
		Size: 262.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:3.6.12`

```console
$ docker pull arangodb@sha256:a8409dff6597f2ef5f7ecd3c672671bb2af9a390073efd74f95c54aa41cba22a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:

## `arangodb:3.7`

```console
$ docker pull arangodb@sha256:0c723b690261d331ef9aa307be4c046f35ec671c5f63a6d101acb30734f54463
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `arangodb:3.7` - linux; amd64

```console
$ docker pull arangodb@sha256:43f86488880c5df118545a262cb0174b2bd06ee1abb78e8e76b7be75b721af29
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.2 MB (128152418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a2c07a33395c180d500c2dee5629bcff8bfe35736d7daf69e18a54c3deca2a8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Wed, 24 Feb 2021 20:20:11 GMT
ADD file:7eeea546ecde7a036bf634c08719879d32c7ec6ae599708cd91dc1b830735223 in / 
# Wed, 24 Feb 2021 20:20:12 GMT
CMD ["/bin/sh"]
# Wed, 24 Feb 2021 20:36:06 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Wed, 24 Feb 2021 20:36:41 GMT
ENV ARANGO_VERSION=3.7.8
# Wed, 24 Feb 2021 20:36:41 GMT
ENV ARANGO_URL=https://download.arangodb.com/arangodb37/DEBIAN/amd64
# Wed, 24 Feb 2021 20:36:41 GMT
ENV ARANGO_PACKAGE=arangodb3_3.7.8-1_amd64.deb
# Wed, 24 Feb 2021 20:36:41 GMT
ENV ARANGO_PACKAGE_URL=https://download.arangodb.com/arangodb37/DEBIAN/amd64/arangodb3_3.7.8-1_amd64.deb
# Wed, 24 Feb 2021 20:36:42 GMT
ENV ARANGO_SIGNATURE_URL=https://download.arangodb.com/arangodb37/DEBIAN/amd64/arangodb3_3.7.8-1_amd64.deb.asc
# Wed, 24 Feb 2021 20:37:09 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli &&     apk del yarn &&     gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     echo chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     echo chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Wed, 24 Feb 2021 20:37:09 GMT
ENV GLIBCXX_FORCE_NEW=1
# Wed, 24 Feb 2021 20:37:10 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Wed, 24 Feb 2021 20:37:10 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Wed, 24 Feb 2021 20:37:10 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Wed, 24 Feb 2021 20:37:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Feb 2021 20:37:10 GMT
EXPOSE 8529
# Wed, 24 Feb 2021 20:37:11 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:e95f33c60a645d6d31f52fdc334aecec0d79a1b410789eae37fbf69efcd587ab`  
		Last Modified: Wed, 24 Feb 2021 20:20:43 GMT  
		Size: 2.8 MB (2815313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2af0a15c1eae3074fca33dce943301ba04f649d8b938794ac946f3bf18f9048e`  
		Last Modified: Wed, 24 Feb 2021 20:38:10 GMT  
		Size: 125.3 MB (125334758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a49236682e8db8727d481a5f618f351b0e3eb979620284f047b1b85fb19090c5`  
		Last Modified: Wed, 24 Feb 2021 20:37:49 GMT  
		Size: 2.1 KB (2086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba3b8a72fc08b3b6d9af5ef040a77deb3d43d1bdba6a8e8ec90630796adb6fd1`  
		Last Modified: Wed, 24 Feb 2021 20:37:49 GMT  
		Size: 261.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:3.7.8`

```console
$ docker pull arangodb@sha256:0c723b690261d331ef9aa307be4c046f35ec671c5f63a6d101acb30734f54463
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `arangodb:3.7.8` - linux; amd64

```console
$ docker pull arangodb@sha256:43f86488880c5df118545a262cb0174b2bd06ee1abb78e8e76b7be75b721af29
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.2 MB (128152418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a2c07a33395c180d500c2dee5629bcff8bfe35736d7daf69e18a54c3deca2a8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Wed, 24 Feb 2021 20:20:11 GMT
ADD file:7eeea546ecde7a036bf634c08719879d32c7ec6ae599708cd91dc1b830735223 in / 
# Wed, 24 Feb 2021 20:20:12 GMT
CMD ["/bin/sh"]
# Wed, 24 Feb 2021 20:36:06 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Wed, 24 Feb 2021 20:36:41 GMT
ENV ARANGO_VERSION=3.7.8
# Wed, 24 Feb 2021 20:36:41 GMT
ENV ARANGO_URL=https://download.arangodb.com/arangodb37/DEBIAN/amd64
# Wed, 24 Feb 2021 20:36:41 GMT
ENV ARANGO_PACKAGE=arangodb3_3.7.8-1_amd64.deb
# Wed, 24 Feb 2021 20:36:41 GMT
ENV ARANGO_PACKAGE_URL=https://download.arangodb.com/arangodb37/DEBIAN/amd64/arangodb3_3.7.8-1_amd64.deb
# Wed, 24 Feb 2021 20:36:42 GMT
ENV ARANGO_SIGNATURE_URL=https://download.arangodb.com/arangodb37/DEBIAN/amd64/arangodb3_3.7.8-1_amd64.deb.asc
# Wed, 24 Feb 2021 20:37:09 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli &&     apk del yarn &&     gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     echo chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     echo chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Wed, 24 Feb 2021 20:37:09 GMT
ENV GLIBCXX_FORCE_NEW=1
# Wed, 24 Feb 2021 20:37:10 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Wed, 24 Feb 2021 20:37:10 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Wed, 24 Feb 2021 20:37:10 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Wed, 24 Feb 2021 20:37:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Feb 2021 20:37:10 GMT
EXPOSE 8529
# Wed, 24 Feb 2021 20:37:11 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:e95f33c60a645d6d31f52fdc334aecec0d79a1b410789eae37fbf69efcd587ab`  
		Last Modified: Wed, 24 Feb 2021 20:20:43 GMT  
		Size: 2.8 MB (2815313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2af0a15c1eae3074fca33dce943301ba04f649d8b938794ac946f3bf18f9048e`  
		Last Modified: Wed, 24 Feb 2021 20:38:10 GMT  
		Size: 125.3 MB (125334758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a49236682e8db8727d481a5f618f351b0e3eb979620284f047b1b85fb19090c5`  
		Last Modified: Wed, 24 Feb 2021 20:37:49 GMT  
		Size: 2.1 KB (2086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba3b8a72fc08b3b6d9af5ef040a77deb3d43d1bdba6a8e8ec90630796adb6fd1`  
		Last Modified: Wed, 24 Feb 2021 20:37:49 GMT  
		Size: 261.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:latest`

```console
$ docker pull arangodb@sha256:0c723b690261d331ef9aa307be4c046f35ec671c5f63a6d101acb30734f54463
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `arangodb:latest` - linux; amd64

```console
$ docker pull arangodb@sha256:43f86488880c5df118545a262cb0174b2bd06ee1abb78e8e76b7be75b721af29
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.2 MB (128152418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a2c07a33395c180d500c2dee5629bcff8bfe35736d7daf69e18a54c3deca2a8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Wed, 24 Feb 2021 20:20:11 GMT
ADD file:7eeea546ecde7a036bf634c08719879d32c7ec6ae599708cd91dc1b830735223 in / 
# Wed, 24 Feb 2021 20:20:12 GMT
CMD ["/bin/sh"]
# Wed, 24 Feb 2021 20:36:06 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Wed, 24 Feb 2021 20:36:41 GMT
ENV ARANGO_VERSION=3.7.8
# Wed, 24 Feb 2021 20:36:41 GMT
ENV ARANGO_URL=https://download.arangodb.com/arangodb37/DEBIAN/amd64
# Wed, 24 Feb 2021 20:36:41 GMT
ENV ARANGO_PACKAGE=arangodb3_3.7.8-1_amd64.deb
# Wed, 24 Feb 2021 20:36:41 GMT
ENV ARANGO_PACKAGE_URL=https://download.arangodb.com/arangodb37/DEBIAN/amd64/arangodb3_3.7.8-1_amd64.deb
# Wed, 24 Feb 2021 20:36:42 GMT
ENV ARANGO_SIGNATURE_URL=https://download.arangodb.com/arangodb37/DEBIAN/amd64/arangodb3_3.7.8-1_amd64.deb.asc
# Wed, 24 Feb 2021 20:37:09 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli &&     apk del yarn &&     gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     echo chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     echo chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Wed, 24 Feb 2021 20:37:09 GMT
ENV GLIBCXX_FORCE_NEW=1
# Wed, 24 Feb 2021 20:37:10 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Wed, 24 Feb 2021 20:37:10 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Wed, 24 Feb 2021 20:37:10 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Wed, 24 Feb 2021 20:37:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Feb 2021 20:37:10 GMT
EXPOSE 8529
# Wed, 24 Feb 2021 20:37:11 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:e95f33c60a645d6d31f52fdc334aecec0d79a1b410789eae37fbf69efcd587ab`  
		Last Modified: Wed, 24 Feb 2021 20:20:43 GMT  
		Size: 2.8 MB (2815313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2af0a15c1eae3074fca33dce943301ba04f649d8b938794ac946f3bf18f9048e`  
		Last Modified: Wed, 24 Feb 2021 20:38:10 GMT  
		Size: 125.3 MB (125334758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a49236682e8db8727d481a5f618f351b0e3eb979620284f047b1b85fb19090c5`  
		Last Modified: Wed, 24 Feb 2021 20:37:49 GMT  
		Size: 2.1 KB (2086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba3b8a72fc08b3b6d9af5ef040a77deb3d43d1bdba6a8e8ec90630796adb6fd1`  
		Last Modified: Wed, 24 Feb 2021 20:37:49 GMT  
		Size: 261.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
