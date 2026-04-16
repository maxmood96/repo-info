## `xwiki:lts`

```console
$ docker pull xwiki@sha256:9e65669ec903c94032a7c64ae8e1730d9ca77b2ade0287434b41409fde3b0a45
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:lts` - linux; amd64

```console
$ docker pull xwiki@sha256:dd8cadcca1d6279faa398e786b912f7ad0d086bafc882631afcdf0a369bcb29e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **639.2 MB (639184587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9ee5e036b2e1a687f9af7c39e18b56df32d0907f7b82311daa7cd5e7f066950`
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
# Wed, 15 Apr 2026 23:17:08 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 15 Apr 2026 23:17:08 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 15 Apr 2026 23:17:08 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 15 Apr 2026 23:17:08 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 15 Apr 2026 23:17:08 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 15 Apr 2026 23:17:08 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 15 Apr 2026 23:17:08 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 23:17:08 GMT
ENV XWIKI_VERSION=17.10.7
# Wed, 15 Apr 2026 23:17:08 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/17.10.7
# Wed, 15 Apr 2026 23:17:08 GMT
ENV XWIKI_DOWNLOAD_SHA256=df33fb71c7149bfc05a24db32ed0d2c3fd91c15d2a562cfed425c71d5f47a91f
# Wed, 15 Apr 2026 23:17:33 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Wed, 15 Apr 2026 23:17:33 GMT
ENV MYSQL_JDBC_VERSION=9.6.0
# Wed, 15 Apr 2026 23:17:33 GMT
ENV MYSQL_JDBC_SHA256=66df1d453789dc8cb759a7dc17f58646893bf28483f262328650f170472a6ead
# Wed, 15 Apr 2026 23:17:33 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/9.6.0
# Wed, 15 Apr 2026 23:17:33 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-9.6.0.jar
# Wed, 15 Apr 2026 23:17:33 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-9.6.0.jar
# Wed, 15 Apr 2026 23:17:34 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c - # buildkit
# Wed, 15 Apr 2026 23:17:34 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Wed, 15 Apr 2026 23:17:34 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Wed, 15 Apr 2026 23:17:34 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Wed, 15 Apr 2026 23:17:34 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Wed, 15 Apr 2026 23:17:34 GMT
VOLUME [/usr/local/xwiki]
# Wed, 15 Apr 2026 23:17:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 23:17:34 GMT
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
	-	`sha256:73921747dcc9e939023b62f1800e0333d1557bee538405cb10391395d68ab628`  
		Last Modified: Wed, 15 Apr 2026 23:18:16 GMT  
		Size: 191.2 MB (191192524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23bb75c601ea8cecebf3b4251c52a0d4542b6817cbbcea729d68134dd8bc7d74`  
		Last Modified: Wed, 15 Apr 2026 23:18:19 GMT  
		Size: 331.3 MB (331302917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d43fd24c770cebb730df667b53952f39718705a08f743a77b280a7d6cce4fadb`  
		Last Modified: Wed, 15 Apr 2026 23:18:09 GMT  
		Size: 2.4 MB (2441665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80339f7839494de0b33bb765f7ceab7a3248da3b98ccb221c502a4f1deae41ad`  
		Last Modified: Wed, 15 Apr 2026 23:18:09 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00465cd8256c6d42789ec1bf41c529c83121073949078cbcf4ead80d26845d56`  
		Last Modified: Wed, 15 Apr 2026 23:18:10 GMT  
		Size: 2.4 KB (2372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54b998c80dcf2893e03d977c525d3a5c1edeb47fe286b4d3d93daa9920fcc9bc`  
		Last Modified: Wed, 15 Apr 2026 23:18:10 GMT  
		Size: 10.7 KB (10678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07b71818e17117c03299659761b0d02f29f32c21917960abff42c51e9a29bae2`  
		Last Modified: Wed, 15 Apr 2026 23:18:11 GMT  
		Size: 2.5 KB (2533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:lts` - unknown; unknown

```console
$ docker pull xwiki@sha256:70c043b75e41579a60197d20c5db0366af83e1d440dfcd50af28406272d13198
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9222462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d8f7d30bc24386ccd158c0b0ded142142d83662b5fb3e378ecd141aef36ef5f`

```dockerfile
```

-	Layers:
	-	`sha256:22cd647a6ba6b8cdf1e8a20372d9b3dd6ce31c21cc30bd755764c32f0f95e479`  
		Last Modified: Wed, 15 Apr 2026 23:18:09 GMT  
		Size: 9.2 MB (9180967 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e88b79eba0ac167bda7bb9bf54df901c5919308d7d84c8b9ad9e9e881298ff3e`  
		Last Modified: Wed, 15 Apr 2026 23:18:08 GMT  
		Size: 41.5 KB (41495 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:lts` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:0da1f85d610d4c728dd5515877e5e412903668f66802165d180a5853aeee78cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **635.2 MB (635172682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9d24be65e66cd226d8a08a84efa52d16e55fe092d8d88340d010825f7b68dd9`
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
# Wed, 15 Apr 2026 23:15:05 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 15 Apr 2026 23:15:05 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 15 Apr 2026 23:15:05 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 15 Apr 2026 23:15:05 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 15 Apr 2026 23:15:05 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 15 Apr 2026 23:15:05 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 15 Apr 2026 23:15:05 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 23:15:05 GMT
ENV XWIKI_VERSION=17.10.7
# Wed, 15 Apr 2026 23:15:05 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/17.10.7
# Wed, 15 Apr 2026 23:15:05 GMT
ENV XWIKI_DOWNLOAD_SHA256=df33fb71c7149bfc05a24db32ed0d2c3fd91c15d2a562cfed425c71d5f47a91f
# Wed, 15 Apr 2026 23:15:28 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Wed, 15 Apr 2026 23:15:28 GMT
ENV MYSQL_JDBC_VERSION=9.6.0
# Wed, 15 Apr 2026 23:15:28 GMT
ENV MYSQL_JDBC_SHA256=66df1d453789dc8cb759a7dc17f58646893bf28483f262328650f170472a6ead
# Wed, 15 Apr 2026 23:15:28 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/9.6.0
# Wed, 15 Apr 2026 23:15:28 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-9.6.0.jar
# Wed, 15 Apr 2026 23:15:28 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-9.6.0.jar
# Wed, 15 Apr 2026 23:15:28 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c - # buildkit
# Wed, 15 Apr 2026 23:15:28 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Wed, 15 Apr 2026 23:15:28 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Wed, 15 Apr 2026 23:15:28 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Wed, 15 Apr 2026 23:15:28 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Wed, 15 Apr 2026 23:15:28 GMT
VOLUME [/usr/local/xwiki]
# Wed, 15 Apr 2026 23:15:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 23:15:28 GMT
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
	-	`sha256:e8a8b0f29cc0a388466ee60a2f81f1af6e6c075a0c038d3a7f5b01db28a6ba30`  
		Last Modified: Wed, 15 Apr 2026 23:16:10 GMT  
		Size: 188.9 MB (188852204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ec2663e0fc01fdafb9232a088b2986b0e1fb6d7f94a784cf16f4b602824c230`  
		Last Modified: Wed, 15 Apr 2026 23:16:13 GMT  
		Size: 331.3 MB (331302974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97cb0734211c2e583bafd34512eafcf3f5e9af5e025e15c79a877becdc0827d3`  
		Last Modified: Wed, 15 Apr 2026 23:16:01 GMT  
		Size: 2.4 MB (2441663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af0e644212bfaf83eb247ed6230309fe77a6421321fada845f4dce7412ffd84b`  
		Last Modified: Wed, 15 Apr 2026 23:16:01 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5aaa07bce10cd752646536fc80eddd5620214f7f2ef6e298420d9b2b3a17b97`  
		Last Modified: Wed, 15 Apr 2026 23:16:03 GMT  
		Size: 2.4 KB (2373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f4844be76a42c9e3b20811c749203bd14f2df95561986fce11e37588b0bd73b`  
		Last Modified: Wed, 15 Apr 2026 23:16:03 GMT  
		Size: 10.7 KB (10677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72920b53feaec420936641c5132bee9b4d4e0ef52d0d7af6ee6db2c2a97ad968`  
		Last Modified: Wed, 15 Apr 2026 23:16:04 GMT  
		Size: 2.5 KB (2536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:lts` - unknown; unknown

```console
$ docker pull xwiki@sha256:cd3c917ce35ef944a503d53b97683941829daf4455fe08716edd5e709ae75f3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9223460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:198d93e8eee77e4c815c88d07372441538c6d8eea249799d07b4f487f8031b6a`

```dockerfile
```

-	Layers:
	-	`sha256:8625a72bc6c4effb9c2b009f67c2c2ce30d39454a966ac89d00cd808ab23c9ba`  
		Last Modified: Wed, 15 Apr 2026 23:16:01 GMT  
		Size: 9.2 MB (9181756 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5dbf01ef7f62ac8e6c48ba3c3ae441a17b7d4d51c9d2e988fc374d5e8a7fb4c`  
		Last Modified: Wed, 15 Apr 2026 23:16:01 GMT  
		Size: 41.7 KB (41704 bytes)  
		MIME: application/vnd.in-toto+json
