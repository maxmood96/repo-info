## `amazoncorretto:25-alpine3.22`

```console
$ docker pull amazoncorretto@sha256:404c807947831a67c64f750ec34f37e2a038668c489375d4e9465b70d8724448
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:25-alpine3.22` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:0d793ecebe763f0695841932b7f4a1788259cf59149e3acc547b9a7812c8eeab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.6 MB (184573607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35789ef0c5f4579ef54a4c057badf297119800f422e6e6f6ffabe9dcc56c6241`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:23:12 GMT
ARG version=25.0.2.10.1
# Fri, 17 Apr 2026 00:23:12 GMT
# ARGS: version=25.0.2.10.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-25=$version-r0 &&     rm -rf /usr/lib/jvm/java-25-amazon-corretto/lib/src.zip # buildkit
# Fri, 17 Apr 2026 00:23:12 GMT
ENV LANG=C.UTF-8
# Fri, 17 Apr 2026 00:23:12 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 17 Apr 2026 00:23:12 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e46b686b92956200aaafb1e6d76fb0e40e76df2cef79f3168aef6c466a479da`  
		Last Modified: Fri, 17 Apr 2026 00:23:34 GMT  
		Size: 180.8 MB (180765418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-alpine3.22` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:f44edc439fc4ccec69508219dd290755dd36c889a3c70b0d9f7b72a3f3336cf2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **601.5 KB (601509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a721d694a43dc428ad0acce7179352dccafe4ec4e9ec1bbd54fcebfd2311051`

```dockerfile
```

-	Layers:
	-	`sha256:ab1530af602d4e72bb03eb7e9f498b3fbd7526fbd09a0f64db7d42b3c3632273`  
		Last Modified: Fri, 17 Apr 2026 00:23:30 GMT  
		Size: 592.1 KB (592137 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1368cc50e91f2c17127206a8c83cd247a9c18e5794115cbf13ca48ab7066aeff`  
		Last Modified: Fri, 17 Apr 2026 00:23:29 GMT  
		Size: 9.4 KB (9372 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:25-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:36f3d8cf2df2d52fb09e7570aba6cbce9716583c44a3c796630a02ebcee6c7bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.6 MB (182552619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2ce186a62dd6a0ecf9dd5c1d81f7cb7969b5ddfa6182df295dc147b2284692c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:25:16 GMT
ARG version=25.0.2.10.1
# Fri, 17 Apr 2026 00:25:16 GMT
# ARGS: version=25.0.2.10.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-25=$version-r0 &&     rm -rf /usr/lib/jvm/java-25-amazon-corretto/lib/src.zip # buildkit
# Fri, 17 Apr 2026 00:25:16 GMT
ENV LANG=C.UTF-8
# Fri, 17 Apr 2026 00:25:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 17 Apr 2026 00:25:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18a18b251f6d0682919c2704e428b3e4cc3310607c7abb2afdb54537ed3b35b8`  
		Last Modified: Fri, 17 Apr 2026 00:25:38 GMT  
		Size: 178.4 MB (178410725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-alpine3.22` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:6cf211e1c28ebb604364e4345baabf0291ce3aa5bb1acb6618757612417c3099
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **601.0 KB (601029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b508e5118806e17b1711fac39ee574825a9021be9364d5956500de69a74ce0e9`

```dockerfile
```

-	Layers:
	-	`sha256:fe45a838ab64e4bee1a906d7e08140d992e30237a283462253dbb24c75fb55b4`  
		Last Modified: Fri, 17 Apr 2026 00:25:33 GMT  
		Size: 591.6 KB (591553 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f97a77223cb0bb5beaf895df32fd9fbdd962ea32aaabfe42086e5141c8d670d`  
		Last Modified: Fri, 17 Apr 2026 00:25:33 GMT  
		Size: 9.5 KB (9476 bytes)  
		MIME: application/vnd.in-toto+json
