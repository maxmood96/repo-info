## `maven:3-amazoncorretto-11-alpine`

```console
$ docker pull maven@sha256:1c5d7b52929b64736eaf7db6c9140227f7c7b00cc08ac70c4f6bd0a2efdcf4fe
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-11-alpine` - linux; amd64

```console
$ docker pull maven@sha256:7b578f358d14bf0495825c684ca5ba56b277732edce74b011f0999f6a7e150c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.1 MB (159135243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7adfda38a11f1930bc205b301a43e39df6944d02e793efb9f7b57d3a9a915d63`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:29 GMT
ADD alpine-minirootfs-3.24.1-x86_64.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:29 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:19:20 GMT
ARG version=11.0.31.11.1
# Tue, 16 Jun 2026 00:19:20 GMT
# ARGS: version=11.0.31.11.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Jun 2026 00:19:20 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jun 2026 00:19:20 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 16 Jun 2026 00:19:20 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Tue, 16 Jun 2026 01:22:51 GMT
RUN apk add --no-cache bash openssh-client # buildkit
# Tue, 16 Jun 2026 01:22:51 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 16 Jun 2026 01:22:51 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 16 Jun 2026 01:22:51 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 16 Jun 2026 01:22:51 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 16 Jun 2026 01:22:51 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 16 Jun 2026 01:22:51 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 16 Jun 2026 01:22:51 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 16 Jun 2026 01:22:51 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 16 Jun 2026 01:22:51 GMT
ARG USER_HOME_DIR=/root
# Tue, 16 Jun 2026 01:22:51 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 16 Jun 2026 01:22:51 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 16 Jun 2026 01:22:51 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:55afa1ecc21d2bb5e5045f32dafee56272ffd89860bac26f6c32123439af26a4`  
		Last Modified: Sun, 14 Jun 2026 06:44:06 GMT  
		Size: 3.8 MB (3846391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cd05ab84418d679b0cbd17930ab8ae0f501d530d01b3010e9127bef7ff2d9d4`  
		Last Modified: Tue, 16 Jun 2026 00:19:38 GMT  
		Size: 143.7 MB (143712107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10170b1f8e5e874674c7b8a9cadc83d7a198007f1353501cd99870c6c240ffe9`  
		Last Modified: Tue, 16 Jun 2026 01:22:59 GMT  
		Size: 2.2 MB (2215771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0baec083dc414b0fdb85523c52091a72f279f67cfc008ed6329de72f86d4b56d`  
		Last Modified: Tue, 16 Jun 2026 01:22:59 GMT  
		Size: 9.4 MB (9359967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec774bf725cd288074bfa46e722f28c4b1451bdc73dc920724b4b038ce432694`  
		Last Modified: Tue, 16 Jun 2026 01:22:59 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d02ec0f5fba84941808311b45b75c80bcb33b52a8972ca049f9ef74b01dc9be`  
		Last Modified: Tue, 16 Jun 2026 01:22:59 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-11-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:54b1ddefad240f3205d716d9f46b27786f1ad1ce5f01ec95a2cf5c9b18c0324c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **748.1 KB (748099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35a8228d166e7b194742d3ba25f2aa5fef2481ebec593daf3f43398cab6df5c6`

```dockerfile
```

-	Layers:
	-	`sha256:0311bb83b24faa6e9549950b8c340cf067474d27f8f596346831c73d07c8f576`  
		Last Modified: Tue, 16 Jun 2026 01:22:59 GMT  
		Size: 733.6 KB (733574 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef9a1cc7a83edb9faa2133821d0c6f4ec02ba18404130073420f2b4cba0b2296`  
		Last Modified: Tue, 16 Jun 2026 01:22:59 GMT  
		Size: 14.5 KB (14525 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-11-alpine` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:c3d707b0fb36ca865b8d7e31e29966bf57cfd36107d98aeddaa3b5cc02e7a0fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.8 MB (157777576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad81ba5b413368fb14c21073acc5c65f192ce883d770c019d7825603ee415fcc`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:20 GMT
ADD alpine-minirootfs-3.24.1-aarch64.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:20 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:17:31 GMT
ARG version=11.0.31.11.1
# Tue, 16 Jun 2026 00:17:31 GMT
# ARGS: version=11.0.31.11.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Jun 2026 00:17:31 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jun 2026 00:17:31 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 16 Jun 2026 00:17:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Tue, 16 Jun 2026 01:25:07 GMT
RUN apk add --no-cache bash openssh-client # buildkit
# Tue, 16 Jun 2026 01:25:07 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 16 Jun 2026 01:25:07 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 16 Jun 2026 01:25:07 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 16 Jun 2026 01:25:07 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 16 Jun 2026 01:25:07 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 16 Jun 2026 01:25:07 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 16 Jun 2026 01:25:07 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 16 Jun 2026 01:25:07 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 16 Jun 2026 01:25:07 GMT
ARG USER_HOME_DIR=/root
# Tue, 16 Jun 2026 01:25:07 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 16 Jun 2026 01:25:07 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 16 Jun 2026 01:25:07 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:5de55e5ef9c033997441461efe7ba23a986db059c0bb78b38f84ee0d72b99167`  
		Last Modified: Sun, 14 Jun 2026 06:44:31 GMT  
		Size: 4.2 MB (4183037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc2379e7ac2d3112fce3f64d9467e0e7bc41de0426fcb06d70f72ebe1b22dfcb`  
		Last Modified: Tue, 16 Jun 2026 00:17:48 GMT  
		Size: 142.0 MB (141977832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3111124750a78cdb47ffb7f079f6396018a2b74e97b9deb5cdcecef06e6b4227`  
		Last Modified: Tue, 16 Jun 2026 01:25:14 GMT  
		Size: 2.3 MB (2255740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19b1b6d092eb39d4fca91aa4bae8d6adddd3b84d408a252a014d904e0bd4134f`  
		Last Modified: Tue, 16 Jun 2026 01:25:15 GMT  
		Size: 9.4 MB (9359961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:515667f9ddca9f37e4be05c554bd3a9151076b4695668e03384e153f78ba1331`  
		Last Modified: Tue, 16 Jun 2026 01:25:14 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90c950b8b52a6b1884078b5960c938de3dc4a0d98580546c4e596fbd574271c6`  
		Last Modified: Tue, 16 Jun 2026 01:25:14 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-11-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:69bf2ed47b1928088de51ac3008fa0da75f3a2bae0f07e614817d1ad85732dd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **747.6 KB (747627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d863fb33569adb6856cd0be14315d4956bded54e840dfefff3f249997ee91c7d`

```dockerfile
```

-	Layers:
	-	`sha256:024f11d014167eb142d965ff6e1f1edae9ff08d54619233323de39180b28558c`  
		Last Modified: Tue, 16 Jun 2026 01:25:15 GMT  
		Size: 733.0 KB (732968 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:085f12118106b1b8ee10e9890fbf668d7f153120ef6fa820d4392094bd4845eb`  
		Last Modified: Tue, 16 Jun 2026 01:25:14 GMT  
		Size: 14.7 KB (14659 bytes)  
		MIME: application/vnd.in-toto+json
