## `xwiki:16-mysql-tomcat`

```console
$ docker pull xwiki@sha256:addd52169b361abc07ea409ef01cd126a0d0c03a7bfe778530421ab535e60a15
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:16-mysql-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:5681e9c45bb4724630f53520a4bbbedf41cfa17efba8fb1dfe7fc055cb8e8f4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **628.9 MB (628889878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2cbb23281727d595f82667c4df8dfe602a48e0d23aa7d725e10f6d3dbe94800`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 01 Aug 2024 14:23:53 GMT
ARG RELEASE
# Thu, 01 Aug 2024 14:23:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 01 Aug 2024 14:23:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 01 Aug 2024 14:23:53 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 01 Aug 2024 14:23:55 GMT
ADD file:c2e78eb585ec4e503f14c4ea98f4962c998f5eb075749507953f85387742694b in / 
# Thu, 01 Aug 2024 14:23:55 GMT
CMD ["/bin/bash"]
# Tue, 06 Aug 2024 08:03:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 06 Aug 2024 08:03:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Aug 2024 08:03:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 06 Aug 2024 08:03:42 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 Aug 2024 08:03:42 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Tue, 06 Aug 2024 08:03:42 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        riscv64)          ESUM='2d1ed42918305a1a0754a6e1e9294c7d4d7fda4bff6dba7bc5682037d860dbc9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 06 Aug 2024 08:03:42 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 06 Aug 2024 08:03:42 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 06 Aug 2024 08:03:42 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 06 Aug 2024 08:03:42 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 06 Aug 2024 08:03:42 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Aug 2024 08:03:42 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 06 Aug 2024 08:03:42 GMT
WORKDIR /usr/local/tomcat
# Tue, 06 Aug 2024 08:03:42 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 06 Aug 2024 08:03:42 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 06 Aug 2024 08:03:42 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 06 Aug 2024 08:03:42 GMT
ENV TOMCAT_MAJOR=9
# Tue, 06 Aug 2024 08:03:42 GMT
ENV TOMCAT_VERSION=9.0.93
# Tue, 06 Aug 2024 08:03:42 GMT
ENV TOMCAT_SHA512=3069924eb7041ccc0f2aeceb7d8626793a1a073a5b739a840d7974a18ebeb26cc3374cc5f4a3ffc74d3b019c0cb33e3d1fe96296e6663ac75a73c1171811726d
# Tue, 06 Aug 2024 08:03:42 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 06 Aug 2024 08:03:42 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 Aug 2024 08:03:42 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 06 Aug 2024 08:03:42 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 06 Aug 2024 08:03:42 GMT
ENTRYPOINT []
# Tue, 06 Aug 2024 08:03:42 GMT
CMD ["catalina.sh" "run"]
# Mon, 26 Aug 2024 14:19:12 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Mon, 26 Aug 2024 14:19:12 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Mon, 26 Aug 2024 14:19:12 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Mon, 26 Aug 2024 14:19:12 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Mon, 26 Aug 2024 14:19:12 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Mon, 26 Aug 2024 14:19:12 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Mon, 26 Aug 2024 14:19:12 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 26 Aug 2024 14:19:12 GMT
ENV XWIKI_VERSION=16.7.0
# Mon, 26 Aug 2024 14:19:12 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/16.7.0
# Mon, 26 Aug 2024 14:19:12 GMT
ENV XWIKI_DOWNLOAD_SHA256=79f3a71d1dab6457179b7c3e780e85cc412797e3f6db845080721902377a1493
# Mon, 26 Aug 2024 14:19:12 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Mon, 26 Aug 2024 14:19:12 GMT
ENV MYSQL_JDBC_VERSION=9.0.0
# Mon, 26 Aug 2024 14:19:12 GMT
ENV MYSQL_JDBC_SHA256=a221c4106b7fe68a45912cdbf8351f1b43ad3c53a43c3bc966181cc14f86fa30
# Mon, 26 Aug 2024 14:19:12 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/9.0.0
# Mon, 26 Aug 2024 14:19:12 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-9.0.0.jar
# Mon, 26 Aug 2024 14:19:12 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-9.0.0.jar
# Mon, 26 Aug 2024 14:19:12 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c - # buildkit
# Mon, 26 Aug 2024 14:19:12 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Mon, 26 Aug 2024 14:19:12 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Mon, 26 Aug 2024 14:19:12 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Mon, 26 Aug 2024 14:19:12 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Mon, 26 Aug 2024 14:19:12 GMT
VOLUME [/usr/local/xwiki]
# Mon, 26 Aug 2024 14:19:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Aug 2024 14:19:12 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:eb993dcd6942ffcb7633f2cb271bd4b0a275fc9bdc8f5100c5b4d24694cacf50`  
		Last Modified: Fri, 02 Aug 2024 03:03:23 GMT  
		Size: 30.6 MB (30567306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62ad162d7203142bab0c47850dd2fcd205f950b3f9261ed4b68917cf906ca25a`  
		Last Modified: Sat, 17 Aug 2024 01:10:20 GMT  
		Size: 13.8 MB (13767059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403a7de2f3419f182b36dfb976cca6c350851e5d0dc4d185bebd30f65c1a972d`  
		Last Modified: Fri, 23 Aug 2024 19:28:02 GMT  
		Size: 47.3 MB (47280248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff46ed4d14452b7ff34cefa07b3268f4ccac9a56ade29c1c14f7929e8dedad44`  
		Last Modified: Fri, 23 Aug 2024 19:27:55 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dcea8ed07ba94678acd43d918bb23c6085b53205962f8c85d5c1cfab6463acd`  
		Last Modified: Fri, 23 Aug 2024 19:27:55 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a69ef327f4210661f76311e2d1bea08c5f222496011eaf65c3d6254a5fed9009`  
		Last Modified: Fri, 23 Aug 2024 21:10:35 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5ce55f2f57de3c372a918939f6b93d7cfcc42e815f590acd7ad154617535c75`  
		Last Modified: Fri, 23 Aug 2024 21:10:36 GMT  
		Size: 12.8 MB (12764989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20a0811f2f6e8079deaf7f7555a780634dd4fc765e2f6b49997d9d7922d38a20`  
		Last Modified: Fri, 23 Aug 2024 21:10:36 GMT  
		Size: 15.7 MB (15699780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4145c1a36b1a846ac861a3288de00ddb5425468e88911bb7aed8ed5fa0806be1`  
		Last Modified: Mon, 26 Aug 2024 21:59:51 GMT  
		Size: 194.9 MB (194880664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74fb444f5b21668a78e968cd94316556dd6dc9b3cc04547a9727a3efd36ca9be`  
		Last Modified: Mon, 26 Aug 2024 21:59:53 GMT  
		Size: 311.5 MB (311487042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f11c2fb43d4949e15f5ac02557b5a21d8d8c6849270de7f7428fc3fb3f6a952a`  
		Last Modified: Mon, 26 Aug 2024 21:59:49 GMT  
		Size: 2.4 MB (2427536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83e09279fb5e11c2dcfc9564adcf907bd2670494c44c92bb1b9dd94826f3c382`  
		Last Modified: Mon, 26 Aug 2024 21:59:49 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9164590197118b0bbc980c6f7ba2afea83ac73f6cc03be4dd4fe37fef37e09e`  
		Last Modified: Mon, 26 Aug 2024 21:59:49 GMT  
		Size: 2.4 KB (2369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a9691cb5bb47092fa800e558d8231f9826234a7d68eadd0406d51ae7196d89f`  
		Last Modified: Mon, 26 Aug 2024 21:59:49 GMT  
		Size: 6.6 KB (6564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f42086c93d339c2d6547dab4cd4c3f77600632a075e494bb7ce34b3dc2d0c48`  
		Last Modified: Mon, 26 Aug 2024 21:59:50 GMT  
		Size: 2.5 KB (2510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:16-mysql-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:18be9b7a2c1883e9dca7ad03b97435f02e5b77b4d6b20c8ddb637a35a590fe88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 MB (8646921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68a0f4eb3a414496fa09cf72b47d9b35266e7a800048f7d04c201c0b5c4807d9`

```dockerfile
```

-	Layers:
	-	`sha256:18104b0e326a523fd634906281393dd477113564a32b6f4985037e49f69e6f15`  
		Last Modified: Mon, 26 Aug 2024 21:59:49 GMT  
		Size: 8.6 MB (8604273 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a479979df8d94bd6265885e2ce389faaebe96c453efc27baf74a7483889a044`  
		Last Modified: Mon, 26 Aug 2024 21:59:49 GMT  
		Size: 42.6 KB (42648 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:16-mysql-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:76f9714b22abc21f833c25951bed56d02c11bfa4e1532d77e8c7caecc776d009
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **624.8 MB (624785087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5def60de081c9ace8700dc1fa651a9b443db851a09b38632831cfff26d06a100`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Mon, 29 Jul 2024 15:54:10 GMT
ARG RELEASE
# Mon, 29 Jul 2024 15:54:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 29 Jul 2024 15:54:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 29 Jul 2024 15:54:10 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 29 Jul 2024 15:54:10 GMT
ADD file:154285ca3d49a142bc6d59c9d48f14546f32b2d6de94387c30c1ba3759249b0f in / 
# Mon, 29 Jul 2024 15:54:10 GMT
CMD ["/bin/bash"]
# Mon, 29 Jul 2024 15:54:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 29 Jul 2024 15:54:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Jul 2024 15:54:10 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 29 Jul 2024 15:54:10 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Jul 2024 15:54:10 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Mon, 29 Jul 2024 15:54:10 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        riscv64)          ESUM='2d1ed42918305a1a0754a6e1e9294c7d4d7fda4bff6dba7bc5682037d860dbc9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 29 Jul 2024 15:54:10 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 29 Jul 2024 15:54:10 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 29 Jul 2024 15:54:10 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 29 Jul 2024 15:54:10 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 29 Jul 2024 15:54:10 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Jul 2024 15:54:10 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 29 Jul 2024 15:54:10 GMT
WORKDIR /usr/local/tomcat
# Mon, 29 Jul 2024 15:54:10 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 29 Jul 2024 15:54:10 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 29 Jul 2024 15:54:10 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Mon, 29 Jul 2024 15:54:10 GMT
ENV TOMCAT_MAJOR=9
# Mon, 29 Jul 2024 15:54:10 GMT
ENV TOMCAT_VERSION=9.0.93
# Mon, 29 Jul 2024 15:54:10 GMT
ENV TOMCAT_SHA512=3069924eb7041ccc0f2aeceb7d8626793a1a073a5b739a840d7974a18ebeb26cc3374cc5f4a3ffc74d3b019c0cb33e3d1fe96296e6663ac75a73c1171811726d
# Mon, 29 Jul 2024 15:54:10 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 29 Jul 2024 15:54:10 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Jul 2024 15:54:10 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 29 Jul 2024 15:54:10 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 29 Jul 2024 15:54:10 GMT
ENTRYPOINT []
# Mon, 29 Jul 2024 15:54:10 GMT
CMD ["catalina.sh" "run"]
# Mon, 29 Jul 2024 15:54:10 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Mon, 29 Jul 2024 15:54:10 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Mon, 29 Jul 2024 15:54:10 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Mon, 29 Jul 2024 15:54:10 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Mon, 29 Jul 2024 15:54:10 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Mon, 29 Jul 2024 15:54:10 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Mon, 29 Jul 2024 15:54:10 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Jul 2024 15:54:10 GMT
ENV XWIKI_VERSION=16.6.0
# Mon, 29 Jul 2024 15:54:10 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/16.6.0
# Mon, 29 Jul 2024 15:54:10 GMT
ENV XWIKI_DOWNLOAD_SHA256=504e3fc3707d222d4a2be7c4e51e01242d4a7092380234d5076616d170390fe7
# Mon, 29 Jul 2024 15:54:10 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Mon, 29 Jul 2024 15:54:10 GMT
ENV MYSQL_JDBC_VERSION=9.0.0
# Mon, 29 Jul 2024 15:54:10 GMT
ENV MYSQL_JDBC_SHA256=a221c4106b7fe68a45912cdbf8351f1b43ad3c53a43c3bc966181cc14f86fa30
# Mon, 29 Jul 2024 15:54:10 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/9.0.0
# Mon, 29 Jul 2024 15:54:10 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-9.0.0.jar
# Mon, 29 Jul 2024 15:54:10 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-9.0.0.jar
# Mon, 29 Jul 2024 15:54:10 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c - # buildkit
# Mon, 29 Jul 2024 15:54:10 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Mon, 29 Jul 2024 15:54:10 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Mon, 29 Jul 2024 15:54:10 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Mon, 29 Jul 2024 15:54:10 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Mon, 29 Jul 2024 15:54:10 GMT
VOLUME [/usr/local/xwiki]
# Mon, 29 Jul 2024 15:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jul 2024 15:54:10 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:1567e7ea90b67fc95ccdeeec39bdc3045098dee7e0c604975b957a9f8c0e9616`  
		Last Modified: Fri, 02 Aug 2024 07:40:09 GMT  
		Size: 29.9 MB (29910029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:923b74992e2f6b4e4be4f1c2bf6930b93c7593d6c834159867d3bd8ea14005ff`  
		Last Modified: Sat, 17 Aug 2024 01:33:27 GMT  
		Size: 13.8 MB (13795899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:169b61747edd8caded770386f82148a86bed83337fc5d5d3c98d9068fd166940`  
		Last Modified: Fri, 23 Aug 2024 19:45:30 GMT  
		Size: 46.7 MB (46746370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a57a7471d94a9e3dbc7a2319293c1c0b9855c26bf4faf9308850b20ef0f92ba1`  
		Last Modified: Fri, 23 Aug 2024 19:45:25 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1428cdfeb2dcadba80a0f2b8c442b1e07d23961a8a4813d0d54d2201653d5cc1`  
		Last Modified: Fri, 23 Aug 2024 19:45:25 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f0d2fddeb86a8f16b9a6be3ad63f486f16cc6d834c895db3e2f892aef48a21c`  
		Last Modified: Sat, 24 Aug 2024 02:56:18 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51a0ed2a59c90ffe2e8225ea8358568b0ccabc7ba10dce90ef4cfdc3c787aeca`  
		Last Modified: Sat, 24 Aug 2024 02:58:47 GMT  
		Size: 12.8 MB (12774973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9fe30fde83ee65499a1f87112a488bb92254332c127cb4b15cc968a7988d083`  
		Last Modified: Sat, 24 Aug 2024 02:58:47 GMT  
		Size: 15.3 MB (15259599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:444ea4e55033140f8c92e4907ead90d09931d83c6bb087f44988b82d45c22b8f`  
		Last Modified: Sat, 24 Aug 2024 03:53:06 GMT  
		Size: 192.5 MB (192513048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4af95d476eaa327afb2008f4700f7d503b003c5e219a564e9feb0953f6910091`  
		Last Modified: Sat, 24 Aug 2024 03:53:08 GMT  
		Size: 311.3 MB (311342381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2229da95e3780c4c414355d9bfabf78bf6332c8c33b5f2ef70d5da8898ecf40a`  
		Last Modified: Sat, 24 Aug 2024 03:53:01 GMT  
		Size: 2.4 MB (2427546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:071268f0496e605e6ac6159487b35b265d3ab1722ee994c1e10f6f66ce6735df`  
		Last Modified: Sat, 24 Aug 2024 03:53:00 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65355163ec48e07b47f106a18407efc6ab5ca0d3469a5787b80bf03e779bcc1e`  
		Last Modified: Sat, 24 Aug 2024 03:53:01 GMT  
		Size: 2.4 KB (2374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:846d6ae7e0442df805bdff0c2a4cb1564578502339f89a4e49b882deab7cf039`  
		Last Modified: Sat, 24 Aug 2024 03:53:03 GMT  
		Size: 6.5 KB (6544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3731e487d22aa649c76c8b18cb3b2e3b1ee8bf3f8785511a2cb2d161c888c390`  
		Last Modified: Sat, 24 Aug 2024 03:53:02 GMT  
		Size: 2.5 KB (2512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:16-mysql-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:9b2cc358606f6f12e993c135bfb742cc266308df2f0d3c9f58eb4faf991c3612
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 MB (8647699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5755db093b372d92e62ba89418b1f8f10a19f524fa5bd44fb705ed09c20a77cf`

```dockerfile
```

-	Layers:
	-	`sha256:4fadac3c5dd07e38bb8f801245f052e36664e75a1aef870348dbe0017c37353c`  
		Last Modified: Sat, 24 Aug 2024 03:53:01 GMT  
		Size: 8.6 MB (8604341 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:596b3cdfa206d1bfd3710a84cc02c0171da275c83dde8f4617bf9abde12eaa2d`  
		Last Modified: Sat, 24 Aug 2024 03:53:00 GMT  
		Size: 43.4 KB (43358 bytes)  
		MIME: application/vnd.in-toto+json
