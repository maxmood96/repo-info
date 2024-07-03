## `maven:3-eclipse-temurin-21-alpine`

```console
$ docker pull maven@sha256:4b910e445bdb31e5dd5f2ceadbae8671f423633d2f6ba09827ef4bb5a39a0639
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-eclipse-temurin-21-alpine` - linux; amd64

```console
$ docker pull maven@sha256:3f349873e6e82549c0dc95d4b0f48456314e8487d528b75aa2928f2d6b8311fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.1 MB (187074349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bec7cf5a88e90044e7eb1ac23b3cd54571f3fba9806ed0075e98807918fc586`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 20 Jun 2024 20:17:04 GMT
ADD file:fb066571462e703f86645131b43d211ff8531ffac77ea394456bfe569a6f17fe in / 
# Thu, 20 Jun 2024 20:17:04 GMT
CMD ["/bin/sh"]
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 Apr 2024 20:51:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Apr 2024 20:51:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata     ;     rm -rf /var/cache/apk/* # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_VERSION=jdk-21.0.3+9
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64|arm64)          ESUM='0f68a9122054149861f6ce9d1b1c176bbe30dd76b36b74c916ba897c12e9d970';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jdk_aarch64_alpine-linux_hotspot_21.0.3_9.tar.gz';          ;;        amd64|x86_64)          ESUM='8e861638bf6b08c6d5837de6dc929930550928ec5fcc81b9fa7e8296afd0f9c0';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jdk_x64_alpine-linux_hotspot_21.0.3_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 23 Apr 2024 20:51:38 GMT
CMD ["jshell"]
# Thu, 27 Jun 2024 09:17:07 GMT
RUN apk add --no-cache bash procps curl tar # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Thu, 27 Jun 2024 09:17:07 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 27 Jun 2024 09:17:07 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
ARG MAVEN_VERSION=3.9.8
# Thu, 27 Jun 2024 09:17:07 GMT
ARG USER_HOME_DIR=/root
# Thu, 27 Jun 2024 09:17:07 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 27 Jun 2024 09:17:07 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 27 Jun 2024 09:17:07 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:b84a74cde5af5c5199bfc2ce2a8c8951a29a7716d17327e923f1a14c870a858b`  
		Last Modified: Thu, 20 Jun 2024 20:17:43 GMT  
		Size: 3.4 MB (3417332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60acd7138d3e0a8e35e097d75b62e0b1cfd99cdad83e29656157ec622e1c51e2`  
		Last Modified: Mon, 24 Jun 2024 16:42:45 GMT  
		Size: 13.1 MB (13142550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dc2499efbfe7968f2522df896fbe2f8a8c2134f7cc93e191f836eec5d02edb4`  
		Last Modified: Mon, 24 Jun 2024 16:43:37 GMT  
		Size: 158.7 MB (158716169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21c492bf7da0e834114a9d2878918d8cfe522854c4df9fc7730e2f4b72b32775`  
		Last Modified: Mon, 24 Jun 2024 16:43:24 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d851ea679543ce279a7828ea806caaaa880c9ae89f2ded39374d44dd11a2fd2`  
		Last Modified: Mon, 24 Jun 2024 16:43:24 GMT  
		Size: 717.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:400ea5878bd3fa6dd6349c2f6691b9fccf7dad84d5bf6ab71bdb41e9966bc75d`  
		Last Modified: Tue, 02 Jul 2024 09:09:06 GMT  
		Size: 2.6 MB (2634561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8e00dd7823a38b21ad511951803f3011a565487bbee343f60d2690e59b30cdd`  
		Last Modified: Tue, 02 Jul 2024 09:09:06 GMT  
		Size: 9.2 MB (9161815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf32fa2f80c32339676f54a24509dc479a8e0b197bef3266dc576290dbbff898`  
		Last Modified: Tue, 02 Jul 2024 09:09:06 GMT  
		Size: 857.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afacf042c3113c21ef5be1dc8d91cbb622ab263ec975edefb3304af74d100fad`  
		Last Modified: Tue, 02 Jul 2024 09:09:05 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-21-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:74d1379065cdd34ab03d04c6912fc0b06659bcd6b614bccc782293dd1689ce8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1322012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52afc4da0d68ee8cbfdf2917580d54cb24f4c40b339ba8b90c8d4d2a1bbb662e`

```dockerfile
```

-	Layers:
	-	`sha256:3b0d5d42ec4344b6b0ce3dd234ec3d63348718aaa69c6e2a034f268ccb01b96c`  
		Last Modified: Tue, 02 Jul 2024 09:09:05 GMT  
		Size: 1.3 MB (1302696 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b029369b767fbd1002d09ff2e9021c9e6b10ffe7bd8eb819bddbcd6fdb4bf510`  
		Last Modified: Tue, 02 Jul 2024 09:09:05 GMT  
		Size: 19.3 KB (19316 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-eclipse-temurin-21-alpine` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:6ba7619eac2e52e185ffe08650fa3370a06c2287e1ddd007c7afd302b9a8c819
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.4 MB (185377131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a2a54f7fc17e7cbfcfa5cdbee40a0ef2e963a95bf323e72b26fc69ad90c5a63`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 20 Jun 2024 17:40:38 GMT
ADD file:f5632bd5469a9b26f7ff1739bb0b5dd166613259104f7bf76d587a8a428debcc in / 
# Thu, 20 Jun 2024 17:40:38 GMT
CMD ["/bin/sh"]
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 Apr 2024 20:51:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Apr 2024 20:51:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata     ;     rm -rf /var/cache/apk/* # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_VERSION=jdk-21.0.3+9
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64|arm64)          ESUM='0f68a9122054149861f6ce9d1b1c176bbe30dd76b36b74c916ba897c12e9d970';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jdk_aarch64_alpine-linux_hotspot_21.0.3_9.tar.gz';          ;;        amd64|x86_64)          ESUM='8e861638bf6b08c6d5837de6dc929930550928ec5fcc81b9fa7e8296afd0f9c0';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jdk_x64_alpine-linux_hotspot_21.0.3_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 23 Apr 2024 20:51:38 GMT
CMD ["jshell"]
# Thu, 27 Jun 2024 09:17:07 GMT
RUN apk add --no-cache bash procps curl tar # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Thu, 27 Jun 2024 09:17:07 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 27 Jun 2024 09:17:07 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
ARG MAVEN_VERSION=3.9.8
# Thu, 27 Jun 2024 09:17:07 GMT
ARG USER_HOME_DIR=/root
# Thu, 27 Jun 2024 09:17:07 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 27 Jun 2024 09:17:07 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 27 Jun 2024 09:17:07 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:d4f2d2bd5ed999e04bfbfb910f14154b488ad32abf053954bff805f47fc3ad1e`  
		Last Modified: Thu, 20 Jun 2024 17:41:12 GMT  
		Size: 3.4 MB (3357202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6db88ea1e6a26d6517be6a6098be6964b10513b0bfdfea893bc9752c9c04b6e1`  
		Last Modified: Thu, 20 Jun 2024 19:04:39 GMT  
		Size: 13.4 MB (13425513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66b0682e580b8b1aea7e2a977909ae9bbc90e100935552a7b6421a8e6dc7d1b6`  
		Last Modified: Thu, 20 Jun 2024 19:04:48 GMT  
		Size: 156.6 MB (156642191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5483442b5e5e84e7ae2ea9fae5136bd6c4f733ea6148becc7c0957531e3cd47d`  
		Last Modified: Thu, 20 Jun 2024 19:04:37 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:133900c1550c17ba4fc70c056a0119b660f80ef8f03f73d3a2cf42e890cb8136`  
		Last Modified: Thu, 20 Jun 2024 19:04:37 GMT  
		Size: 717.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:220dcbaf368e7f9a4bbf87fcd6d6b1c429af01f73574661418dc9568e1255518`  
		Last Modified: Wed, 03 Jul 2024 10:24:17 GMT  
		Size: 2.8 MB (2788529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a1bc6d74ceace19ce6582c6008b64c5081fae8ac87e24919fc617a25a971085`  
		Last Modified: Wed, 03 Jul 2024 10:24:17 GMT  
		Size: 9.2 MB (9161772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5743d2810f10cdd9bdcc2dac4901f1dcfcba437df9e653c66b23030a96441782`  
		Last Modified: Wed, 03 Jul 2024 10:24:16 GMT  
		Size: 860.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72180dc359cee8e6b3fceb2400c3b68cf8a92ca8967d4e8641de077bb21d8351`  
		Last Modified: Wed, 03 Jul 2024 10:24:17 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-21-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:06bf940301ad2f189de137770d6cc9e1280cbf15e96d5f78f1810bfab4000dd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.4 MB (1427969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3716ee77ca612b6dce2e61050f072748dfb1657262009056981896841aea514`

```dockerfile
```

-	Layers:
	-	`sha256:e75d99f743641d47e8176886a294c3355f71bcae338833f4199286af56dc4270`  
		Last Modified: Wed, 03 Jul 2024 10:24:17 GMT  
		Size: 1.4 MB (1407995 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9274087fe6cd1d816ec50918627f3df44746cb136541f307eca2a02d868a7660`  
		Last Modified: Wed, 03 Jul 2024 10:24:16 GMT  
		Size: 20.0 KB (19974 bytes)  
		MIME: application/vnd.in-toto+json
