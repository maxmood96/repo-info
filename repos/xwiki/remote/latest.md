## `xwiki:latest`

```console
$ docker pull xwiki@sha256:79dd3ed3b51bdd03a10b84fb03c1c076372550e23f5cd03230d266598ced4a3d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:latest` - linux; amd64

```console
$ docker pull xwiki@sha256:3a5e8f51682ca823ddc35562c5b4839bff5d823cd67466b8d1514936373fe4f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **647.5 MB (647537615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a30d6c9e84aa2e3cd882c967f422ca21fcdbf31e7c1dbe6244693424d1bc3e00`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Mon, 23 Feb 2026 17:17:53 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:17:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:17:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:17:53 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:17:55 GMT
ADD file:3f78aa860931e0853077f09eb31eddbeeef8a9dd70977305b4876aa176770721 in / 
# Mon, 23 Feb 2026 17:17:56 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:22:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 01:22:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 01:22:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 17 Mar 2026 01:22:45 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 01:22:45 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Tue, 17 Mar 2026 01:23:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='991be6ac6725e76109ecbd131d658f992dcbeacba3a8b4b6650302c8012b52fb';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_x64_linux_hotspot_21.0.10_7.tar.gz';          ;;        arm64)          ESUM='3ca84da7c4f57eee8d7e7f0645dc904a3a06456d32b37a4dd57a5e7527245250';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.10_7.tar.gz';          ;;        ppc64el)          ESUM='1a49cffcb348a28c017cf0deeb9322b7296dbfb002a8e43bd7f65ad671e10eb7';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.10_7.tar.gz';          ;;        riscv64)          ESUM='02cf763836c14bad4d689eb3b4efd691657de753dba07193cd1fb8691c8fe7b8';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_riscv64_linux_hotspot_21.0.10_7.tar.gz';          ;;        s390x)          ESUM='48f8529714c90c6cc61aa729cf8952f2fc47f2f2890551ba7f9e1c061b04be13';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_s390x_linux_hotspot_21.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 17 Mar 2026 01:23:09 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 17 Mar 2026 01:23:09 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 17 Mar 2026 01:23:09 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 23 Mar 2026 22:04:36 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 23 Mar 2026 22:04:36 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 23 Mar 2026 22:04:36 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 23 Mar 2026 22:04:36 GMT
WORKDIR /usr/local/tomcat
# Mon, 23 Mar 2026 22:04:36 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 23 Mar 2026 22:04:36 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 23 Mar 2026 22:04:36 GMT
ENV TOMCAT_MAJOR=10
# Mon, 23 Mar 2026 22:04:36 GMT
ENV TOMCAT_VERSION=10.1.53
# Mon, 23 Mar 2026 22:04:36 GMT
ENV TOMCAT_SHA512=0b21ad1e61b3163125866e8f5f317b23886998fccb4398f305c39a0bc1f688f6c566ab040da9f559ab50af4d699bda771d1ca89e229ead052336559a25753b45
# Mon, 23 Mar 2026 22:04:36 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 23 Mar 2026 22:04:45 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Mar 2026 22:04:45 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 23 Mar 2026 22:04:45 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 23 Mar 2026 22:04:45 GMT
ENTRYPOINT []
# Mon, 23 Mar 2026 22:04:45 GMT
CMD ["catalina.sh" "run"]
# Tue, 31 Mar 2026 17:41:23 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 31 Mar 2026 17:41:23 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 31 Mar 2026 17:41:23 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 31 Mar 2026 17:41:23 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 31 Mar 2026 17:41:23 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 31 Mar 2026 17:41:23 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 31 Mar 2026 17:41:23 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 31 Mar 2026 17:41:23 GMT
ENV XWIKI_VERSION=18.2.0
# Tue, 31 Mar 2026 17:41:23 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/18.2.0
# Tue, 31 Mar 2026 17:41:23 GMT
ENV XWIKI_DOWNLOAD_SHA256=1dbbf05fcb593f738a3f922c0d12bd4524c789a9f404e0e035bd6b2da2d1d26f
# Tue, 31 Mar 2026 17:41:44 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Tue, 31 Mar 2026 17:41:44 GMT
ENV MYSQL_JDBC_VERSION=9.6.0
# Tue, 31 Mar 2026 17:41:44 GMT
ENV MYSQL_JDBC_SHA256=66df1d453789dc8cb759a7dc17f58646893bf28483f262328650f170472a6ead
# Tue, 31 Mar 2026 17:41:44 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/9.6.0
# Tue, 31 Mar 2026 17:41:44 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-9.6.0.jar
# Tue, 31 Mar 2026 17:41:44 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-9.6.0.jar
# Tue, 31 Mar 2026 17:41:45 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c - # buildkit
# Tue, 31 Mar 2026 17:41:45 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Tue, 31 Mar 2026 17:41:45 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Tue, 31 Mar 2026 17:41:45 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Tue, 31 Mar 2026 17:41:45 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 31 Mar 2026 17:41:45 GMT
VOLUME [/usr/local/xwiki]
# Tue, 31 Mar 2026 17:41:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 31 Mar 2026 17:41:45 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:817807f3c64e0b90b66edc7d90297f121cad2a7c2a3ee05a731557762f91e6c7`  
		Last Modified: Mon, 23 Feb 2026 17:51:17 GMT  
		Size: 29.7 MB (29731993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6502333748a9e5b5a7e8aaabb484e42b3cc861ca1dcf4d70331259c318eb596d`  
		Last Modified: Tue, 17 Mar 2026 01:23:01 GMT  
		Size: 17.0 MB (16983392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92b331859550d0b667a6ab32159d398031b1c5ed2e351a645be1e3dcd633f6ab`  
		Last Modified: Tue, 17 Mar 2026 01:23:21 GMT  
		Size: 53.0 MB (52985455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ded334408097f08dde9507428976abc2f844eae59856aecc45671fb699f88f74`  
		Last Modified: Tue, 17 Mar 2026 01:23:20 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf6ab2a4ddd47ce46630077d0e137301e2294ad28cbbd10ed888d2782bc027be`  
		Last Modified: Tue, 17 Mar 2026 01:23:20 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51c2dc091ebedc9315302a630901af180a57b4abb57fe43fe8581cd7391ce508`  
		Last Modified: Mon, 23 Mar 2026 22:04:53 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5824f78df6e1a7c5d7bc0e737ef4233cb51138047a5858cab3c83b19ad0804e2`  
		Last Modified: Mon, 23 Mar 2026 22:04:54 GMT  
		Size: 14.3 MB (14299459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d957a3566929627214f7a1e1de92ca86d874f95c3c9565b2bc433a082051fda5`  
		Last Modified: Mon, 23 Mar 2026 22:04:54 GMT  
		Size: 1.6 MB (1639788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db833620a30f7f719fc97dc03457e51495dd10ab04fe21b8e800e9b2f1b7be4c`  
		Last Modified: Tue, 31 Mar 2026 17:42:29 GMT  
		Size: 191.2 MB (191193262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fa114018db413e45a37679f9eae62fa2aff4fc9614aca875c0b60a153912989`  
		Last Modified: Tue, 31 Mar 2026 17:42:33 GMT  
		Size: 338.2 MB (338242750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:176e468af8d75d284c43a64deae37ed7f54d624a79be06c73a444916daafd3dc`  
		Last Modified: Tue, 31 Mar 2026 17:42:22 GMT  
		Size: 2.4 MB (2441664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7e4b86a12d9b15ced2419661b167b81c79d0217e76fa4a82533553aa94f6ade`  
		Last Modified: Tue, 31 Mar 2026 17:42:22 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be8e4e5e6ca825c2f468a331954d233a226c624787b8c402a3603241ed57e3d1`  
		Last Modified: Tue, 31 Mar 2026 17:42:23 GMT  
		Size: 2.4 KB (2375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f61505fb792a9dbe7153d5145689f4a19ac566a0453d236c04fbef265f9e176f`  
		Last Modified: Tue, 31 Mar 2026 17:42:23 GMT  
		Size: 11.0 KB (10954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eaf561aa8e6ceedf318e6c4ed13067c8f0bd042a714445c1372f4aff2663bd5`  
		Last Modified: Tue, 31 Mar 2026 17:42:25 GMT  
		Size: 2.5 KB (2536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:latest` - unknown; unknown

```console
$ docker pull xwiki@sha256:5d603ecb254acda0417bb19ac21d7fb99b7508c271d01be8432b979faa413b41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9236381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9207fee23418b4a808035a05f0bddb9928467a857a62116b4642cc94a38f72f`

```dockerfile
```

-	Layers:
	-	`sha256:3b286559ac5bc86454b7fc7d9c6e1eb3b5a15de3e79e89b809f233701f39fe27`  
		Last Modified: Tue, 31 Mar 2026 17:42:22 GMT  
		Size: 9.2 MB (9194270 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3389384bd6d06268ca570ccb9865a724743333f50191329e87e324140e938316`  
		Last Modified: Tue, 31 Mar 2026 17:42:22 GMT  
		Size: 42.1 KB (42111 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:latest` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:6d43c8abc5a0ff48b19ad0daf99d1a97186e1c5d54f80025e87dbd1730fc8a63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **643.6 MB (643599403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbeb81ad75fba9d92a173c19a54220d5d94ea45db60392b6b76067de3043f277`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Mon, 23 Feb 2026 17:19:30 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:19:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:19:32 GMT
ADD file:2763d61bc43bd178306ae0d4151c2477166ebf199b8d7294d9ea410f9891993f in / 
# Mon, 23 Feb 2026 17:19:33 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:23:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 01:23:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 01:23:54 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 17 Mar 2026 01:23:54 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 01:23:54 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Tue, 17 Mar 2026 01:24:40 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='991be6ac6725e76109ecbd131d658f992dcbeacba3a8b4b6650302c8012b52fb';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_x64_linux_hotspot_21.0.10_7.tar.gz';          ;;        arm64)          ESUM='3ca84da7c4f57eee8d7e7f0645dc904a3a06456d32b37a4dd57a5e7527245250';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.10_7.tar.gz';          ;;        ppc64el)          ESUM='1a49cffcb348a28c017cf0deeb9322b7296dbfb002a8e43bd7f65ad671e10eb7';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.10_7.tar.gz';          ;;        riscv64)          ESUM='02cf763836c14bad4d689eb3b4efd691657de753dba07193cd1fb8691c8fe7b8';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_riscv64_linux_hotspot_21.0.10_7.tar.gz';          ;;        s390x)          ESUM='48f8529714c90c6cc61aa729cf8952f2fc47f2f2890551ba7f9e1c061b04be13';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_s390x_linux_hotspot_21.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 17 Mar 2026 01:24:40 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 17 Mar 2026 01:24:40 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 17 Mar 2026 01:24:40 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 23 Mar 2026 22:04:55 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 23 Mar 2026 22:04:55 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 23 Mar 2026 22:04:55 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 23 Mar 2026 22:04:55 GMT
WORKDIR /usr/local/tomcat
# Mon, 23 Mar 2026 22:04:55 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 23 Mar 2026 22:04:55 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 23 Mar 2026 22:04:55 GMT
ENV TOMCAT_MAJOR=10
# Mon, 23 Mar 2026 22:04:55 GMT
ENV TOMCAT_VERSION=10.1.53
# Mon, 23 Mar 2026 22:04:55 GMT
ENV TOMCAT_SHA512=0b21ad1e61b3163125866e8f5f317b23886998fccb4398f305c39a0bc1f688f6c566ab040da9f559ab50af4d699bda771d1ca89e229ead052336559a25753b45
# Mon, 23 Mar 2026 22:04:55 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 23 Mar 2026 22:05:06 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Mar 2026 22:05:07 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 23 Mar 2026 22:05:07 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 23 Mar 2026 22:05:07 GMT
ENTRYPOINT []
# Mon, 23 Mar 2026 22:05:07 GMT
CMD ["catalina.sh" "run"]
# Tue, 31 Mar 2026 17:41:20 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 31 Mar 2026 17:41:20 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 31 Mar 2026 17:41:20 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 31 Mar 2026 17:41:20 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 31 Mar 2026 17:41:20 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 31 Mar 2026 17:41:20 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 31 Mar 2026 17:41:20 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 31 Mar 2026 17:41:20 GMT
ENV XWIKI_VERSION=18.2.0
# Tue, 31 Mar 2026 17:41:20 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/18.2.0
# Tue, 31 Mar 2026 17:41:20 GMT
ENV XWIKI_DOWNLOAD_SHA256=1dbbf05fcb593f738a3f922c0d12bd4524c789a9f404e0e035bd6b2da2d1d26f
# Tue, 31 Mar 2026 17:41:42 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Tue, 31 Mar 2026 17:41:42 GMT
ENV MYSQL_JDBC_VERSION=9.6.0
# Tue, 31 Mar 2026 17:41:42 GMT
ENV MYSQL_JDBC_SHA256=66df1d453789dc8cb759a7dc17f58646893bf28483f262328650f170472a6ead
# Tue, 31 Mar 2026 17:41:42 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/9.6.0
# Tue, 31 Mar 2026 17:41:42 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-9.6.0.jar
# Tue, 31 Mar 2026 17:41:42 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-9.6.0.jar
# Tue, 31 Mar 2026 17:41:43 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c - # buildkit
# Tue, 31 Mar 2026 17:41:43 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Tue, 31 Mar 2026 17:41:43 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Tue, 31 Mar 2026 17:41:43 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Tue, 31 Mar 2026 17:41:43 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 31 Mar 2026 17:41:43 GMT
VOLUME [/usr/local/xwiki]
# Tue, 31 Mar 2026 17:41:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 31 Mar 2026 17:41:43 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:86790fc5660dcd86928b849ae0826aba701bf9e005e92c8f9e06c917e82c87f7`  
		Last Modified: Mon, 23 Feb 2026 17:51:24 GMT  
		Size: 28.9 MB (28869709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5135b685185570494910edd394b8134172c97bab64cfef4134685bc7a7adf965`  
		Last Modified: Tue, 17 Mar 2026 01:24:08 GMT  
		Size: 17.0 MB (16996055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa618972369eec5997c7c2a43c076f8237d95b3c56ab24e45bbe1196cd969d4f`  
		Last Modified: Tue, 17 Mar 2026 01:24:57 GMT  
		Size: 52.2 MB (52155671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d719861772c215e9e1cdc82ae81b5a5009e75c9adb2502f42cb33948ac1f0168`  
		Last Modified: Tue, 17 Mar 2026 01:24:52 GMT  
		Size: 161.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd79f03dbf43ae3059af78550ba432373910eb86b58ffaf54e088f81646486ec`  
		Last Modified: Tue, 17 Mar 2026 01:24:53 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f5f2a6537baa97a27317a29a28cb79cbf140ab380496dd5acbe4859ae3afa08`  
		Last Modified: Mon, 23 Mar 2026 22:05:16 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2617b716139c37c212f4e8e33e1c5229598d2c161bde440f6dbb2f5d503d5c72`  
		Last Modified: Mon, 23 Mar 2026 22:05:16 GMT  
		Size: 14.3 MB (14301350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27c8a7602f6499e0b9d7b3abca21f74c4754562c60483e6cb5a140ab9eb9fbb1`  
		Last Modified: Mon, 23 Mar 2026 22:05:16 GMT  
		Size: 1.7 MB (1719570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc311595cb1f6bd3fec050ac2d282405e8382ff3661e711cfaafbadba4920edb`  
		Last Modified: Tue, 31 Mar 2026 17:42:25 GMT  
		Size: 188.9 MB (188852759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16881b3bf67516770ef4e9de4a93c9b4e2b16bf54b4e3a797e9fa3b13267f0b7`  
		Last Modified: Tue, 31 Mar 2026 17:42:31 GMT  
		Size: 338.2 MB (338242789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f6e417266bc0ce29887595fa968ba27386be5556b709db6935c6e1718b83606`  
		Last Modified: Tue, 31 Mar 2026 17:42:17 GMT  
		Size: 2.4 MB (2441660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b8f2d8065ebe7d0981bed228ea9629687f662d38f4800c80b8ae87e33072e44`  
		Last Modified: Tue, 31 Mar 2026 17:42:17 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e255b40924758171470678b3af0ca72c5ffc25734c35dd3039655b3cae4c9b2`  
		Last Modified: Tue, 31 Mar 2026 17:42:19 GMT  
		Size: 2.4 KB (2369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1df9654a4c2e78e1f33f83daae66fd8b18017a54903feff9ef190262944f3bb2`  
		Last Modified: Tue, 31 Mar 2026 17:42:19 GMT  
		Size: 11.0 KB (10952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8713614b7228e141d3cdcf8b519053c5127ae4a03a99189ec3a6755f2d1c5f85`  
		Last Modified: Tue, 31 Mar 2026 17:42:20 GMT  
		Size: 2.5 KB (2532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:latest` - unknown; unknown

```console
$ docker pull xwiki@sha256:c34b616b15a952f15c96ec4d03578b6f89530258fa33406db6d376ffbfb9e60c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9237427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c3065c9ea396f22ad4c3bdae16244a06755619bcc59e608e1e97993b41d295b`

```dockerfile
```

-	Layers:
	-	`sha256:b1056a84eecb9205e6dfa965e5fc4ba9b5214b2be1a151a1e345d67ea1d71352`  
		Last Modified: Tue, 31 Mar 2026 17:42:17 GMT  
		Size: 9.2 MB (9195083 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10aff5079c306991fce0f396cadb3221338f6c0fbaebc4df2e6f67e2e4e72664`  
		Last Modified: Tue, 31 Mar 2026 17:42:17 GMT  
		Size: 42.3 KB (42344 bytes)  
		MIME: application/vnd.in-toto+json
