<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `arangodb`

-	[`arangodb:3.5`](#arangodb35)
-	[`arangodb:3.5.6`](#arangodb356)
-	[`arangodb:3.6`](#arangodb36)
-	[`arangodb:3.6.7`](#arangodb367)
-	[`arangodb:3.7`](#arangodb37)
-	[`arangodb:3.7.2`](#arangodb372)
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
$ docker pull arangodb@sha256:98107d2b59707c6b56bdf8c7b1b0291f770ab745d3a75cab9f9ddbe1838f5374
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `arangodb:3.6` - linux; amd64

```console
$ docker pull arangodb@sha256:f267529388835f061f62a517f2071160156ae262d5d6ef18ea9432a3ccbc8d12
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.6 MB (118601261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:343365b334734804f9f9a7b8c54654351d915b5ea321190ac3f523f81c4038a4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:03 GMT
ADD file:b91adb67b670d3a6ff9463e48b7def903ed516be66fc4282d22c53e41512be49 in / 
# Fri, 24 Apr 2020 01:05:03 GMT
CMD ["/bin/sh"]
# Wed, 19 Aug 2020 19:19:32 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Wed, 16 Sep 2020 22:48:42 GMT
ENV ARANGO_VERSION=3.6.6
# Wed, 16 Sep 2020 22:48:42 GMT
ENV ARANGO_URL=https://download.arangodb.com/arangodb36/DEBIAN/amd64
# Wed, 16 Sep 2020 22:48:42 GMT
ENV ARANGO_PACKAGE=arangodb3_3.6.6-1_amd64.deb
# Wed, 16 Sep 2020 22:48:42 GMT
ENV ARANGO_PACKAGE_URL=https://download.arangodb.com/arangodb36/DEBIAN/amd64/arangodb3_3.6.6-1_amd64.deb
# Wed, 16 Sep 2020 22:48:42 GMT
ENV ARANGO_SIGNATURE_URL=https://download.arangodb.com/arangodb36/DEBIAN/amd64/arangodb3_3.6.6-1_amd64.deb.asc
# Wed, 16 Sep 2020 22:49:06 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli &&     apk del yarn &&     gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     echo chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     echo chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Wed, 16 Sep 2020 22:49:07 GMT
ENV GLIBCXX_FORCE_NEW=1
# Wed, 16 Sep 2020 22:49:07 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Wed, 16 Sep 2020 22:49:07 GMT
COPY file:3a0ad717437ce87e5e260280982f3288fcfff74b46a1f17e5cd07f64d64ee5fa in /entrypoint.sh 
# Wed, 16 Sep 2020 22:49:08 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Wed, 16 Sep 2020 22:49:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 16 Sep 2020 22:49:08 GMT
EXPOSE 8529
# Wed, 16 Sep 2020 22:49:08 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:cbdbe7a5bc2a134ca8ec91be58565ec07d037386d1f1d8385412d224deafca08`  
		Last Modified: Thu, 23 Apr 2020 14:07:19 GMT  
		Size: 2.8 MB (2813316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11f3515a41cc8aa1e712f93110aea4529796089ef59ec2208fb82722870d27c1`  
		Last Modified: Wed, 16 Sep 2020 22:50:14 GMT  
		Size: 115.8 MB (115785505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b409c5653962f1d0e2f2258f22e1642bd157ac5eb4b149c6fa2fc6201d01483`  
		Last Modified: Wed, 16 Sep 2020 22:49:54 GMT  
		Size: 2.2 KB (2179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57bbd486f1931d85b38406198eaa157c6346dc1ffdb6717ba1ebefe87d4b17a2`  
		Last Modified: Wed, 16 Sep 2020 22:49:54 GMT  
		Size: 261.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:3.6.7`

```console
$ docker pull arangodb@sha256:a8409dff6597f2ef5f7ecd3c672671bb2af9a390073efd74f95c54aa41cba22a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:

## `arangodb:3.7`

```console
$ docker pull arangodb@sha256:8c140e0c22c03f116de84aa543dd05936a73564f667490f4fad459f4e352b82e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `arangodb:3.7` - linux; amd64

```console
$ docker pull arangodb@sha256:2e2c38b14744c92e6c8a19ce959809654dc7c5f72a98b24417c2a4c9cf889ec9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.2 MB (127226791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0770011bfdb7b6b64e9589a4b4ea206a68295a1361b35f36f20703be422e350b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:03 GMT
ADD file:b91adb67b670d3a6ff9463e48b7def903ed516be66fc4282d22c53e41512be49 in / 
# Fri, 24 Apr 2020 01:05:03 GMT
CMD ["/bin/sh"]
# Wed, 19 Aug 2020 19:19:32 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Wed, 16 Sep 2020 22:49:16 GMT
ENV ARANGO_VERSION=3.7.2.1
# Wed, 16 Sep 2020 22:49:16 GMT
ENV ARANGO_URL=https://download.arangodb.com/arangodb37/DEBIAN/amd64
# Wed, 16 Sep 2020 22:49:16 GMT
ENV ARANGO_PACKAGE=arangodb3_3.7.2.1-1_amd64.deb
# Wed, 16 Sep 2020 22:49:16 GMT
ENV ARANGO_PACKAGE_URL=https://download.arangodb.com/arangodb37/DEBIAN/amd64/arangodb3_3.7.2.1-1_amd64.deb
# Wed, 16 Sep 2020 22:49:16 GMT
ENV ARANGO_SIGNATURE_URL=https://download.arangodb.com/arangodb37/DEBIAN/amd64/arangodb3_3.7.2.1-1_amd64.deb.asc
# Wed, 16 Sep 2020 22:49:41 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli &&     apk del yarn &&     gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     echo chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     echo chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Wed, 16 Sep 2020 22:49:42 GMT
ENV GLIBCXX_FORCE_NEW=1
# Wed, 16 Sep 2020 22:49:42 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Wed, 16 Sep 2020 22:49:42 GMT
COPY file:3a0ad717437ce87e5e260280982f3288fcfff74b46a1f17e5cd07f64d64ee5fa in /entrypoint.sh 
# Wed, 16 Sep 2020 22:49:43 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Wed, 16 Sep 2020 22:49:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 16 Sep 2020 22:49:43 GMT
EXPOSE 8529
# Wed, 16 Sep 2020 22:49:43 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:cbdbe7a5bc2a134ca8ec91be58565ec07d037386d1f1d8385412d224deafca08`  
		Last Modified: Thu, 23 Apr 2020 14:07:19 GMT  
		Size: 2.8 MB (2813316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d71e2f18c9e19054c4c5974135cb1c50b7f84700b4a2d99152f81c248336e10`  
		Last Modified: Wed, 16 Sep 2020 22:50:41 GMT  
		Size: 124.4 MB (124411036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a38b86a9b99e36c7de443597112528ddd748c44a4205ab2f173333d42fd7f7fd`  
		Last Modified: Wed, 16 Sep 2020 22:50:19 GMT  
		Size: 2.2 KB (2179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ef4ccba8a06a65a348dae95f4f6cf7b24d3e39ebc79510003c04c9d683b2766`  
		Last Modified: Wed, 16 Sep 2020 22:50:19 GMT  
		Size: 260.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:3.7.2`

```console
$ docker pull arangodb@sha256:8c140e0c22c03f116de84aa543dd05936a73564f667490f4fad459f4e352b82e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `arangodb:3.7.2` - linux; amd64

```console
$ docker pull arangodb@sha256:2e2c38b14744c92e6c8a19ce959809654dc7c5f72a98b24417c2a4c9cf889ec9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.2 MB (127226791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0770011bfdb7b6b64e9589a4b4ea206a68295a1361b35f36f20703be422e350b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:03 GMT
ADD file:b91adb67b670d3a6ff9463e48b7def903ed516be66fc4282d22c53e41512be49 in / 
# Fri, 24 Apr 2020 01:05:03 GMT
CMD ["/bin/sh"]
# Wed, 19 Aug 2020 19:19:32 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Wed, 16 Sep 2020 22:49:16 GMT
ENV ARANGO_VERSION=3.7.2.1
# Wed, 16 Sep 2020 22:49:16 GMT
ENV ARANGO_URL=https://download.arangodb.com/arangodb37/DEBIAN/amd64
# Wed, 16 Sep 2020 22:49:16 GMT
ENV ARANGO_PACKAGE=arangodb3_3.7.2.1-1_amd64.deb
# Wed, 16 Sep 2020 22:49:16 GMT
ENV ARANGO_PACKAGE_URL=https://download.arangodb.com/arangodb37/DEBIAN/amd64/arangodb3_3.7.2.1-1_amd64.deb
# Wed, 16 Sep 2020 22:49:16 GMT
ENV ARANGO_SIGNATURE_URL=https://download.arangodb.com/arangodb37/DEBIAN/amd64/arangodb3_3.7.2.1-1_amd64.deb.asc
# Wed, 16 Sep 2020 22:49:41 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli &&     apk del yarn &&     gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     echo chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     echo chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Wed, 16 Sep 2020 22:49:42 GMT
ENV GLIBCXX_FORCE_NEW=1
# Wed, 16 Sep 2020 22:49:42 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Wed, 16 Sep 2020 22:49:42 GMT
COPY file:3a0ad717437ce87e5e260280982f3288fcfff74b46a1f17e5cd07f64d64ee5fa in /entrypoint.sh 
# Wed, 16 Sep 2020 22:49:43 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Wed, 16 Sep 2020 22:49:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 16 Sep 2020 22:49:43 GMT
EXPOSE 8529
# Wed, 16 Sep 2020 22:49:43 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:cbdbe7a5bc2a134ca8ec91be58565ec07d037386d1f1d8385412d224deafca08`  
		Last Modified: Thu, 23 Apr 2020 14:07:19 GMT  
		Size: 2.8 MB (2813316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d71e2f18c9e19054c4c5974135cb1c50b7f84700b4a2d99152f81c248336e10`  
		Last Modified: Wed, 16 Sep 2020 22:50:41 GMT  
		Size: 124.4 MB (124411036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a38b86a9b99e36c7de443597112528ddd748c44a4205ab2f173333d42fd7f7fd`  
		Last Modified: Wed, 16 Sep 2020 22:50:19 GMT  
		Size: 2.2 KB (2179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ef4ccba8a06a65a348dae95f4f6cf7b24d3e39ebc79510003c04c9d683b2766`  
		Last Modified: Wed, 16 Sep 2020 22:50:19 GMT  
		Size: 260.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:latest`

```console
$ docker pull arangodb@sha256:8c140e0c22c03f116de84aa543dd05936a73564f667490f4fad459f4e352b82e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `arangodb:latest` - linux; amd64

```console
$ docker pull arangodb@sha256:2e2c38b14744c92e6c8a19ce959809654dc7c5f72a98b24417c2a4c9cf889ec9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.2 MB (127226791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0770011bfdb7b6b64e9589a4b4ea206a68295a1361b35f36f20703be422e350b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:03 GMT
ADD file:b91adb67b670d3a6ff9463e48b7def903ed516be66fc4282d22c53e41512be49 in / 
# Fri, 24 Apr 2020 01:05:03 GMT
CMD ["/bin/sh"]
# Wed, 19 Aug 2020 19:19:32 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Wed, 16 Sep 2020 22:49:16 GMT
ENV ARANGO_VERSION=3.7.2.1
# Wed, 16 Sep 2020 22:49:16 GMT
ENV ARANGO_URL=https://download.arangodb.com/arangodb37/DEBIAN/amd64
# Wed, 16 Sep 2020 22:49:16 GMT
ENV ARANGO_PACKAGE=arangodb3_3.7.2.1-1_amd64.deb
# Wed, 16 Sep 2020 22:49:16 GMT
ENV ARANGO_PACKAGE_URL=https://download.arangodb.com/arangodb37/DEBIAN/amd64/arangodb3_3.7.2.1-1_amd64.deb
# Wed, 16 Sep 2020 22:49:16 GMT
ENV ARANGO_SIGNATURE_URL=https://download.arangodb.com/arangodb37/DEBIAN/amd64/arangodb3_3.7.2.1-1_amd64.deb.asc
# Wed, 16 Sep 2020 22:49:41 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli &&     apk del yarn &&     gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     echo chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     echo chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Wed, 16 Sep 2020 22:49:42 GMT
ENV GLIBCXX_FORCE_NEW=1
# Wed, 16 Sep 2020 22:49:42 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Wed, 16 Sep 2020 22:49:42 GMT
COPY file:3a0ad717437ce87e5e260280982f3288fcfff74b46a1f17e5cd07f64d64ee5fa in /entrypoint.sh 
# Wed, 16 Sep 2020 22:49:43 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Wed, 16 Sep 2020 22:49:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 16 Sep 2020 22:49:43 GMT
EXPOSE 8529
# Wed, 16 Sep 2020 22:49:43 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:cbdbe7a5bc2a134ca8ec91be58565ec07d037386d1f1d8385412d224deafca08`  
		Last Modified: Thu, 23 Apr 2020 14:07:19 GMT  
		Size: 2.8 MB (2813316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d71e2f18c9e19054c4c5974135cb1c50b7f84700b4a2d99152f81c248336e10`  
		Last Modified: Wed, 16 Sep 2020 22:50:41 GMT  
		Size: 124.4 MB (124411036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a38b86a9b99e36c7de443597112528ddd748c44a4205ab2f173333d42fd7f7fd`  
		Last Modified: Wed, 16 Sep 2020 22:50:19 GMT  
		Size: 2.2 KB (2179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ef4ccba8a06a65a348dae95f4f6cf7b24d3e39ebc79510003c04c9d683b2766`  
		Last Modified: Wed, 16 Sep 2020 22:50:19 GMT  
		Size: 260.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
