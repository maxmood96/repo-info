## `maven:3-amazoncorretto-8-alpine`

```console
$ docker pull maven@sha256:6f7f539e14a8c3c9d2d7aba5bcaec8d5f7425815af1836e573737001b2ed6347
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-8-alpine` - linux; amd64

```console
$ docker pull maven@sha256:4d95203ad528ecb5ea807038c666723217a678c5373d466dc7ab3b3148ef11d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 MB (115340924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0af69fe506ded002c17202bf686d2806db6ba56e85025ec0cb799a5939173b9b`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 24 Sep 2024 11:57:06 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Tue, 24 Sep 2024 11:57:06 GMT
CMD ["/bin/sh"]
# Tue, 24 Sep 2024 11:57:06 GMT
ARG version=8.442.06.1
# Tue, 24 Sep 2024 11:57:06 GMT
# ARGS: version=8.442.06.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
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
	-	`sha256:d9000c39c2c168206c9f08f2a7a337e88e644ccc0d1c2711f8703c083c38b26e`  
		Last Modified: Thu, 23 Jan 2025 18:26:59 GMT  
		Size: 100.2 MB (100224365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9a29799561672670f8f179ec47e009fef12991ba5fa7bc01461eff6498d1418`  
		Last Modified: Thu, 23 Jan 2025 19:27:43 GMT  
		Size: 2.3 MB (2318822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:878c14fd7eb716b4a0372866d5051327587f2c1d9a63873b9926f4653a04ee7f`  
		Last Modified: Thu, 23 Jan 2025 19:27:43 GMT  
		Size: 9.2 MB (9170438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52fede84a756b1bc8d59b4021d14cfaed17b6258b185de8c2b662260bacfd159`  
		Last Modified: Thu, 23 Jan 2025 19:27:43 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc09e27bb0170192d36a380d6aa31bfb42ce010f0c3a86debd26d0a2be8d50f7`  
		Last Modified: Thu, 23 Jan 2025 19:27:43 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:8dbbd3b2d5597208e2dd76bc06f1b374b431c8f4d0f5eb0e350034230416185b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.6 KB (396563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b21242ee94674a5b2f4957035a2eb473a5be34e23445f1d63d05a3ee8582b2f`

```dockerfile
```

-	Layers:
	-	`sha256:4f46bfb9dce3f196ee9cdf7a8da2a3b609503257878b92fee8f795af47043fcc`  
		Last Modified: Thu, 23 Jan 2025 19:27:43 GMT  
		Size: 380.2 KB (380178 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ec4cf391cb7bbc959f59f6bf2cabe4e0484d80199eb7d9e3448fc8669254c41`  
		Last Modified: Thu, 23 Jan 2025 19:27:43 GMT  
		Size: 16.4 KB (16385 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-8-alpine` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:e94fa98d22d65521eef691c0d3d959db82ca6b87be61d239bdb414b6b3bf7da6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.7 MB (115653049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ffb2ba696b2824d70705dc9222bd5977fb741866330bc4c7bfd6f77f201b341`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 24 Sep 2024 11:57:06 GMT
ADD alpine-minirootfs-3.20.5-aarch64.tar.gz / # buildkit
# Tue, 24 Sep 2024 11:57:06 GMT
CMD ["/bin/sh"]
# Tue, 24 Sep 2024 11:57:06 GMT
ARG version=8.442.06.1
# Tue, 24 Sep 2024 11:57:06 GMT
# ARGS: version=8.442.06.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
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
	-	`sha256:3f7095b8d01767496a8a3b5354570296d6bea31e7dd4414ce5cd6f039faa159f`  
		Last Modified: Thu, 23 Jan 2025 18:33:36 GMT  
		Size: 100.0 MB (100010072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e496f77555b449da1b125db2a222d73d8f5eb403bc60d42193805dd8122dfcc7`  
		Last Modified: Thu, 23 Jan 2025 20:03:44 GMT  
		Size: 2.4 MB (2380732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9af3033106ca463199e6764b159e7cb521749c6019e7372903471eeeb191a559`  
		Last Modified: Thu, 23 Jan 2025 20:03:44 GMT  
		Size: 9.2 MB (9170435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a453c4938a6549d02680e13dd61ca64453b10fda49e6aed97d5eda932faf22a3`  
		Last Modified: Thu, 23 Jan 2025 20:03:44 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a32bbbdbe785b7f499c5f4d5ade4e834e7a8eafec60ba0fdf958642ddfcc83c9`  
		Last Modified: Thu, 23 Jan 2025 20:03:44 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:7944d5067b0100b49f38c7a354bacacf89189966209dea90dd2fa68e9036974f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.8 KB (396815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5eeae76b916416474ce935f2b0945cab7842b3d03ae307829c88736bc86b4da`

```dockerfile
```

-	Layers:
	-	`sha256:ac2b3fa5ca94f012319ae33e8d40999533e5b7a77b7573f5a0be08cdf3d55177`  
		Last Modified: Thu, 23 Jan 2025 20:03:44 GMT  
		Size: 380.3 KB (380298 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57a3bd387f58dc9078dcf1444a3a7a20b68aae8432eae4cfd8ccb2d8196b6d95`  
		Last Modified: Thu, 23 Jan 2025 20:03:43 GMT  
		Size: 16.5 KB (16517 bytes)  
		MIME: application/vnd.in-toto+json
