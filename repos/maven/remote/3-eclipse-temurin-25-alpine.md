## `maven:3-eclipse-temurin-25-alpine`

```console
$ docker pull maven@sha256:33759f8556cf6f6f80dac0198ecace92bec08249b7b2f9c2616525a4e6825b37
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-eclipse-temurin-25-alpine` - linux; amd64

```console
$ docker pull maven@sha256:1cdda0148fc425518af0945202547b400a790b847a9c3e0b30a0186f8c6b41b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.0 MB (123011926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fae4a7a18397f525809e63746f38cd2608d74bfa066deab31799814e8040e43`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 25 Sep 2025 19:59:06 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Thu, 25 Sep 2025 19:59:06 GMT
CMD ["/bin/sh"]
# Thu, 25 Sep 2025 19:59:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 25 Sep 2025 19:59:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Sep 2025 19:59:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 25 Sep 2025 19:59:06 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Thu, 25 Sep 2025 19:59:06 GMT
ENV JAVA_VERSION=jdk-25+36
# Thu, 25 Sep 2025 19:59:06 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='1f18ba69ca7d674724307a66928a9b80049748b4276c629450935543db2cdfb1';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jdk_aarch64_alpine-linux_hotspot_25_36.tar.gz';          ;;        x86_64)          ESUM='637e47474d411ed86134f413af7d5fef4180ddb0bf556347b7e74a88cf8904c8';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jdk_x64_alpine-linux_hotspot_25_36.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     apk add --no-cache --virtual .fetch-deps gnupg;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     apk del --no-network .fetch-deps; # buildkit
# Thu, 25 Sep 2025 19:59:06 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 25 Sep 2025 19:59:06 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 25 Sep 2025 19:59:06 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 25 Sep 2025 19:59:06 GMT
CMD ["jshell"]
# Fri, 26 Sep 2025 11:21:48 GMT
RUN apk add --no-cache bash procps curl tar openssh-client # buildkit
# Fri, 26 Sep 2025 11:21:48 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 26 Sep 2025 11:21:48 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 26 Sep 2025 11:21:48 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 26 Sep 2025 11:21:48 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 26 Sep 2025 11:21:48 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 26 Sep 2025 11:21:48 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 26 Sep 2025 11:21:48 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 26 Sep 2025 11:21:48 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Fri, 26 Sep 2025 11:21:48 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 26 Sep 2025 11:21:48 GMT
ARG MAVEN_VERSION=3.9.11
# Fri, 26 Sep 2025 11:21:48 GMT
ARG USER_HOME_DIR=/root
# Fri, 26 Sep 2025 11:21:48 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 26 Sep 2025 11:21:48 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 26 Sep 2025 11:21:48 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db03fa3ac16472a254962ebcd81ad021907bbad285d0f6cdc9a1502f80e25f71`  
		Last Modified: Wed, 08 Oct 2025 23:34:17 GMT  
		Size: 14.2 MB (14245319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a39bec576f64b4114bdea072e5b630129dd7815e2001b4fbdf0d8777eec25ab`  
		Last Modified: Wed, 08 Oct 2025 23:34:31 GMT  
		Size: 91.3 MB (91266716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55c248d02cde76c58f066897343c950bf9da798d7213e690f2205a87b12de4da`  
		Last Modified: Wed, 08 Oct 2025 23:34:14 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0249b6ee0600ac5bf443cd0634e2ffa05dc60ee1940d165feab4071b10180121`  
		Last Modified: Wed, 08 Oct 2025 23:34:13 GMT  
		Size: 2.3 KB (2279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4824419d1f0b961c203c6a2a9dbdfe4a7404aefeb16fbcf580a0a9cb0fd49484`  
		Last Modified: Thu, 09 Oct 2025 22:50:02 GMT  
		Size: 4.5 MB (4451396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d604ea288c96737d5841e2e3940e0aca37a46d0ea78c05bf33f4cfbf1cd847ea`  
		Last Modified: Thu, 09 Oct 2025 22:49:36 GMT  
		Size: 9.2 MB (9242592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd2ee55e73e95444ce26737d01d6fa02d8e4d3db260d0470117b8aee9ec7e9d8`  
		Last Modified: Thu, 09 Oct 2025 22:49:34 GMT  
		Size: 856.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7af5a38cae98fa790aaedfe0c0cb0909cadf24e8776e866c9ccdb927f2869e01`  
		Last Modified: Thu, 09 Oct 2025 22:49:34 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-25-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:63cfa5c4a255aa8f077e9e2c009de29fad136c8b6a8dc5364349378f671e50db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1138377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5bc255449b1d662ff568d7857045eb8a47840b700c8e1274aa3f1afe1276730`

```dockerfile
```

-	Layers:
	-	`sha256:3b48032bf1f62f268fd7eb9964bcef91ebe747700b3bcb3727fa740de2352f44`  
		Last Modified: Fri, 10 Oct 2025 05:32:20 GMT  
		Size: 1.1 MB (1119001 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c495378b06351cb5481be3d4a924e05e178f5a781be2d6856de36a53ac1ee35`  
		Last Modified: Fri, 10 Oct 2025 05:32:21 GMT  
		Size: 19.4 KB (19376 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-eclipse-temurin-25-alpine` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:5812be412d7f2bef21f76df3680652f2146427ea22841dee4403d706a3455229
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.4 MB (122423535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:654fd1cdfcee3037dcb55738994c7429d09b019671b266d80fd0aef31fdd1657`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 25 Sep 2025 19:59:06 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Thu, 25 Sep 2025 19:59:06 GMT
CMD ["/bin/sh"]
# Thu, 25 Sep 2025 19:59:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 25 Sep 2025 19:59:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Sep 2025 19:59:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 25 Sep 2025 19:59:06 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Thu, 25 Sep 2025 19:59:06 GMT
ENV JAVA_VERSION=jdk-25+36
# Thu, 25 Sep 2025 19:59:06 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='1f18ba69ca7d674724307a66928a9b80049748b4276c629450935543db2cdfb1';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jdk_aarch64_alpine-linux_hotspot_25_36.tar.gz';          ;;        x86_64)          ESUM='637e47474d411ed86134f413af7d5fef4180ddb0bf556347b7e74a88cf8904c8';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jdk_x64_alpine-linux_hotspot_25_36.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     apk add --no-cache --virtual .fetch-deps gnupg;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     apk del --no-network .fetch-deps; # buildkit
# Thu, 25 Sep 2025 19:59:06 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 25 Sep 2025 19:59:06 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 25 Sep 2025 19:59:06 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 25 Sep 2025 19:59:06 GMT
CMD ["jshell"]
# Fri, 26 Sep 2025 11:21:48 GMT
RUN apk add --no-cache bash procps curl tar openssh-client # buildkit
# Fri, 26 Sep 2025 11:21:48 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 26 Sep 2025 11:21:48 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 26 Sep 2025 11:21:48 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 26 Sep 2025 11:21:48 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 26 Sep 2025 11:21:48 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 26 Sep 2025 11:21:48 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 26 Sep 2025 11:21:48 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 26 Sep 2025 11:21:48 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Fri, 26 Sep 2025 11:21:48 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 26 Sep 2025 11:21:48 GMT
ARG MAVEN_VERSION=3.9.11
# Fri, 26 Sep 2025 11:21:48 GMT
ARG USER_HOME_DIR=/root
# Fri, 26 Sep 2025 11:21:48 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 26 Sep 2025 11:21:48 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 26 Sep 2025 11:21:48 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ade06a7471c002bcf656675566f358b0a11940fe7d9e6ff2c531e329a39c893`  
		Last Modified: Wed, 08 Oct 2025 21:49:10 GMT  
		Size: 14.4 MB (14352503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8f393f605afb3f2558c3e606e83caffd55f6d504cce6766329478332fa835e3`  
		Last Modified: Wed, 08 Oct 2025 21:49:13 GMT  
		Size: 90.2 MB (90170879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efd42f05d849ba1bbf31d4c7de1e475760b5930603787e167ae5175e231af087`  
		Last Modified: Wed, 08 Oct 2025 21:49:08 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b5157fd5631d15dfdd67c1e40b54fbdd30adf2eac3929ce9ac5cf21ac9c341a`  
		Last Modified: Wed, 08 Oct 2025 21:49:09 GMT  
		Size: 2.3 KB (2279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c29b1524a4903373186f23ef3ccc83bb8c352b79dc419a100aaf43225e6cd309`  
		Last Modified: Thu, 09 Oct 2025 22:53:34 GMT  
		Size: 4.5 MB (4516043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dabfa09bfa5728a565ece6ed44e9329b973ff9e3dd40cdacba97653c8c4be59`  
		Last Modified: Thu, 09 Oct 2025 22:53:35 GMT  
		Size: 9.2 MB (9242591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eb7bed24d7018a267477b57345f3c21accce5510fedb0d0d6f9d4ae4735db51`  
		Last Modified: Thu, 09 Oct 2025 22:53:35 GMT  
		Size: 857.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae931e54c446138890722515f667cc38ac289eff9f92ebfe3d8e99f8757c8483`  
		Last Modified: Thu, 09 Oct 2025 22:53:35 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-25-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:248fe988165c260e51fa34fd3a31ea51fca4312bda056f10b3a4c0de33d3f461
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1288509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f41a7b7fca9b0ebf3cb4886b664a556938c370b23aafb3970c071f60006ef03a`

```dockerfile
```

-	Layers:
	-	`sha256:a7c08f3ec9cf61502f8ae74710014b2cee631479cf79200cc46cb93c0685e0ce`  
		Last Modified: Fri, 10 Oct 2025 05:32:24 GMT  
		Size: 1.3 MB (1269000 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76f60241b58bbc98deea1e4667ca0dd72f79e7aaff603bcfb04c8aa76491caf0`  
		Last Modified: Fri, 10 Oct 2025 05:32:25 GMT  
		Size: 19.5 KB (19509 bytes)  
		MIME: application/vnd.in-toto+json
