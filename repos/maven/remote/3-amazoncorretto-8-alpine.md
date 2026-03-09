## `maven:3-amazoncorretto-8-alpine`

```console
$ docker pull maven@sha256:2c99d579c949ad625d59ca117f1ad85ce95a40ee53b1b6b648e0ec6c540270a4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-8-alpine` - linux; amd64

```console
$ docker pull maven@sha256:74d2e1e6624db63134568a38b3d7b26f6b8d0b13a049c4ed8632670463a94ce2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.7 MB (116743451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c962d847d61f07fdb7e661e315f3ba8cdeb860c0c49ad23fd4c4b41f811ef0d`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:43:25 GMT
ARG version=8.482.08.1
# Wed, 28 Jan 2026 02:43:25 GMT
# ARGS: version=8.482.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 28 Jan 2026 02:43:25 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:43:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 28 Jan 2026 02:43:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Mon, 09 Mar 2026 19:14:46 GMT
RUN apk add --no-cache bash openssh-client # buildkit
# Mon, 09 Mar 2026 19:14:46 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 09 Mar 2026 19:14:46 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 09 Mar 2026 19:14:46 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 09 Mar 2026 19:14:46 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 09 Mar 2026 19:14:46 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 09 Mar 2026 19:14:46 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 09 Mar 2026 19:14:46 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 09 Mar 2026 19:14:46 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 09 Mar 2026 19:14:46 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 09 Mar 2026 19:14:46 GMT
ARG MAVEN_VERSION=3.9.13
# Mon, 09 Mar 2026 19:14:46 GMT
ARG USER_HOME_DIR=/root
# Mon, 09 Mar 2026 19:14:46 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 09 Mar 2026 19:14:46 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 09 Mar 2026 19:14:46 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c6833e8b5869e0f48dfb0827fe8ce0f2ec7bc4abc9a375d40ddca18d755ab20`  
		Last Modified: Wed, 28 Jan 2026 02:43:38 GMT  
		Size: 100.8 MB (100776920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0efd67d6c12f654d2fe4fd91f09887d7600fdbff89f84b2e5ea5d9fc083a5eee`  
		Last Modified: Mon, 09 Mar 2026 19:14:53 GMT  
		Size: 2.4 MB (2406153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e44fc2476b682128613d6642386491b3932e798c217a3bf80cd3147b71737134`  
		Last Modified: Mon, 09 Mar 2026 19:14:54 GMT  
		Size: 9.7 MB (9697517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:223d45962778a39a949d54e8c769881a203b29482fb13b1c8fb84eded912374d`  
		Last Modified: Mon, 09 Mar 2026 19:14:53 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbee05abbb7bccd72e881a252c17b9b046316b633117d8021bb71aa4a4fa310e`  
		Last Modified: Mon, 09 Mar 2026 19:14:53 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:cfd918e83a6799b8052235e1ee8782d0b5ac5276b02502795bf6321d9c3c5469
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **415.1 KB (415095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fe89802ce49c8a5f268c6bdbf3cb114ab06d9ebc517740ea8edf24d1bf58028`

```dockerfile
```

-	Layers:
	-	`sha256:3ff6c680b5bfe95c8e06391582c186376c4d9612f83dbd5779dc84796a13869e`  
		Last Modified: Mon, 09 Mar 2026 19:14:53 GMT  
		Size: 398.7 KB (398743 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f8993feac14302966d86e071312cf372f376f0e501bec39b74cb29455c4c8ec`  
		Last Modified: Mon, 09 Mar 2026 19:14:53 GMT  
		Size: 16.4 KB (16352 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-8-alpine` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:701251952759eb463632bdd02df827d68442d04cb298c15f8c012c6becc98484
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.9 MB (116908122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bf7e786152fae31d88201521377a86b310b5fef3012698eaa77231ee7e57667`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:44:37 GMT
ARG version=8.482.08.1
# Wed, 28 Jan 2026 02:44:37 GMT
# ARGS: version=8.482.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 28 Jan 2026 02:44:37 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:44:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 28 Jan 2026 02:44:37 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Mon, 09 Mar 2026 19:14:17 GMT
RUN apk add --no-cache bash openssh-client # buildkit
# Mon, 09 Mar 2026 19:14:17 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 09 Mar 2026 19:14:17 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 09 Mar 2026 19:14:17 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 09 Mar 2026 19:14:17 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 09 Mar 2026 19:14:17 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 09 Mar 2026 19:14:17 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 09 Mar 2026 19:14:17 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 09 Mar 2026 19:14:17 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 09 Mar 2026 19:14:17 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 09 Mar 2026 19:14:17 GMT
ARG MAVEN_VERSION=3.9.13
# Mon, 09 Mar 2026 19:14:17 GMT
ARG USER_HOME_DIR=/root
# Mon, 09 Mar 2026 19:14:17 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 09 Mar 2026 19:14:17 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 09 Mar 2026 19:14:17 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6de2205b433b6497cae9348f3c144e29b2543b5f31a88ac9bd1041c4ca96f43`  
		Last Modified: Wed, 28 Jan 2026 02:44:51 GMT  
		Size: 100.6 MB (100563666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5c4af485ac68a577ba9716a636c72ffac0ebeae01386cd2222513beea60f48b`  
		Last Modified: Mon, 09 Mar 2026 19:14:24 GMT  
		Size: 2.4 MB (2448773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f63189da67b16e4a16013eeacd0fb9ec8272b0273d9b5d337f07cff87d869dbb`  
		Last Modified: Mon, 09 Mar 2026 19:14:25 GMT  
		Size: 9.7 MB (9697554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e855b144368561eb16255b5163faff3f8acc9a199446c5bd613655f26d251d6c`  
		Last Modified: Mon, 09 Mar 2026 19:14:24 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:893094c0b4e388c7174ff2b279ae58c01286a036f533abf794be5827b75ef31b`  
		Last Modified: Mon, 09 Mar 2026 19:14:24 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:4c3030020631c28ce1872e7057645218e00e44990b8a32f2f79c2520dabdf66b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **414.7 KB (414699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ec36ec010eb6fc7a99c3374d885acc970f9bca877d08c61eb372645bdb5da39`

```dockerfile
```

-	Layers:
	-	`sha256:92ce4d139e47f8615b348a859ad019d786e1692bd201d1f15afadfa8b2c0dffe`  
		Last Modified: Mon, 09 Mar 2026 19:14:25 GMT  
		Size: 398.2 KB (398213 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d93204d86bd41457840fafa30d2f9a09809b8cbbe5ab5cf8c3c6a004eee08972`  
		Last Modified: Mon, 09 Mar 2026 19:14:24 GMT  
		Size: 16.5 KB (16486 bytes)  
		MIME: application/vnd.in-toto+json
