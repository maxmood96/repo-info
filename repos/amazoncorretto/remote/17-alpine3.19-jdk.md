## `amazoncorretto:17-alpine3.19-jdk`

```console
$ docker pull amazoncorretto@sha256:2ea305152a0da99a62347f3935ca8124809352ccc32d2406e5a87e41d7bdb4d9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-alpine3.19-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:f1845883c3c2fa90c7ec8cc4809271b913a8147e195af38ee9de5d07ee252b58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.1 MB (149098793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9d66d5e548b716f5331065b81238dc6abae222f9a4235c25cb7fee5ce841ffd`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:06:42 GMT
ADD alpine-minirootfs-3.19.6-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:06:42 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2025 01:09:23 GMT
ARG version=17.0.14.7.1
# Thu, 23 Jan 2025 01:09:23 GMT
# ARGS: version=17.0.14.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Thu, 23 Jan 2025 01:09:23 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jan 2025 01:09:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Thu, 23 Jan 2025 01:09:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:861950bce9fa55e0462bb22503f61d8e7396f292af10969506b51e7bdb701d60`  
		Last Modified: Tue, 14 Jan 2025 20:33:01 GMT  
		Size: 3.4 MB (3420242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9db193675e7af473366c03038923c5b6d950ef2d00f425379a4a78d0ad0c13e2`  
		Last Modified: Tue, 04 Feb 2025 01:11:56 GMT  
		Size: 145.7 MB (145678551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine3.19-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:1c4b590684e72bd607a50827617f97dbb03c9ce75a422c994340e885e8eeac0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **390.3 KB (390310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d235472f9c3ef3e83b5c9ed3f284893f6b0d9babdc104ac9bc3b7d71b2df413a`

```dockerfile
```

-	Layers:
	-	`sha256:f7512ae5d41950ebb29fdc6f090f01d4d9b2d3557af87422d4d4fbe2cd54b4da`  
		Last Modified: Thu, 23 Jan 2025 18:27:30 GMT  
		Size: 380.9 KB (380893 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dade4e967d27134bd93618251135b7186b10cba653b05529e8fb408ab6dee865`  
		Last Modified: Thu, 23 Jan 2025 18:27:25 GMT  
		Size: 9.4 KB (9417 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-alpine3.19-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:27977af4513edf641a7d549e976a73aafabe032a9068680c92daa775d165cba3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.4 MB (147382386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9672a44fb8e730c7cc500e8dd28e2c31823d37784c49065c61206e0d92157ed9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:06:42 GMT
ADD alpine-minirootfs-3.19.6-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:06:42 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2025 01:09:23 GMT
ARG version=17.0.14.7.1
# Thu, 23 Jan 2025 01:09:23 GMT
# ARGS: version=17.0.14.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Thu, 23 Jan 2025 01:09:23 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jan 2025 01:09:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Thu, 23 Jan 2025 01:09:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:88b83b407e415cb5cb78776f0e83bf403b89f77eb02721ce6a3cbf1eba723438`  
		Last Modified: Tue, 14 Jan 2025 20:33:05 GMT  
		Size: 3.4 MB (3360532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4764cc5cfceb8f11be8768feb456ba10642f2ef3caef7921575286ca20551ef3`  
		Last Modified: Wed, 05 Feb 2025 09:22:42 GMT  
		Size: 144.0 MB (144021854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine3.19-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:6f94ca04c8f585fe6ecaf5fe4a6c7c27672739d2277fdcadf6e4eddf9986bbfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.8 KB (389833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71896a2fcce59365e5804c471d55549dbc7746bd620ad1f7add84cca30af4301`

```dockerfile
```

-	Layers:
	-	`sha256:4639c8de075d975362c9ef467312ab1add84d7ac7e5d885951a8f4140029228e`  
		Last Modified: Thu, 23 Jan 2025 18:48:10 GMT  
		Size: 380.3 KB (380312 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a85ae0245d32402bebbc106f2e3b129c176f8b94c8b5ed93ea33767a43677b2`  
		Last Modified: Thu, 23 Jan 2025 18:48:10 GMT  
		Size: 9.5 KB (9521 bytes)  
		MIME: application/vnd.in-toto+json
