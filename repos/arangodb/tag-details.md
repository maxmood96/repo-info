<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `arangodb`

-	[`arangodb:3.5`](#arangodb35)
-	[`arangodb:3.5.6`](#arangodb356)
-	[`arangodb:3.6`](#arangodb36)
-	[`arangodb:3.6.9`](#arangodb369)
-	[`arangodb:3.7`](#arangodb37)
-	[`arangodb:3.7.5`](#arangodb375)
-	[`arangodb:latest`](#arangodblatest)

## `arangodb:3.5`

```console
$ docker pull arangodb@sha256:c7bd218af58eafbe39a90fa5a06fdbdd9c849b8766c292ddb005b6aad21482c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `arangodb:3.5` - linux; amd64

```console
$ docker pull arangodb@sha256:f9cfe65fa9197337f91aecae23f9ad48b354e706e5fee5596a6942dbcbd8582d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.4 MB (118432957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc3bcac35abc2dafcd9cafcb5f6c5ae908b38a6b5310043da776a78a8efc4a43`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:03 GMT
ADD file:b91adb67b670d3a6ff9463e48b7def903ed516be66fc4282d22c53e41512be49 in / 
# Fri, 24 Apr 2020 01:05:03 GMT
CMD ["/bin/sh"]
# Wed, 19 Aug 2020 19:19:32 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Thu, 17 Sep 2020 23:19:32 GMT
ENV ARANGO_VERSION=3.5.6
# Thu, 17 Sep 2020 23:19:32 GMT
ENV ARANGO_URL=https://download.arangodb.com/arangodb35/DEBIAN/amd64
# Thu, 17 Sep 2020 23:19:33 GMT
ENV ARANGO_PACKAGE=arangodb3_3.5.6-1_amd64.deb
# Thu, 17 Sep 2020 23:19:33 GMT
ENV ARANGO_PACKAGE_URL=https://download.arangodb.com/arangodb35/DEBIAN/amd64/arangodb3_3.5.6-1_amd64.deb
# Thu, 17 Sep 2020 23:19:33 GMT
ENV ARANGO_SIGNATURE_URL=https://download.arangodb.com/arangodb35/DEBIAN/amd64/arangodb3_3.5.6-1_amd64.deb.asc
# Thu, 17 Sep 2020 23:19:58 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli &&     apk del yarn &&     gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     echo chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     echo chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Thu, 17 Sep 2020 23:19:58 GMT
ENV GLIBCXX_FORCE_NEW=1
# Thu, 17 Sep 2020 23:19:59 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Thu, 17 Sep 2020 23:19:59 GMT
COPY file:3a0ad717437ce87e5e260280982f3288fcfff74b46a1f17e5cd07f64d64ee5fa in /entrypoint.sh 
# Thu, 17 Sep 2020 23:19:59 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Thu, 17 Sep 2020 23:19:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 17 Sep 2020 23:19:59 GMT
EXPOSE 8529
# Thu, 17 Sep 2020 23:19:59 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:cbdbe7a5bc2a134ca8ec91be58565ec07d037386d1f1d8385412d224deafca08`  
		Last Modified: Thu, 23 Apr 2020 14:07:19 GMT  
		Size: 2.8 MB (2813316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46406dd87dce45c1a5ce89d8ec5b6ec65734299f35ac4a2155b3b6610a995d3b`  
		Last Modified: Thu, 17 Sep 2020 23:20:38 GMT  
		Size: 115.6 MB (115617201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98a934e98a23370bdbabba4d1b7ca9b8b2e2d3818082104eefd658de059d3fa6`  
		Last Modified: Thu, 17 Sep 2020 23:20:18 GMT  
		Size: 2.2 KB (2180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a2632cf46e5d3d52c1c1ea4409b815cb1a5b22b5aa404d6eee090be27f48af6`  
		Last Modified: Thu, 17 Sep 2020 23:20:19 GMT  
		Size: 260.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:3.5.6`

```console
$ docker pull arangodb@sha256:c7bd218af58eafbe39a90fa5a06fdbdd9c849b8766c292ddb005b6aad21482c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `arangodb:3.5.6` - linux; amd64

```console
$ docker pull arangodb@sha256:f9cfe65fa9197337f91aecae23f9ad48b354e706e5fee5596a6942dbcbd8582d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.4 MB (118432957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc3bcac35abc2dafcd9cafcb5f6c5ae908b38a6b5310043da776a78a8efc4a43`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:03 GMT
ADD file:b91adb67b670d3a6ff9463e48b7def903ed516be66fc4282d22c53e41512be49 in / 
# Fri, 24 Apr 2020 01:05:03 GMT
CMD ["/bin/sh"]
# Wed, 19 Aug 2020 19:19:32 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Thu, 17 Sep 2020 23:19:32 GMT
ENV ARANGO_VERSION=3.5.6
# Thu, 17 Sep 2020 23:19:32 GMT
ENV ARANGO_URL=https://download.arangodb.com/arangodb35/DEBIAN/amd64
# Thu, 17 Sep 2020 23:19:33 GMT
ENV ARANGO_PACKAGE=arangodb3_3.5.6-1_amd64.deb
# Thu, 17 Sep 2020 23:19:33 GMT
ENV ARANGO_PACKAGE_URL=https://download.arangodb.com/arangodb35/DEBIAN/amd64/arangodb3_3.5.6-1_amd64.deb
# Thu, 17 Sep 2020 23:19:33 GMT
ENV ARANGO_SIGNATURE_URL=https://download.arangodb.com/arangodb35/DEBIAN/amd64/arangodb3_3.5.6-1_amd64.deb.asc
# Thu, 17 Sep 2020 23:19:58 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli &&     apk del yarn &&     gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     echo chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     echo chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Thu, 17 Sep 2020 23:19:58 GMT
ENV GLIBCXX_FORCE_NEW=1
# Thu, 17 Sep 2020 23:19:59 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Thu, 17 Sep 2020 23:19:59 GMT
COPY file:3a0ad717437ce87e5e260280982f3288fcfff74b46a1f17e5cd07f64d64ee5fa in /entrypoint.sh 
# Thu, 17 Sep 2020 23:19:59 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Thu, 17 Sep 2020 23:19:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 17 Sep 2020 23:19:59 GMT
EXPOSE 8529
# Thu, 17 Sep 2020 23:19:59 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:cbdbe7a5bc2a134ca8ec91be58565ec07d037386d1f1d8385412d224deafca08`  
		Last Modified: Thu, 23 Apr 2020 14:07:19 GMT  
		Size: 2.8 MB (2813316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46406dd87dce45c1a5ce89d8ec5b6ec65734299f35ac4a2155b3b6610a995d3b`  
		Last Modified: Thu, 17 Sep 2020 23:20:38 GMT  
		Size: 115.6 MB (115617201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98a934e98a23370bdbabba4d1b7ca9b8b2e2d3818082104eefd658de059d3fa6`  
		Last Modified: Thu, 17 Sep 2020 23:20:18 GMT  
		Size: 2.2 KB (2180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a2632cf46e5d3d52c1c1ea4409b815cb1a5b22b5aa404d6eee090be27f48af6`  
		Last Modified: Thu, 17 Sep 2020 23:20:19 GMT  
		Size: 260.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:3.6`

```console
$ docker pull arangodb@sha256:ba98084773491efddf75ed66e3970116d604cc172c70ec0d08c6ec13d4c651d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `arangodb:3.6` - linux; amd64

```console
$ docker pull arangodb@sha256:82d06236c3ba4d5bddc51edbbfe041f189bc9f37aa1b34b76f5cbc8be28e46e8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.2 MB (119238394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48f18c315c097906a97a3eedb3c983b3c38e0571e6ae8df67894d24625dcb468`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:03 GMT
ADD file:b91adb67b670d3a6ff9463e48b7def903ed516be66fc4282d22c53e41512be49 in / 
# Fri, 24 Apr 2020 01:05:03 GMT
CMD ["/bin/sh"]
# Wed, 19 Aug 2020 19:19:32 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Wed, 11 Nov 2020 01:19:35 GMT
ENV ARANGO_VERSION=3.6.9
# Wed, 11 Nov 2020 01:19:36 GMT
ENV ARANGO_URL=https://download.arangodb.com/arangodb36/DEBIAN/amd64
# Wed, 11 Nov 2020 01:19:36 GMT
ENV ARANGO_PACKAGE=arangodb3_3.6.9-1_amd64.deb
# Wed, 11 Nov 2020 01:19:36 GMT
ENV ARANGO_PACKAGE_URL=https://download.arangodb.com/arangodb36/DEBIAN/amd64/arangodb3_3.6.9-1_amd64.deb
# Wed, 11 Nov 2020 01:19:36 GMT
ENV ARANGO_SIGNATURE_URL=https://download.arangodb.com/arangodb36/DEBIAN/amd64/arangodb3_3.6.9-1_amd64.deb.asc
# Wed, 11 Nov 2020 01:20:05 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli &&     apk del yarn &&     gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     echo chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     echo chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Wed, 11 Nov 2020 01:20:06 GMT
ENV GLIBCXX_FORCE_NEW=1
# Wed, 11 Nov 2020 01:20:06 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Wed, 11 Nov 2020 01:20:06 GMT
COPY file:3a0ad717437ce87e5e260280982f3288fcfff74b46a1f17e5cd07f64d64ee5fa in /entrypoint.sh 
# Wed, 11 Nov 2020 01:20:07 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Wed, 11 Nov 2020 01:20:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Nov 2020 01:20:07 GMT
EXPOSE 8529
# Wed, 11 Nov 2020 01:20:07 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:cbdbe7a5bc2a134ca8ec91be58565ec07d037386d1f1d8385412d224deafca08`  
		Last Modified: Thu, 23 Apr 2020 14:07:19 GMT  
		Size: 2.8 MB (2813316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3713826c6d50c72c70843c00a89603e80c536c02f65187ef34b57998a77ad96b`  
		Last Modified: Wed, 11 Nov 2020 01:20:46 GMT  
		Size: 116.4 MB (116422637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd0f9c7e98c9231345d6c167f93671f21882469d3b19d3cb8f7a7cd173df8ff2`  
		Last Modified: Wed, 11 Nov 2020 01:20:26 GMT  
		Size: 2.2 KB (2180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d57bf8c49f556a688d6aad1781a3e058a7f88bb222b4e1886a95a42ec76a288a`  
		Last Modified: Wed, 11 Nov 2020 01:20:26 GMT  
		Size: 261.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:3.6.9`

```console
$ docker pull arangodb@sha256:ba98084773491efddf75ed66e3970116d604cc172c70ec0d08c6ec13d4c651d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `arangodb:3.6.9` - linux; amd64

```console
$ docker pull arangodb@sha256:82d06236c3ba4d5bddc51edbbfe041f189bc9f37aa1b34b76f5cbc8be28e46e8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.2 MB (119238394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48f18c315c097906a97a3eedb3c983b3c38e0571e6ae8df67894d24625dcb468`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:03 GMT
ADD file:b91adb67b670d3a6ff9463e48b7def903ed516be66fc4282d22c53e41512be49 in / 
# Fri, 24 Apr 2020 01:05:03 GMT
CMD ["/bin/sh"]
# Wed, 19 Aug 2020 19:19:32 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Wed, 11 Nov 2020 01:19:35 GMT
ENV ARANGO_VERSION=3.6.9
# Wed, 11 Nov 2020 01:19:36 GMT
ENV ARANGO_URL=https://download.arangodb.com/arangodb36/DEBIAN/amd64
# Wed, 11 Nov 2020 01:19:36 GMT
ENV ARANGO_PACKAGE=arangodb3_3.6.9-1_amd64.deb
# Wed, 11 Nov 2020 01:19:36 GMT
ENV ARANGO_PACKAGE_URL=https://download.arangodb.com/arangodb36/DEBIAN/amd64/arangodb3_3.6.9-1_amd64.deb
# Wed, 11 Nov 2020 01:19:36 GMT
ENV ARANGO_SIGNATURE_URL=https://download.arangodb.com/arangodb36/DEBIAN/amd64/arangodb3_3.6.9-1_amd64.deb.asc
# Wed, 11 Nov 2020 01:20:05 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli &&     apk del yarn &&     gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     echo chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     echo chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Wed, 11 Nov 2020 01:20:06 GMT
ENV GLIBCXX_FORCE_NEW=1
# Wed, 11 Nov 2020 01:20:06 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Wed, 11 Nov 2020 01:20:06 GMT
COPY file:3a0ad717437ce87e5e260280982f3288fcfff74b46a1f17e5cd07f64d64ee5fa in /entrypoint.sh 
# Wed, 11 Nov 2020 01:20:07 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Wed, 11 Nov 2020 01:20:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Nov 2020 01:20:07 GMT
EXPOSE 8529
# Wed, 11 Nov 2020 01:20:07 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:cbdbe7a5bc2a134ca8ec91be58565ec07d037386d1f1d8385412d224deafca08`  
		Last Modified: Thu, 23 Apr 2020 14:07:19 GMT  
		Size: 2.8 MB (2813316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3713826c6d50c72c70843c00a89603e80c536c02f65187ef34b57998a77ad96b`  
		Last Modified: Wed, 11 Nov 2020 01:20:46 GMT  
		Size: 116.4 MB (116422637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd0f9c7e98c9231345d6c167f93671f21882469d3b19d3cb8f7a7cd173df8ff2`  
		Last Modified: Wed, 11 Nov 2020 01:20:26 GMT  
		Size: 2.2 KB (2180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d57bf8c49f556a688d6aad1781a3e058a7f88bb222b4e1886a95a42ec76a288a`  
		Last Modified: Wed, 11 Nov 2020 01:20:26 GMT  
		Size: 261.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:3.7`

```console
$ docker pull arangodb@sha256:e8173f33ebb2048b29685dfb5b5a2397cf65353a4a1b98ebb6414d104eb2f4e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `arangodb:3.7` - linux; amd64

```console
$ docker pull arangodb@sha256:e6d27abfe67cf286234f01fc29ec22a5025cfc3729e8989c302c9df1471e46b1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.0 MB (127978306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddf07df96ced3f4891a9a31fb4c55cd994d366b6a60b157a4f4d2c49badac01d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:03 GMT
ADD file:b91adb67b670d3a6ff9463e48b7def903ed516be66fc4282d22c53e41512be49 in / 
# Fri, 24 Apr 2020 01:05:03 GMT
CMD ["/bin/sh"]
# Wed, 19 Aug 2020 19:19:32 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Tue, 20 Oct 2020 23:48:43 GMT
ENV ARANGO_VERSION=3.7.3
# Tue, 20 Oct 2020 23:48:43 GMT
ENV ARANGO_URL=https://download.arangodb.com/arangodb37/DEBIAN/amd64
# Tue, 20 Oct 2020 23:48:43 GMT
ENV ARANGO_PACKAGE=arangodb3_3.7.3-1_amd64.deb
# Tue, 20 Oct 2020 23:48:44 GMT
ENV ARANGO_PACKAGE_URL=https://download.arangodb.com/arangodb37/DEBIAN/amd64/arangodb3_3.7.3-1_amd64.deb
# Tue, 20 Oct 2020 23:48:44 GMT
ENV ARANGO_SIGNATURE_URL=https://download.arangodb.com/arangodb37/DEBIAN/amd64/arangodb3_3.7.3-1_amd64.deb.asc
# Tue, 20 Oct 2020 23:49:14 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli &&     apk del yarn &&     gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     echo chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     echo chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Tue, 20 Oct 2020 23:49:15 GMT
ENV GLIBCXX_FORCE_NEW=1
# Tue, 20 Oct 2020 23:49:15 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Tue, 20 Oct 2020 23:49:16 GMT
COPY file:3a0ad717437ce87e5e260280982f3288fcfff74b46a1f17e5cd07f64d64ee5fa in /entrypoint.sh 
# Tue, 20 Oct 2020 23:49:16 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Tue, 20 Oct 2020 23:49:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 20 Oct 2020 23:49:16 GMT
EXPOSE 8529
# Tue, 20 Oct 2020 23:49:16 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:cbdbe7a5bc2a134ca8ec91be58565ec07d037386d1f1d8385412d224deafca08`  
		Last Modified: Thu, 23 Apr 2020 14:07:19 GMT  
		Size: 2.8 MB (2813316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6165cae7ad6a92a606da0d90b4b97a72050a95da21aefc46ac1fe6120158d24`  
		Last Modified: Tue, 20 Oct 2020 23:49:50 GMT  
		Size: 125.2 MB (125162549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21d9e77c864eb446107fc9ee3aadcea6de1e7a35d670ff1c8f61331ae34bbd0c`  
		Last Modified: Tue, 20 Oct 2020 23:49:28 GMT  
		Size: 2.2 KB (2181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b92f35f1d36f6de1a70ffcdedc2190f5178ea461ec3743a65a3f7de05d96c3b6`  
		Last Modified: Tue, 20 Oct 2020 23:49:28 GMT  
		Size: 260.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:3.7.5`

**does not exist** (yet?)

## `arangodb:latest`

```console
$ docker pull arangodb@sha256:e8173f33ebb2048b29685dfb5b5a2397cf65353a4a1b98ebb6414d104eb2f4e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `arangodb:latest` - linux; amd64

```console
$ docker pull arangodb@sha256:e6d27abfe67cf286234f01fc29ec22a5025cfc3729e8989c302c9df1471e46b1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.0 MB (127978306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddf07df96ced3f4891a9a31fb4c55cd994d366b6a60b157a4f4d2c49badac01d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:03 GMT
ADD file:b91adb67b670d3a6ff9463e48b7def903ed516be66fc4282d22c53e41512be49 in / 
# Fri, 24 Apr 2020 01:05:03 GMT
CMD ["/bin/sh"]
# Wed, 19 Aug 2020 19:19:32 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Tue, 20 Oct 2020 23:48:43 GMT
ENV ARANGO_VERSION=3.7.3
# Tue, 20 Oct 2020 23:48:43 GMT
ENV ARANGO_URL=https://download.arangodb.com/arangodb37/DEBIAN/amd64
# Tue, 20 Oct 2020 23:48:43 GMT
ENV ARANGO_PACKAGE=arangodb3_3.7.3-1_amd64.deb
# Tue, 20 Oct 2020 23:48:44 GMT
ENV ARANGO_PACKAGE_URL=https://download.arangodb.com/arangodb37/DEBIAN/amd64/arangodb3_3.7.3-1_amd64.deb
# Tue, 20 Oct 2020 23:48:44 GMT
ENV ARANGO_SIGNATURE_URL=https://download.arangodb.com/arangodb37/DEBIAN/amd64/arangodb3_3.7.3-1_amd64.deb.asc
# Tue, 20 Oct 2020 23:49:14 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli &&     apk del yarn &&     gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     echo chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     echo chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Tue, 20 Oct 2020 23:49:15 GMT
ENV GLIBCXX_FORCE_NEW=1
# Tue, 20 Oct 2020 23:49:15 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Tue, 20 Oct 2020 23:49:16 GMT
COPY file:3a0ad717437ce87e5e260280982f3288fcfff74b46a1f17e5cd07f64d64ee5fa in /entrypoint.sh 
# Tue, 20 Oct 2020 23:49:16 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Tue, 20 Oct 2020 23:49:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 20 Oct 2020 23:49:16 GMT
EXPOSE 8529
# Tue, 20 Oct 2020 23:49:16 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:cbdbe7a5bc2a134ca8ec91be58565ec07d037386d1f1d8385412d224deafca08`  
		Last Modified: Thu, 23 Apr 2020 14:07:19 GMT  
		Size: 2.8 MB (2813316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6165cae7ad6a92a606da0d90b4b97a72050a95da21aefc46ac1fe6120158d24`  
		Last Modified: Tue, 20 Oct 2020 23:49:50 GMT  
		Size: 125.2 MB (125162549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21d9e77c864eb446107fc9ee3aadcea6de1e7a35d670ff1c8f61331ae34bbd0c`  
		Last Modified: Tue, 20 Oct 2020 23:49:28 GMT  
		Size: 2.2 KB (2181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b92f35f1d36f6de1a70ffcdedc2190f5178ea461ec3743a65a3f7de05d96c3b6`  
		Last Modified: Tue, 20 Oct 2020 23:49:28 GMT  
		Size: 260.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
