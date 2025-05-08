## `amazoncorretto:8u452-alpine3.19-jre`

```console
$ docker pull amazoncorretto@sha256:e9e8600afe72af341f8cc5ec59fb314abbc6a2886ac33c99450ffd38a680fe9c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u452-alpine3.19-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:928fbbaf212a524823a21990f3d5671f42d74237502413301da84a205b337990
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.1 MB (45083895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:180db4a582abb4eb5b2085c7b6ad949d956f2a3edcce69112fc9f57d1c3825e8`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:05:02 GMT
ADD alpine-minirootfs-3.19.7-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:05:02 GMT
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
	-	`sha256:83abf496f1b833f01c8f72695520b8975cc8b730d14a8ac270d6201bd0f1877e`  
		Last Modified: Fri, 14 Feb 2025 14:30:10 GMT  
		Size: 3.4 MB (3420868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f0527d65ed2cad318a92a80b12909c6abe47e9500a0de7871dfe9217e3943a9`  
		Last Modified: Tue, 15 Apr 2025 23:55:13 GMT  
		Size: 41.7 MB (41663027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u452-alpine3.19-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:5640155b5dddca979461fa6935e5ab22bcccf6de24fbf3e6ed77e86c03ef4b41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.0 KB (194030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b07a0aa510a94976cbfca4438c9aaff3b22e41d88fdd01f9b86284b36ff6821`

```dockerfile
```

-	Layers:
	-	`sha256:6a96fdaaecd7dda2d3adcf72786d2ecba8dcb3238ff2f2278be71d87eacbd844`  
		Last Modified: Tue, 15 Apr 2025 23:55:13 GMT  
		Size: 185.3 KB (185331 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d59cf7df08714f01bb084e94ff75bbff2ad041bf806d8ed5dc6a45395c3158af`  
		Last Modified: Tue, 15 Apr 2025 23:55:12 GMT  
		Size: 8.7 KB (8699 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8u452-alpine3.19-jre` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:ac9209859383440c1b653a88a63980c001c5e77844244c5ba386a3e82ac8a920
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.7 MB (44727214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d45a8afe77a47a2831c10c4a9e0b8eb035d3bc0c78df060f121e321750361a06`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:05:02 GMT
ADD alpine-minirootfs-3.19.7-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:05:02 GMT
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
	-	`sha256:d13a3fff434d56c3504596695435266be8d07061a80359aa09366eea2e094aa0`  
		Last Modified: Fri, 14 Feb 2025 14:31:17 GMT  
		Size: 3.4 MB (3361424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:937d8ce4aacd9aec4f066e9be1bf2953bc362a71153f95f97e1d6923a9ccea52`  
		Last Modified: Tue, 15 Apr 2025 23:59:00 GMT  
		Size: 41.4 MB (41365790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u452-alpine3.19-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:fef9183e78ea98ce005da5840626743f26b151a7d95c96a6be62eeb1cf34d8fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.2 KB (194218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a5e1904fa56324dd4c8133f8490bfab18f743876feff726752e20372194ffb9`

```dockerfile
```

-	Layers:
	-	`sha256:5c2f6816a09ea4fd8b26b65093df3793e211291e610217278dd5849586ffde76`  
		Last Modified: Tue, 15 Apr 2025 23:58:58 GMT  
		Size: 185.4 KB (185439 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3089376a6c65f1a4945d1ed71476db613797debb0ca10879aff452efe6f12f1a`  
		Last Modified: Tue, 15 Apr 2025 23:58:58 GMT  
		Size: 8.8 KB (8779 bytes)  
		MIME: application/vnd.in-toto+json
