## `maven:3-amazoncorretto-21-alpine`

```console
$ docker pull maven@sha256:b1c6098e28d3d1bf6141bd1353551fb5d36983ee79a04357e86307fd95575d22
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-21-alpine` - linux; amd64

```console
$ docker pull maven@sha256:3fa3b67894c3848f234e6c8bb8c2982ee6b6323f913947404ab1da44358c3935
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.2 MB (177184449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb669288730cf985bfda001fcd6d9b42a738c475bff5f54ffaa1eb09fdfb8783`
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
# Thu, 12 Mar 2026 20:13:26 GMT
RUN apk add --no-cache bash openssh-client # buildkit
# Thu, 12 Mar 2026 20:13:26 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Thu, 12 Mar 2026 20:13:26 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Thu, 12 Mar 2026 20:13:26 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Thu, 12 Mar 2026 20:13:26 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Thu, 12 Mar 2026 20:13:26 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 12 Mar 2026 20:13:26 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 12 Mar 2026 20:13:26 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 12 Mar 2026 20:13:26 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 12 Mar 2026 20:13:26 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 12 Mar 2026 20:13:26 GMT
ARG MAVEN_VERSION=3.9.14
# Thu, 12 Mar 2026 20:13:26 GMT
ARG USER_HOME_DIR=/root
# Thu, 12 Mar 2026 20:13:26 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 12 Mar 2026 20:13:26 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 12 Mar 2026 20:13:26 GMT
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
	-	`sha256:1a0152425803fe723f6841a920cab19819fc36ef652cf3440a2e49fff5e306c5`  
		Last Modified: Thu, 12 Mar 2026 20:13:34 GMT  
		Size: 2.4 MB (2420119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2e3456a17d4e1028515c088517498bedc8c56d74ac26f3b70be7aa1028833d9`  
		Last Modified: Thu, 12 Mar 2026 20:13:34 GMT  
		Size: 9.3 MB (9311179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59009272078e3b14808361c67aa454debaeac086b76f0313ab4d20b7d813f1b8`  
		Last Modified: Thu, 12 Mar 2026 20:13:34 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d1f9e7dc705faf82f234f6001bc591512cfa9d9af3d16d4dbe91004425a9409`  
		Last Modified: Thu, 12 Mar 2026 20:13:34 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-21-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:c9f59df55b2d93af61db90ce9bf8837c5b467d1f492c60e6be9c7f1cbcd1b6fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **744.0 KB (743977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a01110c5c1537db3c077d59a6c76d548434508e8f68581ae1ecb2fda2e66fb8`

```dockerfile
```

-	Layers:
	-	`sha256:28d05ad0e9b577bea27cc14cb9563e21844c13a8f6060b13db412a417cec38d5`  
		Last Modified: Thu, 12 Mar 2026 20:13:34 GMT  
		Size: 727.6 KB (727615 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba88970df88fbc5b44214fbac83a84819ff7455939a8a5b5f87dfab9ae822095`  
		Last Modified: Thu, 12 Mar 2026 20:13:34 GMT  
		Size: 16.4 KB (16362 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-21-alpine` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:92b38e8550c4c3754c0db53618544f612887f9d838d004d2bb0a9e6a49188e64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.6 MB (175586062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ff5a3659f74351e2add409b955bf12972ea6597d6188a8ee446e10360753ade`
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
# Thu, 12 Mar 2026 20:12:08 GMT
RUN apk add --no-cache bash openssh-client # buildkit
# Thu, 12 Mar 2026 20:12:08 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Thu, 12 Mar 2026 20:12:08 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Thu, 12 Mar 2026 20:12:08 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Thu, 12 Mar 2026 20:12:08 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Thu, 12 Mar 2026 20:12:08 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 12 Mar 2026 20:12:08 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 12 Mar 2026 20:12:08 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 12 Mar 2026 20:12:08 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 12 Mar 2026 20:12:08 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 12 Mar 2026 20:12:08 GMT
ARG MAVEN_VERSION=3.9.14
# Thu, 12 Mar 2026 20:12:08 GMT
ARG USER_HOME_DIR=/root
# Thu, 12 Mar 2026 20:12:08 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 12 Mar 2026 20:12:08 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 12 Mar 2026 20:12:08 GMT
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
	-	`sha256:50e54caf4a8591f4be31b47d4098930ff25b6d9d9b64af960943ca35e46d8306`  
		Last Modified: Thu, 12 Mar 2026 20:12:16 GMT  
		Size: 2.5 MB (2461155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:180910d56d8dddc170a4df13b3bd661602507dd5d1e8c2474f1f7704ed315ccb`  
		Last Modified: Thu, 12 Mar 2026 20:12:16 GMT  
		Size: 9.3 MB (9311185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7198294b426477b19c8dcb6f57bc0d582ac670826c9fa3ec9fd8f94616b87787`  
		Last Modified: Thu, 12 Mar 2026 20:12:16 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19dc366d0387bbb1b670c1c463f6c91bec969399c7c217b4846f2b65c5644ef5`  
		Last Modified: Thu, 12 Mar 2026 20:12:16 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-21-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:662159b1dbe3961c131ed7c92a6679efa15297a3036250fb932c2388ca11ad2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **742.9 KB (742867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc7d413c365033725a23ae901db61055e4ecbeef92f212fc47ac62392cede4ad`

```dockerfile
```

-	Layers:
	-	`sha256:36f1ae907a6afe9acb18b7064cf05a7f08805db51dbdabd3d535459791843346`  
		Last Modified: Thu, 12 Mar 2026 20:12:16 GMT  
		Size: 726.4 KB (726372 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:713ce8a925fcbb22331c7385e9d1ce45cc8279ae35f484e4ef68f3452693ba7e`  
		Last Modified: Thu, 12 Mar 2026 20:12:16 GMT  
		Size: 16.5 KB (16495 bytes)  
		MIME: application/vnd.in-toto+json
