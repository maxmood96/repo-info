## `xwiki:15-mysql-tomcat`

```console
$ docker pull xwiki@sha256:2a286ba808ca989f0894608e2b696a98a6a301b0a71f611b507654e0302b8f32
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:15-mysql-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:94df11f193f65bca19bb66867cb98b4b1ab8193319ca83adaade23e6685e8602
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **609.3 MB (609303502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79af69e9124e871730519c412a01688f1d72ce8b767679f53ca8f6e1d70ebf40`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 03 Sep 2024 05:14:18 GMT
ARG RELEASE
# Tue, 03 Sep 2024 05:14:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 03 Sep 2024 05:14:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 03 Sep 2024 05:14:18 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 03 Sep 2024 05:14:18 GMT
ADD file:6f881131af38dde06e3705e8376701ae22ce479e4824821a9580d4e0e0bcf0ac in / 
# Tue, 03 Sep 2024 05:14:18 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        riscv64)          ESUM='2d1ed42918305a1a0754a6e1e9294c7d4d7fda4bff6dba7bc5682037d860dbc9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 03 Sep 2024 05:14:18 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 03 Sep 2024 05:14:18 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Sep 2024 05:14:18 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 03 Sep 2024 05:14:18 GMT
WORKDIR /usr/local/tomcat
# Tue, 03 Sep 2024 05:14:18 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 03 Sep 2024 05:14:18 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 03 Sep 2024 05:14:18 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 03 Sep 2024 05:14:18 GMT
ENV TOMCAT_MAJOR=9
# Tue, 03 Sep 2024 05:14:18 GMT
ENV TOMCAT_VERSION=9.0.95
# Tue, 03 Sep 2024 05:14:18 GMT
ENV TOMCAT_SHA512=b18103153169c7bf98da055f8ba0ac3e141d121c78869881d3be480e90fcbc3a178a8e71fa70a11aee7f2584727df72be15d30331faec65f4e57c7e67c85c1cf
# Tue, 03 Sep 2024 05:14:18 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 03 Sep 2024 05:14:18 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Sep 2024 05:14:18 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 03 Sep 2024 05:14:18 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 03 Sep 2024 05:14:18 GMT
ENTRYPOINT []
# Tue, 03 Sep 2024 05:14:18 GMT
CMD ["catalina.sh" "run"]
# Tue, 03 Sep 2024 05:14:18 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 03 Sep 2024 05:14:18 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 03 Sep 2024 05:14:18 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 03 Sep 2024 05:14:18 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 03 Sep 2024 05:14:18 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 03 Sep 2024 05:14:18 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 03 Sep 2024 05:14:18 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Sep 2024 05:14:18 GMT
ENV XWIKI_VERSION=15.10.12
# Tue, 03 Sep 2024 05:14:18 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.10.12
# Tue, 03 Sep 2024 05:14:18 GMT
ENV XWIKI_DOWNLOAD_SHA256=bf9658d49dd1cb1735864f09b88d19b9b26a3df5d3fe73a003e2171fa07e327c
# Tue, 03 Sep 2024 05:14:18 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Tue, 03 Sep 2024 05:14:18 GMT
ENV MYSQL_JDBC_VERSION=8.4.0
# Tue, 03 Sep 2024 05:14:18 GMT
ENV MYSQL_JDBC_SHA256=d77962877d010777cff997015da90ee689f0f4bb76848340e1488f2b83332af5
# Tue, 03 Sep 2024 05:14:18 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/8.4.0
# Tue, 03 Sep 2024 05:14:18 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-8.4.0.jar
# Tue, 03 Sep 2024 05:14:18 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-8.4.0.jar
# Tue, 03 Sep 2024 05:14:18 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c - # buildkit
# Tue, 03 Sep 2024 05:14:18 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Tue, 03 Sep 2024 05:14:18 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Tue, 03 Sep 2024 05:14:18 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Tue, 03 Sep 2024 05:14:18 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 03 Sep 2024 05:14:18 GMT
VOLUME [/usr/local/xwiki]
# Tue, 03 Sep 2024 05:14:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Sep 2024 05:14:18 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:c9d5878ec977245f708710279e48c0cbd915438e6f9f9d54a89d6ec7b72c10ec`  
		Last Modified: Mon, 16 Sep 2024 10:01:56 GMT  
		Size: 30.6 MB (30611480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19e2b658c0415582a9e1e9e5e778b5a30dcef669f8cfb52328d877f5119fa975`  
		Last Modified: Wed, 02 Oct 2024 02:20:50 GMT  
		Size: 13.8 MB (13770567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d70706c17bac15dc03bd8003b9759f3c17ca534520872f203ec47a93d3ebf41`  
		Last Modified: Wed, 02 Oct 2024 02:23:42 GMT  
		Size: 47.3 MB (47280216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f38b2cb3461381dc800fef399f230710e1e6f252046b0407f9fa8f0ae53aed90`  
		Last Modified: Wed, 02 Oct 2024 02:23:36 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10e52ba1b5dc27a31b061fab0ca39b995930c3125db5effbf3ab06353765d26d`  
		Last Modified: Wed, 02 Oct 2024 02:23:36 GMT  
		Size: 2.1 KB (2107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf30497a5f5a3d62a1e7e57e404ccbaf2c90c1984bf6638e734c5c3f7e4a51a4`  
		Last Modified: Wed, 02 Oct 2024 03:57:05 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aad30440d6ce1f1359974329573042be5d966af209f98b7b621bba4b1089a35a`  
		Last Modified: Wed, 02 Oct 2024 03:57:07 GMT  
		Size: 13.4 MB (13378068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19f1f48a918fa8610539a3d9a79e47ed108c7add729797f180a62a4958abfc15`  
		Last Modified: Wed, 02 Oct 2024 03:57:07 GMT  
		Size: 212.4 KB (212439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c5db9986fab60430f16cb1b76ba7b96e7fcc359e66e92416b124b112e6c47a8`  
		Last Modified: Wed, 02 Oct 2024 04:56:29 GMT  
		Size: 194.6 MB (194635027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0a830d89528b4f3f1410e91e649c5ddb6ad56020593c2ddc23dbb0f99d94504`  
		Last Modified: Wed, 02 Oct 2024 04:56:33 GMT  
		Size: 307.0 MB (307006982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f888601510130b0dd2f2ed7e76fdb9f2964bfdf0616cd30b4ebc16942ef2256`  
		Last Modified: Wed, 02 Oct 2024 04:56:24 GMT  
		Size: 2.4 MB (2393572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fb3d6c6c2e8538f11da6fca0cd57f20ecb868382c0fe0f16aedf84c92331650`  
		Last Modified: Wed, 02 Oct 2024 04:56:24 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61113b5645303a4fab4d910d9e2e9f04a4725a3c5e7e3779f104b1c2271d9745`  
		Last Modified: Wed, 02 Oct 2024 04:56:24 GMT  
		Size: 2.4 KB (2370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c346ed92bb8a3c82902d94661fbbff8ee043d4382a3def0cd66e9ec7e08aac13`  
		Last Modified: Wed, 02 Oct 2024 04:56:25 GMT  
		Size: 6.5 KB (6462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff10125bebaabeb805ff3ba588f17c65f50b24a951a103f07138fbb8bb67bfd2`  
		Last Modified: Wed, 02 Oct 2024 04:56:26 GMT  
		Size: 2.5 KB (2508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:15-mysql-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:123a9442a3180ffb5f84f53ac47b353e3de285b627e36ab31eeb7c942d22ac11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8706833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b96239a46f9c44de4d41f1b534f7ea67e37f7e4109d85ce0cf702c7702e52a05`

```dockerfile
```

-	Layers:
	-	`sha256:8fd80acbaf43ffbef991348374875e7522962f1846062f4e7963e9bb730a1b28`  
		Last Modified: Wed, 02 Oct 2024 04:56:24 GMT  
		Size: 8.7 MB (8664789 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1914a5b2bc1b306c1592f027a34464aa2956398a5dfe81a29fdc82f22f370f3`  
		Last Modified: Wed, 02 Oct 2024 04:56:23 GMT  
		Size: 42.0 KB (42044 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:15-mysql-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:50d0297ae4c356329e44535425d4ab4387451c8227cad54318919411bf9d6596
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **607.7 MB (607692913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9f9d5c853caf77ceeddc487dde9c63398202aefdef87c37812a185838b95b23`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 27 Aug 2024 15:55:18 GMT
ARG RELEASE
# Tue, 27 Aug 2024 15:55:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Aug 2024 15:55:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Aug 2024 15:55:18 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 27 Aug 2024 15:55:20 GMT
ADD file:326f7645aedaef39f6ed8d915cfab4d497b0b35ba156d1d1449a5a2eea30f71c in / 
# Tue, 27 Aug 2024 15:55:20 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        riscv64)          ESUM='2d1ed42918305a1a0754a6e1e9294c7d4d7fda4bff6dba7bc5682037d860dbc9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 03 Sep 2024 05:14:18 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 03 Sep 2024 05:14:18 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Sep 2024 05:14:18 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 03 Sep 2024 05:14:18 GMT
WORKDIR /usr/local/tomcat
# Tue, 03 Sep 2024 05:14:18 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 03 Sep 2024 05:14:18 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 03 Sep 2024 05:14:18 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 03 Sep 2024 05:14:18 GMT
ENV TOMCAT_MAJOR=9
# Tue, 03 Sep 2024 05:14:18 GMT
ENV TOMCAT_VERSION=9.0.95
# Tue, 03 Sep 2024 05:14:18 GMT
ENV TOMCAT_SHA512=b18103153169c7bf98da055f8ba0ac3e141d121c78869881d3be480e90fcbc3a178a8e71fa70a11aee7f2584727df72be15d30331faec65f4e57c7e67c85c1cf
# Tue, 03 Sep 2024 05:14:18 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 03 Sep 2024 05:14:18 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Sep 2024 05:14:18 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 03 Sep 2024 05:14:18 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 03 Sep 2024 05:14:18 GMT
ENTRYPOINT []
# Tue, 03 Sep 2024 05:14:18 GMT
CMD ["catalina.sh" "run"]
# Tue, 03 Sep 2024 05:14:18 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 03 Sep 2024 05:14:18 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 03 Sep 2024 05:14:18 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 03 Sep 2024 05:14:18 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 03 Sep 2024 05:14:18 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 03 Sep 2024 05:14:18 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 03 Sep 2024 05:14:18 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Sep 2024 05:14:18 GMT
ENV XWIKI_VERSION=15.10.12
# Tue, 03 Sep 2024 05:14:18 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.10.12
# Tue, 03 Sep 2024 05:14:18 GMT
ENV XWIKI_DOWNLOAD_SHA256=bf9658d49dd1cb1735864f09b88d19b9b26a3df5d3fe73a003e2171fa07e327c
# Tue, 03 Sep 2024 05:14:18 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Tue, 03 Sep 2024 05:14:18 GMT
ENV MYSQL_JDBC_VERSION=8.4.0
# Tue, 03 Sep 2024 05:14:18 GMT
ENV MYSQL_JDBC_SHA256=d77962877d010777cff997015da90ee689f0f4bb76848340e1488f2b83332af5
# Tue, 03 Sep 2024 05:14:18 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/8.4.0
# Tue, 03 Sep 2024 05:14:18 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-8.4.0.jar
# Tue, 03 Sep 2024 05:14:18 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-8.4.0.jar
# Tue, 03 Sep 2024 05:14:18 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c - # buildkit
# Tue, 03 Sep 2024 05:14:18 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Tue, 03 Sep 2024 05:14:18 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Tue, 03 Sep 2024 05:14:18 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Tue, 03 Sep 2024 05:14:18 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 03 Sep 2024 05:14:18 GMT
VOLUME [/usr/local/xwiki]
# Tue, 03 Sep 2024 05:14:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Sep 2024 05:14:18 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:8a9c853c85e5a53a79f6bc6965cf01799f75bd947d761fc492da5738058f87a2`  
		Last Modified: Sat, 31 Aug 2024 18:28:27 GMT  
		Size: 30.0 MB (29953205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc10c682b9856cc71f6540269cbf6510c4d5c4b07d334875eb836c645d4cd40c`  
		Last Modified: Tue, 17 Sep 2024 01:37:44 GMT  
		Size: 16.0 MB (16010924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5717cce9082839b9cfb5f9b7614bc727f29f41b61f4f2feaaf9d55458acf33a`  
		Last Modified: Tue, 17 Sep 2024 01:40:18 GMT  
		Size: 46.7 MB (46746410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abec6865e9dddd9444d0e2eca0f0eb03af187efef87b0481c225769487e02a5b`  
		Last Modified: Tue, 17 Sep 2024 01:40:13 GMT  
		Size: 161.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6f03107128f2014deac55fbb63e2c5001daf5fc478434cc12956f8b3e6e9fc7`  
		Last Modified: Tue, 17 Sep 2024 01:40:13 GMT  
		Size: 2.1 KB (2107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b3985e20664facef15e0968e68c03e74f1f65a521d1bc9c483dc6b33cfd1f99`  
		Last Modified: Tue, 17 Sep 2024 09:57:10 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baac26d95b31ca8518f3c7bdbe63cdd4169865021fbe03c49e5f8a983c90f962`  
		Last Modified: Wed, 18 Sep 2024 02:09:01 GMT  
		Size: 13.4 MB (13386829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f0724226eed5f20e24828f190b427ea98df49c5ed0539d0e9639b85594daa2c`  
		Last Modified: Wed, 18 Sep 2024 02:09:01 GMT  
		Size: 212.2 KB (212168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc26d15b9f3691e6a28febd11ad81e6aec17a84befa87e777e473c6156634960`  
		Last Modified: Wed, 18 Sep 2024 02:52:14 GMT  
		Size: 192.0 MB (191967705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c02c63de6dc99f5a2d3311b7009619fe174656053cfab67887d8a3ea3b8421a`  
		Last Modified: Wed, 18 Sep 2024 02:55:02 GMT  
		Size: 307.0 MB (307006946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58531c58ba01ffb2a7e745d296cb90bf28dd7224047bb673523ff918e7d35c7f`  
		Last Modified: Wed, 18 Sep 2024 02:54:54 GMT  
		Size: 2.4 MB (2393575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eb06cc8e9f7f3df27087dec1ca2be67936e2e17a34634a2f1e59a51e4c09561`  
		Last Modified: Wed, 18 Sep 2024 02:54:54 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f22779eefb5ffc8984c90a50edc83e5134e5be84fc66bb659271e69da25c391`  
		Last Modified: Wed, 18 Sep 2024 02:54:54 GMT  
		Size: 2.4 KB (2371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6767aaa417ccc8bc91a90ab13005a9c6a002dfc53d10a47ec48a8e82aba742ca`  
		Last Modified: Wed, 18 Sep 2024 02:54:55 GMT  
		Size: 6.5 KB (6462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03ff0ead339c628c30446590242aad965bf5c2091d1c16c4e1873c767f36585c`  
		Last Modified: Wed, 18 Sep 2024 02:54:55 GMT  
		Size: 2.5 KB (2506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:15-mysql-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:fdb9a0f2cd8bc7cba890990c9653c611b8877a0670bf3e139fa85c335940eb88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 MB (8642467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baa67189024a23bf84a4147880688f16c46b1834bd06e0318949923a626b8ffc`

```dockerfile
```

-	Layers:
	-	`sha256:b4afcd4964c571d77556b074387cd35153f03f07458e9e517e933d807e73532b`  
		Last Modified: Wed, 18 Sep 2024 02:54:54 GMT  
		Size: 8.6 MB (8599744 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91324e3dc29ce50d39b96d98c0ce03cf3f718032dbcd2f6d7aaa1a629d76d6ce`  
		Last Modified: Wed, 18 Sep 2024 02:54:53 GMT  
		Size: 42.7 KB (42723 bytes)  
		MIME: application/vnd.in-toto+json
