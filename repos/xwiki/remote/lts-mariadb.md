## `xwiki:lts-mariadb`

```console
$ docker pull xwiki@sha256:81ef65cdfdb2c3290a2da37f64b6d01567108cf3072c16aca13bfc0b365db923
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:lts-mariadb` - linux; amd64

```console
$ docker pull xwiki@sha256:c7ba2d357a59535a73d2d4f5f2b5ae39fac85a47d7a70644b38ec20a0e97508a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **596.0 MB (595973469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50da018dc55bdf6980c171bf745c69527106b1fad1bcba14ef880bceb0f7ae91`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Fri, 01 Dec 2023 07:49:48 GMT
ARG RELEASE
# Fri, 01 Dec 2023 07:49:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Dec 2023 07:49:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Dec 2023 07:49:48 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 01 Dec 2023 07:49:50 GMT
ADD file:36d444e2cede3abe58191dcf28890b874c0908f5259bf7e8855338555701c4c5 in / 
# Fri, 01 Dec 2023 07:49:50 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 01:58:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 02 Dec 2023 01:58:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 02 Dec 2023 01:58:08 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 02 Dec 2023 02:01:05 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 02:01:05 GMT
ENV JAVA_VERSION=jdk-17.0.9+9
# Sat, 02 Dec 2023 02:01:43 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='05b192f81ed478178ba953a2a779b67fc5a810acadb633ad69f8c4412399edb8';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.9_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='c37f729200b572884b8f8e157852c739be728d61d9a1da0f920104876d324733';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_x64_linux_hotspot_17.0.9_9.tar.gz';          ;;        armhf|arm)          ESUM='5ae1f8cae358e41083a6b44f53c6f0daeb657f83c293da6c8733f68278e13703';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_arm_linux_hotspot_17.0.9_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='79c85ecf1320c67b828310167e1ced62e402bc86a5d47ca9cc7bfa3b708cb07a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.9_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c4f2249bee785aa8c754741aa24d035e02b4e6d844e35b2b20030374d8fbab75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_s390x_linux_hotspot_17.0.9_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Sat, 02 Dec 2023 02:01:44 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Sat, 02 Dec 2023 02:01:44 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Sat, 02 Dec 2023 02:01:44 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 02 Dec 2023 08:19:42 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Sat, 02 Dec 2023 08:19:42 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 02 Dec 2023 08:19:42 GMT
RUN mkdir -p "$CATALINA_HOME"
# Sat, 02 Dec 2023 08:19:43 GMT
WORKDIR /usr/local/tomcat
# Sat, 02 Dec 2023 08:19:43 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Sat, 02 Dec 2023 08:19:43 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Sat, 02 Dec 2023 08:22:07 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Sat, 02 Dec 2023 08:22:07 GMT
ENV TOMCAT_MAJOR=9
# Sat, 02 Dec 2023 08:22:07 GMT
ENV TOMCAT_VERSION=9.0.83
# Sat, 02 Dec 2023 08:22:07 GMT
ENV TOMCAT_SHA512=3f022ec8552bce1b72eb85d0778c93052ccb00226de3302544ec844ab93a9991e19c2db56ed06c18f03e5d75f34a46cedac46ae83bdd225518a55c62fc69ea04
# Sat, 02 Dec 2023 08:22:07 GMT
COPY dir:54663baa1dcf8d5fe6f26193de9a4eda99745defba6fa996068e77095b84f55f in /usr/local/tomcat 
# Sat, 02 Dec 2023 08:22:11 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 08:22:13 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Sat, 02 Dec 2023 08:22:13 GMT
EXPOSE 8080
# Sat, 02 Dec 2023 08:22:13 GMT
ENTRYPOINT []
# Sat, 02 Dec 2023 08:22:13 GMT
CMD ["catalina.sh" "run"]
# Sat, 02 Dec 2023 13:21:16 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Sat, 02 Dec 2023 13:21:16 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Sat, 02 Dec 2023 13:21:17 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Sat, 02 Dec 2023 13:21:17 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Sat, 02 Dec 2023 13:21:17 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Sat, 02 Dec 2023 13:21:17 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Sat, 02 Dec 2023 13:24:18 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 13:26:39 GMT
ENV XWIKI_VERSION=14.10.19
# Sat, 02 Dec 2023 13:26:39 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.10.19
# Sat, 02 Dec 2023 13:26:39 GMT
ENV XWIKI_DOWNLOAD_SHA256=14b88314f9af3c122e3329d13ad2a8a473a774fa1bc8b5b96d08bbf36e56c453
# Sat, 02 Dec 2023 13:27:17 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Sat, 02 Dec 2023 13:28:17 GMT
ENV MARIADB_JDBC_VERSION=3.2.0
# Sat, 02 Dec 2023 13:28:17 GMT
ENV MARIADB_JDBC_SHA256=adf9df10bc9b2a137def36d6a495812258f430d4a8f7946727c61558e6c73941
# Sat, 02 Dec 2023 13:28:17 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.2.0
# Sat, 02 Dec 2023 13:28:17 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.2.0.jar
# Sat, 02 Dec 2023 13:28:17 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.2.0.jar
# Sat, 02 Dec 2023 13:28:18 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c -
# Sat, 02 Dec 2023 13:28:18 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Sat, 02 Dec 2023 13:28:18 GMT
COPY file:eb83c176c15b3f58dfe8a9489b3339583ffd67428f115d02fc75fd828ba98995 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Sat, 02 Dec 2023 13:28:19 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Sat, 02 Dec 2023 13:28:19 GMT
COPY file:999bc8865c34789d8e469cd12cf9ae2fc932b27d4508dd5ae18997c8eca23a9b in /usr/local/bin/docker-entrypoint.sh 
# Sat, 02 Dec 2023 13:28:19 GMT
VOLUME [/usr/local/xwiki]
# Sat, 02 Dec 2023 13:28:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 02 Dec 2023 13:28:19 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:cbe3537751ce03ea42788c2fbe2d5d336180dc2e20472c8cdba8b3224191d101`  
		Last Modified: Wed, 29 Nov 2023 19:24:54 GMT  
		Size: 30.4 MB (30446322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cd63fc495d1a4839e5239c716fa5a6ec48209bff26db1e7d7af7b0701ac4ee7`  
		Last Modified: Sat, 02 Dec 2023 02:06:15 GMT  
		Size: 17.5 MB (17455452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c42674dea4fe1d59945de1102de69ceb99f21310cb6b7f6fcccdd43b07a8acf`  
		Last Modified: Sat, 02 Dec 2023 02:06:58 GMT  
		Size: 47.1 MB (47149362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a992519bbaeefaec0b90db8a0d65735dd823a054e2f332d4dade7315733bf084`  
		Last Modified: Sat, 02 Dec 2023 02:06:52 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:506583e9517b9e597323949bc904a17f5054f4ac1e7a64d3bd587a9b87226f61`  
		Last Modified: Sat, 02 Dec 2023 02:06:52 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d76eec8f511751601d4c750c85aae4e5ccbb964961e9b9eb29220a58a53680b6`  
		Last Modified: Sat, 02 Dec 2023 08:38:09 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b5b83be0deb6c81545cf156387e2f9c8a9819dccdb5bcd909477633a0c63de9`  
		Last Modified: Sat, 02 Dec 2023 08:41:00 GMT  
		Size: 12.4 MB (12391439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa46ac8c25ce022e0b73186446482028d101a0fdb3095d4105bac44dc01d583c`  
		Last Modified: Sat, 02 Dec 2023 08:40:59 GMT  
		Size: 458.5 KB (458501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f01cf1c5b55745adfca0f90134e0d6c0a52dc267a8092ee93d91c7ed5f94d92`  
		Last Modified: Sat, 02 Dec 2023 08:40:59 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef176cd8152010e031460e724a3950c4baffee331115c54210da7c164b5e2fca`  
		Last Modified: Sat, 02 Dec 2023 13:31:58 GMT  
		Size: 178.4 MB (178375891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0c1b42eccbc3a3b2e1c9bad9ceb71b502d77cb1a1d7eb96472add4431265ae9`  
		Last Modified: Sat, 02 Dec 2023 13:33:48 GMT  
		Size: 309.1 MB (309079811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77f6865fe5aeef8931f473a2a2a50e01a073dbf350dcbb26e07d0d8c7a42284c`  
		Last Modified: Sat, 02 Dec 2023 13:34:48 GMT  
		Size: 603.4 KB (603392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6830733230e3eff73f9be3d71c00e365815bb653eb9378d4f5e19214a4877a7d`  
		Last Modified: Sat, 02 Dec 2023 13:34:47 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fc507b82cd5908ce07dd490597f97f0ca92536cc1a58b3cc91e0b9613646f72`  
		Last Modified: Sat, 02 Dec 2023 13:34:47 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25d649dbd479cc1e45b29fab1bba67a7ff4fb2c17bf86e659fcd82d1ce34ceba`  
		Last Modified: Sat, 02 Dec 2023 13:34:48 GMT  
		Size: 6.0 KB (6012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ec475c42d4e3d238632518b6b98655032c3c88a19a7933c294d745b37986dd3`  
		Last Modified: Sat, 02 Dec 2023 13:34:47 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:lts-mariadb` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:7fca8e118b422d14354df82e2dd725e18e70b6ad60e8985eb154f59618709b74
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **589.9 MB (589907964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd5a9eefaa1e0d3edebe26aa7a68c90be7acc275c4c6e71967c7e457d0d423aa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Fri, 01 Dec 2023 07:43:19 GMT
ARG RELEASE
# Fri, 01 Dec 2023 07:43:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Dec 2023 07:43:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Dec 2023 07:43:20 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 01 Dec 2023 07:43:21 GMT
ADD file:891dcab0c4ce2880c4dca013d326a3efd7601003b6f5076938d678101e301b79 in / 
# Fri, 01 Dec 2023 07:43:22 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 05:30:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 02 Dec 2023 05:30:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 02 Dec 2023 05:30:53 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 02 Dec 2023 05:32:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:32:58 GMT
ENV JAVA_VERSION=jdk-17.0.9+9
# Sat, 02 Dec 2023 05:33:23 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='05b192f81ed478178ba953a2a779b67fc5a810acadb633ad69f8c4412399edb8';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.9_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='c37f729200b572884b8f8e157852c739be728d61d9a1da0f920104876d324733';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_x64_linux_hotspot_17.0.9_9.tar.gz';          ;;        armhf|arm)          ESUM='5ae1f8cae358e41083a6b44f53c6f0daeb657f83c293da6c8733f68278e13703';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_arm_linux_hotspot_17.0.9_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='79c85ecf1320c67b828310167e1ced62e402bc86a5d47ca9cc7bfa3b708cb07a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.9_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c4f2249bee785aa8c754741aa24d035e02b4e6d844e35b2b20030374d8fbab75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_s390x_linux_hotspot_17.0.9_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Sat, 02 Dec 2023 05:33:24 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Sat, 02 Dec 2023 05:33:24 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Sat, 02 Dec 2023 05:33:24 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 02 Dec 2023 10:28:30 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Sat, 02 Dec 2023 10:28:30 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 02 Dec 2023 10:28:31 GMT
RUN mkdir -p "$CATALINA_HOME"
# Sat, 02 Dec 2023 10:28:31 GMT
WORKDIR /usr/local/tomcat
# Sat, 02 Dec 2023 10:28:31 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Sat, 02 Dec 2023 10:28:31 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Sat, 02 Dec 2023 10:30:26 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Sat, 02 Dec 2023 10:30:26 GMT
ENV TOMCAT_MAJOR=9
# Sat, 02 Dec 2023 10:30:27 GMT
ENV TOMCAT_VERSION=9.0.83
# Sat, 02 Dec 2023 10:30:27 GMT
ENV TOMCAT_SHA512=3f022ec8552bce1b72eb85d0778c93052ccb00226de3302544ec844ab93a9991e19c2db56ed06c18f03e5d75f34a46cedac46ae83bdd225518a55c62fc69ea04
# Sat, 02 Dec 2023 10:30:27 GMT
COPY dir:d6b60e5b0b304db2603b49a081467fb682702117dcde9645b1500750745b853b in /usr/local/tomcat 
# Sat, 02 Dec 2023 10:30:30 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 10:30:31 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Sat, 02 Dec 2023 10:30:31 GMT
EXPOSE 8080
# Sat, 02 Dec 2023 10:30:32 GMT
ENTRYPOINT []
# Sat, 02 Dec 2023 10:30:32 GMT
CMD ["catalina.sh" "run"]
# Sat, 02 Dec 2023 13:55:56 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Sat, 02 Dec 2023 13:55:56 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Sat, 02 Dec 2023 13:55:56 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Sat, 02 Dec 2023 13:55:56 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Sat, 02 Dec 2023 13:55:56 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Sat, 02 Dec 2023 13:55:56 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Sat, 02 Dec 2023 13:57:45 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Tue, 05 Dec 2023 18:59:54 GMT
ENV XWIKI_VERSION=14.10.20
# Tue, 05 Dec 2023 18:59:54 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.10.20
# Tue, 05 Dec 2023 18:59:54 GMT
ENV XWIKI_DOWNLOAD_SHA256=c418601676d61893ccb9e066b1f2bcce56717b49e5c2456656b6960db6bd6e4c
# Tue, 05 Dec 2023 19:00:39 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Tue, 05 Dec 2023 19:01:39 GMT
ENV MARIADB_JDBC_VERSION=3.3.0
# Tue, 05 Dec 2023 19:01:39 GMT
ENV MARIADB_JDBC_SHA256=8262c79463e6b0932f60f55b61ca14087fdcafb117caa87259cd3a64409cd4fa
# Tue, 05 Dec 2023 19:01:39 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.3.0
# Tue, 05 Dec 2023 19:01:39 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.3.0.jar
# Tue, 05 Dec 2023 19:01:39 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.3.0.jar
# Tue, 05 Dec 2023 19:01:40 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c -
# Tue, 05 Dec 2023 19:01:40 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Tue, 05 Dec 2023 19:01:40 GMT
COPY file:eb83c176c15b3f58dfe8a9489b3339583ffd67428f115d02fc75fd828ba98995 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Tue, 05 Dec 2023 19:01:41 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Tue, 05 Dec 2023 19:01:41 GMT
COPY file:999bc8865c34789d8e469cd12cf9ae2fc932b27d4508dd5ae18997c8eca23a9b in /usr/local/bin/docker-entrypoint.sh 
# Tue, 05 Dec 2023 19:01:41 GMT
VOLUME [/usr/local/xwiki]
# Tue, 05 Dec 2023 19:01:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Dec 2023 19:01:41 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:aeb9f260d781cd1e09daf0d0a9e5bcb581efce5b33b221f2f4a27de8db66e463`  
		Last Modified: Thu, 30 Nov 2023 02:35:43 GMT  
		Size: 28.4 MB (28399939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9c3988b1198250f931d321166ff7a5f1bbd03b8fa06eae348c92ef639a62393`  
		Last Modified: Sat, 02 Dec 2023 05:37:12 GMT  
		Size: 18.9 MB (18857837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0451cfbb70a802ae4861e4e9957e778b9fd0d5072b981d80950164d639df6ecb`  
		Last Modified: Sat, 02 Dec 2023 05:37:50 GMT  
		Size: 46.6 MB (46624045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:332ede580b745c8969408589f1921b71bdf198c6aefc33463d3d2dc815df73e8`  
		Last Modified: Sat, 02 Dec 2023 05:37:44 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96b8f9c326b7dd6d03972c72e618e72c738e042baf084b2b2be95c25203c6ca0`  
		Last Modified: Sat, 02 Dec 2023 05:37:44 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af3f0afaced9459acf9df8ee72f1e9c5d5b2b83bfd4c230f016dd8f2d3792a9b`  
		Last Modified: Sat, 02 Dec 2023 10:43:28 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f57d0d84391e644fca51444d40f90ca6ee47e7f12e167c3bdfb991920043b65d`  
		Last Modified: Sat, 02 Dec 2023 10:46:10 GMT  
		Size: 12.4 MB (12398043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c06c74138864f58213ae7147e3c1fdf9f767387b223c051e3c65be7e73283bbc`  
		Last Modified: Sat, 02 Dec 2023 10:46:09 GMT  
		Size: 458.2 KB (458184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cd271d133e344644de2ffbb1ac8a8fbdac941b26c7a462901c51862ad0953e1`  
		Last Modified: Sat, 02 Dec 2023 10:46:09 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30d0336d2acdb89f25f9f5f91680e7453771e216fb0249e2abc33b697ea14705`  
		Last Modified: Sat, 02 Dec 2023 14:05:27 GMT  
		Size: 173.4 MB (173401114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb7b3d2629d4295ee2d7db6123ae798813cee038194f7438b1ca92d77a4239bb`  
		Last Modified: Tue, 05 Dec 2023 19:02:31 GMT  
		Size: 309.1 MB (309149421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbbf674fdc8d994931738225d3b41557c2371845c03635caefa9f1b2b2ddf0cb`  
		Last Modified: Tue, 05 Dec 2023 19:03:32 GMT  
		Size: 606.0 KB (605962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ec1009bd9d3011258e4533cb8b2b0c544da1776c4d26e63da60dfe22cc7c147`  
		Last Modified: Tue, 05 Dec 2023 19:03:31 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44acefe9b5957d3056ff7b5f20bf9749b3eae460760009d2db2354cb8b0bb14b`  
		Last Modified: Tue, 05 Dec 2023 19:03:31 GMT  
		Size: 2.3 KB (2308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf566973cfd104001b2d2aadbe8d34974b69dfd3bfe4380c59bc926317e695f8`  
		Last Modified: Tue, 05 Dec 2023 19:03:31 GMT  
		Size: 6.1 KB (6128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:233aba09a1f204acb151f0ad19ad1f2f8ea1decb68e96f32781ec26f3b69f010`  
		Last Modified: Tue, 05 Dec 2023 19:03:31 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
