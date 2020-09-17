<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `arangodb`

-	[`arangodb:3.5`](#arangodb35)
-	[`arangodb:3.5.6`](#arangodb356)
-	[`arangodb:3.6`](#arangodb36)
-	[`arangodb:3.6.6`](#arangodb366)
-	[`arangodb:3.7`](#arangodb37)
-	[`arangodb:3.7.2`](#arangodb372)
-	[`arangodb:latest`](#arangodblatest)

## `arangodb:3.5`

```console
$ docker pull arangodb@sha256:43598bf9d7fb0ed26ed05882ef15c0bb9066a1ebf6e73c2ca0d475246d3020f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `arangodb:3.5` - linux; amd64

```console
$ docker pull arangodb@sha256:3a0a9fe72cf6d11a8b3826939a267e03da552ed5547b9a1cc763c8c901ffb232
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.3 MB (117286153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ace622ab4890ec354c4a0c5432f40eee6a4df85e163e734d2b54acdc3ab6abf1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:03 GMT
ADD file:b91adb67b670d3a6ff9463e48b7def903ed516be66fc4282d22c53e41512be49 in / 
# Fri, 24 Apr 2020 01:05:03 GMT
CMD ["/bin/sh"]
# Wed, 19 Aug 2020 19:19:32 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Wed, 19 Aug 2020 19:19:32 GMT
ENV ARANGO_VERSION=3.5.5.1
# Wed, 19 Aug 2020 19:19:32 GMT
ENV ARANGO_URL=https://download.arangodb.com/arangodb35/DEBIAN/amd64
# Wed, 19 Aug 2020 19:19:33 GMT
ENV ARANGO_PACKAGE=arangodb3_3.5.5.1-1_amd64.deb
# Wed, 19 Aug 2020 19:19:33 GMT
ENV ARANGO_PACKAGE_URL=https://download.arangodb.com/arangodb35/DEBIAN/amd64/arangodb3_3.5.5.1-1_amd64.deb
# Wed, 19 Aug 2020 19:19:33 GMT
ENV ARANGO_SIGNATURE_URL=https://download.arangodb.com/arangodb35/DEBIAN/amd64/arangodb3_3.5.5.1-1_amd64.deb.asc
# Wed, 19 Aug 2020 19:19:59 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli &&     apk del yarn &&     gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     echo chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     echo chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Wed, 19 Aug 2020 19:20:00 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Wed, 19 Aug 2020 19:20:00 GMT
COPY file:912d8c5e20cd837dbed0bf2608b1376ffffdd2d6de3e5b0af4cc869508443235 in /entrypoint.sh 
# Wed, 19 Aug 2020 19:20:00 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Wed, 19 Aug 2020 19:20:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 19 Aug 2020 19:20:00 GMT
EXPOSE 8529
# Wed, 19 Aug 2020 19:20:00 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:cbdbe7a5bc2a134ca8ec91be58565ec07d037386d1f1d8385412d224deafca08`  
		Last Modified: Thu, 23 Apr 2020 14:07:19 GMT  
		Size: 2.8 MB (2813316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72fd54a8bb06916d1e3db5627b265f40c929f60159429518bb69346821f547e0`  
		Last Modified: Wed, 19 Aug 2020 19:21:34 GMT  
		Size: 114.5 MB (114470371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:018a4718e5dacc3fc6c4e7d0e6d329aa108e094db6196c00c45a1e502fc711c2`  
		Last Modified: Wed, 19 Aug 2020 19:21:14 GMT  
		Size: 2.2 KB (2205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9829441de346bad79496a3b52bab3c4e72299ba57f8ffdc7c04095958dfe3780`  
		Last Modified: Wed, 19 Aug 2020 19:21:14 GMT  
		Size: 261.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:3.5.6`

**does not exist** (yet?)

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

## `arangodb:3.6.6`

```console
$ docker pull arangodb@sha256:98107d2b59707c6b56bdf8c7b1b0291f770ab745d3a75cab9f9ddbe1838f5374
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `arangodb:3.6.6` - linux; amd64

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
