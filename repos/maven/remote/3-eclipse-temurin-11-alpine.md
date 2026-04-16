## `maven:3-eclipse-temurin-11-alpine`

```console
$ docker pull maven@sha256:6b23414c3730457d130d22da2f9cb257c221a530904b6975d5a9f1cad26b3183
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `maven:3-eclipse-temurin-11-alpine` - linux; amd64

```console
$ docker pull maven@sha256:e4141b97b9a692c3b01084bb1ff1122c7b346fc05a9cc0ec0c149aa64b1e6fd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.5 MB (174520035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c594edcb48fa41d38da9aff1f72af8e58f7a1b8df442e4b5afdca7fb1348e18`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:32:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 20:32:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:32:47 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 20:32:47 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 15 Apr 2026 20:32:47 GMT
ENV JAVA_VERSION=jdk-11.0.30+7
# Wed, 15 Apr 2026 20:32:55 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='b55a38b75ba99d86f4adb47552ee5306b9589e2026861a3b8f030993c42aedc7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_x64_alpine-linux_hotspot_11.0.30_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 15 Apr 2026 20:32:56 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 15 Apr 2026 20:32:56 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:32:56 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 15 Apr 2026 20:32:56 GMT
CMD ["jshell"]
# Wed, 15 Apr 2026 22:53:35 GMT
RUN apk add --no-cache bash procps curl tar openssh-client # buildkit
# Wed, 15 Apr 2026 22:53:35 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 15 Apr 2026 22:53:35 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 15 Apr 2026 22:53:35 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 15 Apr 2026 22:53:35 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 15 Apr 2026 22:53:35 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 15 Apr 2026 22:53:35 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 15 Apr 2026 22:53:35 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 15 Apr 2026 22:53:35 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 15 Apr 2026 22:53:35 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 15 Apr 2026 22:53:35 GMT
ARG MAVEN_VERSION=3.9.14
# Wed, 15 Apr 2026 22:53:35 GMT
ARG USER_HOME_DIR=/root
# Wed, 15 Apr 2026 22:53:35 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 15 Apr 2026 22:53:35 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 15 Apr 2026 22:53:35 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ec914d871e26d0465399fedbb12a944add78359e4bacb45111654e407011389`  
		Last Modified: Wed, 15 Apr 2026 20:33:10 GMT  
		Size: 16.8 MB (16837789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43e0f2de0712b22eb820b820ec9d10381f0162a40034dd9db90063cf9bc5b7f9`  
		Last Modified: Wed, 15 Apr 2026 20:33:13 GMT  
		Size: 140.9 MB (140916718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97836bb5bbf19dc634eaea3ff5cfbc9b0ca22932b1bbb49c9a806a0bb040b842`  
		Last Modified: Wed, 15 Apr 2026 20:33:09 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c470514f36b76e7d4fbd25626009aade331446b35fde7acb2f42ae8b0b5c53a1`  
		Last Modified: Wed, 15 Apr 2026 20:33:09 GMT  
		Size: 2.3 KB (2276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:158a88a9fad63b8c1409e3d8a898039fb6fcbe15063947ec1f3025dd2cf7f766`  
		Last Modified: Wed, 15 Apr 2026 22:53:46 GMT  
		Size: 3.6 MB (3586708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3c2603c46232ce87c80b8ae7510b09bc0a8ca5344d297c4fe4aa75ac525d90a`  
		Last Modified: Wed, 15 Apr 2026 22:53:46 GMT  
		Size: 9.3 MB (9311182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94c536618a6f25f3dfc0f660ae0503cec1cfab0fe456e8639a05f6ca04a70536`  
		Last Modified: Wed, 15 Apr 2026 22:53:45 GMT  
		Size: 857.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7eee2ea6b26ac14536445cc4524e3d31c26f0a127b1cdabf02e7a7f0f4656a9`  
		Last Modified: Wed, 15 Apr 2026 22:53:45 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-11-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:06ba60ae3809f79f393e23492cd735e7c75cd7984b56eb53005e3b21e576f2eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1162863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:905f94b0439c74395c6c76aee55176a8b28a099e5f9d3493e2b5bbbe5b45b31d`

```dockerfile
```

-	Layers:
	-	`sha256:53e27e1fa40e040cbf67c4876b2ecaf323cfeb57febceea2694b138d37517818`  
		Last Modified: Wed, 15 Apr 2026 22:53:45 GMT  
		Size: 1.1 MB (1143516 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd807e5936d2c923a11d6534cec4048d4755c6117f07aedcb3e8d3002b64aae6`  
		Last Modified: Wed, 15 Apr 2026 22:53:45 GMT  
		Size: 19.3 KB (19347 bytes)  
		MIME: application/vnd.in-toto+json
