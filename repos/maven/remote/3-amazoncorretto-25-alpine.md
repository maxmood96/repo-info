## `maven:3-amazoncorretto-25-alpine`

```console
$ docker pull maven@sha256:b54da525d29be4a20b6ca1a8496ac750f4e19224cd4431cc208d3ff5a3720d49
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-25-alpine` - linux; amd64

```console
$ docker pull maven@sha256:1ca06ea24b187a46a8b7e1cad4b539a76c7ecf4478e66a87b16c21f25cd6a141
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.6 MB (196644569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27a96dd1390764d05ff5b982f98dfb81e9db0d143efb5ecede7e86580fc7035a`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 22 Apr 2026 21:35:23 GMT
ARG version=25.0.3.9.1
# Wed, 22 Apr 2026 21:35:23 GMT
# ARGS: version=25.0.3.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-25=$version-r0 &&     rm -rf /usr/lib/jvm/java-25-amazon-corretto/lib/src.zip # buildkit
# Wed, 22 Apr 2026 21:35:23 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 21:35:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 22 Apr 2026 21:35:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Tue, 02 Jun 2026 10:27:29 GMT
RUN apk add --no-cache bash openssh-client # buildkit
# Tue, 02 Jun 2026 10:27:29 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 02 Jun 2026 10:27:29 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 02 Jun 2026 10:27:29 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 02 Jun 2026 10:27:29 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 02 Jun 2026 10:27:29 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 02 Jun 2026 10:27:29 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 02 Jun 2026 10:27:29 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 02 Jun 2026 10:27:29 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 02 Jun 2026 10:27:29 GMT
ARG USER_HOME_DIR=/root
# Tue, 02 Jun 2026 10:27:29 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 02 Jun 2026 10:27:29 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 02 Jun 2026 10:27:29 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6130299703f5831bc35b5254b4eb5549c81fd91109769f9225c20dd65844ae64`  
		Last Modified: Wed, 22 Apr 2026 21:35:44 GMT  
		Size: 181.0 MB (180998980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fc3b2b2011e111cdd1e0c9f033fd643b3299ef3fdc60a412f10b3edbfac0389`  
		Last Modified: Tue, 02 Jun 2026 10:27:37 GMT  
		Size: 2.4 MB (2420426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0836d082caa4e15b95c6464beb238c462557f7b6da0ef521816f17b0efc9ec72`  
		Last Modified: Tue, 02 Jun 2026 10:27:38 GMT  
		Size: 9.4 MB (9359967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e18ac91d9122f67aff7834c2e4e4ca036c4a5ec2d4457e33d6c5902d8e0c753`  
		Last Modified: Tue, 02 Jun 2026 10:27:37 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be688a50e610ac210d0739a5087f308fbb6ec7dfdb583d9451f3120b6f2b9c80`  
		Last Modified: Tue, 02 Jun 2026 10:27:37 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-25-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:664458403bd14f906f6762dbc1fb067bdcb41830d1d64131bec2fb8ea73adef0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **751.9 KB (751914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c678100c0417a9ed0162f0c8c405ed602b5cdf4a79342bbd849f0a3a91c0eb24`

```dockerfile
```

-	Layers:
	-	`sha256:17d951ba95da2c710c74a27dd5eb49702c47a7f892f9760ea54c68a7b73ee173`  
		Last Modified: Tue, 02 Jun 2026 10:27:37 GMT  
		Size: 737.4 KB (737388 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a757b2d13e04f543d5edd104d55a0ec087ba06f246df2107d6da95f280e9d9f6`  
		Last Modified: Tue, 02 Jun 2026 10:27:37 GMT  
		Size: 14.5 KB (14526 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-25-alpine` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:15ab624d2507a252cd71ce15bf5d2636e99dfbf6526cad21a69c2465d398aa7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.6 MB (194644438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc424bcf30201829928052180391c85189a63339ffbdb829f5c548dbc5ba95cd`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 22 Apr 2026 21:35:17 GMT
ARG version=25.0.3.9.1
# Wed, 22 Apr 2026 21:35:17 GMT
# ARGS: version=25.0.3.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-25=$version-r0 &&     rm -rf /usr/lib/jvm/java-25-amazon-corretto/lib/src.zip # buildkit
# Wed, 22 Apr 2026 21:35:17 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 21:35:17 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 22 Apr 2026 21:35:17 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Tue, 02 Jun 2026 10:24:31 GMT
RUN apk add --no-cache bash openssh-client # buildkit
# Tue, 02 Jun 2026 10:24:31 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 02 Jun 2026 10:24:31 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 02 Jun 2026 10:24:31 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 02 Jun 2026 10:24:31 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 02 Jun 2026 10:24:31 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 02 Jun 2026 10:24:31 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 02 Jun 2026 10:24:32 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 02 Jun 2026 10:24:32 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 02 Jun 2026 10:24:32 GMT
ARG USER_HOME_DIR=/root
# Tue, 02 Jun 2026 10:24:32 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 02 Jun 2026 10:24:32 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 02 Jun 2026 10:24:32 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d236e04af56142e3286d8350a8586b6e1a108498823e2f4b6b22a514d970c21`  
		Last Modified: Wed, 22 Apr 2026 21:35:40 GMT  
		Size: 178.6 MB (178621799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd0561c3f9efa44c2f306a5e600da10582cd4a80289b0a8273166914ef523fb3`  
		Last Modified: Tue, 02 Jun 2026 10:24:39 GMT  
		Size: 2.5 MB (2461789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26c01d92f862c46258be50ecd5bfb3596575c33ca8adffc928052166155d278e`  
		Last Modified: Tue, 02 Jun 2026 10:24:39 GMT  
		Size: 9.4 MB (9359973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a53659c1506a6123c8bf8a57ddb0421bafcc4cd23b0e30bff20e31fc2012ce8b`  
		Last Modified: Tue, 02 Jun 2026 10:24:39 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ef7aba850018bbd25cb77c22e8a419cb46fa14d262f66d8a5f9a1a8ebee8667`  
		Last Modified: Tue, 02 Jun 2026 10:24:39 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-25-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:c511ab9f2b47f3a9b73c1cb59647972012c2e04d7c313d920bd17c79883c7e68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **750.8 KB (750801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97a5efc80ada0ebf7e71ebc2f520e5abc4e91b0ff8506523d1c435cbcf4576bf`

```dockerfile
```

-	Layers:
	-	`sha256:215d93aaa9d388ad405f6135a4b47402fe0e13c49291d49c92514b3f57d52a06`  
		Last Modified: Tue, 02 Jun 2026 10:24:39 GMT  
		Size: 736.1 KB (736142 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0783e1351194553d6111efd1c863f4adf9350c70f91e55ab1ed34609e60b9298`  
		Last Modified: Tue, 02 Jun 2026 10:24:39 GMT  
		Size: 14.7 KB (14659 bytes)  
		MIME: application/vnd.in-toto+json
