## `xwiki:stable-postgres-tomcat`

```console
$ docker pull xwiki@sha256:988f3c974bccfe02e889ad8cf3547539684c27b58f997715a4de51a895dc1625
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:stable-postgres-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:66e79e38c8e8abb53bb2b2a78588538d772c1f59c433224a7ca36e079bcab061
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **651.1 MB (651075970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:607daaf7589f1c1a38f0a5254248ac8c8748a750716f7736ef63b92236bda0e6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:34:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 20:34:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:34:15 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 20:34:15 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:34:15 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Wed, 15 Apr 2026 20:34:18 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='991be6ac6725e76109ecbd131d658f992dcbeacba3a8b4b6650302c8012b52fb';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_x64_linux_hotspot_21.0.10_7.tar.gz';          ;;        arm64)          ESUM='3ca84da7c4f57eee8d7e7f0645dc904a3a06456d32b37a4dd57a5e7527245250';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.10_7.tar.gz';          ;;        ppc64el)          ESUM='1a49cffcb348a28c017cf0deeb9322b7296dbfb002a8e43bd7f65ad671e10eb7';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.10_7.tar.gz';          ;;        riscv64)          ESUM='02cf763836c14bad4d689eb3b4efd691657de753dba07193cd1fb8691c8fe7b8';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_riscv64_linux_hotspot_21.0.10_7.tar.gz';          ;;        s390x)          ESUM='48f8529714c90c6cc61aa729cf8952f2fc47f2f2890551ba7f9e1c061b04be13';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_s390x_linux_hotspot_21.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 15 Apr 2026 20:34:18 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 15 Apr 2026 20:34:18 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:34:18 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 15 Apr 2026 22:33:25 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 15 Apr 2026 22:33:25 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:33:25 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Wed, 15 Apr 2026 22:33:25 GMT
WORKDIR /usr/local/tomcat
# Wed, 15 Apr 2026 22:33:25 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 15 Apr 2026 22:33:25 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 15 Apr 2026 22:33:25 GMT
ENV TOMCAT_MAJOR=10
# Wed, 15 Apr 2026 22:33:25 GMT
ENV TOMCAT_VERSION=10.1.54
# Wed, 15 Apr 2026 22:33:25 GMT
ENV TOMCAT_SHA512=8694b94324cf6f62ab032fa2438d7334518dcfcbf7878361b147246c46eb1e558c327f32c05fb4b7705c01fcca92fde392ce320934410f1169ff4ab36a1c7139
# Wed, 15 Apr 2026 22:33:26 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Wed, 15 Apr 2026 22:33:32 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 22:33:33 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Wed, 15 Apr 2026 22:33:33 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 15 Apr 2026 22:33:33 GMT
ENTRYPOINT []
# Wed, 15 Apr 2026 22:33:33 GMT
CMD ["catalina.sh" "run"]
# Tue, 28 Apr 2026 23:12:31 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 28 Apr 2026 23:12:31 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 28 Apr 2026 23:12:31 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 28 Apr 2026 23:12:31 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 28 Apr 2026 23:12:31 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 28 Apr 2026 23:12:31 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 28 Apr 2026 23:12:31 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 28 Apr 2026 23:12:31 GMT
ENV XWIKI_VERSION=18.3.0
# Tue, 28 Apr 2026 23:12:31 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/18.3.0
# Tue, 28 Apr 2026 23:12:31 GMT
ENV XWIKI_DOWNLOAD_SHA256=3a0594e4260bc832c8a42f9ea1d6f47d9da7c8ffb7bbe65b7c363e7e8308051a
# Tue, 28 Apr 2026 23:12:54 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Tue, 28 Apr 2026 23:12:54 GMT
ENV POSTGRES_JDBC_VERSION=42.7.10
# Tue, 28 Apr 2026 23:12:54 GMT
ENV POSTGRES_JDBC_SHA256=cab1cd67cfa25c25de4348e532298028288a877ba01c77d1619fe45416193387
# Tue, 28 Apr 2026 23:12:54 GMT
ENV POSTGRES_JDBC_PREFIX=https://repo1.maven.org/maven2/org/postgresql/postgresql/42.7.10
# Tue, 28 Apr 2026 23:12:54 GMT
ENV POSTGRES_JDBC_ARTIFACT=postgresql-42.7.10.jar
# Tue, 28 Apr 2026 23:12:54 GMT
ENV POSTGRES_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/postgresql-42.7.10.jar
# Tue, 28 Apr 2026 23:12:54 GMT
RUN curl -fSL "${POSTGRES_JDBC_PREFIX}/${POSTGRES_JDBC_ARTIFACT}" -o $POSTGRES_JDBC_TARGET &&   echo "$POSTGRES_JDBC_SHA256 $POSTGRES_JDBC_TARGET" | sha256sum -c - # buildkit
# Tue, 28 Apr 2026 23:12:54 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Tue, 28 Apr 2026 23:12:54 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Tue, 28 Apr 2026 23:12:54 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Tue, 28 Apr 2026 23:12:55 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 28 Apr 2026 23:12:55 GMT
VOLUME [/usr/local/xwiki]
# Tue, 28 Apr 2026 23:12:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Apr 2026 23:12:55 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:166e3ac40fcac6c067aeb2526197d059af1ae4fbadf54b828f5dd81987af050c`  
		Last Modified: Wed, 15 Apr 2026 20:34:31 GMT  
		Size: 17.0 MB (16983398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a89ec8f5419f9af7b5bebf84595d9fadf8482375c3d8e56a7b5f6877cdb14e2`  
		Last Modified: Wed, 15 Apr 2026 20:34:32 GMT  
		Size: 53.0 MB (52985497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea035da72e5f5703c867853ddef78ebc7f9e1a36c5dc6e3fb9d52ac5d4e88408`  
		Last Modified: Wed, 15 Apr 2026 20:34:30 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c5d8083e928e6b185b981f8eacd53e2978658f685409fd506f96b73fee282e0`  
		Last Modified: Wed, 15 Apr 2026 20:34:30 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30c386aabe50ea9001b7d60fc42a908ed739d9f42c1de6c3e3266cc6bedcad93`  
		Last Modified: Wed, 15 Apr 2026 22:33:41 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:815e75efbdfc357ea1c282bc46d0c05078cc39f8542ecdaa316aa419d2a035c7`  
		Last Modified: Wed, 15 Apr 2026 22:33:42 GMT  
		Size: 14.3 MB (14301294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f65b8fbfc6e446502597cdfd6721e6481b592b818e40e9e23ec92d692a5e7834`  
		Last Modified: Wed, 15 Apr 2026 22:33:42 GMT  
		Size: 224.7 KB (224743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c7a901610f451a71a29354ccb88526064ed9a32c7f5c6239ef0ed0e6e898df2`  
		Last Modified: Tue, 28 Apr 2026 23:13:38 GMT  
		Size: 191.2 MB (191244150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c283bad56bd7baf193e210d98c4fecd8e301aa7d4aaf94e6aa737c0840e1c4c3`  
		Last Modified: Tue, 28 Apr 2026 23:13:40 GMT  
		Size: 344.5 MB (344522432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5af2ae8ab2e73ef4ea68ac0485e0097689d8def627a2b2d4e4330bc45844c1e1`  
		Last Modified: Tue, 28 Apr 2026 23:13:30 GMT  
		Size: 1.1 MB (1061586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d23cfcacd9aa55726084c41e908426c58cde3d90aa19ec0a507e670f7923ff1c`  
		Last Modified: Tue, 28 Apr 2026 23:13:30 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b31ff1a361d30a0b98d20d0b52124f3da05f91528468172094b2968fda01d57`  
		Last Modified: Tue, 28 Apr 2026 23:13:32 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:350a2dba6f1e0fade1d2596afec92587f8e4f22409069af917a5b8d92824dc16`  
		Last Modified: Tue, 28 Apr 2026 23:13:32 GMT  
		Size: 11.0 KB (11008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4029036b6de66ef4f1d53d0d26eaa8f41b3a7324d933562af498440622df46c7`  
		Last Modified: Tue, 28 Apr 2026 23:13:33 GMT  
		Size: 2.4 KB (2439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:stable-postgres-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:babdf68c13776f88e14e8775fa47f0eea9250da7efee575d05a72e82de9f1d74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9239041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:289de9a991007da37fb135c991c465ae7fb48740dcac2431c0c9accbaa850494`

```dockerfile
```

-	Layers:
	-	`sha256:99846801ae2f6bd5ed1bdb9a177d346a86e92b4554a7c73c3df5daefec5966e9`  
		Last Modified: Tue, 28 Apr 2026 23:13:31 GMT  
		Size: 9.2 MB (9198292 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33caf70a41d5f585148042e4bb9104367e26b49847b0cd58ebbb5266996826b1`  
		Last Modified: Tue, 28 Apr 2026 23:13:30 GMT  
		Size: 40.7 KB (40749 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:stable-postgres-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:c8b39ccb6f51f003612281c8df50bbe62d5f0c7ae0a68fc00b7b786e8905e070
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **647.1 MB (647075772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04916c6ee2219a9d7b8e781e76cb0fc70551cbc8f4d6781e3ff8f4820a9c903b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:34:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 20:34:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:34:21 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 20:34:21 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:34:21 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Wed, 15 Apr 2026 20:34:25 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='991be6ac6725e76109ecbd131d658f992dcbeacba3a8b4b6650302c8012b52fb';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_x64_linux_hotspot_21.0.10_7.tar.gz';          ;;        arm64)          ESUM='3ca84da7c4f57eee8d7e7f0645dc904a3a06456d32b37a4dd57a5e7527245250';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.10_7.tar.gz';          ;;        ppc64el)          ESUM='1a49cffcb348a28c017cf0deeb9322b7296dbfb002a8e43bd7f65ad671e10eb7';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.10_7.tar.gz';          ;;        riscv64)          ESUM='02cf763836c14bad4d689eb3b4efd691657de753dba07193cd1fb8691c8fe7b8';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_riscv64_linux_hotspot_21.0.10_7.tar.gz';          ;;        s390x)          ESUM='48f8529714c90c6cc61aa729cf8952f2fc47f2f2890551ba7f9e1c061b04be13';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_s390x_linux_hotspot_21.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 15 Apr 2026 20:34:25 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 15 Apr 2026 20:34:25 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:34:25 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 15 Apr 2026 22:42:07 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 15 Apr 2026 22:42:07 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:42:07 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Wed, 15 Apr 2026 22:42:07 GMT
WORKDIR /usr/local/tomcat
# Wed, 15 Apr 2026 22:42:07 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 15 Apr 2026 22:42:07 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 15 Apr 2026 22:42:07 GMT
ENV TOMCAT_MAJOR=10
# Wed, 15 Apr 2026 22:42:07 GMT
ENV TOMCAT_VERSION=10.1.54
# Wed, 15 Apr 2026 22:42:07 GMT
ENV TOMCAT_SHA512=8694b94324cf6f62ab032fa2438d7334518dcfcbf7878361b147246c46eb1e558c327f32c05fb4b7705c01fcca92fde392ce320934410f1169ff4ab36a1c7139
# Wed, 15 Apr 2026 22:42:09 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Wed, 15 Apr 2026 22:42:16 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 22:42:17 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Wed, 15 Apr 2026 22:42:17 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 15 Apr 2026 22:42:17 GMT
ENTRYPOINT []
# Wed, 15 Apr 2026 22:42:17 GMT
CMD ["catalina.sh" "run"]
# Tue, 28 Apr 2026 23:12:22 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 28 Apr 2026 23:12:22 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 28 Apr 2026 23:12:22 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 28 Apr 2026 23:12:22 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 28 Apr 2026 23:12:22 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 28 Apr 2026 23:12:22 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 28 Apr 2026 23:12:22 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 28 Apr 2026 23:12:22 GMT
ENV XWIKI_VERSION=18.3.0
# Tue, 28 Apr 2026 23:12:22 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/18.3.0
# Tue, 28 Apr 2026 23:12:22 GMT
ENV XWIKI_DOWNLOAD_SHA256=3a0594e4260bc832c8a42f9ea1d6f47d9da7c8ffb7bbe65b7c363e7e8308051a
# Tue, 28 Apr 2026 23:12:45 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Tue, 28 Apr 2026 23:12:45 GMT
ENV POSTGRES_JDBC_VERSION=42.7.10
# Tue, 28 Apr 2026 23:12:45 GMT
ENV POSTGRES_JDBC_SHA256=cab1cd67cfa25c25de4348e532298028288a877ba01c77d1619fe45416193387
# Tue, 28 Apr 2026 23:12:45 GMT
ENV POSTGRES_JDBC_PREFIX=https://repo1.maven.org/maven2/org/postgresql/postgresql/42.7.10
# Tue, 28 Apr 2026 23:12:45 GMT
ENV POSTGRES_JDBC_ARTIFACT=postgresql-42.7.10.jar
# Tue, 28 Apr 2026 23:12:45 GMT
ENV POSTGRES_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/postgresql-42.7.10.jar
# Tue, 28 Apr 2026 23:12:45 GMT
RUN curl -fSL "${POSTGRES_JDBC_PREFIX}/${POSTGRES_JDBC_ARTIFACT}" -o $POSTGRES_JDBC_TARGET &&   echo "$POSTGRES_JDBC_SHA256 $POSTGRES_JDBC_TARGET" | sha256sum -c - # buildkit
# Tue, 28 Apr 2026 23:12:45 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Tue, 28 Apr 2026 23:12:45 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Tue, 28 Apr 2026 23:12:45 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Tue, 28 Apr 2026 23:12:45 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 28 Apr 2026 23:12:45 GMT
VOLUME [/usr/local/xwiki]
# Tue, 28 Apr 2026 23:12:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Apr 2026 23:12:45 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:486a631f69c80b7795b8fcf134dbf766e684abb5f464f7f30c96e9875066a00e`  
		Last Modified: Wed, 15 Apr 2026 20:34:38 GMT  
		Size: 17.0 MB (16996216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f83e74af606fee97adef59c5c51391a86142bddd1eb4f5dc49b67c7ce855ed6`  
		Last Modified: Wed, 15 Apr 2026 20:34:39 GMT  
		Size: 52.2 MB (52155661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afbbab386f637266b7f19044839d529552165a7c76252310b921b5eceae7c31a`  
		Last Modified: Wed, 15 Apr 2026 20:34:37 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5df7fb31528c8565b18b86816315d1be1846c63b50782910b07e8df7b77c5fea`  
		Last Modified: Wed, 15 Apr 2026 20:34:38 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f257f30df764150a5589d300f5da1a40c3ced8ccdb5f2ccbc5bf4f0653ddd0e8`  
		Last Modified: Wed, 15 Apr 2026 22:42:25 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cd178cecdcc11ad6d0cf4af9f2287b1c7a57b1e20fc91e4f50616ccffdc32b4`  
		Last Modified: Wed, 15 Apr 2026 22:42:26 GMT  
		Size: 14.3 MB (14303388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a6cf75b8e1ed519c92739e54319fc713315690c62bf14ab011b5b168252f061`  
		Last Modified: Wed, 15 Apr 2026 22:42:25 GMT  
		Size: 225.2 KB (225215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5e76cc95ebff658e05feec0cd78ab40f1817bdb69311368e44cc8be1ccfc45f`  
		Last Modified: Tue, 28 Apr 2026 23:13:25 GMT  
		Size: 188.9 MB (188915571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:508bf62efaf7a4717bf84e22fcd705334a71a0cef0b97edc41a527e95fb600ed`  
		Last Modified: Tue, 28 Apr 2026 23:13:28 GMT  
		Size: 344.5 MB (344522443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:192225c1f3be3f172e30b382dc94ba2e76b6b1c71496eab22efe4608b7f997d4`  
		Last Modified: Tue, 28 Apr 2026 23:13:18 GMT  
		Size: 1.1 MB (1061591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d1c61d660d9b9df5e49056bb26eb0b779c2ee8ac2cf3c89d85bc8ea0c330ab8`  
		Last Modified: Tue, 28 Apr 2026 23:13:18 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4eaa606b7a54c59ae03c5cf7db3b8060a2ac95a07cfe9704d996882b671f408`  
		Last Modified: Tue, 28 Apr 2026 23:13:20 GMT  
		Size: 2.5 KB (2465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7887ae60f33168eadce16e0872447354d6094cbc3c26f06dd8483a6edebc9333`  
		Last Modified: Tue, 28 Apr 2026 23:13:20 GMT  
		Size: 11.0 KB (11009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b0fb20f9f1f82dd798dc34e8bd304dd2537a582a3204a2e4b0e61cfccf22516`  
		Last Modified: Tue, 28 Apr 2026 23:13:21 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:stable-postgres-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:258e64f8ae846a500f5e245e27210d6c12213fb1f80bfdf79bc3bb42757a61cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9239967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0795e4f0855f8eda1b09f34164b5780eb613d9e2db4729cd68b32ed0aa1d556c`

```dockerfile
```

-	Layers:
	-	`sha256:ccfcbfc7aeb0c3cc22ee6636f6b9c414684f978823441b50e4e766d3e4c18ec0`  
		Last Modified: Tue, 28 Apr 2026 23:13:19 GMT  
		Size: 9.2 MB (9199045 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c298a313cbec005f8884d882565b8a8ad602e8aa222701b38ed0cc572b8a7ca8`  
		Last Modified: Tue, 28 Apr 2026 23:13:18 GMT  
		Size: 40.9 KB (40922 bytes)  
		MIME: application/vnd.in-toto+json
