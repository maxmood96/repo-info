## `maven:3-amazoncorretto-24-alpine`

```console
$ docker pull maven@sha256:27b538530bc1d3c6523d123104328d951997185c662f30fcfacc25a1df3f704c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-24-alpine` - linux; amd64

```console
$ docker pull maven@sha256:08fcab57fd2be57ce4dd53128245679b5308592e176923c719e2cc27bed7f992
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.2 MB (192179386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5d8df36f61c6dd1bad48bad7d2d0dfba497a7fcb038a2c07bcd412881a8570f`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 16 Jul 2025 06:51:38 GMT
ARG version=24.0.2.12.1
# Wed, 16 Jul 2025 06:51:38 GMT
# ARGS: version=24.0.2.12.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-24=$version-r0 &&     rm -rf /usr/lib/jvm/java-24-amazon-corretto/lib/src.zip # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
ENV LANG=C.UTF-8
# Wed, 16 Jul 2025 06:51:38 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 16 Jul 2025 06:51:38 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Wed, 16 Jul 2025 06:51:38 GMT
RUN apk add --no-cache bash openssh-client # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 16 Jul 2025 06:51:38 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 16 Jul 2025 06:51:38 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
ARG MAVEN_VERSION=3.9.11
# Wed, 16 Jul 2025 06:51:38 GMT
ARG USER_HOME_DIR=/root
# Wed, 16 Jul 2025 06:51:38 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 16 Jul 2025 06:51:38 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 16 Jul 2025 06:51:38 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da6044ea9c8a1ef640a4f19ab13afda53c68d55374d877a5f49f223648ee77d0`  
		Last Modified: Fri, 18 Jul 2025 20:07:59 GMT  
		Size: 176.8 MB (176770797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:546e31c7313b468450003a953471a8a5c3358d8e2ebd5feb07243749560b0a22`  
		Last Modified: Tue, 02 Sep 2025 01:14:00 GMT  
		Size: 2.4 MB (2365283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b1c05ddefb0030b08fceae7a79d225ecd83cd2a6884fc74bd7c221652aa067f`  
		Last Modified: Tue, 02 Sep 2025 01:14:02 GMT  
		Size: 9.2 MB (9242578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8a721776155d7c0a97d69a00f0cb59e3c6384a889d45905fc328c1c47564937`  
		Last Modified: Tue, 02 Sep 2025 01:14:00 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38314554cb891f382bc36e5c4ba05ec700bb320d394a90e8a1f1604bb33cb187`  
		Last Modified: Tue, 02 Sep 2025 01:14:01 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-24-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:57f9f86b7bb8e92b06f755281e0bcd46390b4d17f5e3e172b1953d7589d6d5c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **553.6 KB (553635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81448b3118785fdb97ae71b150f3a1f34eaf80531b0329c378e6b687883d26b1`

```dockerfile
```

-	Layers:
	-	`sha256:25c64e955feabb5dfa4cf096c221174a0a3f54c21901cc3fd6931fdd289fdc3e`  
		Last Modified: Tue, 02 Sep 2025 02:28:39 GMT  
		Size: 537.2 KB (537230 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54c21ecd74b4a62a0e2dac01b4e37f50299dcef1d175ed77fb28fa8398dba725`  
		Last Modified: Tue, 02 Sep 2025 02:28:40 GMT  
		Size: 16.4 KB (16405 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-24-alpine` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:7c25c7aae3361f54e7a17a4d1801b924366b73b7ba2e956acebd81b68d759a61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.3 MB (190288483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a90b2060b06b496974fa28bf843fe8400e85c13c82e345e7d1462f66d5af852d`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 16 Jul 2025 06:51:38 GMT
ARG version=24.0.2.12.1
# Wed, 16 Jul 2025 06:51:38 GMT
# ARGS: version=24.0.2.12.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-24=$version-r0 &&     rm -rf /usr/lib/jvm/java-24-amazon-corretto/lib/src.zip # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
ENV LANG=C.UTF-8
# Wed, 16 Jul 2025 06:51:38 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 16 Jul 2025 06:51:38 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Wed, 16 Jul 2025 06:51:38 GMT
RUN apk add --no-cache bash openssh-client # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 16 Jul 2025 06:51:38 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 16 Jul 2025 06:51:38 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
ARG MAVEN_VERSION=3.9.11
# Wed, 16 Jul 2025 06:51:38 GMT
ARG USER_HOME_DIR=/root
# Wed, 16 Jul 2025 06:51:38 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 16 Jul 2025 06:51:38 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 16 Jul 2025 06:51:38 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7de9585f1b7564cbcb01d30dbbbf1693f75039bedbf47afb1c24cb8380f5d989`  
		Last Modified: Fri, 18 Jul 2025 22:13:41 GMT  
		Size: 174.5 MB (174517397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:278121b9b963d7009c4424d7259b82e8bbbcab6407e5a7da8877ef6610986dc0`  
		Last Modified: Tue, 02 Sep 2025 12:05:33 GMT  
		Size: 2.4 MB (2396712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55f1d2207446414ad1dc194028fcb69c67b38a10049f06844b70db7697c89e31`  
		Last Modified: Tue, 02 Sep 2025 12:05:36 GMT  
		Size: 9.2 MB (9242585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:911814f2e9fa350bf76790557c7f3a21c34fed9804f94df9d4fa713d412086e5`  
		Last Modified: Tue, 02 Sep 2025 12:05:33 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a40c04ca6216e41b2c4454cde85e2436f74b9878ce903f4fbe71d43f48f88b6`  
		Last Modified: Tue, 02 Sep 2025 12:05:34 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-24-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:0f9ab4cddb6e889ce7c59bd90e51602c4ff6303fc2476bbb99a584fe0ee58fdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **553.2 KB (553172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6bfb063929e5e4b56d64136fa67bf31f5a342fbe58501979950bb6e04960343`

```dockerfile
```

-	Layers:
	-	`sha256:89d91416df7d843e01b9f490d4105fa37658f34e1a7badbe192a605cf53fc6ee`  
		Last Modified: Tue, 02 Sep 2025 14:28:39 GMT  
		Size: 536.6 KB (536634 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26aa20a68bda1b0dbe169275277e39d7abc891b55ccfc75f240ac38553952af7`  
		Last Modified: Tue, 02 Sep 2025 14:28:40 GMT  
		Size: 16.5 KB (16538 bytes)  
		MIME: application/vnd.in-toto+json
