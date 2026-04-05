## `xwiki:stable-postgres`

```console
$ docker pull xwiki@sha256:a0a191db82cdfa165a69791822d077692ad3006f0d151d2b13cd91663fd802a3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:stable-postgres` - linux; amd64

```console
$ docker pull xwiki@sha256:f3627e06de53cc2cb51c8314ecd2a1fcddae9ad2db20755121148e453a2a3caf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **646.2 MB (646159241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:798e2684d7eb3d5beae809bba4c766f4f77597f0033c93cc041dda8060d0e4da`
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
# Fri, 03 Apr 2026 18:10:41 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 03 Apr 2026 18:10:41 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 Apr 2026 18:10:41 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Fri, 03 Apr 2026 18:10:41 GMT
WORKDIR /usr/local/tomcat
# Fri, 03 Apr 2026 18:10:41 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 03 Apr 2026 18:10:41 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 03 Apr 2026 18:10:41 GMT
ENV TOMCAT_MAJOR=10
# Fri, 03 Apr 2026 18:10:41 GMT
ENV TOMCAT_VERSION=10.1.54
# Fri, 03 Apr 2026 18:10:41 GMT
ENV TOMCAT_SHA512=8694b94324cf6f62ab032fa2438d7334518dcfcbf7878361b147246c46eb1e558c327f32c05fb4b7705c01fcca92fde392ce320934410f1169ff4ab36a1c7139
# Fri, 03 Apr 2026 18:10:41 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Fri, 03 Apr 2026 18:10:50 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 03 Apr 2026 18:10:50 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Fri, 03 Apr 2026 18:10:50 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 03 Apr 2026 18:10:50 GMT
ENTRYPOINT []
# Fri, 03 Apr 2026 18:10:50 GMT
CMD ["catalina.sh" "run"]
# Fri, 03 Apr 2026 19:11:16 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Fri, 03 Apr 2026 19:11:16 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Fri, 03 Apr 2026 19:11:16 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Fri, 03 Apr 2026 19:11:16 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Fri, 03 Apr 2026 19:11:16 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Fri, 03 Apr 2026 19:11:16 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Fri, 03 Apr 2026 19:11:16 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 03 Apr 2026 19:11:16 GMT
ENV XWIKI_VERSION=18.2.0
# Fri, 03 Apr 2026 19:11:16 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/18.2.0
# Fri, 03 Apr 2026 19:11:16 GMT
ENV XWIKI_DOWNLOAD_SHA256=1dbbf05fcb593f738a3f922c0d12bd4524c789a9f404e0e035bd6b2da2d1d26f
# Fri, 03 Apr 2026 19:11:39 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Fri, 03 Apr 2026 19:11:39 GMT
ENV POSTGRES_JDBC_VERSION=42.7.10
# Fri, 03 Apr 2026 19:11:39 GMT
ENV POSTGRES_JDBC_SHA256=cab1cd67cfa25c25de4348e532298028288a877ba01c77d1619fe45416193387
# Fri, 03 Apr 2026 19:11:39 GMT
ENV POSTGRES_JDBC_PREFIX=https://repo1.maven.org/maven2/org/postgresql/postgresql/42.7.10
# Fri, 03 Apr 2026 19:11:39 GMT
ENV POSTGRES_JDBC_ARTIFACT=postgresql-42.7.10.jar
# Fri, 03 Apr 2026 19:11:39 GMT
ENV POSTGRES_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/postgresql-42.7.10.jar
# Fri, 03 Apr 2026 19:11:40 GMT
RUN curl -fSL "${POSTGRES_JDBC_PREFIX}/${POSTGRES_JDBC_ARTIFACT}" -o $POSTGRES_JDBC_TARGET &&   echo "$POSTGRES_JDBC_SHA256 $POSTGRES_JDBC_TARGET" | sha256sum -c - # buildkit
# Fri, 03 Apr 2026 19:11:40 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Fri, 03 Apr 2026 19:11:40 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Fri, 03 Apr 2026 19:11:40 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Fri, 03 Apr 2026 19:11:40 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Fri, 03 Apr 2026 19:11:40 GMT
VOLUME [/usr/local/xwiki]
# Fri, 03 Apr 2026 19:11:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Apr 2026 19:11:40 GMT
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
	-	`sha256:131d49d157d95cbd54bf28befca298a2b188d01cd7353f56b361a011ef2a959b`  
		Last Modified: Fri, 03 Apr 2026 18:11:00 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:417e9af362e01e7131442569686c288308fb221bc78f5a6658847ed4b744ee4c`  
		Last Modified: Fri, 03 Apr 2026 18:11:00 GMT  
		Size: 14.3 MB (14301288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98c083d14ca258a3f5b4d89ecab64719562974385bd7d8a810e5248d77e09cc3`  
		Last Modified: Fri, 03 Apr 2026 18:11:00 GMT  
		Size: 1.6 MB (1639761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74cea2430eea35ba6b55723e4fd187954e6fea05764ba77460939907165c0865`  
		Last Modified: Fri, 03 Apr 2026 19:12:24 GMT  
		Size: 191.2 MB (191193086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c23d634c23047ecea1fe23519011b66d99e54b6b44f4576086d4c7ddbd89e2fc`  
		Last Modified: Fri, 03 Apr 2026 19:12:27 GMT  
		Size: 338.2 MB (338242837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11fbc65cdd7ae99323718d8d9aada7a15777859020b98b0cc20bb5f5a94de650`  
		Last Modified: Fri, 03 Apr 2026 19:12:17 GMT  
		Size: 1.1 MB (1061584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a1844e154a8e1d3d3e51bbb5888e47e12bd405a0f6d6495581b61dd2fdbd4f`  
		Last Modified: Fri, 03 Apr 2026 19:12:17 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3365e7fb0e2afa60018832ebc35958dc000b9b79689ab7f9b7301a7c80d947b`  
		Last Modified: Fri, 03 Apr 2026 19:12:19 GMT  
		Size: 2.5 KB (2463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83b7f2ddfd0c85ec0d05764d95d9f4f2ee7eaa70f7d70e36725c9d8fd141e4ca`  
		Last Modified: Fri, 03 Apr 2026 19:12:19 GMT  
		Size: 11.0 KB (10953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6002b2898f341588fc2c7e202a0fc1d6657d626c4ab3b5e4045fdf3670d643b1`  
		Last Modified: Fri, 03 Apr 2026 19:12:20 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:stable-postgres` - unknown; unknown

```console
$ docker pull xwiki@sha256:3f26376d101c228552459644121c1a9de80bf0e22152ab036304f6e86415e3ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9233532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec3def4597c7e7563f93d965668be4b024ad03df6061ee21a17c1a85cc2065ad`

```dockerfile
```

-	Layers:
	-	`sha256:3334654daf26bb0c57e99372014d4e05617542bcb3dcdc1ecd770876ba69d7ee`  
		Last Modified: Fri, 03 Apr 2026 19:12:18 GMT  
		Size: 9.2 MB (9192775 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13a864d7598bb0742d871cd867ef6ddec48087102bebeda082e4d84d7c4ac265`  
		Last Modified: Fri, 03 Apr 2026 19:12:17 GMT  
		Size: 40.8 KB (40757 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:stable-postgres` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:a43d6cdd2dd91c9f7e37b033d5fc2db53d236cb8f2f22302cbc5518f0fba4de0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **642.2 MB (642221097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8636abfd52e6ae35dac46fb138af8c9a3c4a5d8485dee911cdffbb106d22d8b4`
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
# Fri, 03 Apr 2026 18:10:38 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 03 Apr 2026 18:10:38 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 Apr 2026 18:10:38 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Fri, 03 Apr 2026 18:10:38 GMT
WORKDIR /usr/local/tomcat
# Fri, 03 Apr 2026 18:10:38 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 03 Apr 2026 18:10:38 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 03 Apr 2026 18:10:38 GMT
ENV TOMCAT_MAJOR=10
# Fri, 03 Apr 2026 18:10:38 GMT
ENV TOMCAT_VERSION=10.1.54
# Fri, 03 Apr 2026 18:10:38 GMT
ENV TOMCAT_SHA512=8694b94324cf6f62ab032fa2438d7334518dcfcbf7878361b147246c46eb1e558c327f32c05fb4b7705c01fcca92fde392ce320934410f1169ff4ab36a1c7139
# Fri, 03 Apr 2026 18:10:38 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Fri, 03 Apr 2026 18:10:48 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 03 Apr 2026 18:10:49 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Fri, 03 Apr 2026 18:10:49 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 03 Apr 2026 18:10:49 GMT
ENTRYPOINT []
# Fri, 03 Apr 2026 18:10:49 GMT
CMD ["catalina.sh" "run"]
# Fri, 03 Apr 2026 19:11:16 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Fri, 03 Apr 2026 19:11:16 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Fri, 03 Apr 2026 19:11:16 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Fri, 03 Apr 2026 19:11:16 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Fri, 03 Apr 2026 19:11:16 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Fri, 03 Apr 2026 19:11:16 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Fri, 03 Apr 2026 19:11:16 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 03 Apr 2026 19:11:16 GMT
ENV XWIKI_VERSION=18.2.0
# Fri, 03 Apr 2026 19:11:16 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/18.2.0
# Fri, 03 Apr 2026 19:11:16 GMT
ENV XWIKI_DOWNLOAD_SHA256=1dbbf05fcb593f738a3f922c0d12bd4524c789a9f404e0e035bd6b2da2d1d26f
# Fri, 03 Apr 2026 19:11:42 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Fri, 03 Apr 2026 19:11:42 GMT
ENV POSTGRES_JDBC_VERSION=42.7.10
# Fri, 03 Apr 2026 19:11:42 GMT
ENV POSTGRES_JDBC_SHA256=cab1cd67cfa25c25de4348e532298028288a877ba01c77d1619fe45416193387
# Fri, 03 Apr 2026 19:11:42 GMT
ENV POSTGRES_JDBC_PREFIX=https://repo1.maven.org/maven2/org/postgresql/postgresql/42.7.10
# Fri, 03 Apr 2026 19:11:42 GMT
ENV POSTGRES_JDBC_ARTIFACT=postgresql-42.7.10.jar
# Fri, 03 Apr 2026 19:11:42 GMT
ENV POSTGRES_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/postgresql-42.7.10.jar
# Fri, 03 Apr 2026 19:11:42 GMT
RUN curl -fSL "${POSTGRES_JDBC_PREFIX}/${POSTGRES_JDBC_ARTIFACT}" -o $POSTGRES_JDBC_TARGET &&   echo "$POSTGRES_JDBC_SHA256 $POSTGRES_JDBC_TARGET" | sha256sum -c - # buildkit
# Fri, 03 Apr 2026 19:11:42 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Fri, 03 Apr 2026 19:11:42 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Fri, 03 Apr 2026 19:11:42 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Fri, 03 Apr 2026 19:11:42 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Fri, 03 Apr 2026 19:11:42 GMT
VOLUME [/usr/local/xwiki]
# Fri, 03 Apr 2026 19:11:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Apr 2026 19:11:42 GMT
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
	-	`sha256:2fdbb005420d0488ac01418ae996fab349cb6d2d14740e23099bc1c826800a4e`  
		Last Modified: Fri, 03 Apr 2026 18:10:58 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6981e2ba09a603636306253c42625aaeac324110d92404bab431ff6127f3da5f`  
		Last Modified: Fri, 03 Apr 2026 18:10:58 GMT  
		Size: 14.3 MB (14303386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:947eeb35156714dc336354678cfcdd43f54b3cfed9a911a49d09aedfa7fc5335`  
		Last Modified: Fri, 03 Apr 2026 18:10:58 GMT  
		Size: 1.7 MB (1719582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27e7376fa5a4f8464b3b439ba323c4b1ca01e99eb3b3c4040f5075e08070eca0`  
		Last Modified: Fri, 03 Apr 2026 19:12:23 GMT  
		Size: 188.9 MB (188852540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6983fc0da81eef8e2a7cd6f19d66ae0afe1e48de8d510c7c2ee2fd59e7a0d113`  
		Last Modified: Fri, 03 Apr 2026 19:12:25 GMT  
		Size: 338.2 MB (338242713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbc5a0e56f1bbdceb71423173465453d3d7940691648a5010bfa6de4dbaa8686`  
		Last Modified: Fri, 03 Apr 2026 19:12:15 GMT  
		Size: 1.1 MB (1061589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77853612691c1a482e436d2bf1b2fdfde01d61e33e8d03c9b00ef21144e9a5b0`  
		Last Modified: Fri, 03 Apr 2026 19:12:15 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0365be6a61255953bfbb1d14b234f2fc998a116933bd50c95d5edd7f47b63b1`  
		Last Modified: Fri, 03 Apr 2026 19:12:16 GMT  
		Size: 2.5 KB (2466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a7b2f65785ff1cf235abb29ba05aefe72d43f44df80aa9ee409d64514dd2288`  
		Last Modified: Fri, 03 Apr 2026 19:12:17 GMT  
		Size: 11.0 KB (10956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d22e9d841deaad6a31cd9a002b9a5f384610bf464c5c640f94f96ba619fbf44f`  
		Last Modified: Fri, 03 Apr 2026 19:12:18 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:stable-postgres` - unknown; unknown

```console
$ docker pull xwiki@sha256:6495771e573ffd44cd14a7c51b2253920969f4159bfafd79bc8a5a5a88541e3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9234457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:113166d1d9605e1fbf16339a93a60d9c6af030dfccd865da8fe7f419b37eb33d`

```dockerfile
```

-	Layers:
	-	`sha256:dc1614fc89c022851635a65dd08e64fdd35fd7dd24e6e44dd0a5f21b3507bd9f`  
		Last Modified: Fri, 03 Apr 2026 19:12:16 GMT  
		Size: 9.2 MB (9193528 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d609f8943ce4289dde4caa88f7fec7ff0e993cd39296ccacc11bf11c59f106ef`  
		Last Modified: Fri, 03 Apr 2026 19:12:15 GMT  
		Size: 40.9 KB (40929 bytes)  
		MIME: application/vnd.in-toto+json
