## `xwiki:16-mysql-tomcat`

```console
$ docker pull xwiki@sha256:b72760aeac5ef5faa472b74a884ba1538cc18f8267e7f9cdbecb96e1668ca559
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:16-mysql-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:8a2fb1378949add2e70ceafaa7965e87c5fedf388ec90e3f6a12764b63bbc222
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **626.8 MB (626836229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da979e81b39dbd15adaa465c6aeded25b227a3c51e585324569276822b2a0025`
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
# Fri, 20 Mar 2026 21:01:55 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 20 Mar 2026 21:01:55 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Mar 2026 21:01:55 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Fri, 20 Mar 2026 21:01:55 GMT
WORKDIR /usr/local/tomcat
# Fri, 20 Mar 2026 21:01:55 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 20 Mar 2026 21:01:55 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 20 Mar 2026 21:01:55 GMT
ENV TOMCAT_MAJOR=9
# Fri, 20 Mar 2026 21:01:55 GMT
ENV TOMCAT_VERSION=9.0.116
# Fri, 20 Mar 2026 21:01:55 GMT
ENV TOMCAT_SHA512=a0992861f7615f0a79d372e84969a1bb48f603ef1687380d9a3579164dae7a1dea6b440e1bad27447f91a676528b2951634a0707616707f1df73cd27534ea5f9
# Fri, 20 Mar 2026 21:01:55 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Fri, 20 Mar 2026 21:02:02 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 20 Mar 2026 21:02:02 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Fri, 20 Mar 2026 21:02:02 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 20 Mar 2026 21:02:02 GMT
ENTRYPOINT []
# Fri, 20 Mar 2026 21:02:02 GMT
CMD ["catalina.sh" "run"]
# Fri, 20 Mar 2026 21:09:17 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Fri, 20 Mar 2026 21:09:17 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Fri, 20 Mar 2026 21:09:17 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Fri, 20 Mar 2026 21:09:17 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Fri, 20 Mar 2026 21:09:17 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Fri, 20 Mar 2026 21:09:17 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Fri, 20 Mar 2026 21:09:17 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 20 Mar 2026 21:09:17 GMT
ENV XWIKI_VERSION=16.10.17
# Fri, 20 Mar 2026 21:09:17 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/16.10.17
# Fri, 20 Mar 2026 21:09:17 GMT
ENV XWIKI_DOWNLOAD_SHA256=4e43dde6d4f971e789b8d38c06404ce14f40c65e2e541303fbb7d2151c113a85
# Fri, 20 Mar 2026 21:09:37 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Fri, 20 Mar 2026 21:09:37 GMT
ENV MYSQL_JDBC_VERSION=9.6.0
# Fri, 20 Mar 2026 21:09:37 GMT
ENV MYSQL_JDBC_SHA256=66df1d453789dc8cb759a7dc17f58646893bf28483f262328650f170472a6ead
# Fri, 20 Mar 2026 21:09:37 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/9.6.0
# Fri, 20 Mar 2026 21:09:37 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-9.6.0.jar
# Fri, 20 Mar 2026 21:09:37 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-9.6.0.jar
# Fri, 20 Mar 2026 21:09:37 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c - # buildkit
# Fri, 20 Mar 2026 21:09:37 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Fri, 20 Mar 2026 21:09:37 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Fri, 20 Mar 2026 21:09:38 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Fri, 20 Mar 2026 21:09:38 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Fri, 20 Mar 2026 21:09:38 GMT
VOLUME [/usr/local/xwiki]
# Fri, 20 Mar 2026 21:09:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Mar 2026 21:09:38 GMT
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
	-	`sha256:a27971d93a2204d3dee68a1b54d8ea5824ba8af1babf7522947557832ecc98c2`  
		Last Modified: Fri, 20 Mar 2026 21:02:11 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44c3c4fe46a502d7a5e8699a3e51c16ef6eb2764f8736f414f1018fa98ad8f7b`  
		Last Modified: Fri, 20 Mar 2026 21:02:12 GMT  
		Size: 13.8 MB (13785488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a00678576a6ed17d5e7caf209620f96c3fad4749e6478bc980cb038b6fe497c`  
		Last Modified: Fri, 20 Mar 2026 21:02:12 GMT  
		Size: 1.6 MB (1639745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b7be196d25150c302bdef909e16d1ec2deca6d04d329c970319587b86dc97a8`  
		Last Modified: Fri, 20 Mar 2026 21:10:19 GMT  
		Size: 191.2 MB (191193023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb4ab7d6268a7ba3e534e6ffe288f4f32d0f619788fd5ff5ee218e4b7edeecc9`  
		Last Modified: Fri, 20 Mar 2026 21:10:22 GMT  
		Size: 318.1 MB (318059891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0c48aa887ca826eae62d53406553235758a6828fa0e59ac770b6f203d1649b8`  
		Last Modified: Fri, 20 Mar 2026 21:10:13 GMT  
		Size: 2.4 MB (2441660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a464405e6855330d1af2c3f4d7f025a679ae07f14d5c524678c75efb12cef1a`  
		Last Modified: Fri, 20 Mar 2026 21:10:13 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44409a2dc6085f0c4ae44493a58e4b9d3ae5a0f094058518a79ca89b9acf0b29`  
		Last Modified: Fri, 20 Mar 2026 21:10:14 GMT  
		Size: 2.4 KB (2371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:902a98fcd599991ae4e6125dd8798eae52578deae11ecfc45c08327a86861363`  
		Last Modified: Fri, 20 Mar 2026 21:10:14 GMT  
		Size: 6.7 KB (6722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a0e9a2172487a466de9c41806308c657323749a683fefdc03d411efe3bb1139`  
		Last Modified: Fri, 20 Mar 2026 21:10:15 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:16-mysql-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:f7fd7f6fa0613500df1eedbfd91c8dba8fec1e6c34a08d7eeaac8c14177d14c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9151853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:949d44fa311b0a98a6e9fa0345200ddba3254a2ea61f4aef5113bb15027484cf`

```dockerfile
```

-	Layers:
	-	`sha256:915ef54ed5235a3e40e94278a78a68d9b6d86a9f87123ebd6d7c4bb71efe1657`  
		Last Modified: Fri, 20 Mar 2026 21:10:13 GMT  
		Size: 9.1 MB (9111256 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f9cfa3e08f11a5f31976715f506a57142c369f1357334bc19165a03649f332b`  
		Last Modified: Fri, 20 Mar 2026 21:10:12 GMT  
		Size: 40.6 KB (40597 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:16-mysql-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:4fa4e2541f5cf619cfcd83d7e596168b2e6a213dce0895073455e511dd5af229
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **622.9 MB (622905933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0bacac49e9bf81289a90c6c844a90bd30a3a92693c54313d18813d688dded02`
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
# Fri, 20 Mar 2026 21:06:22 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 20 Mar 2026 21:06:22 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Mar 2026 21:06:22 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Fri, 20 Mar 2026 21:06:22 GMT
WORKDIR /usr/local/tomcat
# Fri, 20 Mar 2026 21:06:22 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 20 Mar 2026 21:06:22 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 20 Mar 2026 21:06:22 GMT
ENV TOMCAT_MAJOR=9
# Fri, 20 Mar 2026 21:06:22 GMT
ENV TOMCAT_VERSION=9.0.116
# Fri, 20 Mar 2026 21:06:22 GMT
ENV TOMCAT_SHA512=a0992861f7615f0a79d372e84969a1bb48f603ef1687380d9a3579164dae7a1dea6b440e1bad27447f91a676528b2951634a0707616707f1df73cd27534ea5f9
# Fri, 20 Mar 2026 21:06:22 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Fri, 20 Mar 2026 21:06:30 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 20 Mar 2026 21:06:31 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Fri, 20 Mar 2026 21:06:31 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 20 Mar 2026 21:06:31 GMT
ENTRYPOINT []
# Fri, 20 Mar 2026 21:06:31 GMT
CMD ["catalina.sh" "run"]
# Fri, 20 Mar 2026 21:12:08 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Fri, 20 Mar 2026 21:12:08 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Fri, 20 Mar 2026 21:12:08 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Fri, 20 Mar 2026 21:12:08 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Fri, 20 Mar 2026 21:12:08 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Fri, 20 Mar 2026 21:12:08 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Fri, 20 Mar 2026 21:12:08 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 20 Mar 2026 21:12:08 GMT
ENV XWIKI_VERSION=16.10.17
# Fri, 20 Mar 2026 21:12:08 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/16.10.17
# Fri, 20 Mar 2026 21:12:08 GMT
ENV XWIKI_DOWNLOAD_SHA256=4e43dde6d4f971e789b8d38c06404ce14f40c65e2e541303fbb7d2151c113a85
# Fri, 20 Mar 2026 21:12:27 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Fri, 20 Mar 2026 21:12:27 GMT
ENV MYSQL_JDBC_VERSION=9.6.0
# Fri, 20 Mar 2026 21:12:27 GMT
ENV MYSQL_JDBC_SHA256=66df1d453789dc8cb759a7dc17f58646893bf28483f262328650f170472a6ead
# Fri, 20 Mar 2026 21:12:27 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/9.6.0
# Fri, 20 Mar 2026 21:12:27 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-9.6.0.jar
# Fri, 20 Mar 2026 21:12:27 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-9.6.0.jar
# Fri, 20 Mar 2026 21:12:28 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c - # buildkit
# Fri, 20 Mar 2026 21:12:28 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Fri, 20 Mar 2026 21:12:28 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Fri, 20 Mar 2026 21:12:28 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Fri, 20 Mar 2026 21:12:28 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Fri, 20 Mar 2026 21:12:28 GMT
VOLUME [/usr/local/xwiki]
# Fri, 20 Mar 2026 21:12:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Mar 2026 21:12:28 GMT
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
	-	`sha256:55f673c8a61e39c456a009da128218a6dfeb084091073b2184af3cb75f6e2357`  
		Last Modified: Fri, 20 Mar 2026 21:06:40 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df626aead37acbf8c6c4a650d2bd2ebb0802d27fbf626a851880abaf709e2abe`  
		Last Modified: Fri, 20 Mar 2026 21:06:40 GMT  
		Size: 13.8 MB (13794842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:418b36450a32259ef8ef57c1d8a31a8ade6fe13e1a0b5fa0246608fac87603be`  
		Last Modified: Fri, 20 Mar 2026 21:06:40 GMT  
		Size: 1.7 MB (1719522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39eb1f3c5082d68e9f65792f5374d0b13d225834e30a5aee7825108b20688001`  
		Last Modified: Fri, 20 Mar 2026 21:13:11 GMT  
		Size: 188.9 MB (188852929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45279cff8fc03969c4c9cf3314c3adcc437247b78547995ea39570b78cdff134`  
		Last Modified: Fri, 20 Mar 2026 21:13:15 GMT  
		Size: 318.1 MB (318059937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:402713d8217fd1c12a1b8a2b69f38a16fb22f8e254c78da0335f776547f2a9fe`  
		Last Modified: Fri, 20 Mar 2026 21:13:01 GMT  
		Size: 2.4 MB (2441665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e79b1796c916d97f0b790188d37dd1c8fd3d52f5c05aa8f300b7d1318a9de3`  
		Last Modified: Fri, 20 Mar 2026 21:13:01 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea3ce77f3337393d2881f79a33c018e435dfb0140447376e59481213e892be4a`  
		Last Modified: Fri, 20 Mar 2026 21:13:02 GMT  
		Size: 2.4 KB (2376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1472cf00eb80b156382734629b3936b75e5e87a6b35f79ff51bd61c1f39c52b3`  
		Last Modified: Fri, 20 Mar 2026 21:13:03 GMT  
		Size: 6.7 KB (6724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43caf07cb97895b5459c3084c6aa367a0f5b1f7dfeb736cc3622594038e340fc`  
		Last Modified: Fri, 20 Mar 2026 21:13:04 GMT  
		Size: 2.5 KB (2513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:16-mysql-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:977bf675b7099d390b0d385efd44f71b3a6630967df5a2e13217ead67512dbe6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9152780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf48ec8734f1747212e073f83ddc42f6d4a57793b2bbc491d02ff777a0fe4c3b`

```dockerfile
```

-	Layers:
	-	`sha256:4837bf702e88fcf51427804876baa50cfb03893632da0f984d8a3c77feed049d`  
		Last Modified: Fri, 20 Mar 2026 21:13:01 GMT  
		Size: 9.1 MB (9112009 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2bb214e1bc68e98f319a7a4328dbeddd64f3e8eeeb2fa99b4101c2cedbf53fc4`  
		Last Modified: Fri, 20 Mar 2026 21:13:00 GMT  
		Size: 40.8 KB (40771 bytes)  
		MIME: application/vnd.in-toto+json
