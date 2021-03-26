<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `arangodb`

-	[`arangodb:3.6`](#arangodb36)
-	[`arangodb:3.6.12`](#arangodb3612)
-	[`arangodb:3.7`](#arangodb37)
-	[`arangodb:3.7.10`](#arangodb3710)
-	[`arangodb:latest`](#arangodblatest)

## `arangodb:3.6`

```console
$ docker pull arangodb@sha256:9bcbdd732bc8bcbf22b7af2cf8da8fcea0cb4c05984b79ae610860579526d2af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `arangodb:3.6` - linux; amd64

```console
$ docker pull arangodb@sha256:a9d49fb86842339f0626e7d7c14ba3716737c48b5df373956172378998a0fc9c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.6 MB (119562082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33d40028e7d0aabceda81707173ac7f312d255b63b3e2421bfc5e29fb2b433ad`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Thu, 25 Mar 2021 22:19:43 GMT
ADD file:05adf37fc1a41a31d8e0e0b9371a01161abc0d348adacbc81689a1a34e8fe12d in / 
# Thu, 25 Mar 2021 22:19:43 GMT
CMD ["/bin/sh"]
# Fri, 26 Mar 2021 02:04:00 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Fri, 26 Mar 2021 02:04:01 GMT
ENV ARANGO_VERSION=3.6.12
# Fri, 26 Mar 2021 02:04:01 GMT
ENV ARANGO_URL=https://download.arangodb.com/arangodb36/DEBIAN/amd64
# Fri, 26 Mar 2021 02:04:01 GMT
ENV ARANGO_PACKAGE=arangodb3_3.6.12-1_amd64.deb
# Fri, 26 Mar 2021 02:04:01 GMT
ENV ARANGO_PACKAGE_URL=https://download.arangodb.com/arangodb36/DEBIAN/amd64/arangodb3_3.6.12-1_amd64.deb
# Fri, 26 Mar 2021 02:04:02 GMT
ENV ARANGO_SIGNATURE_URL=https://download.arangodb.com/arangodb36/DEBIAN/amd64/arangodb3_3.6.12-1_amd64.deb.asc
# Fri, 26 Mar 2021 02:04:37 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli &&     apk del yarn &&     gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     echo chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     echo chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Fri, 26 Mar 2021 02:04:38 GMT
ENV GLIBCXX_FORCE_NEW=1
# Fri, 26 Mar 2021 02:04:39 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Fri, 26 Mar 2021 02:04:39 GMT
COPY file:0906ed6b024317ae8adc7caf5905c27c8ed6d7c227bbbfd131411e3fb9a6beaa in /entrypoint.sh 
# Fri, 26 Mar 2021 02:04:39 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Fri, 26 Mar 2021 02:04:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Mar 2021 02:04:40 GMT
EXPOSE 8529
# Fri, 26 Mar 2021 02:04:40 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:839b45e0263abc8ab2dc0bfabc91a19947e932ffbd551a93970ea3ee971eadf6`  
		Last Modified: Thu, 25 Mar 2021 22:20:47 GMT  
		Size: 2.8 MB (2815332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf1759f16c8e9267f79f97ca25ab07249d7bff788cb73c0c40f8d03ec51b1b52`  
		Last Modified: Fri, 26 Mar 2021 02:06:21 GMT  
		Size: 116.7 MB (116744314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25e75d7a17dd5e5aeef52584e938f18f5403ae34da2943c0ec373b75067fefc2`  
		Last Modified: Fri, 26 Mar 2021 02:05:56 GMT  
		Size: 2.2 KB (2176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c40f4f65b3bcd9638a1db43353e25acb390ac4ea55e064ba7fc323ebd9a67e3b`  
		Last Modified: Fri, 26 Mar 2021 02:05:55 GMT  
		Size: 260.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:3.6.12`

```console
$ docker pull arangodb@sha256:9bcbdd732bc8bcbf22b7af2cf8da8fcea0cb4c05984b79ae610860579526d2af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `arangodb:3.6.12` - linux; amd64

```console
$ docker pull arangodb@sha256:a9d49fb86842339f0626e7d7c14ba3716737c48b5df373956172378998a0fc9c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.6 MB (119562082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33d40028e7d0aabceda81707173ac7f312d255b63b3e2421bfc5e29fb2b433ad`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Thu, 25 Mar 2021 22:19:43 GMT
ADD file:05adf37fc1a41a31d8e0e0b9371a01161abc0d348adacbc81689a1a34e8fe12d in / 
# Thu, 25 Mar 2021 22:19:43 GMT
CMD ["/bin/sh"]
# Fri, 26 Mar 2021 02:04:00 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Fri, 26 Mar 2021 02:04:01 GMT
ENV ARANGO_VERSION=3.6.12
# Fri, 26 Mar 2021 02:04:01 GMT
ENV ARANGO_URL=https://download.arangodb.com/arangodb36/DEBIAN/amd64
# Fri, 26 Mar 2021 02:04:01 GMT
ENV ARANGO_PACKAGE=arangodb3_3.6.12-1_amd64.deb
# Fri, 26 Mar 2021 02:04:01 GMT
ENV ARANGO_PACKAGE_URL=https://download.arangodb.com/arangodb36/DEBIAN/amd64/arangodb3_3.6.12-1_amd64.deb
# Fri, 26 Mar 2021 02:04:02 GMT
ENV ARANGO_SIGNATURE_URL=https://download.arangodb.com/arangodb36/DEBIAN/amd64/arangodb3_3.6.12-1_amd64.deb.asc
# Fri, 26 Mar 2021 02:04:37 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli &&     apk del yarn &&     gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     echo chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     echo chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Fri, 26 Mar 2021 02:04:38 GMT
ENV GLIBCXX_FORCE_NEW=1
# Fri, 26 Mar 2021 02:04:39 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Fri, 26 Mar 2021 02:04:39 GMT
COPY file:0906ed6b024317ae8adc7caf5905c27c8ed6d7c227bbbfd131411e3fb9a6beaa in /entrypoint.sh 
# Fri, 26 Mar 2021 02:04:39 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Fri, 26 Mar 2021 02:04:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Mar 2021 02:04:40 GMT
EXPOSE 8529
# Fri, 26 Mar 2021 02:04:40 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:839b45e0263abc8ab2dc0bfabc91a19947e932ffbd551a93970ea3ee971eadf6`  
		Last Modified: Thu, 25 Mar 2021 22:20:47 GMT  
		Size: 2.8 MB (2815332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf1759f16c8e9267f79f97ca25ab07249d7bff788cb73c0c40f8d03ec51b1b52`  
		Last Modified: Fri, 26 Mar 2021 02:06:21 GMT  
		Size: 116.7 MB (116744314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25e75d7a17dd5e5aeef52584e938f18f5403ae34da2943c0ec373b75067fefc2`  
		Last Modified: Fri, 26 Mar 2021 02:05:56 GMT  
		Size: 2.2 KB (2176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c40f4f65b3bcd9638a1db43353e25acb390ac4ea55e064ba7fc323ebd9a67e3b`  
		Last Modified: Fri, 26 Mar 2021 02:05:55 GMT  
		Size: 260.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:3.7`

```console
$ docker pull arangodb@sha256:73b08d782f9ee9e60ba385bfe241a5f97c787b42c1d6389b5f792fc6b0e3e2af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `arangodb:3.7` - linux; amd64

```console
$ docker pull arangodb@sha256:64a8bbda6730e34b68a80fa6d75fdb28764e3703de6ac80f7319ab86f1fd28c5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.4 MB (128398207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6c28d19b02e59ef3872b0462a6b233d019273c846a769edbb1537713d439d39`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Thu, 25 Mar 2021 22:19:43 GMT
ADD file:05adf37fc1a41a31d8e0e0b9371a01161abc0d348adacbc81689a1a34e8fe12d in / 
# Thu, 25 Mar 2021 22:19:43 GMT
CMD ["/bin/sh"]
# Fri, 26 Mar 2021 02:04:00 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Fri, 26 Mar 2021 02:04:52 GMT
ENV ARANGO_VERSION=3.7.10
# Fri, 26 Mar 2021 02:04:52 GMT
ENV ARANGO_URL=https://download.arangodb.com/arangodb37/DEBIAN/amd64
# Fri, 26 Mar 2021 02:04:52 GMT
ENV ARANGO_PACKAGE=arangodb3_3.7.10-1_amd64.deb
# Fri, 26 Mar 2021 02:04:52 GMT
ENV ARANGO_PACKAGE_URL=https://download.arangodb.com/arangodb37/DEBIAN/amd64/arangodb3_3.7.10-1_amd64.deb
# Fri, 26 Mar 2021 02:04:53 GMT
ENV ARANGO_SIGNATURE_URL=https://download.arangodb.com/arangodb37/DEBIAN/amd64/arangodb3_3.7.10-1_amd64.deb.asc
# Fri, 26 Mar 2021 02:05:31 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli &&     apk del yarn &&     gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     echo chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     echo chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Fri, 26 Mar 2021 02:05:32 GMT
ENV GLIBCXX_FORCE_NEW=1
# Fri, 26 Mar 2021 02:05:32 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Fri, 26 Mar 2021 02:05:33 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Fri, 26 Mar 2021 02:05:33 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Fri, 26 Mar 2021 02:05:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Mar 2021 02:05:34 GMT
EXPOSE 8529
# Fri, 26 Mar 2021 02:05:34 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:839b45e0263abc8ab2dc0bfabc91a19947e932ffbd551a93970ea3ee971eadf6`  
		Last Modified: Thu, 25 Mar 2021 22:20:47 GMT  
		Size: 2.8 MB (2815332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94d33e33accc45e31d504b70bbafcd4b948f713b66b97282ee23ee1ada5cca29`  
		Last Modified: Fri, 26 Mar 2021 02:07:02 GMT  
		Size: 125.6 MB (125580528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51661300bad44cba5815b339d697a2204c927c6658bb4b1629395d4aff7cac1e`  
		Last Modified: Fri, 26 Mar 2021 02:06:34 GMT  
		Size: 2.1 KB (2085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c66e45f0010b211336e826f7905d6d082d267d161c5f335bc6478d98467aa88`  
		Last Modified: Fri, 26 Mar 2021 02:06:35 GMT  
		Size: 262.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:3.7.10`

```console
$ docker pull arangodb@sha256:73b08d782f9ee9e60ba385bfe241a5f97c787b42c1d6389b5f792fc6b0e3e2af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `arangodb:3.7.10` - linux; amd64

```console
$ docker pull arangodb@sha256:64a8bbda6730e34b68a80fa6d75fdb28764e3703de6ac80f7319ab86f1fd28c5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.4 MB (128398207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6c28d19b02e59ef3872b0462a6b233d019273c846a769edbb1537713d439d39`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Thu, 25 Mar 2021 22:19:43 GMT
ADD file:05adf37fc1a41a31d8e0e0b9371a01161abc0d348adacbc81689a1a34e8fe12d in / 
# Thu, 25 Mar 2021 22:19:43 GMT
CMD ["/bin/sh"]
# Fri, 26 Mar 2021 02:04:00 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Fri, 26 Mar 2021 02:04:52 GMT
ENV ARANGO_VERSION=3.7.10
# Fri, 26 Mar 2021 02:04:52 GMT
ENV ARANGO_URL=https://download.arangodb.com/arangodb37/DEBIAN/amd64
# Fri, 26 Mar 2021 02:04:52 GMT
ENV ARANGO_PACKAGE=arangodb3_3.7.10-1_amd64.deb
# Fri, 26 Mar 2021 02:04:52 GMT
ENV ARANGO_PACKAGE_URL=https://download.arangodb.com/arangodb37/DEBIAN/amd64/arangodb3_3.7.10-1_amd64.deb
# Fri, 26 Mar 2021 02:04:53 GMT
ENV ARANGO_SIGNATURE_URL=https://download.arangodb.com/arangodb37/DEBIAN/amd64/arangodb3_3.7.10-1_amd64.deb.asc
# Fri, 26 Mar 2021 02:05:31 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli &&     apk del yarn &&     gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     echo chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     echo chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Fri, 26 Mar 2021 02:05:32 GMT
ENV GLIBCXX_FORCE_NEW=1
# Fri, 26 Mar 2021 02:05:32 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Fri, 26 Mar 2021 02:05:33 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Fri, 26 Mar 2021 02:05:33 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Fri, 26 Mar 2021 02:05:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Mar 2021 02:05:34 GMT
EXPOSE 8529
# Fri, 26 Mar 2021 02:05:34 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:839b45e0263abc8ab2dc0bfabc91a19947e932ffbd551a93970ea3ee971eadf6`  
		Last Modified: Thu, 25 Mar 2021 22:20:47 GMT  
		Size: 2.8 MB (2815332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94d33e33accc45e31d504b70bbafcd4b948f713b66b97282ee23ee1ada5cca29`  
		Last Modified: Fri, 26 Mar 2021 02:07:02 GMT  
		Size: 125.6 MB (125580528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51661300bad44cba5815b339d697a2204c927c6658bb4b1629395d4aff7cac1e`  
		Last Modified: Fri, 26 Mar 2021 02:06:34 GMT  
		Size: 2.1 KB (2085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c66e45f0010b211336e826f7905d6d082d267d161c5f335bc6478d98467aa88`  
		Last Modified: Fri, 26 Mar 2021 02:06:35 GMT  
		Size: 262.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:latest`

```console
$ docker pull arangodb@sha256:73b08d782f9ee9e60ba385bfe241a5f97c787b42c1d6389b5f792fc6b0e3e2af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `arangodb:latest` - linux; amd64

```console
$ docker pull arangodb@sha256:64a8bbda6730e34b68a80fa6d75fdb28764e3703de6ac80f7319ab86f1fd28c5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.4 MB (128398207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6c28d19b02e59ef3872b0462a6b233d019273c846a769edbb1537713d439d39`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Thu, 25 Mar 2021 22:19:43 GMT
ADD file:05adf37fc1a41a31d8e0e0b9371a01161abc0d348adacbc81689a1a34e8fe12d in / 
# Thu, 25 Mar 2021 22:19:43 GMT
CMD ["/bin/sh"]
# Fri, 26 Mar 2021 02:04:00 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Fri, 26 Mar 2021 02:04:52 GMT
ENV ARANGO_VERSION=3.7.10
# Fri, 26 Mar 2021 02:04:52 GMT
ENV ARANGO_URL=https://download.arangodb.com/arangodb37/DEBIAN/amd64
# Fri, 26 Mar 2021 02:04:52 GMT
ENV ARANGO_PACKAGE=arangodb3_3.7.10-1_amd64.deb
# Fri, 26 Mar 2021 02:04:52 GMT
ENV ARANGO_PACKAGE_URL=https://download.arangodb.com/arangodb37/DEBIAN/amd64/arangodb3_3.7.10-1_amd64.deb
# Fri, 26 Mar 2021 02:04:53 GMT
ENV ARANGO_SIGNATURE_URL=https://download.arangodb.com/arangodb37/DEBIAN/amd64/arangodb3_3.7.10-1_amd64.deb.asc
# Fri, 26 Mar 2021 02:05:31 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli &&     apk del yarn &&     gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     echo chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     echo chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Fri, 26 Mar 2021 02:05:32 GMT
ENV GLIBCXX_FORCE_NEW=1
# Fri, 26 Mar 2021 02:05:32 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Fri, 26 Mar 2021 02:05:33 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Fri, 26 Mar 2021 02:05:33 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Fri, 26 Mar 2021 02:05:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Mar 2021 02:05:34 GMT
EXPOSE 8529
# Fri, 26 Mar 2021 02:05:34 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:839b45e0263abc8ab2dc0bfabc91a19947e932ffbd551a93970ea3ee971eadf6`  
		Last Modified: Thu, 25 Mar 2021 22:20:47 GMT  
		Size: 2.8 MB (2815332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94d33e33accc45e31d504b70bbafcd4b948f713b66b97282ee23ee1ada5cca29`  
		Last Modified: Fri, 26 Mar 2021 02:07:02 GMT  
		Size: 125.6 MB (125580528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51661300bad44cba5815b339d697a2204c927c6658bb4b1629395d4aff7cac1e`  
		Last Modified: Fri, 26 Mar 2021 02:06:34 GMT  
		Size: 2.1 KB (2085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c66e45f0010b211336e826f7905d6d082d267d161c5f335bc6478d98467aa88`  
		Last Modified: Fri, 26 Mar 2021 02:06:35 GMT  
		Size: 262.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
