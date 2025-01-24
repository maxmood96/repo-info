## `maven:3-amazoncorretto-23-alpine`

```console
$ docker pull maven@sha256:540f5b19767c1a43b5ad63a511ffc98fe66a86947b439ecb9e502ee1eb326b94
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-23-alpine` - linux; amd64

```console
$ docker pull maven@sha256:37da97dd996a05762b6645368d26a8e62517358a429e0f6ccdc5be74de99f7b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.8 MB (181804731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37deaf60b14cac19f34909bcf6b1683554f02c96a995db06e3102ae03a390f4d`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 24 Sep 2024 11:57:06 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Tue, 24 Sep 2024 11:57:06 GMT
CMD ["/bin/sh"]
# Tue, 24 Sep 2024 11:57:06 GMT
ARG version=23.0.2.7.1
# Tue, 24 Sep 2024 11:57:06 GMT
# ARGS: version=23.0.2.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-23=$version-r0 &&     rm -rf /usr/lib/jvm/java-23-amazon-corretto/lib/src.zip # buildkit
# Tue, 24 Sep 2024 11:57:06 GMT
ENV LANG=C.UTF-8
# Tue, 24 Sep 2024 11:57:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 24 Sep 2024 11:57:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Tue, 24 Sep 2024 11:57:06 GMT
RUN apk add --no-cache bash openssh-client # buildkit
# Tue, 24 Sep 2024 11:57:06 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 24 Sep 2024 11:57:06 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 24 Sep 2024 11:57:06 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 24 Sep 2024 11:57:06 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 24 Sep 2024 11:57:06 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 24 Sep 2024 11:57:06 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 24 Sep 2024 11:57:06 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 24 Sep 2024 11:57:06 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 24 Sep 2024 11:57:06 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 24 Sep 2024 11:57:06 GMT
ARG MAVEN_VERSION=3.9.9
# Tue, 24 Sep 2024 11:57:06 GMT
ARG USER_HOME_DIR=/root
# Tue, 24 Sep 2024 11:57:06 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 24 Sep 2024 11:57:06 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 24 Sep 2024 11:57:06 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Wed, 08 Jan 2025 15:55:45 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:586601369655864cd8664041a64a90e1b83d320f2f7c255ecc58d4384aefa9c1`  
		Last Modified: Thu, 23 Jan 2025 18:27:47 GMT  
		Size: 166.7 MB (166687306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab06ec5c60e0d7a1511cb0664695978e462d3f2fa718d1a86f6cd055d56c2f3f`  
		Last Modified: Thu, 23 Jan 2025 19:27:00 GMT  
		Size: 2.3 MB (2319693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f280d25c272c6219a22bba1f05f2ab76b62b01edbbd50c59a4d7560aa729363c`  
		Last Modified: Thu, 23 Jan 2025 19:27:00 GMT  
		Size: 9.2 MB (9170435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89d95f5e247bf24adf37677f22b74dfe314f16c4eb055e6fff7f06273bc88a26`  
		Last Modified: Thu, 23 Jan 2025 19:26:58 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e707462fac32e073040f57acb0a21ad0af58f6c2a2fb729b6acf1e9f17d312a8`  
		Last Modified: Thu, 23 Jan 2025 19:27:00 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-23-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:c3f7c4f102cd6372e2e4431eca0f8c08cc4b41603d913ef2e3daafa6cb395587
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **533.7 KB (533679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb67bbd7787f4eb2956c961ef2ba3b673f06ea412e5db4ab81a8f16a2f32cf4c`

```dockerfile
```

-	Layers:
	-	`sha256:ccf276b5f8ff3f6ec39c387a9ed2129acd50108a7a1b2e64bf8666c1f291af67`  
		Last Modified: Thu, 23 Jan 2025 19:27:00 GMT  
		Size: 517.3 KB (517281 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebbc7655dedb137b66c2ad8d9155611c6332d4f2d094ce74560f902405921e62`  
		Last Modified: Thu, 23 Jan 2025 19:26:59 GMT  
		Size: 16.4 KB (16398 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-23-alpine` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:1e5a70d7e0a4fe2bec1c9cca811ccbc5a5822f00299cd71a8cb7388aeb1a8048
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.1 MB (180054255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87f6fa238854de5e0399413ea95e26774bcef41f8f6f1d2a8e6790c4196192cb`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 24 Sep 2024 11:57:06 GMT
ADD alpine-minirootfs-3.20.5-aarch64.tar.gz / # buildkit
# Tue, 24 Sep 2024 11:57:06 GMT
CMD ["/bin/sh"]
# Tue, 24 Sep 2024 11:57:06 GMT
ARG version=23.0.2.7.1
# Tue, 24 Sep 2024 11:57:06 GMT
# ARGS: version=23.0.2.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-23=$version-r0 &&     rm -rf /usr/lib/jvm/java-23-amazon-corretto/lib/src.zip # buildkit
# Tue, 24 Sep 2024 11:57:06 GMT
ENV LANG=C.UTF-8
# Tue, 24 Sep 2024 11:57:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 24 Sep 2024 11:57:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Tue, 24 Sep 2024 11:57:06 GMT
RUN apk add --no-cache bash openssh-client # buildkit
# Tue, 24 Sep 2024 11:57:06 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 24 Sep 2024 11:57:06 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 24 Sep 2024 11:57:06 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 24 Sep 2024 11:57:06 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 24 Sep 2024 11:57:06 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 24 Sep 2024 11:57:06 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 24 Sep 2024 11:57:06 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 24 Sep 2024 11:57:06 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 24 Sep 2024 11:57:06 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 24 Sep 2024 11:57:06 GMT
ARG MAVEN_VERSION=3.9.9
# Tue, 24 Sep 2024 11:57:06 GMT
ARG USER_HOME_DIR=/root
# Tue, 24 Sep 2024 11:57:06 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 24 Sep 2024 11:57:06 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 24 Sep 2024 11:57:06 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:0152682790bba2052e0b7dc52872083c01ea53c598fe87e3fe3eab5f9d4228cb`  
		Last Modified: Wed, 08 Jan 2025 17:24:05 GMT  
		Size: 4.1 MB (4090769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d8a1b77d8fb2973a5165487ae4f9ba602b01b62aa495d03847f6a44857d4e29`  
		Last Modified: Thu, 23 Jan 2025 18:58:18 GMT  
		Size: 164.4 MB (164408329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f30312c5d677563b114a4ad80a94a73576c29b6c915ebc47cc8abf94cc7ee2e5`  
		Last Modified: Thu, 23 Jan 2025 20:01:13 GMT  
		Size: 2.4 MB (2383682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdc4ad2ee493f9b787ae9d6d9fe0ca209fa48e91e84d38f7308499b810460550`  
		Last Modified: Thu, 23 Jan 2025 20:01:14 GMT  
		Size: 9.2 MB (9170435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bcbeb101b5ca08b0cccea928ce1bf8b36922645daf9a538e5796889e17338f5`  
		Last Modified: Thu, 23 Jan 2025 20:01:13 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbaab11a8ef36b78048c1482a8de69e12c829dc95defe282072cbae4cecf124f`  
		Last Modified: Thu, 23 Jan 2025 20:01:14 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-23-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:1a7c22a8305490aae268c858fa3a7cc5b0f0615063a6ad385fed6de3ea2835ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **532.6 KB (532579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9d46f0b0279d6a688df5f5318f6e5de2b0670ced0b7de019e2611d1e5aedc8f`

```dockerfile
```

-	Layers:
	-	`sha256:b78973913cbe1c6c885b1cae31b21b9d9a537cb2044294f87b6bd2006aac071c`  
		Last Modified: Thu, 23 Jan 2025 20:01:13 GMT  
		Size: 516.0 KB (516048 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2718af8c7b2d270ea262a8db2d132d61fbb387f54b196c3eb19276242fbab2cd`  
		Last Modified: Thu, 23 Jan 2025 20:01:13 GMT  
		Size: 16.5 KB (16531 bytes)  
		MIME: application/vnd.in-toto+json
