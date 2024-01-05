## `xwiki:latest`

```console
$ docker pull xwiki@sha256:d22dfb1381049563ab462e8cc95e8dc9c8325eadbc00c9d0378cd513765a5509
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:latest` - linux; amd64

```console
$ docker pull xwiki@sha256:b7852c65b22ef1c856a72c7ab5766863afebe2a1bec266b6b68d306995cb7e7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **595.6 MB (595588671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de7e1f57d25437c66ad55df9524e4d617bcd3b5d564c5abd100d5583cf0dafc6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 12 Dec 2023 11:38:57 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:38:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:38:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:38:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:38:59 GMT
ADD file:2b3b5254f38a790d40e31cb26155609f7fc99ef7bc99eae1e0d67fa9ae605f77 in / 
# Tue, 12 Dec 2023 11:38:59 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 10:16:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Dec 2023 10:16:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Dec 2023 10:16:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 16 Dec 2023 10:18:54 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 10:18:54 GMT
ENV JAVA_VERSION=jdk-17.0.9+9
# Sat, 16 Dec 2023 10:19:29 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='05b192f81ed478178ba953a2a779b67fc5a810acadb633ad69f8c4412399edb8';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.9_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='c37f729200b572884b8f8e157852c739be728d61d9a1da0f920104876d324733';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_x64_linux_hotspot_17.0.9_9.tar.gz';          ;;        armhf|arm)          ESUM='5ae1f8cae358e41083a6b44f53c6f0daeb657f83c293da6c8733f68278e13703';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_arm_linux_hotspot_17.0.9_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='79c85ecf1320c67b828310167e1ced62e402bc86a5d47ca9cc7bfa3b708cb07a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.9_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c4f2249bee785aa8c754741aa24d035e02b4e6d844e35b2b20030374d8fbab75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_s390x_linux_hotspot_17.0.9_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Sat, 16 Dec 2023 10:19:30 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Sat, 16 Dec 2023 10:19:30 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Sat, 16 Dec 2023 10:19:30 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 16 Dec 2023 16:07:07 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Sat, 16 Dec 2023 16:07:07 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Dec 2023 16:07:07 GMT
RUN mkdir -p "$CATALINA_HOME"
# Sat, 16 Dec 2023 16:07:07 GMT
WORKDIR /usr/local/tomcat
# Sat, 16 Dec 2023 16:07:07 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Sat, 16 Dec 2023 16:07:07 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Sat, 16 Dec 2023 16:09:32 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Sat, 16 Dec 2023 16:09:32 GMT
ENV TOMCAT_MAJOR=9
# Sat, 16 Dec 2023 16:09:32 GMT
ENV TOMCAT_VERSION=9.0.84
# Sat, 16 Dec 2023 16:09:32 GMT
ENV TOMCAT_SHA512=85a42ab5e7e4cb1923888e96a78a0f277a870d06e76147a95457878c124001c9a317eade4ad69c249a460ffe2cbefe894022b84389cdf33038bc456e3699c8e3
# Sat, 16 Dec 2023 16:09:32 GMT
COPY dir:e3a76c94a246a1206356fe923c85a36b030f13bc6f6e832187da5052d71cee0e in /usr/local/tomcat 
# Sat, 16 Dec 2023 16:09:36 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 16:09:38 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Sat, 16 Dec 2023 16:09:38 GMT
EXPOSE 8080
# Sat, 16 Dec 2023 16:09:38 GMT
ENTRYPOINT []
# Sat, 16 Dec 2023 16:09:38 GMT
CMD ["catalina.sh" "run"]
# Wed, 03 Jan 2024 14:50:08 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 03 Jan 2024 14:50:08 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 03 Jan 2024 14:50:08 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 03 Jan 2024 14:50:08 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 03 Jan 2024 14:50:08 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 03 Jan 2024 14:50:08 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 03 Jan 2024 14:50:08 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 03 Jan 2024 14:50:08 GMT
ENV XWIKI_VERSION=15.10.4
# Wed, 03 Jan 2024 14:50:08 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.10.4
# Wed, 03 Jan 2024 14:50:08 GMT
ENV XWIKI_DOWNLOAD_SHA256=8c1bb157f03b714255305aadc0904d35e87ae38df998dcfb5117de3d395d473c
# Wed, 03 Jan 2024 14:50:08 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Wed, 03 Jan 2024 14:50:08 GMT
ENV MYSQL_JDBC_VERSION=8.2.0
# Wed, 03 Jan 2024 14:50:08 GMT
ENV MYSQL_JDBC_SHA256=06f14fbd664d0e382347489e66495ca27ab7e6c2e1d9969a496931736197465f
# Wed, 03 Jan 2024 14:50:08 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/8.2.0
# Wed, 03 Jan 2024 14:50:08 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-8.2.0.jar
# Wed, 03 Jan 2024 14:50:08 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-8.2.0.jar
# Wed, 03 Jan 2024 14:50:08 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c - # buildkit
# Wed, 03 Jan 2024 14:50:08 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Wed, 03 Jan 2024 14:50:08 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Wed, 03 Jan 2024 14:50:08 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Wed, 03 Jan 2024 14:50:08 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Wed, 03 Jan 2024 14:50:08 GMT
VOLUME [/usr/local/xwiki]
# Wed, 03 Jan 2024 14:50:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Jan 2024 14:50:08 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:3dd181f9be599de628e1bc6d868d517125e07f968824bcf7b7ed8d28ad1026b1`  
		Last Modified: Tue, 12 Dec 2023 12:46:19 GMT  
		Size: 30.4 MB (30446577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f838805bddf9c7d83f7f51716a77602920f9057ade57b344c071481b5214767`  
		Last Modified: Sat, 16 Dec 2023 10:23:47 GMT  
		Size: 17.5 MB (17456128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7eee5bc80e633b7f89402fb78469504f2d0662c7c827954ff259867d024278b`  
		Last Modified: Sat, 16 Dec 2023 10:24:28 GMT  
		Size: 47.1 MB (47149325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51526e7965d895bb7535ad46133791589d87f78882f553e5e63f8aed0568dabd`  
		Last Modified: Sat, 16 Dec 2023 10:24:21 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffcdc7c6c1603bef17eec1b194fd954703a005aff5db2d15302f85b01b494351`  
		Last Modified: Sat, 16 Dec 2023 10:24:21 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc81f1b04d3d203216bfcc90d5a6429b5c33ec66e790e3ebf566431088f5212c`  
		Last Modified: Sat, 16 Dec 2023 16:24:58 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a603ca3ebf9e8f0eb997467ce50ef8dfd4e49196308c1a39f9c5c0c39d2846b`  
		Last Modified: Sat, 16 Dec 2023 16:27:49 GMT  
		Size: 12.4 MB (12398194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94b70543ac62867c34368428a8432713e13dbcb451521adfe0879fc51c5cae2e`  
		Last Modified: Sat, 16 Dec 2023 16:27:48 GMT  
		Size: 458.4 KB (458432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a684fd03abd5ec4c3528f0458050f8b03af9c5a885783d748df8617d90250c6`  
		Last Modified: Sat, 16 Dec 2023 16:27:48 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d072a9d73a3429180cadafafa0d71018cf97e810fe065d0322f3ce2b1e5cc72`  
		Last Modified: Thu, 04 Jan 2024 19:58:12 GMT  
		Size: 178.3 MB (178348850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02379dbe41bc4675b1c5421c194513fb0164a0eb69445bb85937d312bce49fa7`  
		Last Modified: Thu, 04 Jan 2024 19:58:16 GMT  
		Size: 307.0 MB (306966412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39c0bfc0713861c7656d9eebffc822d7b12b01dcbd5de712215f5bf6e2c2443e`  
		Last Modified: Thu, 04 Jan 2024 19:58:09 GMT  
		Size: 2.4 MB (2350948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:618d84d157b76050497e4def10324090102430a1495509a2ae5ba65efb8bdce2`  
		Last Modified: Thu, 04 Jan 2024 19:58:09 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0637d7ca92e73d21c7fdd502fea084d04a399dd120f7c733e4e77314198de7c`  
		Last Modified: Thu, 04 Jan 2024 19:58:10 GMT  
		Size: 2.4 KB (2371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92f43f478ea70c175e2af83bc7dbe3f16d0d47e1bc33493f2ba2305c061a2b72`  
		Last Modified: Thu, 04 Jan 2024 19:58:10 GMT  
		Size: 6.4 KB (6414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45423c7fe60a80af31ad71a31f4a7fdca2ab0814a0e85e35c634bf406a860268`  
		Last Modified: Thu, 04 Jan 2024 19:58:11 GMT  
		Size: 2.5 KB (2482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:latest` - unknown; unknown

```console
$ docker pull xwiki@sha256:9995c39f954be1a954c54d793242d3e43039d25c5d08b619bc4d96487b871b0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8083027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98377d4d9b41acafaed2863c9997ac7709557a85193d98e90b400b034916092f`

```dockerfile
```

-	Layers:
	-	`sha256:00fa1045c8e5f1e03329823cb8d07df812daa27eb406f109d9c9b9310b6e61fa`  
		Last Modified: Thu, 04 Jan 2024 19:58:09 GMT  
		Size: 8.0 MB (8039110 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e1c9d23f4efda809762d4b84b9fafb9fb9903d428d9b3414db7bccf4a8ab85b`  
		Last Modified: Thu, 04 Jan 2024 19:58:09 GMT  
		Size: 43.9 KB (43917 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:latest` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:8e37cfd97341640746345bea6967ec08919000545c11876ea89916b75fdd6d12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **589.5 MB (589466990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41aea4712306d567626c4750a112a68dc34c879ada850229dc246c6e66c20557`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 12 Dec 2023 11:41:50 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:41:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:41:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:41:51 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:41:54 GMT
ADD file:50f947da69b3b6c63695be9c49eee16f7a7dcdecdceb51e5bee1609b845bf483 in / 
# Tue, 12 Dec 2023 11:41:54 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 10:02:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Dec 2023 10:02:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Dec 2023 10:02:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 16 Dec 2023 10:04:31 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 10:04:32 GMT
ENV JAVA_VERSION=jdk-17.0.9+9
# Sat, 16 Dec 2023 10:04:56 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='05b192f81ed478178ba953a2a779b67fc5a810acadb633ad69f8c4412399edb8';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.9_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='c37f729200b572884b8f8e157852c739be728d61d9a1da0f920104876d324733';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_x64_linux_hotspot_17.0.9_9.tar.gz';          ;;        armhf|arm)          ESUM='5ae1f8cae358e41083a6b44f53c6f0daeb657f83c293da6c8733f68278e13703';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_arm_linux_hotspot_17.0.9_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='79c85ecf1320c67b828310167e1ced62e402bc86a5d47ca9cc7bfa3b708cb07a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.9_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c4f2249bee785aa8c754741aa24d035e02b4e6d844e35b2b20030374d8fbab75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_s390x_linux_hotspot_17.0.9_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Sat, 16 Dec 2023 10:04:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Sat, 16 Dec 2023 10:04:57 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Sat, 16 Dec 2023 10:04:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 16 Dec 2023 14:58:15 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Sat, 16 Dec 2023 14:58:15 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Dec 2023 14:58:16 GMT
RUN mkdir -p "$CATALINA_HOME"
# Sat, 16 Dec 2023 14:58:16 GMT
WORKDIR /usr/local/tomcat
# Sat, 16 Dec 2023 14:58:16 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Sat, 16 Dec 2023 14:58:16 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Sat, 16 Dec 2023 15:00:13 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Sat, 16 Dec 2023 15:00:13 GMT
ENV TOMCAT_MAJOR=9
# Sat, 16 Dec 2023 15:00:13 GMT
ENV TOMCAT_VERSION=9.0.84
# Sat, 16 Dec 2023 15:00:13 GMT
ENV TOMCAT_SHA512=85a42ab5e7e4cb1923888e96a78a0f277a870d06e76147a95457878c124001c9a317eade4ad69c249a460ffe2cbefe894022b84389cdf33038bc456e3699c8e3
# Sat, 16 Dec 2023 15:00:13 GMT
COPY dir:14fe7e4b8e31f53a38fe02615c860260f06f1bfa5d55349e5c610bb0eaaf3673 in /usr/local/tomcat 
# Sat, 16 Dec 2023 15:00:17 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 15:00:18 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Sat, 16 Dec 2023 15:00:18 GMT
EXPOSE 8080
# Sat, 16 Dec 2023 15:00:18 GMT
ENTRYPOINT []
# Sat, 16 Dec 2023 15:00:18 GMT
CMD ["catalina.sh" "run"]
# Wed, 03 Jan 2024 14:50:08 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 03 Jan 2024 14:50:08 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 03 Jan 2024 14:50:08 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 03 Jan 2024 14:50:08 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 03 Jan 2024 14:50:08 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 03 Jan 2024 14:50:08 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 03 Jan 2024 14:50:08 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 03 Jan 2024 14:50:08 GMT
ENV XWIKI_VERSION=15.10.4
# Wed, 03 Jan 2024 14:50:08 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.10.4
# Wed, 03 Jan 2024 14:50:08 GMT
ENV XWIKI_DOWNLOAD_SHA256=8c1bb157f03b714255305aadc0904d35e87ae38df998dcfb5117de3d395d473c
# Wed, 03 Jan 2024 14:50:08 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Wed, 03 Jan 2024 14:50:08 GMT
ENV MYSQL_JDBC_VERSION=8.2.0
# Wed, 03 Jan 2024 14:50:08 GMT
ENV MYSQL_JDBC_SHA256=06f14fbd664d0e382347489e66495ca27ab7e6c2e1d9969a496931736197465f
# Wed, 03 Jan 2024 14:50:08 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/8.2.0
# Wed, 03 Jan 2024 14:50:08 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-8.2.0.jar
# Wed, 03 Jan 2024 14:50:08 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-8.2.0.jar
# Wed, 03 Jan 2024 14:50:08 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c - # buildkit
# Wed, 03 Jan 2024 14:50:08 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Wed, 03 Jan 2024 14:50:08 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Wed, 03 Jan 2024 14:50:08 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Wed, 03 Jan 2024 14:50:08 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Wed, 03 Jan 2024 14:50:08 GMT
VOLUME [/usr/local/xwiki]
# Wed, 03 Jan 2024 14:50:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Jan 2024 14:50:08 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:7734efb8b826f955c6a3bb51d7c84cb262d0e600ea3980f5bce69fa7f4f92d24`  
		Last Modified: Tue, 12 Dec 2023 16:00:15 GMT  
		Size: 28.4 MB (28400282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a83d9c33e24ca521e40939a701f20c41285b4488136968b6007b00f5ea0e1267`  
		Last Modified: Sat, 16 Dec 2023 10:08:54 GMT  
		Size: 18.9 MB (18857814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ced1602447389bf6ad2464c27ffc94e85095dbfdb47f78a2096081e80388ad97`  
		Last Modified: Sat, 16 Dec 2023 10:09:35 GMT  
		Size: 46.6 MB (46624027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6457113e3d5d5e26e07af4b78a197170e362a87e9acf2597817bf8e41b61b864`  
		Last Modified: Sat, 16 Dec 2023 10:09:30 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:764df9f717c8b617f5bd26b1b7a44dfb44e89d4a1bc26be0eb4a08d0696d3e49`  
		Last Modified: Sat, 16 Dec 2023 10:09:30 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3fdc1608413c55e6f71ba5c11e8a186c5cdf1ffd462d135094650174976fd36`  
		Last Modified: Sat, 16 Dec 2023 15:13:29 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:040f9b1d3ea5ed9193ca2803556daa46af53b68c910758193f72f2d9ea7583f6`  
		Last Modified: Sat, 16 Dec 2023 15:16:19 GMT  
		Size: 12.4 MB (12407499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b105fa48bd69dab1ec528eb0a9cdaf37f46e8af363a642b3f44e619e7751d4ed`  
		Last Modified: Sat, 16 Dec 2023 15:16:18 GMT  
		Size: 458.5 KB (458463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b656c2cf87b11b1a6165fa929daa3b987a92d55dd64f4151810c4a9d3ee4cd8`  
		Last Modified: Sat, 16 Dec 2023 15:16:18 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:866db4f6d3f9c32e6b0b7a7a0ac76b87055b68929760bdf76fa6aa9c5ef0ec7f`  
		Last Modified: Thu, 04 Jan 2024 22:12:34 GMT  
		Size: 173.4 MB (173387965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97af4f188a69dd921d8e5b4b5cde29e2b83eec1caa3b42e26d7a0fe7577d7af4`  
		Last Modified: Thu, 04 Jan 2024 22:12:39 GMT  
		Size: 307.0 MB (306966167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f8ef20ff7c128088e06d8605f724e4b5c463aa00d9d3c851f78eb0e85e24868`  
		Last Modified: Thu, 04 Jan 2024 22:12:31 GMT  
		Size: 2.4 MB (2350958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:347db250f13e1ecaceab0e22218d981c4e6b9803eeed402f7ca55ba5a8772541`  
		Last Modified: Thu, 04 Jan 2024 22:12:31 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:313bf76ec5d69e4dd70365401f1272faddaf2d92ac9733b31a7908628d9eaa5d`  
		Last Modified: Thu, 04 Jan 2024 22:12:32 GMT  
		Size: 2.4 KB (2375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7cd89f2068f95c42c36b5602d951f2957259db8626fb17f55d2034136bf7684`  
		Last Modified: Thu, 04 Jan 2024 22:12:32 GMT  
		Size: 6.4 KB (6416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbfecb9f4cc6d8ddd94082ba52797ecb936366e3c32eec25093a4129b17351ca`  
		Last Modified: Thu, 04 Jan 2024 22:12:33 GMT  
		Size: 2.5 KB (2483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:latest` - unknown; unknown

```console
$ docker pull xwiki@sha256:7b341ad42c6eceeecbcc0380e0207529210182e328bd4dc868be1ead776c5f4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8167099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:648de08c28a19172f05a23689e395ae1cbde8265aac09730344f252225e44285`

```dockerfile
```

-	Layers:
	-	`sha256:7ee72a106c43132bf01cc851aeb12161109e7b30fbb927e6c1900046cbfb949e`  
		Last Modified: Thu, 04 Jan 2024 22:12:30 GMT  
		Size: 8.1 MB (8123152 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6183975ff9890cf745c7017abe5faf78e54fc48b850e884bbd5fc6a65763ed52`  
		Last Modified: Thu, 04 Jan 2024 22:12:29 GMT  
		Size: 43.9 KB (43947 bytes)  
		MIME: application/vnd.in-toto+json
