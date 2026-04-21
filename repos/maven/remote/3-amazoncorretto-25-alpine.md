## `maven:3-amazoncorretto-25-alpine`

```console
$ docker pull maven@sha256:b9e58b357a103d9f441d2b723a880c67d1941451fbbcbc6ff7e244ee4983f62e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-25-alpine` - linux; amd64

```console
$ docker pull maven@sha256:2196e98a73da4d4dcd13b838b2057841f21853fef09d1d69d08793cd19d9f7b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.4 MB (196356995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1aed19bbaa13cfaec1d785c656e723e57e1c21613edaa8daf0c2ec5dfe577704`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:24:33 GMT
ARG version=25.0.2.10.1
# Wed, 15 Apr 2026 20:24:33 GMT
# ARGS: version=25.0.2.10.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-25=$version-r0 &&     rm -rf /usr/lib/jvm/java-25-amazon-corretto/lib/src.zip # buildkit
# Wed, 15 Apr 2026 20:24:33 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 20:24:33 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 15 Apr 2026 20:24:33 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Tue, 21 Apr 2026 18:12:25 GMT
RUN apk add --no-cache bash openssh-client # buildkit
# Tue, 21 Apr 2026 18:12:25 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 21 Apr 2026 18:12:25 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 21 Apr 2026 18:12:25 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 21 Apr 2026 18:12:25 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 21 Apr 2026 18:12:25 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 21 Apr 2026 18:12:25 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 21 Apr 2026 18:12:25 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 21 Apr 2026 18:12:25 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 21 Apr 2026 18:12:25 GMT
ARG USER_HOME_DIR=/root
# Tue, 21 Apr 2026 18:12:25 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 21 Apr 2026 18:12:25 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 21 Apr 2026 18:12:25 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f961561d31cd5037ff5298d6237cb82f4e652e35bbe8021a675c623cdeb1b35`  
		Last Modified: Wed, 15 Apr 2026 20:24:54 GMT  
		Size: 180.8 MB (180759200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bfec9e28b151c8a74820946e975bd436c50c849979a1195fba55189253a51d9`  
		Last Modified: Tue, 21 Apr 2026 18:12:34 GMT  
		Size: 2.4 MB (2420402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc2996243648f67b8083761e08a4efaf76255125ed6c373268141595ec322bb6`  
		Last Modified: Tue, 21 Apr 2026 18:12:34 GMT  
		Size: 9.3 MB (9312198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a77bdcb8f39520badcbdcd35d66f335f4db31b1f764aadfd4fa9156414178e5b`  
		Last Modified: Tue, 21 Apr 2026 18:12:33 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3be2201a60b3be42801214fb790bafa9ff9a846a9271cb2bc3452ac8a657f0dc`  
		Last Modified: Tue, 21 Apr 2026 18:12:33 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-25-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:f7f2907d79175a27129463d56a1b6550e6d886d2941f7cbcb7fc82735897ffe5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **751.3 KB (751269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7aaa0c294a406dc0befda16728b7c1e8ce734c93ddd3e443a685f12b966ab01d`

```dockerfile
```

-	Layers:
	-	`sha256:e4ea5a114c971b50cb9dfbb59e7e745f43ce9fced5bbbe51b50043bd6bd4c97f`  
		Last Modified: Tue, 21 Apr 2026 18:12:34 GMT  
		Size: 736.7 KB (736743 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91e3bd939294de115797910933793ecb86189c80d23e484ac62772daf7f2132b`  
		Last Modified: Tue, 21 Apr 2026 18:12:34 GMT  
		Size: 14.5 KB (14526 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-25-alpine` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:1116ea916c983fd6b9a067ba773db447b629a002f530d1f34f1f063c539a41b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.4 MB (194386825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c851f8603b42c01db1c04d7e53853bce789d1838652368e59504f9d3a30019c2`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:23:59 GMT
ARG version=25.0.2.10.1
# Wed, 15 Apr 2026 20:23:59 GMT
# ARGS: version=25.0.2.10.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-25=$version-r0 &&     rm -rf /usr/lib/jvm/java-25-amazon-corretto/lib/src.zip # buildkit
# Wed, 15 Apr 2026 20:23:59 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 20:23:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 15 Apr 2026 20:23:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Tue, 21 Apr 2026 18:12:15 GMT
RUN apk add --no-cache bash openssh-client # buildkit
# Tue, 21 Apr 2026 18:12:15 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 21 Apr 2026 18:12:15 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 21 Apr 2026 18:12:15 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 21 Apr 2026 18:12:15 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 21 Apr 2026 18:12:15 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 21 Apr 2026 18:12:15 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 21 Apr 2026 18:12:15 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 21 Apr 2026 18:12:15 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 21 Apr 2026 18:12:15 GMT
ARG USER_HOME_DIR=/root
# Tue, 21 Apr 2026 18:12:15 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 21 Apr 2026 18:12:15 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 21 Apr 2026 18:12:15 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5d751edfe3e5205eea6210b418197b25f4c7c31b99665652de330dfd754bd47`  
		Last Modified: Wed, 15 Apr 2026 20:24:26 GMT  
		Size: 178.4 MB (178411940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25489f2432bf71ce978a986e772fa58ca8aec6fcf764d6150cfc2462bb64c43b`  
		Last Modified: Tue, 21 Apr 2026 18:12:24 GMT  
		Size: 2.5 MB (2461755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25cbc84530da57fc2c520ffd98df7d44461076e23e255f3eafac619a38ab9b35`  
		Last Modified: Tue, 21 Apr 2026 18:12:24 GMT  
		Size: 9.3 MB (9312254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:690a2642f9c0d4f695af7ec51c776abe5cebfeab2b2858bac9152bddd6120415`  
		Last Modified: Tue, 21 Apr 2026 18:12:23 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b60e199eacfe8ce73c0f863eeda72eb48e257c18e335df4084429ab1c987462`  
		Last Modified: Tue, 21 Apr 2026 18:12:23 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-25-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:7a58386a0811e4bb827148e4bfb4355b566dd99620183093526ec78580f4c58c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **750.2 KB (750156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4b86ecdad171e43a763f3cfe9d10c1f044ce4a7c21db858eba2ce3c0cc179d8`

```dockerfile
```

-	Layers:
	-	`sha256:7002aeb8415534ac65d98b72d8cbaed743a1f75d2ec782c0e1d1c64d99c66d52`  
		Last Modified: Tue, 21 Apr 2026 18:12:23 GMT  
		Size: 735.5 KB (735497 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:928929e3f73663474fe0fc10cb32283978a5ce6357346dcfdef902d466d3bb0e`  
		Last Modified: Tue, 21 Apr 2026 18:12:23 GMT  
		Size: 14.7 KB (14659 bytes)  
		MIME: application/vnd.in-toto+json
