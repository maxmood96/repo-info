## `amazoncorretto:21-alpine3.19-jdk`

```console
$ docker pull amazoncorretto@sha256:46448496807990e3c46369813dbb8b5c4d9b55606801bf281da3ba232f68a9fc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-alpine3.19-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:dbf1e7be683beb43db0cb662791a9e604ea600145cd50f82d3a0c1fd0eba482e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.3 MB (162342904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2654770972711ec50cf1995de18ff1ff6333b66fcc558aaed5056d206c0efe9e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 13 Dec 2024 23:01:14 GMT
ADD alpine-minirootfs-3.19.5-x86_64.tar.gz / # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 23:01:14 GMT
ARG version=21.0.5.11.1
# Fri, 13 Dec 2024 23:01:14 GMT
# ARGS: version=21.0.5.11.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 23:01:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 13 Dec 2024 23:01:14 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:eb002c13a70b63d5677b5a03f11b7b8b60f7d62f296fbb7475169a617500d3cb`  
		Last Modified: Tue, 07 Jan 2025 02:28:43 GMT  
		Size: 3.4 MB (3413271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:071f74a8a79e848ab70968d35ea6a1430e950e0d91fe31561af9f1715b421f16`  
		Last Modified: Wed, 08 Jan 2025 04:29:18 GMT  
		Size: 158.9 MB (158929633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.19-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:c6ba2850671450931e44433be2e787e5acefbf8fefd3e7f49a9c52e3827928f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **390.2 KB (390207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb8e4eaefdfdae8149be484caf19ab437db65f217c72a09cbe0873b4fbe6bdc9`

```dockerfile
```

-	Layers:
	-	`sha256:c77a4a189a475d3c2c22d78319f02c49cb95d2de9a9035307ff541ba80b13f27`  
		Last Modified: Tue, 07 Jan 2025 03:30:27 GMT  
		Size: 380.8 KB (380792 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89eb4567960f192552761f7274268a2eed65b5e360d6aeb115ffea6f3ca657f7`  
		Last Modified: Wed, 08 Jan 2025 04:29:14 GMT  
		Size: 9.4 KB (9415 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-alpine3.19-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:99ab2b6d36310049f2a5a4d758545c4a7c6a332d5a72b204e9aabdd8d1bc715a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.2 MB (160230443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0698a2f6072b1339a4ba57b7ac691cc03bfb04a27c2a17f605d992cda0b27eb`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 13 Dec 2024 23:01:14 GMT
ADD alpine-minirootfs-3.19.5-aarch64.tar.gz / # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 23:01:14 GMT
ARG version=21.0.5.11.1
# Fri, 13 Dec 2024 23:01:14 GMT
# ARGS: version=21.0.5.11.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 23:01:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 13 Dec 2024 23:01:14 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:f2178dde0fb65be0d15359886bb642d5d8dac86ca2d709ab90f8f0ee62211ca2`  
		Last Modified: Tue, 07 Jan 2025 03:03:15 GMT  
		Size: 3.4 MB (3351948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97daba5a9b8a7f42a3fbd1580bd00dac20183704cc8aa4747fe56af7f9d6bdbd`  
		Last Modified: Tue, 07 Jan 2025 07:24:44 GMT  
		Size: 156.9 MB (156878495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.19-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:61c62545f47eee2fc445830d82aff882b44f8358801fd2533b5d6af153aba993
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.7 KB (389730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6eeb8d8548278e135823204b03ab3dd2daeea2f690d54d6e5db8f25a0357ac8e`

```dockerfile
```

-	Layers:
	-	`sha256:74c0f0847ea162e1266f97ef426953f28bc1ef0cd359c1623d7c464d76595281`  
		Last Modified: Tue, 07 Jan 2025 07:24:41 GMT  
		Size: 380.2 KB (380211 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ba7989df23d55b31fbad9aa3af9586aecd7dea620dc8f35ba99a4a94856d556`  
		Last Modified: Tue, 07 Jan 2025 07:24:40 GMT  
		Size: 9.5 KB (9519 bytes)  
		MIME: application/vnd.in-toto+json
