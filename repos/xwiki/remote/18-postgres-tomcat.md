## `xwiki:18-postgres-tomcat`

```console
$ docker pull xwiki@sha256:fa407715ce845fe3c00a451974869b637541b46cc81aeaffd377e80b5c6b05b1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:18-postgres-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:334b0a72cb310b5d5e8a0cededb2c82038023087f5bf5763a275f247f4de2a68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **646.2 MB (646157534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:283778fe421a03b5818b95340aab680ea0070fe52053cec839b9888740b29d80`
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
# Tue, 31 Mar 2026 17:42:49 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 31 Mar 2026 17:42:49 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 31 Mar 2026 17:42:49 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 31 Mar 2026 17:42:49 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 31 Mar 2026 17:42:49 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 31 Mar 2026 17:42:49 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 31 Mar 2026 17:42:49 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 31 Mar 2026 17:42:49 GMT
ENV XWIKI_VERSION=18.2.0
# Tue, 31 Mar 2026 17:42:49 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/18.2.0
# Tue, 31 Mar 2026 17:42:49 GMT
ENV XWIKI_DOWNLOAD_SHA256=1dbbf05fcb593f738a3f922c0d12bd4524c789a9f404e0e035bd6b2da2d1d26f
# Tue, 31 Mar 2026 17:43:10 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Tue, 31 Mar 2026 17:43:10 GMT
ENV POSTGRES_JDBC_VERSION=42.7.10
# Tue, 31 Mar 2026 17:43:10 GMT
ENV POSTGRES_JDBC_SHA256=cab1cd67cfa25c25de4348e532298028288a877ba01c77d1619fe45416193387
# Tue, 31 Mar 2026 17:43:10 GMT
ENV POSTGRES_JDBC_PREFIX=https://repo1.maven.org/maven2/org/postgresql/postgresql/42.7.10
# Tue, 31 Mar 2026 17:43:10 GMT
ENV POSTGRES_JDBC_ARTIFACT=postgresql-42.7.10.jar
# Tue, 31 Mar 2026 17:43:10 GMT
ENV POSTGRES_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/postgresql-42.7.10.jar
# Tue, 31 Mar 2026 17:43:10 GMT
RUN curl -fSL "${POSTGRES_JDBC_PREFIX}/${POSTGRES_JDBC_ARTIFACT}" -o $POSTGRES_JDBC_TARGET &&   echo "$POSTGRES_JDBC_SHA256 $POSTGRES_JDBC_TARGET" | sha256sum -c - # buildkit
# Tue, 31 Mar 2026 17:43:11 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Tue, 31 Mar 2026 17:43:11 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Tue, 31 Mar 2026 17:43:11 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Tue, 31 Mar 2026 17:43:11 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 31 Mar 2026 17:43:11 GMT
VOLUME [/usr/local/xwiki]
# Tue, 31 Mar 2026 17:43:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 31 Mar 2026 17:43:11 GMT
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
	-	`sha256:72106e8d7dd76f30212f14ea24d4cc48f3fe7f728589d59bd9ec8466626b1e15`  
		Last Modified: Tue, 31 Mar 2026 17:43:53 GMT  
		Size: 191.2 MB (191193180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cda07725cb6379e0b945e18a3b12c82453137829fbff5f1586feef637a8768e6`  
		Last Modified: Tue, 31 Mar 2026 17:43:56 GMT  
		Size: 338.2 MB (338242836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99b14f5bdf67c3c7095e87697d3569336e7be7e7101b20e93ed67ffe4b98d4b4`  
		Last Modified: Tue, 31 Mar 2026 17:43:46 GMT  
		Size: 1.1 MB (1061584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a894c725c69032061a9730be14de9649b842df78acd2ca1319df446817d79af2`  
		Last Modified: Tue, 31 Mar 2026 17:43:46 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7459101549fd7b007a5e23aac22f48b1217aa4e66f7b1b15ae3961ecd873cb18`  
		Last Modified: Tue, 31 Mar 2026 17:43:48 GMT  
		Size: 2.5 KB (2464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f560f2ea35fbf6793701d6fc4ff7e3100c767615bed0c90e393d8f9b77eab73c`  
		Last Modified: Tue, 31 Mar 2026 17:43:48 GMT  
		Size: 11.0 KB (10955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd1178c11ac656e16a950e6a01862a9c46908e280ee4f857d8d54763efe27622`  
		Last Modified: Tue, 31 Mar 2026 17:43:49 GMT  
		Size: 2.4 KB (2441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:18-postgres-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:879cf7bd92eaf41c73db8dc3ad54cb637aa73aedc2f7a162ea78a9b863bfa06b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9233532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d706739e3af0c380480442fc40d01c8ba13acf03339025122fd0b91340f3b640`

```dockerfile
```

-	Layers:
	-	`sha256:bc54a944b03586aaac6f71b1d63d8da836e87238b6d6786f4f25d5842efd941a`  
		Last Modified: Tue, 31 Mar 2026 17:43:46 GMT  
		Size: 9.2 MB (9192775 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:694b25eb13a3c3fcb276dbcfaff62d63953283c0603c22f044b7053614e5fca0`  
		Last Modified: Tue, 31 Mar 2026 17:43:45 GMT  
		Size: 40.8 KB (40757 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:18-postgres-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:c025f1f68e99d3758d64a77617c05e5e9aed558e72fd2640557985f7eeb16386
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **642.2 MB (642219564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:051c6bc4d088f5263888d7e1aa5231a3facf8eb10d1c552273161c99c37de887`
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
# Tue, 31 Mar 2026 17:42:20 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 31 Mar 2026 17:42:20 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 31 Mar 2026 17:42:20 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 31 Mar 2026 17:42:20 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 31 Mar 2026 17:42:20 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 31 Mar 2026 17:42:20 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 31 Mar 2026 17:42:20 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 31 Mar 2026 17:42:20 GMT
ENV XWIKI_VERSION=18.2.0
# Tue, 31 Mar 2026 17:42:20 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/18.2.0
# Tue, 31 Mar 2026 17:42:20 GMT
ENV XWIKI_DOWNLOAD_SHA256=1dbbf05fcb593f738a3f922c0d12bd4524c789a9f404e0e035bd6b2da2d1d26f
# Tue, 31 Mar 2026 17:42:42 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Tue, 31 Mar 2026 17:42:42 GMT
ENV POSTGRES_JDBC_VERSION=42.7.10
# Tue, 31 Mar 2026 17:42:42 GMT
ENV POSTGRES_JDBC_SHA256=cab1cd67cfa25c25de4348e532298028288a877ba01c77d1619fe45416193387
# Tue, 31 Mar 2026 17:42:42 GMT
ENV POSTGRES_JDBC_PREFIX=https://repo1.maven.org/maven2/org/postgresql/postgresql/42.7.10
# Tue, 31 Mar 2026 17:42:42 GMT
ENV POSTGRES_JDBC_ARTIFACT=postgresql-42.7.10.jar
# Tue, 31 Mar 2026 17:42:42 GMT
ENV POSTGRES_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/postgresql-42.7.10.jar
# Tue, 31 Mar 2026 17:42:43 GMT
RUN curl -fSL "${POSTGRES_JDBC_PREFIX}/${POSTGRES_JDBC_ARTIFACT}" -o $POSTGRES_JDBC_TARGET &&   echo "$POSTGRES_JDBC_SHA256 $POSTGRES_JDBC_TARGET" | sha256sum -c - # buildkit
# Tue, 31 Mar 2026 17:42:43 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Tue, 31 Mar 2026 17:42:43 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Tue, 31 Mar 2026 17:42:43 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Tue, 31 Mar 2026 17:42:43 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 31 Mar 2026 17:42:43 GMT
VOLUME [/usr/local/xwiki]
# Tue, 31 Mar 2026 17:42:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 31 Mar 2026 17:42:43 GMT
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
	-	`sha256:238e29475b3cd5e16910c76586c842693f7569397d0283ddea10d1f4415029a4`  
		Last Modified: Tue, 31 Mar 2026 17:43:27 GMT  
		Size: 188.9 MB (188852958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:985539c5d5c1de41afcdb842089a755eeca195abdb39a5d4ec110984aa0642d2`  
		Last Modified: Tue, 31 Mar 2026 17:43:31 GMT  
		Size: 338.2 MB (338242805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a212a2dd167a04a2699580456055c40da43fe4e81495973e84d2c82fb2dcdf3c`  
		Last Modified: Tue, 31 Mar 2026 17:43:16 GMT  
		Size: 1.1 MB (1061592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d510f925a976ecff145e7ffb904949495ff7c169749baed9668ba5e203c75bd0`  
		Last Modified: Tue, 31 Mar 2026 17:43:16 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2f4f47a19f961cf350c14e08a3a1e6b044a15e36243a4af3c21b608cefb19f0`  
		Last Modified: Tue, 31 Mar 2026 17:43:17 GMT  
		Size: 2.5 KB (2464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fb81aa60c45e4d2aeb9e0b3bc58bc67667099abaa36400536f62bc9d20ffcee`  
		Last Modified: Tue, 31 Mar 2026 17:43:18 GMT  
		Size: 11.0 KB (10956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45f4f0079cecb90b10bcd205a0a1eb5b997d0c0c61fbc0d798e1c2c5c3e2110e`  
		Last Modified: Tue, 31 Mar 2026 17:43:19 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:18-postgres-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:f6869c9099d48487348a6f403548ddbd62de7695be62ecd9bc46835215a2ac11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9234458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da25b6118bd6aca308ec7f0a5ba00f823b8bfd01970e96ef25c3779cfca5099e`

```dockerfile
```

-	Layers:
	-	`sha256:08c2a4c3c89a4ff00b9cba249b55944b7701bcc1fe18f06c77cfedd51e007e2b`  
		Last Modified: Tue, 31 Mar 2026 17:43:16 GMT  
		Size: 9.2 MB (9193528 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10859a06d267b70cfde7bc2d981618330e50f81613bb651661f6af303b5809bb`  
		Last Modified: Tue, 31 Mar 2026 17:43:16 GMT  
		Size: 40.9 KB (40930 bytes)  
		MIME: application/vnd.in-toto+json
