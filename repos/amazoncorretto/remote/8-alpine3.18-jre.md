## `amazoncorretto:8-alpine3.18-jre`

```console
$ docker pull amazoncorretto@sha256:aa5c92e8590f864e1f5fff1793572c4b7117e1b70c56324f239cfef226ac5742
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-alpine3.18-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:c215e4d588c1e4ccf3967c176bd2e09ac57b00e228cfe352c20fedc5a4d71f15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.1 MB (45080989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6a85fb448b425d8ed878bb6adea6fbb56c87c2118fb4b52c2cdceb23b7e7e90`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:03:06 GMT
ADD alpine-minirootfs-3.18.12-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:03:06 GMT
CMD ["/bin/sh"]
# Tue, 15 Apr 2025 21:50:45 GMT
ARG version=8.452.09.1
# Tue, 15 Apr 2025 21:50:45 GMT
# ARGS: version=8.452.09.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
ENV LANG=C.UTF-8
# Tue, 15 Apr 2025 21:50:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:44cf07d57ee4424189f012074a59110ee2065adfdde9c7d9826bebdffce0a885`  
		Last Modified: Fri, 14 Feb 2025 14:36:09 GMT  
		Size: 3.4 MB (3418409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcd2e5823c287a5acc28400a455f7653e11e6e505ab59dd3be29a939c6d8f94e`  
		Last Modified: Tue, 15 Apr 2025 23:55:26 GMT  
		Size: 41.7 MB (41662580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.18-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:8a70b545889306c3d8d40e2482e84a20a86860b1fb90a9bea4f601e43399b29c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.4 KB (193371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d22c9987e412a257191f19acb02f415e43857a6455f6ddbeaf2ebe1337b4d2c4`

```dockerfile
```

-	Layers:
	-	`sha256:a17bdefe34b81fffbca53632df9eccc2bc4716f3cdc1d54905cbe42c51c4bd0f`  
		Last Modified: Tue, 15 Apr 2025 23:55:25 GMT  
		Size: 184.7 KB (184672 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6dbe487ed03eb1cb4dcbfece43a1d79b9592dfa119af345ac1ff8a41c41b6f48`  
		Last Modified: Tue, 15 Apr 2025 23:55:25 GMT  
		Size: 8.7 KB (8699 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-alpine3.18-jre` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:178a1cfeaba78e7d67d349e8a843b57285d5c8fb8f560c5ee85259a0e9ce0c7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.7 MB (44708594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d16125148d0330c38f9a8c841ec54fc56e6a622ff8372de544f145f04246515`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:03:06 GMT
ADD alpine-minirootfs-3.18.12-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:03:06 GMT
CMD ["/bin/sh"]
# Tue, 15 Apr 2025 21:50:45 GMT
ARG version=8.452.09.1
# Tue, 15 Apr 2025 21:50:45 GMT
# ARGS: version=8.452.09.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
ENV LANG=C.UTF-8
# Tue, 15 Apr 2025 21:50:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:95459497489f07b9d71d294c852a09f9bbf1af51bb35db752a31f6f48935e293`  
		Last Modified: Fri, 14 Feb 2025 14:36:47 GMT  
		Size: 3.3 MB (3342657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:052af466c6290e8bfb24433ac2ae8eef01b2a8fd74a3b76bc70ab9ca504c81de`  
		Last Modified: Tue, 15 Apr 2025 23:58:15 GMT  
		Size: 41.4 MB (41365937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.18-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:ea063a40bfabb2f1b90a5a8e3552a23f8698df83e793f15b73ead982894e711b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.6 KB (193558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4658a12ddfc5e9c5a8bc3b14a40558cdb231e6772282c41b783e49778221f286`

```dockerfile
```

-	Layers:
	-	`sha256:765510491550f2ffd220248cdd4432c8ce99fad9f7eebbb77556cabc9b8887e4`  
		Last Modified: Tue, 15 Apr 2025 23:58:14 GMT  
		Size: 184.8 KB (184780 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:714bc4734836aa71d175494a5fb53d0f9389ea7a32ea814c4c4d23a7a84813b8`  
		Last Modified: Tue, 15 Apr 2025 23:58:14 GMT  
		Size: 8.8 KB (8778 bytes)  
		MIME: application/vnd.in-toto+json
