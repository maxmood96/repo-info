## `maven:3-amazoncorretto-21-alpine`

```console
$ docker pull maven@sha256:bdfee8306b4586a20d6a61301a703ac920383dd28205ba3b009e2d94227ffd2a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-21-alpine` - linux; amd64

```console
$ docker pull maven@sha256:08fcedf64e8f99d5eb476f2c77b5548a05c8f8a6aaebbe862412d5581ba91a20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.2 MB (177184459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c998d5bb4816002a672e8541307cf2dcee308999d2096d5d1c0fec223a8d029c`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:50:24 GMT
ARG version=21.0.10.7.1
# Wed, 28 Jan 2026 02:50:24 GMT
# ARGS: version=21.0.10.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Wed, 28 Jan 2026 02:50:24 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:50:24 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 28 Jan 2026 02:50:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Tue, 17 Mar 2026 03:47:57 GMT
RUN apk add --no-cache bash openssh-client # buildkit
# Tue, 17 Mar 2026 03:47:57 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 17 Mar 2026 03:47:57 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 17 Mar 2026 03:47:57 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 17 Mar 2026 03:47:57 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 17 Mar 2026 03:47:57 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 17 Mar 2026 03:47:57 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 17 Mar 2026 03:47:57 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 17 Mar 2026 03:47:57 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 17 Mar 2026 03:47:57 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 17 Mar 2026 03:47:57 GMT
ARG MAVEN_VERSION=3.9.14
# Tue, 17 Mar 2026 03:47:57 GMT
ARG USER_HOME_DIR=/root
# Tue, 17 Mar 2026 03:47:57 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 17 Mar 2026 03:47:57 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 17 Mar 2026 03:47:57 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0476ba18ce4a7d863df3375a1843d00caa67c25f77311a8828c2f340ca01d1fc`  
		Last Modified: Wed, 28 Jan 2026 02:50:43 GMT  
		Size: 161.6 MB (161590292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74b785d426c68dfc31bbe261f42a69c64cf5533beb568c9115d81ffd6fe62eb0`  
		Last Modified: Tue, 17 Mar 2026 03:48:05 GMT  
		Size: 2.4 MB (2420129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d92edea4f33d0cd0cddc9f27b2ef0e374a5296a0cb4a32e8c85cfd4b23006a9`  
		Last Modified: Tue, 17 Mar 2026 03:48:05 GMT  
		Size: 9.3 MB (9311179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06c87d68d30373770fa288de176bfea436bac9c3ef8ae742d568e975134756c3`  
		Last Modified: Tue, 17 Mar 2026 03:48:05 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c926e5415d7e3283d1b8849f6c03e27723e8f14daca5c0c2f318c2dd9fb3b22`  
		Last Modified: Tue, 17 Mar 2026 03:48:05 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-21-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:4858f72b5b4b4c8ba9b4e8578766de09f1a2aa01dcf3884a593e2fce9cd3d982
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **744.0 KB (743977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91b0a33bf4b90b410023afaccb87834d2675c50bf989c5a1e57534e82d4cb04d`

```dockerfile
```

-	Layers:
	-	`sha256:311b8317a38534e71590a45876ef991970090a1a4ac64904d552e33227d4a43d`  
		Last Modified: Tue, 17 Mar 2026 03:48:05 GMT  
		Size: 727.6 KB (727615 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0354495dd5e42cbeb5f5d1224570ef97713ff663d6f0f9f1c261b0f9d4dfd60f`  
		Last Modified: Tue, 17 Mar 2026 03:48:05 GMT  
		Size: 16.4 KB (16362 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-21-alpine` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:d9060749cd448fa96bc77a39fd15c1e1ebf43a0aa045e93ed2d1a14f79dd2a7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.6 MB (175586053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4b8c419768e2aa2b15cbf39764ccb6040fd8dcd44d653350f8636c6050d275d`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:51:47 GMT
ARG version=21.0.10.7.1
# Wed, 28 Jan 2026 02:51:47 GMT
# ARGS: version=21.0.10.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Wed, 28 Jan 2026 02:51:47 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:51:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 28 Jan 2026 02:51:47 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Tue, 17 Mar 2026 03:48:52 GMT
RUN apk add --no-cache bash openssh-client # buildkit
# Tue, 17 Mar 2026 03:48:52 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 17 Mar 2026 03:48:52 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 17 Mar 2026 03:48:52 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 17 Mar 2026 03:48:52 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 17 Mar 2026 03:48:52 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 17 Mar 2026 03:48:52 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 17 Mar 2026 03:48:52 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 17 Mar 2026 03:48:52 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 17 Mar 2026 03:48:52 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 17 Mar 2026 03:48:52 GMT
ARG MAVEN_VERSION=3.9.14
# Tue, 17 Mar 2026 03:48:52 GMT
ARG USER_HOME_DIR=/root
# Tue, 17 Mar 2026 03:48:52 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 17 Mar 2026 03:48:52 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 17 Mar 2026 03:48:52 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:429b075c73c3fb61a2595fbd83c3d77b387659de25ba9b2d1de05f9d24ee5f70`  
		Last Modified: Wed, 28 Jan 2026 02:52:06 GMT  
		Size: 159.6 MB (159615593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d979ab730a148a770c6ba445ea3ee92c031afc7168ce8987e76438cc3e671e82`  
		Last Modified: Tue, 17 Mar 2026 03:49:00 GMT  
		Size: 2.5 MB (2461153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e69365f67e77179de40c3257e032ad37f11e4be4efea86917c9a332acc30675e`  
		Last Modified: Tue, 17 Mar 2026 03:49:00 GMT  
		Size: 9.3 MB (9311179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d560f973c3102fbbb406733c06a43f7cd57fe76a0876905f5d5fdbd74cd510dc`  
		Last Modified: Tue, 17 Mar 2026 03:49:00 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:594d51743eadd0d253f0b7cf45d08f61557318e87d37e83f5e77186d505f4ff1`  
		Last Modified: Tue, 17 Mar 2026 03:49:00 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-21-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:4e4a26a58d85c49559c0e75019533711b29407897aeca51a048f45d5e4d68ee5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **742.9 KB (742867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff8d556da20bd8cdc3b14297c239f86dc340cb8d8f1fda4fc225e421612ef557`

```dockerfile
```

-	Layers:
	-	`sha256:0ac6ac36f78412087f3df1114af813137766c2188a2a7087276eff3842cfe05f`  
		Last Modified: Tue, 17 Mar 2026 03:49:00 GMT  
		Size: 726.4 KB (726372 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8876530b3c497ca7ea9704ca0a654c2feb68f5805910818721d00a012f4840b`  
		Last Modified: Tue, 17 Mar 2026 03:48:59 GMT  
		Size: 16.5 KB (16495 bytes)  
		MIME: application/vnd.in-toto+json
