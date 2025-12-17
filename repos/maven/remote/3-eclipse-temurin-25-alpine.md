## `maven:3-eclipse-temurin-25-alpine`

```console
$ docker pull maven@sha256:9b429142f13b23ed2627052500d4804b2a24bbd74040b412f8cd059a91e19ec7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-eclipse-temurin-25-alpine` - linux; amd64

```console
$ docker pull maven@sha256:dc62635430da5c8724b18a7bbd1fe04022ad96d46f3ccbca1b13a1d845e3dbc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.1 MB (123095322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86b75161a518bac8d78bb19452a7fb3e39fe4ea4fe4b3deff5e31f0be3aec9b1`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Sat, 08 Nov 2025 18:00:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 18:00:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:00:04 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 18:00:04 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Sat, 08 Nov 2025 18:00:04 GMT
ENV JAVA_VERSION=jdk-25.0.1+8
# Sat, 08 Nov 2025 18:00:10 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='e95584c7fb7d4020003b325d5c3af9c29dde514571da362aac04586a88f2d728';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_aarch64_alpine-linux_hotspot_25.0.1_8.tar.gz';          ;;        x86_64)          ESUM='375a1f22ef1a488737330ea10bbc7418a1a49c5d0df36d4f59d18fd82fc63593';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_x64_alpine-linux_hotspot_25.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     apk add --no-cache --virtual .fetch-deps gnupg;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     apk del --no-network .fetch-deps; # buildkit
# Sat, 08 Nov 2025 18:00:11 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 18:00:11 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 18:00:11 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 18:00:11 GMT
CMD ["jshell"]
# Wed, 17 Dec 2025 20:07:19 GMT
RUN apk add --no-cache bash procps curl tar openssh-client # buildkit
# Wed, 17 Dec 2025 20:07:19 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 17 Dec 2025 20:07:19 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 17 Dec 2025 20:07:19 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 17 Dec 2025 20:07:19 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 17 Dec 2025 20:07:19 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 17 Dec 2025 20:07:19 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 17 Dec 2025 20:07:19 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 17 Dec 2025 20:07:19 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 17 Dec 2025 20:07:19 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 17 Dec 2025 20:07:19 GMT
ARG MAVEN_VERSION=3.9.12
# Wed, 17 Dec 2025 20:07:19 GMT
ARG USER_HOME_DIR=/root
# Wed, 17 Dec 2025 20:07:19 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 17 Dec 2025 20:07:19 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 17 Dec 2025 20:07:19 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Sun, 07 Dec 2025 13:53:31 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc0ab655b026e5703579820f0d4485d514c6ec9d4b5b462890ac71da2da0ae46`  
		Last Modified: Sat, 08 Nov 2025 18:00:40 GMT  
		Size: 14.2 MB (14245329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:669f1a65d0fae852f6718306326728109ed1ddecfbfd653037dda93a9669e4a7`  
		Last Modified: Sat, 08 Nov 2025 18:00:50 GMT  
		Size: 91.3 MB (91279717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f288373361582707b01fea1abf34f4ff1053f3baee5acb21cf34af46e4f8c85`  
		Last Modified: Sat, 08 Nov 2025 18:00:37 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ce3137254c0a4b1b24ea31eeee2f470985f40fee31365b16a41a6d5745dac38`  
		Last Modified: Sat, 08 Nov 2025 18:00:38 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68251857306cbb96d3e394f3fa8a9f8080f32d1d574f5070d7fd68b6e0263d80`  
		Last Modified: Wed, 17 Dec 2025 20:07:40 GMT  
		Size: 4.5 MB (4452126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e733813afc6e5b081a54c222741b807ba4d8a88de7769551270a821105ba619`  
		Last Modified: Wed, 17 Dec 2025 20:07:35 GMT  
		Size: 9.3 MB (9312244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc1dab482f2023530b9638a6c502145ce6b11092dc1029b22142690c031e1ee8`  
		Last Modified: Wed, 17 Dec 2025 20:07:34 GMT  
		Size: 860.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce81ba54dac78a5ead6e6663d53e12541d9d7dc6e63d1e87519b8c7c2431ca3c`  
		Last Modified: Wed, 17 Dec 2025 20:07:33 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-25-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:3046bfc1bcae8943a5dea23158b9d9ac952e377f86fa077e9f59e0d10a4ce76e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1138365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a91282f20c8b0f8a36512dda482c873b0d91884a20889a8626cb655a0aebcaa`

```dockerfile
```

-	Layers:
	-	`sha256:0bf65e62b12ea0af415a98c845ae9de0d637913b6a4a133b63c44319cf8c18df`  
		Last Modified: Wed, 17 Dec 2025 21:32:24 GMT  
		Size: 1.1 MB (1119026 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8f05356fe996cac4591320120a1fc23adc0790a4b989a407d99c53d9841be04`  
		Last Modified: Wed, 17 Dec 2025 21:32:25 GMT  
		Size: 19.3 KB (19339 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-eclipse-temurin-25-alpine` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:f85abdfca581ffafcdc00b6dda2eb89b94b32c890fe2b3b79a7ade46a067ee3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.5 MB (122513486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d01a4bcedd27a0c23f8d89d53e81133d8cc212e4657c07405f28828144761c8`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Sat, 08 Nov 2025 17:59:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:59:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:59:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:59:31 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Sat, 08 Nov 2025 17:59:31 GMT
ENV JAVA_VERSION=jdk-25.0.1+8
# Sat, 08 Nov 2025 17:59:40 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='e95584c7fb7d4020003b325d5c3af9c29dde514571da362aac04586a88f2d728';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_aarch64_alpine-linux_hotspot_25.0.1_8.tar.gz';          ;;        x86_64)          ESUM='375a1f22ef1a488737330ea10bbc7418a1a49c5d0df36d4f59d18fd82fc63593';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_x64_alpine-linux_hotspot_25.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     apk add --no-cache --virtual .fetch-deps gnupg;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     apk del --no-network .fetch-deps; # buildkit
# Sat, 08 Nov 2025 17:59:42 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:59:42 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:59:42 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 17:59:42 GMT
CMD ["jshell"]
# Wed, 17 Dec 2025 20:07:52 GMT
RUN apk add --no-cache bash procps curl tar openssh-client # buildkit
# Wed, 17 Dec 2025 20:07:52 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 17 Dec 2025 20:07:52 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 17 Dec 2025 20:07:52 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 17 Dec 2025 20:07:52 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 17 Dec 2025 20:07:52 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 17 Dec 2025 20:07:52 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 17 Dec 2025 20:07:52 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 17 Dec 2025 20:07:52 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 17 Dec 2025 20:07:52 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 17 Dec 2025 20:07:52 GMT
ARG MAVEN_VERSION=3.9.12
# Wed, 17 Dec 2025 20:07:52 GMT
ARG USER_HOME_DIR=/root
# Wed, 17 Dec 2025 20:07:52 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 17 Dec 2025 20:07:52 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 17 Dec 2025 20:07:52 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Sun, 07 Dec 2025 13:54:03 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:942b164f8b4d68be083596089650c1556ab1373815abc8abda59bc45d20ffd1c`  
		Last Modified: Sat, 08 Nov 2025 18:00:15 GMT  
		Size: 14.4 MB (14352513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edde8e40d136c44f0d23e0b4d7594cae8888c80bed021fac4cf5ebebb75434c1`  
		Last Modified: Sat, 08 Nov 2025 18:21:45 GMT  
		Size: 90.2 MB (90190637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13765a23e62e85c56a5a54b976e0378167533c0495d297bb429a218799ab164f`  
		Last Modified: Sat, 08 Nov 2025 18:00:05 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29c959ab9ac7fdf8f6393c84753f989ef0811ac7c86a2d184030c23e2d067c93`  
		Last Modified: Sat, 08 Nov 2025 18:00:04 GMT  
		Size: 2.3 KB (2277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6913c5ba3a6c4531c09f90edca08ca95d7e3ba9406aee3b277ea0bad4fae1d59`  
		Last Modified: Wed, 17 Dec 2025 20:08:07 GMT  
		Size: 4.5 MB (4516565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba98604bdcf3b1f533da66874bd009ba0e2d5477e09bbaaee8c7fdd01cfd058d`  
		Last Modified: Wed, 17 Dec 2025 20:08:08 GMT  
		Size: 9.3 MB (9312248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82596d430ede260a4d583869f49abdf4a3662f62bd71c1b0c20154be30287d7a`  
		Last Modified: Wed, 17 Dec 2025 20:08:07 GMT  
		Size: 861.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d9da2df2bdcf6df5eead83e2a71f4fa4e0faffb4da08264210aea244d488b62`  
		Last Modified: Wed, 17 Dec 2025 20:08:07 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-25-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:291ded0a1c30a52ff46e439713bcbcea7971722293040a8dfa66925e85d15cd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1288497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45ce7d3200f81d60d1206abcb0c8cb254d28026217986abf4741966ddedeea04`

```dockerfile
```

-	Layers:
	-	`sha256:4020ccaa23410f15ea0741b27fb39d95b87cdcf2f7826cfa236088e2cdef062d`  
		Last Modified: Wed, 17 Dec 2025 21:32:29 GMT  
		Size: 1.3 MB (1269025 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3017844d395b90bce82a9e4c8111a600a08bcfadd191a51c3c425be6f98d302d`  
		Last Modified: Wed, 17 Dec 2025 21:32:30 GMT  
		Size: 19.5 KB (19472 bytes)  
		MIME: application/vnd.in-toto+json
