<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `arangodb`

-	[`arangodb:3.6`](#arangodb36)
-	[`arangodb:3.6.11`](#arangodb3611)
-	[`arangodb:3.7`](#arangodb37)
-	[`arangodb:3.7.7`](#arangodb377)
-	[`arangodb:latest`](#arangodblatest)

## `arangodb:3.6`

```console
$ docker pull arangodb@sha256:034294fea74878a5c78c25bd4adea240f956e544b9a45508909f7b8f75592faa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `arangodb:3.6` - linux; amd64

```console
$ docker pull arangodb@sha256:c14945cf61186ccdfb982c14010392522cf026c6b6ad697d5c0f8627777dde97
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.3 MB (119289083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c2ffd0b4e05cb4508c8a0aba926de7c606d7c3471dd482aa75f4f7dae8e6f5f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Thu, 17 Dec 2020 00:19:49 GMT
ADD file:8ed80010e443da19d72546bcee9a35e0a8d244c72052b1994610bf5939d479c2 in / 
# Thu, 17 Dec 2020 00:19:49 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 00:53:15 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Thu, 21 Jan 2021 19:24:28 GMT
ENV ARANGO_VERSION=3.6.11
# Thu, 21 Jan 2021 19:24:29 GMT
ENV ARANGO_URL=https://download.arangodb.com/arangodb36/DEBIAN/amd64
# Thu, 21 Jan 2021 19:24:29 GMT
ENV ARANGO_PACKAGE=arangodb3_3.6.11-1_amd64.deb
# Thu, 21 Jan 2021 19:24:29 GMT
ENV ARANGO_PACKAGE_URL=https://download.arangodb.com/arangodb36/DEBIAN/amd64/arangodb3_3.6.11-1_amd64.deb
# Thu, 21 Jan 2021 19:24:29 GMT
ENV ARANGO_SIGNATURE_URL=https://download.arangodb.com/arangodb36/DEBIAN/amd64/arangodb3_3.6.11-1_amd64.deb.asc
# Thu, 21 Jan 2021 19:24:56 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli &&     apk del yarn &&     gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     echo chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     echo chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Thu, 21 Jan 2021 19:24:57 GMT
ENV GLIBCXX_FORCE_NEW=1
# Thu, 21 Jan 2021 19:24:57 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Thu, 21 Jan 2021 19:24:57 GMT
COPY file:3a0ad717437ce87e5e260280982f3288fcfff74b46a1f17e5cd07f64d64ee5fa in /entrypoint.sh 
# Thu, 21 Jan 2021 19:24:58 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Thu, 21 Jan 2021 19:24:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 21 Jan 2021 19:24:58 GMT
EXPOSE 8529
# Thu, 21 Jan 2021 19:24:58 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:0a6724ff3fcd51338afdfdc2b1d4ffd04569818e31efad957213d67c29b45101`  
		Last Modified: Thu, 17 Dec 2020 00:20:26 GMT  
		Size: 2.8 MB (2814864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af20a041ff67b31d4574aee7a76ddba87d1b749ea3b0a2da6d47fa1dabd7f5c9`  
		Last Modified: Thu, 21 Jan 2021 19:25:36 GMT  
		Size: 116.5 MB (116471775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f22b741c2188fa454ae25c96e22cd84c2603eee4ed70a1c866b850155f2aa20`  
		Last Modified: Thu, 21 Jan 2021 19:25:16 GMT  
		Size: 2.2 KB (2180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:936d6b4e0948dd9dd298b748c6cfaf2996fa68b2e48f94288c02abbed39fc35b`  
		Last Modified: Thu, 21 Jan 2021 19:25:16 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:3.6.11`

```console
$ docker pull arangodb@sha256:034294fea74878a5c78c25bd4adea240f956e544b9a45508909f7b8f75592faa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `arangodb:3.6.11` - linux; amd64

```console
$ docker pull arangodb@sha256:c14945cf61186ccdfb982c14010392522cf026c6b6ad697d5c0f8627777dde97
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.3 MB (119289083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c2ffd0b4e05cb4508c8a0aba926de7c606d7c3471dd482aa75f4f7dae8e6f5f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Thu, 17 Dec 2020 00:19:49 GMT
ADD file:8ed80010e443da19d72546bcee9a35e0a8d244c72052b1994610bf5939d479c2 in / 
# Thu, 17 Dec 2020 00:19:49 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 00:53:15 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Thu, 21 Jan 2021 19:24:28 GMT
ENV ARANGO_VERSION=3.6.11
# Thu, 21 Jan 2021 19:24:29 GMT
ENV ARANGO_URL=https://download.arangodb.com/arangodb36/DEBIAN/amd64
# Thu, 21 Jan 2021 19:24:29 GMT
ENV ARANGO_PACKAGE=arangodb3_3.6.11-1_amd64.deb
# Thu, 21 Jan 2021 19:24:29 GMT
ENV ARANGO_PACKAGE_URL=https://download.arangodb.com/arangodb36/DEBIAN/amd64/arangodb3_3.6.11-1_amd64.deb
# Thu, 21 Jan 2021 19:24:29 GMT
ENV ARANGO_SIGNATURE_URL=https://download.arangodb.com/arangodb36/DEBIAN/amd64/arangodb3_3.6.11-1_amd64.deb.asc
# Thu, 21 Jan 2021 19:24:56 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli &&     apk del yarn &&     gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     echo chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     echo chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Thu, 21 Jan 2021 19:24:57 GMT
ENV GLIBCXX_FORCE_NEW=1
# Thu, 21 Jan 2021 19:24:57 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Thu, 21 Jan 2021 19:24:57 GMT
COPY file:3a0ad717437ce87e5e260280982f3288fcfff74b46a1f17e5cd07f64d64ee5fa in /entrypoint.sh 
# Thu, 21 Jan 2021 19:24:58 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Thu, 21 Jan 2021 19:24:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 21 Jan 2021 19:24:58 GMT
EXPOSE 8529
# Thu, 21 Jan 2021 19:24:58 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:0a6724ff3fcd51338afdfdc2b1d4ffd04569818e31efad957213d67c29b45101`  
		Last Modified: Thu, 17 Dec 2020 00:20:26 GMT  
		Size: 2.8 MB (2814864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af20a041ff67b31d4574aee7a76ddba87d1b749ea3b0a2da6d47fa1dabd7f5c9`  
		Last Modified: Thu, 21 Jan 2021 19:25:36 GMT  
		Size: 116.5 MB (116471775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f22b741c2188fa454ae25c96e22cd84c2603eee4ed70a1c866b850155f2aa20`  
		Last Modified: Thu, 21 Jan 2021 19:25:16 GMT  
		Size: 2.2 KB (2180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:936d6b4e0948dd9dd298b748c6cfaf2996fa68b2e48f94288c02abbed39fc35b`  
		Last Modified: Thu, 21 Jan 2021 19:25:16 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:3.7`

```console
$ docker pull arangodb@sha256:d83ecbebd6f1fa78a44023ec27db269d6ee2ffbbb9bf3e2f51d84d90864efd3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `arangodb:3.7` - linux; amd64

```console
$ docker pull arangodb@sha256:6d6875fe825a2a8807f6dcfdcb7fc64d7af14df07e2d8bc4f2e514d4412c5806
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.1 MB (128064287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab1fac400459c9e78116f1fedb05bf73f1410cebac31fbd2ad5f759c443593da`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Thu, 17 Dec 2020 00:19:49 GMT
ADD file:8ed80010e443da19d72546bcee9a35e0a8d244c72052b1994610bf5939d479c2 in / 
# Thu, 17 Dec 2020 00:19:49 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 00:53:15 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Fri, 08 Jan 2021 19:19:39 GMT
ENV ARANGO_VERSION=3.7.6
# Fri, 08 Jan 2021 19:19:39 GMT
ENV ARANGO_URL=https://download.arangodb.com/arangodb37/DEBIAN/amd64
# Fri, 08 Jan 2021 19:19:39 GMT
ENV ARANGO_PACKAGE=arangodb3_3.7.6-1_amd64.deb
# Fri, 08 Jan 2021 19:19:39 GMT
ENV ARANGO_PACKAGE_URL=https://download.arangodb.com/arangodb37/DEBIAN/amd64/arangodb3_3.7.6-1_amd64.deb
# Fri, 08 Jan 2021 19:19:40 GMT
ENV ARANGO_SIGNATURE_URL=https://download.arangodb.com/arangodb37/DEBIAN/amd64/arangodb3_3.7.6-1_amd64.deb.asc
# Fri, 08 Jan 2021 19:20:05 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli &&     apk del yarn &&     gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     echo chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     echo chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Fri, 08 Jan 2021 19:20:06 GMT
ENV GLIBCXX_FORCE_NEW=1
# Fri, 08 Jan 2021 19:20:06 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Fri, 08 Jan 2021 19:20:06 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Fri, 08 Jan 2021 19:20:06 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Fri, 08 Jan 2021 19:20:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 08 Jan 2021 19:20:07 GMT
EXPOSE 8529
# Fri, 08 Jan 2021 19:20:07 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:0a6724ff3fcd51338afdfdc2b1d4ffd04569818e31efad957213d67c29b45101`  
		Last Modified: Thu, 17 Dec 2020 00:20:26 GMT  
		Size: 2.8 MB (2814864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:112c958e641e47efc09f5254c9d8540cadff891e2d2ee30690d85f8491f0c853`  
		Last Modified: Fri, 08 Jan 2021 19:20:45 GMT  
		Size: 125.2 MB (125247078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e923434bea2919ef7d8ec0948d7f970467b624347dafcdfb6426d72495728e0c`  
		Last Modified: Fri, 08 Jan 2021 19:20:26 GMT  
		Size: 2.1 KB (2085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27ebea37802315b246b3aa12cbdf44e4cb7aaab6a900575b41c1f3e87def2adb`  
		Last Modified: Fri, 08 Jan 2021 19:20:25 GMT  
		Size: 260.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:3.7.7`

**does not exist** (yet?)

## `arangodb:latest`

```console
$ docker pull arangodb@sha256:d83ecbebd6f1fa78a44023ec27db269d6ee2ffbbb9bf3e2f51d84d90864efd3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `arangodb:latest` - linux; amd64

```console
$ docker pull arangodb@sha256:6d6875fe825a2a8807f6dcfdcb7fc64d7af14df07e2d8bc4f2e514d4412c5806
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.1 MB (128064287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab1fac400459c9e78116f1fedb05bf73f1410cebac31fbd2ad5f759c443593da`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Thu, 17 Dec 2020 00:19:49 GMT
ADD file:8ed80010e443da19d72546bcee9a35e0a8d244c72052b1994610bf5939d479c2 in / 
# Thu, 17 Dec 2020 00:19:49 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 00:53:15 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Fri, 08 Jan 2021 19:19:39 GMT
ENV ARANGO_VERSION=3.7.6
# Fri, 08 Jan 2021 19:19:39 GMT
ENV ARANGO_URL=https://download.arangodb.com/arangodb37/DEBIAN/amd64
# Fri, 08 Jan 2021 19:19:39 GMT
ENV ARANGO_PACKAGE=arangodb3_3.7.6-1_amd64.deb
# Fri, 08 Jan 2021 19:19:39 GMT
ENV ARANGO_PACKAGE_URL=https://download.arangodb.com/arangodb37/DEBIAN/amd64/arangodb3_3.7.6-1_amd64.deb
# Fri, 08 Jan 2021 19:19:40 GMT
ENV ARANGO_SIGNATURE_URL=https://download.arangodb.com/arangodb37/DEBIAN/amd64/arangodb3_3.7.6-1_amd64.deb.asc
# Fri, 08 Jan 2021 19:20:05 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli &&     apk del yarn &&     gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     echo chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     echo chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Fri, 08 Jan 2021 19:20:06 GMT
ENV GLIBCXX_FORCE_NEW=1
# Fri, 08 Jan 2021 19:20:06 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Fri, 08 Jan 2021 19:20:06 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Fri, 08 Jan 2021 19:20:06 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Fri, 08 Jan 2021 19:20:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 08 Jan 2021 19:20:07 GMT
EXPOSE 8529
# Fri, 08 Jan 2021 19:20:07 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:0a6724ff3fcd51338afdfdc2b1d4ffd04569818e31efad957213d67c29b45101`  
		Last Modified: Thu, 17 Dec 2020 00:20:26 GMT  
		Size: 2.8 MB (2814864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:112c958e641e47efc09f5254c9d8540cadff891e2d2ee30690d85f8491f0c853`  
		Last Modified: Fri, 08 Jan 2021 19:20:45 GMT  
		Size: 125.2 MB (125247078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e923434bea2919ef7d8ec0948d7f970467b624347dafcdfb6426d72495728e0c`  
		Last Modified: Fri, 08 Jan 2021 19:20:26 GMT  
		Size: 2.1 KB (2085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27ebea37802315b246b3aa12cbdf44e4cb7aaab6a900575b41c1f3e87def2adb`  
		Last Modified: Fri, 08 Jan 2021 19:20:25 GMT  
		Size: 260.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
