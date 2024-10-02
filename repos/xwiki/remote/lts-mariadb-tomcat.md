## `xwiki:lts-mariadb-tomcat`

```console
$ docker pull xwiki@sha256:a13ea155d16a7e71ccc352662edb5474d593b9a35dbe7a72836fea94e13a0fc1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:lts-mariadb-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:3c01000823a3f16ea21253596a67e339a4f721cda48f0ae6438144a93d91ebb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **607.6 MB (607558037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29217881960c065ee26278c55c95ed387fadaa2edee20a32263815cfb5205a85`
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
ENV MARIADB_JDBC_VERSION=3.4.1
# Tue, 03 Sep 2024 05:14:18 GMT
ENV MARIADB_JDBC_SHA256=f60e4b282f1f4bdb74f0a26436ba7078a5e480b6f6702f6a7b45d9ba5e604a24
# Tue, 03 Sep 2024 05:14:18 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.4.1
# Tue, 03 Sep 2024 05:14:18 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.4.1.jar
# Tue, 03 Sep 2024 05:14:18 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.4.1.jar
# Tue, 03 Sep 2024 05:14:18 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c - # buildkit
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
	-	`sha256:751022696de77b018a0b42d3d3b433a30fde4e9022e54d1a49c5d275d8b0904d`  
		Last Modified: Wed, 02 Oct 2024 04:56:28 GMT  
		Size: 194.6 MB (194634696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6013930b595e2556a0b4138ea384c37f871e3006cd2a282ec01445a49aa9556`  
		Last Modified: Wed, 02 Oct 2024 04:56:29 GMT  
		Size: 307.0 MB (307006977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1585cdf91db66d0f126678840a5ada8596dd13ee65a9bf57c2e568e6972702cd`  
		Last Modified: Wed, 02 Oct 2024 04:56:22 GMT  
		Size: 648.5 KB (648529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a26a07c68a3fbfbc676f00238ff6132cc8e5efd6f7a0076af0215aa5daf2a93`  
		Last Modified: Wed, 02 Oct 2024 04:56:21 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79bbec8002c9c1d93a1d5e19728f780682a7257a53c64226b09fccfd91cbad37`  
		Last Modified: Wed, 02 Oct 2024 04:56:22 GMT  
		Size: 2.3 KB (2312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23f21496bd19e2344242c170676f643ae65e0a5ccfc5562df4167d34e2bba86e`  
		Last Modified: Wed, 02 Oct 2024 04:56:23 GMT  
		Size: 6.5 KB (6465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:294efa6069799d5f0d522753f9b02c54917fdea876dd44490b2455294ed8df43`  
		Last Modified: Wed, 02 Oct 2024 04:56:23 GMT  
		Size: 2.5 KB (2477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:lts-mariadb-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:8361e37d57ee3a33dd67cb65c7cb239abc29b6201710ebd31fb6d944a6f64c28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8704606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:893bbf7f77f768149c9bc09f081e864163c498a1c39c17ff68acb85dd35a4d77`

```dockerfile
```

-	Layers:
	-	`sha256:580f22a7830867c757cdecceb6780d8f8fa9099acfe7e6524d2e6b1a837d3d7e`  
		Last Modified: Wed, 02 Oct 2024 04:56:21 GMT  
		Size: 8.7 MB (8663609 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2525efb30c0dfde3da975812f556f548dce530c3baac348d03771650b03f088c`  
		Last Modified: Wed, 02 Oct 2024 04:56:21 GMT  
		Size: 41.0 KB (40997 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:lts-mariadb-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:b6baffedc6db58f00d874c434ea69c9b433bca8d2dadd5f49e6184c08bd1c04c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **604.1 MB (604059327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc1049fae4fb818b6ec7f1cea646a44db08c93d06c4fc37b92db0cb1f4d21b89`
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
ADD file:9d8a15341d364d2508ffca0657b4cb175a35d2edbdb0cf2476f7c4fff4f6c66a in / 
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
ENV MARIADB_JDBC_VERSION=3.4.1
# Tue, 03 Sep 2024 05:14:18 GMT
ENV MARIADB_JDBC_SHA256=f60e4b282f1f4bdb74f0a26436ba7078a5e480b6f6702f6a7b45d9ba5e604a24
# Tue, 03 Sep 2024 05:14:18 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.4.1
# Tue, 03 Sep 2024 05:14:18 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.4.1.jar
# Tue, 03 Sep 2024 05:14:18 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.4.1.jar
# Tue, 03 Sep 2024 05:14:18 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c - # buildkit
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
	-	`sha256:43cc87cb0cd1fc1c0b6c8670fa2a07f84e6af2cd95bce48b7909b42cca8e5fc1`  
		Last Modified: Fri, 20 Sep 2024 15:05:59 GMT  
		Size: 30.0 MB (29952705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0705b8718ddb3ba1d94fa724eee408800a407ccd169899af243b9cfc2ab5481c`  
		Last Modified: Wed, 02 Oct 2024 01:25:17 GMT  
		Size: 13.8 MB (13798035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51ef2dea2cc9c0dbe3c64710e5ffdcfb21a0f8380212beac56d44e94e1a2802c`  
		Last Modified: Wed, 02 Oct 2024 01:28:02 GMT  
		Size: 46.7 MB (46746360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f97ec3778b444f1bb64b53a5f58cb73e31648e1389c755d55b65d2c634c1cd2f`  
		Last Modified: Wed, 02 Oct 2024 01:27:57 GMT  
		Size: 161.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16f4ca8e8b83ad911aeec2a1f3687e6b549782de3f86048819e24bbc9604a9fd`  
		Last Modified: Wed, 02 Oct 2024 01:27:57 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a048a6e5e950d28537247e59cee0c1b682511903da99d5f3a1e2674d985a8651`  
		Last Modified: Wed, 02 Oct 2024 07:53:51 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:417bd3fde4fd7e293e4ad6c87c9d17ef6f935a760203f271899c1090a720eb82`  
		Last Modified: Wed, 02 Oct 2024 07:54:58 GMT  
		Size: 13.4 MB (13386862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:518aac9b4de5a12b5e327345fcbaf13ff9007ba8e4d6234153d8e7764882aabe`  
		Last Modified: Wed, 02 Oct 2024 07:54:58 GMT  
		Size: 212.2 KB (212214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d278f2e664ee88916c8a81cf8a0e2ab8419cb39b4538b67487e2f11363244d7d`  
		Last Modified: Wed, 02 Oct 2024 08:52:38 GMT  
		Size: 192.3 MB (192292652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38d2db5fd0a952b47345de6026654e15e4cda883ee43bf565ccde9db8c62a69d`  
		Last Modified: Wed, 02 Oct 2024 08:55:54 GMT  
		Size: 307.0 MB (307006924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ba31e730ff2d6b1e8867848e7d064b6aff180fcbb490367d15aae0af62a26f9`  
		Last Modified: Wed, 02 Oct 2024 08:57:24 GMT  
		Size: 648.5 KB (648530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ac43b9010468d6dc9772ef39f85ca4949541d9f55bf8b44f4cc1f4e07e0534a`  
		Last Modified: Wed, 02 Oct 2024 08:57:23 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38f6b356813fa3ddca4bee97425fd54a809c78a71f8ead9fca3f2516dac1a28c`  
		Last Modified: Wed, 02 Oct 2024 08:57:23 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2541a2a5f0c6e0e22030a356158460af22fcdb25e05bd4210b21af1ef61bc16c`  
		Last Modified: Wed, 02 Oct 2024 08:57:23 GMT  
		Size: 6.5 KB (6460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5a37342a27ae7903f1e39ea23617e1b6c0d75bbc372491d423d8ef86caa1d65`  
		Last Modified: Wed, 02 Oct 2024 08:57:24 GMT  
		Size: 2.5 KB (2469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:lts-mariadb-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:2478769fd616a712d8066db26d7a8ab84a3439a9a0d8f72386f11bc09434be85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8705746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0ebcbd0b2301de0b3b8ecaaeba969bb7ed34c7f18d67acb57369047607b27b4`

```dockerfile
```

-	Layers:
	-	`sha256:99e7cccffed0f4e80b10695a964021d7d4b2adb4a214a3d2e6a4ec109b83f91f`  
		Last Modified: Wed, 02 Oct 2024 08:57:23 GMT  
		Size: 8.7 MB (8664349 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e6258cb8e8ee636971fbd98ab477642704857e96796ec054559bc32d9db3d42`  
		Last Modified: Wed, 02 Oct 2024 08:57:23 GMT  
		Size: 41.4 KB (41397 bytes)  
		MIME: application/vnd.in-toto+json
