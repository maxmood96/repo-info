## `maven:3-amazoncorretto-17-alpine`

```console
$ docker pull maven@sha256:2d81965c6bfd4e6789a7b278a2a388d84af2925bacb37a20f2eaf59b22af1619
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-17-alpine` - linux; amd64

```console
$ docker pull maven@sha256:af7b330dcac2f261725442f0e0c317d38f2c2e7d38099f0d7b870fdf2286cefa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.8 MB (163771947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcfd83f1ed46992bd3269c458386e16952185507e023b4e9406c59f456032d87`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 21 Oct 2025 20:48:19 GMT
ARG version=17.0.17.10.1
# Tue, 21 Oct 2025 20:48:19 GMT
# ARGS: version=17.0.17.10.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Tue, 21 Oct 2025 20:48:19 GMT
ENV LANG=C.UTF-8
# Tue, 21 Oct 2025 20:48:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 21 Oct 2025 20:48:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Fri, 14 Nov 2025 01:41:57 GMT
RUN apk add --no-cache bash openssh-client # buildkit
# Fri, 14 Nov 2025 01:41:57 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 14 Nov 2025 01:41:57 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 14 Nov 2025 01:41:57 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 14 Nov 2025 01:41:57 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 14 Nov 2025 01:41:57 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 14 Nov 2025 01:41:57 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 14 Nov 2025 01:41:57 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 14 Nov 2025 01:41:57 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Fri, 14 Nov 2025 01:41:57 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 14 Nov 2025 01:41:57 GMT
ARG MAVEN_VERSION=3.9.11
# Fri, 14 Nov 2025 01:41:57 GMT
ARG USER_HOME_DIR=/root
# Fri, 14 Nov 2025 01:41:57 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 14 Nov 2025 01:41:57 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 14 Nov 2025 01:41:57 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Sun, 07 Dec 2025 13:53:31 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb28ef838e56c6ab8cebd0401045d8e34acac54687290ae5630028b628a943b9`  
		Last Modified: Wed, 22 Oct 2025 00:50:53 GMT  
		Size: 148.4 MB (148351194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7153a4a34aec568e57eb586b9df0cbd11d5fea4d149c2cc7668a67a9510da6c1`  
		Last Modified: Fri, 14 Nov 2025 01:42:11 GMT  
		Size: 2.4 MB (2374687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:833996066f26eed0a5e4adc7ed0b7d52a2c5750d3ade33a54f5cf30ef85c9365`  
		Last Modified: Fri, 14 Nov 2025 01:42:11 GMT  
		Size: 9.2 MB (9242572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adcd626eed05def79ead12b172bf3a408a82ed623c8ab4092388dc654c12049d`  
		Last Modified: Fri, 14 Nov 2025 01:42:11 GMT  
		Size: 854.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea04cd4e95a5821bdd9db8be66700c07adda9f2b05e7ed00b93913d1374ceb31`  
		Last Modified: Fri, 14 Nov 2025 01:42:11 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:0d6bbf3183830351b9f10e17076d3bef914ae0a52e27deae6397a8f76899fa8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **743.0 KB (742977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a8a486862d4745487951abd50a091f3473e40e69bc7a51a57fcddce78544314`

```dockerfile
```

-	Layers:
	-	`sha256:08c9a4b6985e36a61653124f873ba55bc2efdbde1f232da7d13ec538cc4ac84a`  
		Last Modified: Fri, 14 Nov 2025 03:28:07 GMT  
		Size: 726.6 KB (726616 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31b9ee9728e87cc6802c23eaec08323bba6345ecc79beeb44800955a8aaa988a`  
		Last Modified: Fri, 14 Nov 2025 03:28:08 GMT  
		Size: 16.4 KB (16361 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-17-alpine` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:622a8c6a7a888fdbeee13b34d5c4891c18408a25076b561f029f357f958e93f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.5 MB (162496881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71dddc0cdfcd7a698638d536b1cae44226754e6fbe73f2c6c853c807bd4843e5`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 21 Oct 2025 20:48:19 GMT
ARG version=17.0.17.10.1
# Tue, 21 Oct 2025 20:48:19 GMT
# ARGS: version=17.0.17.10.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Tue, 21 Oct 2025 20:48:19 GMT
ENV LANG=C.UTF-8
# Tue, 21 Oct 2025 20:48:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 21 Oct 2025 20:48:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Fri, 14 Nov 2025 01:59:01 GMT
RUN apk add --no-cache bash openssh-client # buildkit
# Fri, 14 Nov 2025 01:59:01 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 14 Nov 2025 01:59:01 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 14 Nov 2025 01:59:01 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 14 Nov 2025 01:59:01 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 14 Nov 2025 01:59:01 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 14 Nov 2025 01:59:01 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 14 Nov 2025 01:59:01 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 14 Nov 2025 01:59:02 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Fri, 14 Nov 2025 01:59:02 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 14 Nov 2025 01:59:02 GMT
ARG MAVEN_VERSION=3.9.11
# Fri, 14 Nov 2025 01:59:02 GMT
ARG USER_HOME_DIR=/root
# Fri, 14 Nov 2025 01:59:02 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 14 Nov 2025 01:59:02 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 14 Nov 2025 01:59:02 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Sun, 07 Dec 2025 13:54:03 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c010ce05bd9b6d74dd876e5f1bce365f86d6b710a28f124ed8d1ad6dcd32407`  
		Last Modified: Tue, 21 Oct 2025 22:13:34 GMT  
		Size: 146.7 MB (146709717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89e499d56498e6bbf61e1534bc5d41e699427631fa2c551a75dfe82cee5dae36`  
		Last Modified: Fri, 14 Nov 2025 01:59:15 GMT  
		Size: 2.4 MB (2405475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d93b6664034eb18aa345174374cafc11d23fadd23a49a15732c0952f8efbfb8`  
		Last Modified: Fri, 14 Nov 2025 01:59:16 GMT  
		Size: 9.2 MB (9242577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8700d8bec470bd0db9381f8caedba7e42e6b082c3b8767d92ee6839a567220a`  
		Last Modified: Fri, 14 Nov 2025 01:59:15 GMT  
		Size: 854.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a0ba5be9e2e78389b45a4ca57f66f1522b6a4791c2b31bfba8a4744bcbc9b84`  
		Last Modified: Fri, 14 Nov 2025 01:59:15 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:3bca1b09c9d6f166591ccb2950321d787fdee0d7070273825dc3a21c1ebc1f2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **742.5 KB (742518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:885b210fb234a68abd296e19ee59d0c6ae09b16440d6f7d6786331fff60a0fdf`

```dockerfile
```

-	Layers:
	-	`sha256:f6b45de0679780542674e40735b0a0e913fe85eb27f4142800315babdd20bb34`  
		Last Modified: Fri, 14 Nov 2025 03:28:11 GMT  
		Size: 726.0 KB (726023 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34f6a6b04287f16bf2990fdffeb0d2ac2e26729898bae0d27194f83f56359ec6`  
		Last Modified: Fri, 14 Nov 2025 03:28:12 GMT  
		Size: 16.5 KB (16495 bytes)  
		MIME: application/vnd.in-toto+json
