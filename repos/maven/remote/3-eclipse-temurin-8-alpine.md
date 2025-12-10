## `maven:3-eclipse-temurin-8-alpine`

```console
$ docker pull maven@sha256:5bec2d68a90cfd99c5896b831272679c371f363a7c0f07b60921ba58865d1a37
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `maven:3-eclipse-temurin-8-alpine` - linux; amd64

```console
$ docker pull maven@sha256:06bcdedb783b27f415422c30a1b6a6d8aa5e747f3f59fbdfc4f36d642c2bad41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.8 MB (85778514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58c424338579b5b1d86a8ed81f091945260c920df5d682094917b657dd14cea4`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Sat, 08 Nov 2025 17:52:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:52:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:52:59 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:52:59 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Sat, 08 Nov 2025 17:52:59 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Sat, 08 Nov 2025 17:53:02 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='2ded87ce3a1f912ac7263f7df526fb0a2ccbc09a2a0124e0b35e22c3decb9bc5';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_x64_alpine-linux_hotspot_8u472b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Sat, 08 Nov 2025 17:53:02 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:53:02 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:53:02 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 14 Nov 2025 01:40:24 GMT
RUN apk add --no-cache bash procps curl tar openssh-client # buildkit
# Fri, 14 Nov 2025 01:40:24 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 14 Nov 2025 01:40:24 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 14 Nov 2025 01:40:24 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 14 Nov 2025 01:40:24 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 14 Nov 2025 01:40:24 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 14 Nov 2025 01:40:24 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 14 Nov 2025 01:40:24 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 14 Nov 2025 01:40:24 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Fri, 14 Nov 2025 01:40:24 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 14 Nov 2025 01:40:24 GMT
ARG MAVEN_VERSION=3.9.11
# Fri, 14 Nov 2025 01:40:24 GMT
ARG USER_HOME_DIR=/root
# Fri, 14 Nov 2025 01:40:24 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 14 Nov 2025 01:40:24 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 14 Nov 2025 01:40:24 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Sun, 07 Dec 2025 13:53:31 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93a0c5ed7112f5699c4ac207aaa6ff3f277cd53844121771dc304877183ab78c`  
		Last Modified: Sat, 08 Nov 2025 17:53:22 GMT  
		Size: 16.3 MB (16289673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a00e86805e496de548858bb7bc241431402e110f0ee0f8b305ec3fdadfa6d820`  
		Last Modified: Sat, 08 Nov 2025 17:53:32 GMT  
		Size: 52.6 MB (52637485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8414a6f189f97323a29e1384a0017627bbd029f10c4f53f4e0a246317953e853`  
		Last Modified: Sat, 08 Nov 2025 17:53:20 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bec39477cf2e25f9f8db348d31ff41dd8cc0c64cb6470887efe494699ba11718`  
		Last Modified: Sat, 08 Nov 2025 17:53:20 GMT  
		Size: 2.3 KB (2304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26c33556ed9897e10fd8d378ad2469f648f341fa298eac33ed7bfd939238cb96`  
		Last Modified: Fri, 14 Nov 2025 01:40:38 GMT  
		Size: 3.8 MB (3802851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2afbd5ecbcca1eec0b2ad1f1c60164436cd95cae230a12e07fd4772b0631398c`  
		Last Modified: Fri, 14 Nov 2025 01:40:39 GMT  
		Size: 9.2 MB (9242577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f369cc71e5d4e5b798371441a994602e5e57fb8d8ca798ac9c4d6c9085a0fa9`  
		Last Modified: Fri, 14 Nov 2025 01:40:38 GMT  
		Size: 859.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:becab4c849c5833b69e0fb97b218e03a379ae042442ff213d3a8a43d46c9c129`  
		Last Modified: Fri, 14 Nov 2025 01:40:37 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-8-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:ea9c48c63680af8da4378ad0879cf8c6c61efb8ec5769ab1d05586b5b43d22a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1257691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51a4fa8b6e013f4743ace3e325fa0e72e87416d1e458af45a8d1180162c6ad7a`

```dockerfile
```

-	Layers:
	-	`sha256:d347de7f82ce05213c8d5b60759d5eb0f4e0d679051617f40363e36cc26c40f3`  
		Last Modified: Fri, 14 Nov 2025 03:31:10 GMT  
		Size: 1.2 MB (1238361 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87f08ed9d4ffe471b499dbe6a80a158504505511e2f0a42f258b8a20bcdf50dc`  
		Last Modified: Fri, 14 Nov 2025 03:31:11 GMT  
		Size: 19.3 KB (19330 bytes)  
		MIME: application/vnd.in-toto+json
