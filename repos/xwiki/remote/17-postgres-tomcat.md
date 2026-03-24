## `xwiki:17-postgres-tomcat`

```console
$ docker pull xwiki@sha256:747d4f631b2b7b07a93bdb0bfef020ef376b530afd8a5a1c8596b41c6e9a2547
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:17-postgres-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:8fde23037a3e77f4b1a6f858987253a90e22bd9a7e1a955f309f9c2c92a283a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **638.7 MB (638661968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:531ee4d884a72ad12fe60f63f67c34a0e3c1ee210014eeb1a5e8e621e81ecaf6`
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
# Mon, 23 Mar 2026 22:10:48 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Mon, 23 Mar 2026 22:10:48 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Mon, 23 Mar 2026 22:10:48 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Mon, 23 Mar 2026 22:10:48 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Mon, 23 Mar 2026 22:10:48 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Mon, 23 Mar 2026 22:10:48 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Mon, 23 Mar 2026 22:10:48 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Mar 2026 22:10:48 GMT
ENV XWIKI_VERSION=17.10.4
# Mon, 23 Mar 2026 22:10:48 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/17.10.4
# Mon, 23 Mar 2026 22:10:48 GMT
ENV XWIKI_DOWNLOAD_SHA256=02a853c7d1a171fa9a57d147734b1252fa6c4d89ba3dc5fcde9b0d76119888c3
# Mon, 23 Mar 2026 22:11:09 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Mon, 23 Mar 2026 22:11:09 GMT
ENV POSTGRES_JDBC_VERSION=42.7.10
# Mon, 23 Mar 2026 22:11:09 GMT
ENV POSTGRES_JDBC_SHA256=cab1cd67cfa25c25de4348e532298028288a877ba01c77d1619fe45416193387
# Mon, 23 Mar 2026 22:11:09 GMT
ENV POSTGRES_JDBC_PREFIX=https://repo1.maven.org/maven2/org/postgresql/postgresql/42.7.10
# Mon, 23 Mar 2026 22:11:09 GMT
ENV POSTGRES_JDBC_ARTIFACT=postgresql-42.7.10.jar
# Mon, 23 Mar 2026 22:11:09 GMT
ENV POSTGRES_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/postgresql-42.7.10.jar
# Mon, 23 Mar 2026 22:11:09 GMT
RUN curl -fSL "${POSTGRES_JDBC_PREFIX}/${POSTGRES_JDBC_ARTIFACT}" -o $POSTGRES_JDBC_TARGET &&   echo "$POSTGRES_JDBC_SHA256 $POSTGRES_JDBC_TARGET" | sha256sum -c - # buildkit
# Mon, 23 Mar 2026 22:11:09 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Mon, 23 Mar 2026 22:11:09 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Mon, 23 Mar 2026 22:11:09 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Mon, 23 Mar 2026 22:11:09 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Mon, 23 Mar 2026 22:11:09 GMT
VOLUME [/usr/local/xwiki]
# Mon, 23 Mar 2026 22:11:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2026 22:11:09 GMT
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
	-	`sha256:f073f4570694949f37637d771baf4d7891910a54747a2814f665d9d4a7f89b3b`  
		Last Modified: Mon, 23 Mar 2026 22:11:47 GMT  
		Size: 191.2 MB (191192956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab832f7eca6e13efa17480dd614f263d85a995ff65b630007355e76cc528041d`  
		Last Modified: Mon, 23 Mar 2026 22:11:50 GMT  
		Size: 330.7 MB (330747775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fd81debc711a25e3e993211cdd78c2008ea22247b97193fed8262ce52e40afc`  
		Last Modified: Mon, 23 Mar 2026 22:11:41 GMT  
		Size: 1.1 MB (1061589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab54399c515b732fd7c9e75f23b78ff206d9e831c7ea4fc154e8ef65a31d4f13`  
		Last Modified: Mon, 23 Mar 2026 22:11:41 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:297e462556c2a66b7fa3ab52cb998309535c9dd4eddbc92747154994daf1ea8a`  
		Last Modified: Mon, 23 Mar 2026 22:11:43 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b4c5db74c5bda2d1fb86b6512b0d8f3d331df80b119dd051aa21496b107e581`  
		Last Modified: Mon, 23 Mar 2026 22:11:43 GMT  
		Size: 10.7 KB (10701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dac7a995c9cedf22d2893e6cd6d0a0375ab26d6ca7be0e04aaa1da434b7d3df5`  
		Last Modified: Mon, 23 Mar 2026 22:11:44 GMT  
		Size: 2.4 KB (2414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:17-postgres-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:1b2cb25d7fdc8667b1dd136b9753f5fad517074994b5a05b5f51fbf1969bf5e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9220172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c493f9c29eea73848cb2c3f96ef989ab9d85024ae18e186a57a49463420d6051`

```dockerfile
```

-	Layers:
	-	`sha256:c99e209161b4500c94bbb442ada1b0db583f5f90dfbdee59ca8d6ca69a101f04`  
		Last Modified: Mon, 23 Mar 2026 22:11:42 GMT  
		Size: 9.2 MB (9179727 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2894c2ae02e0b4f130102cf835aa1416f8a6c04b7e329b0c3db3f4dca5dfc55d`  
		Last Modified: Mon, 23 Mar 2026 22:11:41 GMT  
		Size: 40.4 KB (40445 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:17-postgres-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:5f87b5d0f21e51c85707792cd40be8597acf0a20972ac2f3560be028697363b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **634.7 MB (634723957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca2ac4af4b056d4adc40b7aef2fa95c119c764cd2c7b361844f1ae9de2878a8a`
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
# Mon, 23 Mar 2026 22:08:00 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Mon, 23 Mar 2026 22:08:00 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Mon, 23 Mar 2026 22:08:00 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Mon, 23 Mar 2026 22:08:00 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Mon, 23 Mar 2026 22:08:00 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Mon, 23 Mar 2026 22:08:00 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Mon, 23 Mar 2026 22:08:00 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Mar 2026 22:08:00 GMT
ENV XWIKI_VERSION=17.10.4
# Mon, 23 Mar 2026 22:08:00 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/17.10.4
# Mon, 23 Mar 2026 22:08:00 GMT
ENV XWIKI_DOWNLOAD_SHA256=02a853c7d1a171fa9a57d147734b1252fa6c4d89ba3dc5fcde9b0d76119888c3
# Mon, 23 Mar 2026 22:08:23 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Mon, 23 Mar 2026 22:08:23 GMT
ENV POSTGRES_JDBC_VERSION=42.7.10
# Mon, 23 Mar 2026 22:08:23 GMT
ENV POSTGRES_JDBC_SHA256=cab1cd67cfa25c25de4348e532298028288a877ba01c77d1619fe45416193387
# Mon, 23 Mar 2026 22:08:23 GMT
ENV POSTGRES_JDBC_PREFIX=https://repo1.maven.org/maven2/org/postgresql/postgresql/42.7.10
# Mon, 23 Mar 2026 22:08:23 GMT
ENV POSTGRES_JDBC_ARTIFACT=postgresql-42.7.10.jar
# Mon, 23 Mar 2026 22:08:23 GMT
ENV POSTGRES_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/postgresql-42.7.10.jar
# Mon, 23 Mar 2026 22:08:23 GMT
RUN curl -fSL "${POSTGRES_JDBC_PREFIX}/${POSTGRES_JDBC_ARTIFACT}" -o $POSTGRES_JDBC_TARGET &&   echo "$POSTGRES_JDBC_SHA256 $POSTGRES_JDBC_TARGET" | sha256sum -c - # buildkit
# Mon, 23 Mar 2026 22:08:23 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Mon, 23 Mar 2026 22:08:23 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Mon, 23 Mar 2026 22:08:23 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Mon, 23 Mar 2026 22:08:23 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Mon, 23 Mar 2026 22:08:23 GMT
VOLUME [/usr/local/xwiki]
# Mon, 23 Mar 2026 22:08:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2026 22:08:23 GMT
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
	-	`sha256:58b5227a7e80320f8385c40fa0124af724c8c5694ab43ac948dc4d022da82e25`  
		Last Modified: Mon, 23 Mar 2026 22:09:01 GMT  
		Size: 188.9 MB (188852724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09cf302c41df369ad3d56a85f0dd5e5b39acb0326afd3ec8903de1992c1999f6`  
		Last Modified: Mon, 23 Mar 2026 22:09:04 GMT  
		Size: 330.7 MB (330747747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f6f19d9f7074a735cef1dc17efec0f213c7761ab4fa235b8239cfaf3b2206dd`  
		Last Modified: Mon, 23 Mar 2026 22:08:55 GMT  
		Size: 1.1 MB (1061584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd628e3584cea6b39d2089096aff30d29fffe1f8096a3474a55858019444e8d0`  
		Last Modified: Mon, 23 Mar 2026 22:08:55 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe0b4bde88e409a4cfafb94152631be30a104a25040c8b8435700f56a543a87c`  
		Last Modified: Mon, 23 Mar 2026 22:08:56 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dd92d0f6b5e65c5b445e9e05388aa4bd2a72ba388502f6e3f6ff8dc03ffa567`  
		Last Modified: Mon, 23 Mar 2026 22:08:57 GMT  
		Size: 10.7 KB (10695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d625a4455173f8ea28e10aeaa84e0b4313b3c552df341e75383fc74c3d3fc3f9`  
		Last Modified: Mon, 23 Mar 2026 22:08:58 GMT  
		Size: 2.4 KB (2414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:17-postgres-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:f6f69fcee362d972d140675a1108a40f8e5638e4398bd98062e69c45428a968a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9221074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dbd57ca2294b4d966a0e1e90a94e5c3db577193399908ea2a7323bae805de33`

```dockerfile
```

-	Layers:
	-	`sha256:d338b7b5205ca7f693ca47a77561ec022c1466bb4de54087bb83089a8b4fa29d`  
		Last Modified: Mon, 23 Mar 2026 22:08:55 GMT  
		Size: 9.2 MB (9180468 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66226fa6059744301e025e91feaaede2d80ebe2eb273a19216841ec367526c38`  
		Last Modified: Mon, 23 Mar 2026 22:08:55 GMT  
		Size: 40.6 KB (40606 bytes)  
		MIME: application/vnd.in-toto+json
