## `maven:3-amazoncorretto-25-alpine`

```console
$ docker pull maven@sha256:4819a501b772555133b085912e66bd3e2eff5a0df12eb568370b24ae31d6b7f4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-25-alpine` - linux; amd64

```console
$ docker pull maven@sha256:25b50ae7f2c10289c93d1198aa68a977b722fb4c57986063df38257302f43843
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.2 MB (196216318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9991a32014916dfec71e045a93139b8541ea22859f2db477cd4fc3b2712341fd`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 05 Nov 2025 01:07:20 GMT
ARG version=25.0.1.9.1
# Wed, 05 Nov 2025 01:07:20 GMT
# ARGS: version=25.0.1.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-25=$version-r0 &&     rm -rf /usr/lib/jvm/java-25-amazon-corretto/lib/src.zip # buildkit
# Wed, 05 Nov 2025 01:07:20 GMT
ENV LANG=C.UTF-8
# Wed, 05 Nov 2025 01:07:20 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 05 Nov 2025 01:07:20 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Fri, 16 Jan 2026 02:46:12 GMT
RUN apk add --no-cache bash openssh-client # buildkit
# Fri, 16 Jan 2026 02:46:12 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 16 Jan 2026 02:46:12 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 16 Jan 2026 02:46:12 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 16 Jan 2026 02:46:12 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 16 Jan 2026 02:46:12 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 16 Jan 2026 02:46:12 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 16 Jan 2026 02:46:12 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 16 Jan 2026 02:46:12 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Fri, 16 Jan 2026 02:46:13 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 16 Jan 2026 02:46:13 GMT
ARG MAVEN_VERSION=3.9.12
# Fri, 16 Jan 2026 02:46:13 GMT
ARG USER_HOME_DIR=/root
# Fri, 16 Jan 2026 02:46:13 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 16 Jan 2026 02:46:13 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 16 Jan 2026 02:46:13 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:21 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39efdfa875cf11df5af65d4582d8a8c511a684ff9b183b51bad538fe768d8495`  
		Last Modified: Wed, 05 Nov 2025 01:07:40 GMT  
		Size: 180.7 MB (180725412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69ab5ae71ab7237191f599a2ee27d543e27597056eee92149bf606a1899e5cef`  
		Last Modified: Fri, 16 Jan 2026 02:46:28 GMT  
		Size: 2.4 MB (2375162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa616bc0f4a2b431370cc1a294886ed5226a2c6a81e4424814cca88d9ec8d7f5`  
		Last Modified: Fri, 16 Jan 2026 02:46:29 GMT  
		Size: 9.3 MB (9312251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ffd6af2546a45e0df0a05857f8d6025673a6dd93f8b08fe4c0adef4d0d2ecaf`  
		Last Modified: Fri, 16 Jan 2026 02:46:20 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7d34eee0c1db516a1443a1c4616989e6be60ef272bf797e4b9af1a25357b6b8`  
		Last Modified: Fri, 16 Jan 2026 02:46:20 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-25-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:9eece4b61131d078385e495bd9517e62749ee2062ec52bafbf436dccfb0bd995
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **752.0 KB (751988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7360f45f42bdfec42b4f847da46b6fe1db93ce6bc01342e48321cf1b2d1543ce`

```dockerfile
```

-	Layers:
	-	`sha256:600337621620d60c0f69a0ed9293a7d2d96228eadb990f0b8cc491cee7e94ee6`  
		Last Modified: Fri, 16 Jan 2026 02:46:20 GMT  
		Size: 735.6 KB (735626 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1ef5ad5cac85b59e6d6e69d7af7cf43426dd865792ffe246d65ea3d9d92f057`  
		Last Modified: Fri, 16 Jan 2026 02:46:20 GMT  
		Size: 16.4 KB (16362 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-25-alpine` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:f08c318964dffa8ad7bfade33df81d1c8de504f46d3abd4725355aaac256ea3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.2 MB (194229279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fac8bc48fe98cefd35796e60b09da5382e4ac3590e43a3fd49629da0559eba40`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 04 Nov 2025 23:16:08 GMT
ARG version=25.0.1.9.1
# Tue, 04 Nov 2025 23:16:08 GMT
# ARGS: version=25.0.1.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-25=$version-r0 &&     rm -rf /usr/lib/jvm/java-25-amazon-corretto/lib/src.zip # buildkit
# Tue, 04 Nov 2025 23:16:08 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 23:16:08 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 04 Nov 2025 23:16:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Fri, 16 Jan 2026 03:32:45 GMT
RUN apk add --no-cache bash openssh-client # buildkit
# Fri, 16 Jan 2026 03:32:45 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 16 Jan 2026 03:32:45 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 16 Jan 2026 03:32:45 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 16 Jan 2026 03:32:45 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 16 Jan 2026 03:32:45 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 16 Jan 2026 03:32:45 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 16 Jan 2026 03:32:46 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 16 Jan 2026 03:32:46 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Fri, 16 Jan 2026 03:32:46 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 16 Jan 2026 03:32:46 GMT
ARG MAVEN_VERSION=3.9.12
# Fri, 16 Jan 2026 03:32:46 GMT
ARG USER_HOME_DIR=/root
# Fri, 16 Jan 2026 03:32:46 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 16 Jan 2026 03:32:46 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 16 Jan 2026 03:32:46 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:11 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6c3d1078166ba6eb65daea030105157330eb50995e58c176b24e5eb82842fb4`  
		Last Modified: Sun, 04 Jan 2026 04:37:45 GMT  
		Size: 178.4 MB (178371636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c20c8f11eae94d1e99053251df0ea2d9a99b7511111416cbeb4fa60f77116f09`  
		Last Modified: Fri, 16 Jan 2026 03:32:53 GMT  
		Size: 2.4 MB (2406293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b39e66ffc6a06dceee77d9ad3ad89d04c038f8844d34ad8d4f79cc98f8600a31`  
		Last Modified: Fri, 16 Jan 2026 03:32:54 GMT  
		Size: 9.3 MB (9312242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce31d45358823b74ece92a77ada38eba053ceb351bd7647edf324173cb2a75a4`  
		Last Modified: Fri, 16 Jan 2026 03:32:53 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec5cc9021c635b882983af662cdf6fa3aa5b5d8ac0ece3e34416e8d8940a6ad6`  
		Last Modified: Fri, 16 Jan 2026 03:32:53 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-25-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:d9637d15a87b06f507e94f436acb9a28bc9ca11881d1b50a2f82c01e445a4330
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **751.5 KB (751525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b60a00ecbf77765b21026d953133a54c09e85acf422a949c1537084c40955d0`

```dockerfile
```

-	Layers:
	-	`sha256:dec49b4728839895cb4dca7f57fe20edf2e1112a7cc2670efe19d8ca05a70b8d`  
		Last Modified: Fri, 16 Jan 2026 06:28:53 GMT  
		Size: 735.0 KB (735030 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee6ebb0860dd4d0437571c55f70a1db990b42a9658f8f3a19c32481b34166139`  
		Last Modified: Fri, 16 Jan 2026 06:28:54 GMT  
		Size: 16.5 KB (16495 bytes)  
		MIME: application/vnd.in-toto+json
