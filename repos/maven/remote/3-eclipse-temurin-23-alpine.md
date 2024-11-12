## `maven:3-eclipse-temurin-23-alpine`

```console
$ docker pull maven@sha256:1fe39410d42363da75650fb16cb319ac648bf28d437c693a67abba450109766a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-eclipse-temurin-23-alpine` - linux; amd64

```console
$ docker pull maven@sha256:20715c4d42698a05368a096452fe55a6222eefe72840d20ec0798423256b4e79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.6 MB (204576276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abef10b630b6237a8ec19b11934b155be49a0ff196140e2d21057d86dd0c5e94`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Mon, 23 Sep 2024 17:02:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 23 Sep 2024 17:02:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 23 Sep 2024 17:02:08 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 23 Sep 2024 17:02:08 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
ENV JAVA_VERSION=jdk-23.0.1+11
# Mon, 23 Sep 2024 17:02:08 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='ebdd6602d27bd7535bf06f21e8a0c3d563be7b790a90bef00cb6ac4123c66f86';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jdk_aarch64_alpine-linux_hotspot_23.0.1_11.tar.gz';          ;;        x86_64)          ESUM='4c37a9e885c4e099b049c3ba9baa073de1525e28cd5ffca016c5c5bd7ed385a6';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jdk_x64_alpine-linux_hotspot_23.0.1_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 23 Sep 2024 17:02:08 GMT
CMD ["jshell"]
# Mon, 23 Sep 2024 17:02:08 GMT
RUN apk add --no-cache bash procps curl tar openssh-client # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 23 Sep 2024 17:02:08 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 23 Sep 2024 17:02:08 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 23 Sep 2024 17:02:08 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 23 Sep 2024 17:02:08 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 23 Sep 2024 17:02:08 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
ARG MAVEN_VERSION=3.9.9
# Mon, 23 Sep 2024 17:02:08 GMT
ARG USER_HOME_DIR=/root
# Mon, 23 Sep 2024 17:02:08 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 23 Sep 2024 17:02:08 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 23 Sep 2024 17:02:08 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80ac0afaffe8235a13dd8d90914a2d6cd114cf39e349a24c38c2bcdea79ab015`  
		Last Modified: Tue, 12 Nov 2024 02:39:09 GMT  
		Size: 23.0 MB (22953184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0deb3338abfe175e7b298fa61a7147c870fb4aed00f53f4d30d674547e1b45f`  
		Last Modified: Tue, 12 Nov 2024 02:39:12 GMT  
		Size: 165.5 MB (165513301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3915703c046dd63269dbc212a69ec33a47d1030d48b31a874adf6bf73d47c449`  
		Last Modified: Tue, 12 Nov 2024 02:39:07 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c78fe47fe453af682fad0d120e9e4f2a5c05f85ebe5e3bdec8014fc7020c9c7d`  
		Last Modified: Tue, 12 Nov 2024 02:38:50 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:715a90522584f274f202a48c7370ef71bb44f5ba42c2b95431a29a977f55089a`  
		Last Modified: Tue, 12 Nov 2024 03:13:32 GMT  
		Size: 3.3 MB (3311994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6862b13acc097bb00aae7f24a76bc136671fee5f622ff9b9a65ce689c6a3b45`  
		Last Modified: Tue, 12 Nov 2024 03:13:32 GMT  
		Size: 9.2 MB (9170436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1dd44de51134c4dc0e4492f94fcc8f1296836155ec5ffbe8aa69d9ca4cc6c1b`  
		Last Modified: Tue, 12 Nov 2024 03:13:32 GMT  
		Size: 860.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4b177f1143107138abaa86dc3277dfd83049904d62d96827b20b27377c89a3f`  
		Last Modified: Tue, 12 Nov 2024 03:13:32 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-23-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:acea8fc2d8f2739287f2a60f7c3463ed192adc8e5e78260fd2522ce04742a627
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1217813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf1c345a043361ad66e1efe99e7989af016eab81f4680f92027099f1a12d59c8`

```dockerfile
```

-	Layers:
	-	`sha256:767121013941f3dd6bf22d0b3740de68aebc3bd9d5b1dc5da042c21a6d4b2d88`  
		Last Modified: Tue, 12 Nov 2024 03:13:32 GMT  
		Size: 1.2 MB (1198430 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1816f6a5a5f4055a815ec9c6fac9ba49cb2c45f1c0c01b6892be0501d1244c34`  
		Last Modified: Tue, 12 Nov 2024 03:13:32 GMT  
		Size: 19.4 KB (19383 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-eclipse-temurin-23-alpine` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:69c5fb1935a20cee2fec6e23930f9e1ff234fe36a82c0232fda81f8491dbb141
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.7 MB (203735941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3bd5e4a65e39247f750d3eb69fe0f6c89cd3b34c5b43ca709ac78813d04c232`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Mon, 23 Sep 2024 17:02:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 23 Sep 2024 17:02:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 23 Sep 2024 17:02:08 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 23 Sep 2024 17:02:08 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
ENV JAVA_VERSION=jdk-23.0.1+11
# Mon, 23 Sep 2024 17:02:08 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='ebdd6602d27bd7535bf06f21e8a0c3d563be7b790a90bef00cb6ac4123c66f86';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jdk_aarch64_alpine-linux_hotspot_23.0.1_11.tar.gz';          ;;        x86_64)          ESUM='4c37a9e885c4e099b049c3ba9baa073de1525e28cd5ffca016c5c5bd7ed385a6';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jdk_x64_alpine-linux_hotspot_23.0.1_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 23 Sep 2024 17:02:08 GMT
CMD ["jshell"]
# Mon, 23 Sep 2024 17:02:08 GMT
RUN apk add --no-cache bash procps curl tar openssh-client # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 23 Sep 2024 17:02:08 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 23 Sep 2024 17:02:08 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 23 Sep 2024 17:02:08 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 23 Sep 2024 17:02:08 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 23 Sep 2024 17:02:08 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
ARG MAVEN_VERSION=3.9.9
# Mon, 23 Sep 2024 17:02:08 GMT
ARG USER_HOME_DIR=/root
# Mon, 23 Sep 2024 17:02:08 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 23 Sep 2024 17:02:08 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 23 Sep 2024 17:02:08 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba5ab350b8ff57c75640d387c970dd2282464d9836a98c0f02d04ffe85d3db64`  
		Last Modified: Thu, 24 Oct 2024 01:14:18 GMT  
		Size: 23.7 MB (23731419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95498a283ecd538532b8a7cea1be8462e6dbe863fdedd3e095a6a5f1b4a15a9e`  
		Last Modified: Thu, 24 Oct 2024 01:19:42 GMT  
		Size: 163.3 MB (163315840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ed6bb967beba8210b0f1fc248fedf04f00058a1af4816baa27ab290efeaa649`  
		Last Modified: Thu, 24 Oct 2024 01:19:38 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4c1e2e0f6d842ca700db91de478c29907f7a0b9b0eccafdb8602f2a01f8e016`  
		Last Modified: Thu, 24 Oct 2024 01:19:38 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6535c788d4eb08a6edc5ab9f8aacecd75f9c4c2d089e1d9d08f571fc78dd31b5`  
		Last Modified: Thu, 24 Oct 2024 13:05:28 GMT  
		Size: 3.4 MB (3427143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bba010ec5e22a1d1bb9665614b6f1b360e4268a6cfffc5efb3e4f26ea85a232f`  
		Last Modified: Thu, 24 Oct 2024 13:05:28 GMT  
		Size: 9.2 MB (9170435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70ed44e16f359546931838fe6648863e7d139f11234b2762839b6aba19ef9458`  
		Last Modified: Thu, 24 Oct 2024 13:05:28 GMT  
		Size: 861.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e9fac0fdab76b334e41c6b1dfb9c68d81a836458a519f51daf289fa4772d72b`  
		Last Modified: Thu, 24 Oct 2024 13:05:28 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-23-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:78a688e2452d4a84e0e2daa6629eeb25a9e9e7b0e59b8a8ba6e2b6d673b177d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1322038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6397b5957c29f1a63003c16cf87240b50f755e116096cc3f671daf757929ca52`

```dockerfile
```

-	Layers:
	-	`sha256:071f9fcd09aaf8f35db1ad2c3deeadb289d5f136726c444ca8188e146f5c4b7e`  
		Last Modified: Thu, 24 Oct 2024 13:05:28 GMT  
		Size: 1.3 MB (1302488 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0bcea375d7189c389dabd08e7ce5282206b88d8d8b84ebb584a61da70d96747`  
		Last Modified: Thu, 24 Oct 2024 13:05:27 GMT  
		Size: 19.6 KB (19550 bytes)  
		MIME: application/vnd.in-toto+json
