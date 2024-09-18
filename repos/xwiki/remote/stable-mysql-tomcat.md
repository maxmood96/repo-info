## `xwiki:stable-mysql-tomcat`

```console
$ docker pull xwiki@sha256:3d3a900f42c82cd75827775d73499a45295c5238dc27c753a8a9b37b33f6f84f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:stable-mysql-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:934cc933d910ba8f6c19276b360054070c2e60dcd4f40ca76ae46c2dd4d2f14c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **615.9 MB (615920556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3b2164fdb6d115ec6d91bbcb1ea3a4a4ceede6b6aa78bf066e11aecd3d00568`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 27 Aug 2024 15:55:01 GMT
ARG RELEASE
# Tue, 27 Aug 2024 15:55:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Aug 2024 15:55:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Aug 2024 15:55:01 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 27 Aug 2024 15:55:03 GMT
ADD file:aaeb92d3288093ff43a69d19f9133475372ca003b6de902066a2d4641eec2456 in / 
# Tue, 27 Aug 2024 15:55:03 GMT
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
# Thu, 05 Sep 2024 09:53:24 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 05 Sep 2024 09:53:24 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Sep 2024 09:53:24 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Thu, 05 Sep 2024 09:53:24 GMT
WORKDIR /usr/local/tomcat
# Thu, 05 Sep 2024 09:53:24 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 05 Sep 2024 09:53:24 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 05 Sep 2024 09:53:24 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 05 Sep 2024 09:53:24 GMT
ENV TOMCAT_MAJOR=9
# Thu, 05 Sep 2024 09:53:24 GMT
ENV TOMCAT_VERSION=9.0.95
# Thu, 05 Sep 2024 09:53:24 GMT
ENV TOMCAT_SHA512=b18103153169c7bf98da055f8ba0ac3e141d121c78869881d3be480e90fcbc3a178a8e71fa70a11aee7f2584727df72be15d30331faec65f4e57c7e67c85c1cf
# Thu, 05 Sep 2024 09:53:24 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Thu, 05 Sep 2024 09:53:24 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Sep 2024 09:53:24 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Thu, 05 Sep 2024 09:53:24 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 05 Sep 2024 09:53:24 GMT
ENTRYPOINT []
# Thu, 05 Sep 2024 09:53:24 GMT
CMD ["catalina.sh" "run"]
# Thu, 05 Sep 2024 09:53:24 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Thu, 05 Sep 2024 09:53:24 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Thu, 05 Sep 2024 09:53:24 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Thu, 05 Sep 2024 09:53:24 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Thu, 05 Sep 2024 09:53:24 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Thu, 05 Sep 2024 09:53:24 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Thu, 05 Sep 2024 09:53:24 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Sep 2024 09:53:24 GMT
ENV XWIKI_VERSION=16.7.1
# Thu, 05 Sep 2024 09:53:24 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/16.7.1
# Thu, 05 Sep 2024 09:53:24 GMT
ENV XWIKI_DOWNLOAD_SHA256=c1df8c9c0abd0f06fec4414202c25f1c0a48d810f0efe802deb633edf25090c0
# Thu, 05 Sep 2024 09:53:24 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Thu, 05 Sep 2024 09:53:24 GMT
ENV MYSQL_JDBC_VERSION=9.0.0
# Thu, 05 Sep 2024 09:53:24 GMT
ENV MYSQL_JDBC_SHA256=a221c4106b7fe68a45912cdbf8351f1b43ad3c53a43c3bc966181cc14f86fa30
# Thu, 05 Sep 2024 09:53:24 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/9.0.0
# Thu, 05 Sep 2024 09:53:24 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-9.0.0.jar
# Thu, 05 Sep 2024 09:53:24 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-9.0.0.jar
# Thu, 05 Sep 2024 09:53:24 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c - # buildkit
# Thu, 05 Sep 2024 09:53:24 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Thu, 05 Sep 2024 09:53:24 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Thu, 05 Sep 2024 09:53:24 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Thu, 05 Sep 2024 09:53:24 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 05 Sep 2024 09:53:24 GMT
VOLUME [/usr/local/xwiki]
# Thu, 05 Sep 2024 09:53:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Sep 2024 09:53:24 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:32b824d45c6101d459f5d3c13ab8658b6f79713f3bd64e363d3f6bc98faf5d6d`  
		Last Modified: Tue, 27 Aug 2024 21:43:22 GMT  
		Size: 30.6 MB (30611547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a316f85472e42ddf39be81d37cefcaa87cad98b7ca1710864ef2b8e67e9713b`  
		Last Modified: Tue, 17 Sep 2024 01:07:39 GMT  
		Size: 16.2 MB (16177262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bc61f93074679710412ad3cef2fc06379271ccc3fe6224c6048a7940bcd3e31`  
		Last Modified: Tue, 17 Sep 2024 01:10:41 GMT  
		Size: 47.3 MB (47280241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd40a8ba9b9816e6e92a048771912e0203fb0c2366490934aebed10ad169c831`  
		Last Modified: Tue, 17 Sep 2024 01:10:34 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44b1b7b9b07ec925dc69ff02361ed98cf596d711625c013abe78af64e96f6d36`  
		Last Modified: Tue, 17 Sep 2024 01:10:35 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4728163afb9187d5750e424b7036f35e635b66717860195905890b50c67fd7f`  
		Last Modified: Wed, 18 Sep 2024 00:01:26 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b576bb465706f666c66c57588b72e514e874967edb392a5d1c381a309e79e5a`  
		Last Modified: Wed, 18 Sep 2024 00:01:27 GMT  
		Size: 13.4 MB (13378031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78ddd183b95c46d915fe5d8cfa463c94d78600b6e2e7bc570693a947caf044ab`  
		Last Modified: Wed, 18 Sep 2024 00:01:26 GMT  
		Size: 212.3 KB (212297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a21772af10b0d52fe04cc71c48a91005586a35a3c836da1ef4bf4c385f251f17`  
		Last Modified: Wed, 18 Sep 2024 00:53:09 GMT  
		Size: 194.3 MB (194322227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c63e566ccc7b0d93bde1aa175588c2f78481c4029080e89999f6b4e97834c5b`  
		Last Modified: Wed, 18 Sep 2024 00:53:17 GMT  
		Size: 311.5 MB (311496145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25919987386962ff3922b86a618e445b7b9f881cb2897b195fc4cb5cf1c33635`  
		Last Modified: Wed, 18 Sep 2024 00:53:05 GMT  
		Size: 2.4 MB (2427546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47532f81a74dec59e8faf3dacea3dd5d1805fc9b16bf0721827779c39f881d6d`  
		Last Modified: Wed, 18 Sep 2024 00:53:04 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bae99f37448aa70285749629ae8cf6588b81770be9037cbfd35761632db7e67`  
		Last Modified: Wed, 18 Sep 2024 00:53:05 GMT  
		Size: 2.4 KB (2376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:850b97e7f04b4a269cb6ba218a29d1775ecbada2b22e18fd534d74fc3f9317ad`  
		Last Modified: Wed, 18 Sep 2024 00:53:06 GMT  
		Size: 6.6 KB (6563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:869c45b528ccf8f29dadbc690a6db0d8bfcf8c37bd1dec37045de02ad81138ac`  
		Last Modified: Wed, 18 Sep 2024 00:53:07 GMT  
		Size: 2.5 KB (2509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:stable-mysql-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:abed99d5d2f9ce236c0fcf7eabe236465af79ce4d4932b433cb47d1240de2bee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 MB (8645864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78cce8bcfebc4c066d613fe30f1ffc0a2f43891dc2e97fd8922790e6329c7331`

```dockerfile
```

-	Layers:
	-	`sha256:8637c85a3ab15d5f730886e27e03c4e531239c7352d9005d264a1c714f7622d0`  
		Last Modified: Wed, 18 Sep 2024 00:53:06 GMT  
		Size: 8.6 MB (8603231 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb219a580edf1cbc755ccac1932bc862a4fe01c7267220a43b53764b1f055684`  
		Last Modified: Wed, 18 Sep 2024 00:53:04 GMT  
		Size: 42.6 KB (42633 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:stable-mysql-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:ecb29d9297c995f0f9b50bad1a2fe4f2558da0678a7397b0e5fe8db8aa28c404
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **612.2 MB (612216246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71cac71f83410f99cca60619b03d0fbde199aa6cf6fe97a0f27446e16f28ca18`
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
# Thu, 05 Sep 2024 09:53:24 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 05 Sep 2024 09:53:24 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Sep 2024 09:53:24 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Thu, 05 Sep 2024 09:53:24 GMT
WORKDIR /usr/local/tomcat
# Thu, 05 Sep 2024 09:53:24 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 05 Sep 2024 09:53:24 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 05 Sep 2024 09:53:24 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 05 Sep 2024 09:53:24 GMT
ENV TOMCAT_MAJOR=9
# Thu, 05 Sep 2024 09:53:24 GMT
ENV TOMCAT_VERSION=9.0.95
# Thu, 05 Sep 2024 09:53:24 GMT
ENV TOMCAT_SHA512=b18103153169c7bf98da055f8ba0ac3e141d121c78869881d3be480e90fcbc3a178a8e71fa70a11aee7f2584727df72be15d30331faec65f4e57c7e67c85c1cf
# Thu, 05 Sep 2024 09:53:24 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Thu, 05 Sep 2024 09:53:24 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Sep 2024 09:53:24 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Thu, 05 Sep 2024 09:53:24 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 05 Sep 2024 09:53:24 GMT
ENTRYPOINT []
# Thu, 05 Sep 2024 09:53:24 GMT
CMD ["catalina.sh" "run"]
# Thu, 05 Sep 2024 09:53:24 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Thu, 05 Sep 2024 09:53:24 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Thu, 05 Sep 2024 09:53:24 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Thu, 05 Sep 2024 09:53:24 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Thu, 05 Sep 2024 09:53:24 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Thu, 05 Sep 2024 09:53:24 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Thu, 05 Sep 2024 09:53:24 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Sep 2024 09:53:24 GMT
ENV XWIKI_VERSION=16.7.1
# Thu, 05 Sep 2024 09:53:24 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/16.7.1
# Thu, 05 Sep 2024 09:53:24 GMT
ENV XWIKI_DOWNLOAD_SHA256=c1df8c9c0abd0f06fec4414202c25f1c0a48d810f0efe802deb633edf25090c0
# Thu, 05 Sep 2024 09:53:24 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Thu, 05 Sep 2024 09:53:24 GMT
ENV MYSQL_JDBC_VERSION=9.0.0
# Thu, 05 Sep 2024 09:53:24 GMT
ENV MYSQL_JDBC_SHA256=a221c4106b7fe68a45912cdbf8351f1b43ad3c53a43c3bc966181cc14f86fa30
# Thu, 05 Sep 2024 09:53:24 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/9.0.0
# Thu, 05 Sep 2024 09:53:24 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-9.0.0.jar
# Thu, 05 Sep 2024 09:53:24 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-9.0.0.jar
# Thu, 05 Sep 2024 09:53:24 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c - # buildkit
# Thu, 05 Sep 2024 09:53:24 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Thu, 05 Sep 2024 09:53:24 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Thu, 05 Sep 2024 09:53:24 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Thu, 05 Sep 2024 09:53:24 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 05 Sep 2024 09:53:24 GMT
VOLUME [/usr/local/xwiki]
# Thu, 05 Sep 2024 09:53:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Sep 2024 09:53:24 GMT
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
	-	`sha256:35f1c76a726f862e791ab30cffbe94c6164622647b1c44f425eedfa6bc1678a0`  
		Last Modified: Wed, 18 Sep 2024 02:52:16 GMT  
		Size: 311.5 MB (311496207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c01993e4bdc91aea2fbcb6586eb703d35263aa55e0c6993760172f209e5fa642`  
		Last Modified: Wed, 18 Sep 2024 02:52:10 GMT  
		Size: 2.4 MB (2427539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15cf1b0820520334923fc348ce68a0a05701b96425416538e04ebc4f44a1cf66`  
		Last Modified: Wed, 18 Sep 2024 02:52:10 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ac2db23679e22ac163394bb8a00e3bf64b7c378e88e0294711e855d8615edb3`  
		Last Modified: Wed, 18 Sep 2024 02:52:11 GMT  
		Size: 2.4 KB (2372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdee98c24e5b8b7d86824e5c17c9992d817c5ad1751967ef85a5d00c8bc9d8ed`  
		Last Modified: Wed, 18 Sep 2024 02:52:11 GMT  
		Size: 6.6 KB (6558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bc1b5110028637cb3a50ee0b3107ec38112b9bac742219934ad2ebf782038f9`  
		Last Modified: Wed, 18 Sep 2024 02:52:12 GMT  
		Size: 2.5 KB (2513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:stable-mysql-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:eb84b92a0aebdd4125586634fb872c89c268de43a2970a731bfadf2708bc5ca3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 MB (8648004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97878c8f1f803a4626e5bc99d02596a9b0f3a7abf05f104bc11a43a5fcce6795`

```dockerfile
```

-	Layers:
	-	`sha256:49a09d2db822764fda0399db46d072c07c5e2d85647f2c5ddbe25d475fad3a65`  
		Last Modified: Wed, 18 Sep 2024 02:52:10 GMT  
		Size: 8.6 MB (8604662 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d9eb14433ea8ce0c018a20e56f6c66d7d6d4628fc1469d3eef49c2bc2b8b99e`  
		Last Modified: Wed, 18 Sep 2024 02:52:09 GMT  
		Size: 43.3 KB (43342 bytes)  
		MIME: application/vnd.in-toto+json
